---
title: 에너지 수준 예상치 얻기 | Microsoft Docs
description: 에너지 수준 예상치 문서 구하기
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: 0fd457b152083af364d924502c18bc0813e34b83
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442582"
---
# <a name="obtaining-energy-level-estimates"></a>에너지 수준 추정치 얻기
에너지 수준의 값을 예측 하는 것은 퀀텀 화학의 주요 응용 프로그램 중 하나입니다. 여기서는 분자 Hydrogen의 정식 예제에 대해이를 수행 하는 방법을 간략하게 설명 합니다. 이 섹션에서 참조 하는 샘플은 화학 샘플 리포지토리에서 `MolecularHydrogen` 됩니다. 출력을 그리는 시각적 예제는 `MolecularHydrogenGUI` 데모입니다.

첫 번째 단계는 분자 Hydrogen를 나타내는 Hamiltonian를 생성 하는 것입니다. 이는 NWChem 도구를 통해 생성 될 수 있지만,이 샘플에서 간결 하 게 Hamiltonian 용어를 수동으로 추가 합니다.

```csharp
    // These orbital integrals are represented using the OrbitalIntegral
    // data structure.
    var energyOffset = 0.713776188; // This is the coulomb repulsion
    var nElectrons = 2; // Molecular hydrogen has two electrons
    var orbitalIntegrals = new OrbitalIntegral[]
    {
        new OrbitalIntegral(new[] { 0,0 }, -1.252477495),
        new OrbitalIntegral(new[] { 1,1 }, -0.475934275),
        new OrbitalIntegral(new[] { 0,0,0,0 }, 0.674493166),
        new OrbitalIntegral(new[] { 0,1,0,1 }, 0.181287518),
        new OrbitalIntegral(new[] { 0,1,1,0 }, 0.663472101),
        new OrbitalIntegral(new[] { 1,1,1,1 }, 0.697398010),
        // This line adds the identity term.
        new OrbitalIntegral(new int[] { }, energyOffset)
    };

    // We initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Hamiltonian를 시뮬레이션 하려면 fermion 연산자를 연산자로 변환 해야 합니다. 이러한 변환은 다음과 같이 Wigner 인코딩을 통해 수행 됩니다.

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // We also need to create an input quantum state to this Hamiltonian.
    // Let us use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

이제 [Hamiltonian Dynamics 시뮬레이션](xref:microsoft.quantum.libraries.standard.algorithms)에서 Hamiltonian를 나타내는 `qSharpData`를 `TrotterStepOracle` 함수로 전달 합니다. `TrotterStepOracle`는 Hamiltonian의 실시간 진화에 근사치를 계산 하는 퀀텀 작업을 반환 합니다.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operatrion.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

이제 표준 라이브러리의 단계 추정 알고리즘을 사용 하 여 위의 시뮬레이션을 통해 그라운드 상태 에너지를 배울 수 있습니다. 이렇게 하려면 퀀텀 접지 상태에 대 한 적절 한 근사값을 준비 해야 합니다. 이러한 근사치에 대 한 제안은 `Broombridge` 스키마에 제공 되지만, 이러한 제안을 제외 하 고, 기본 접근 방식은 파괴을 적극적 하는 여러 개의 `hamiltonian.NElectrons`를 추가 합니다. 단계 예측 함수 및 작업은 [Microsoft의 특성화 네임 스페이스](xref:microsoft.quantum.characterization in DocFX notation)에 있습니다.

다음 코드 조각은 화학 시뮬레이션 라이브러리의 실시간 진화 출력이 퀀텀 단계 예측과 통합 될 수 있는 방법을 보여 줍니다.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined below.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // We use the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // We obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // We return both the estimated phase, and the estimated energy.
    return (estPhase, estEnergy);
}
```

이제이 Q # 코드는 드라이버 프로그램에서 호출 될 수 있습니다. 다음에서는 전체 상태 시뮬레이터를 만들고 `GetEnergyByTrotterization`를 실행 하 여 그라운드 상태 에너지를 구합니다.

```csharp
using (var qsim = new QuantumSimulator())
{
    // We specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // We specify the step-size of the simulated time-evolution. This needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, let us run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular Hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

두 매개 변수가 반환 됩니다. `energyEst`은 그라운드 상태 에너지를 예상 하는 것으로, 평균적으로 `-1.137`을 기준으로 합니다. `phaseEst`는 단계 추정 알고리즘에서 반환 하는 원시 단계 이며 너무 커서 `trotterStep` 너무 커서 별칭이 발생 하는 경우를 진단 하는 데 유용 합니다.
