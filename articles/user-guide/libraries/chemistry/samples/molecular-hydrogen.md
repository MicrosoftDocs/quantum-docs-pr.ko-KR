---
title: 에너지 수준 추정치 얻기
description: Q#분자 hydrogen의 에너지 수준 값을 예측 하는 샘플 프로그램을 안내 합니다.
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
no-loc:
- Q#
- $$v
ms.openlocfilehash: 81fba0c52c854d61f9143659795fb4d3c3cee8b9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691523"
---
# <a name="obtaining-energy-level-estimates"></a>에너지 수준 추정치 얻기
에너지 수준의 값을 예측 하는 것은 퀀텀 화학의 주요 응용 프로그램 중 하나입니다. 이 문서에서는 분자 hydrogen의 정식 예제에 대해이를 수행 하는 방법을 간략하게 설명 합니다. 이 섹션에서 참조 하는 샘플은 [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogen) 화학 샘플 리포지토리에 있습니다. 출력을 그리는 시각적 예제는 [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogenGUI) 데모입니다.

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a>분자 hydrogen의 에너지 값 추정

첫 번째 단계는 분자 hydrogen를 나타내는 Hamiltonian를 생성 하는 것입니다. NWChem 도구를 사용 하 여이를 생성할 수 있지만, 간단히 하기 위해이 샘플에서는 Hamiltonian 용어를 수동으로 추가 합니다.

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

    // Initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Hamiltonian를 시뮬레이션 하려면 fermion 연산자를 연산자로 변환 해야 합니다. 이러한 변환은 다음과 같이 Jordan-Wigner 인코딩을 통해 수행 됩니다.

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // You also need to create an input quantum state to this Hamiltonian.
    // Use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

그런 다음 `qSharpData` Hamiltonian를 나타내는을 함수에 전달 `TrotterStepOracle` 합니다. `TrotterStepOracle` Hamiltonian의 실시간 진화에 근사치를 주는 퀀텀 작업을 반환 합니다. 자세한 내용은 [Hamiltonian Dynamics 시뮬레이션](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms)을 참조 하세요.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

이제 표준 라이브러리의 [단계 추정 알고리즘](xref:microsoft.quantum.libraries.characterization) 을 사용 하 여 이전 시뮬레이션을 통해 그라운드 상태 에너지를 배울 수 있습니다. 이렇게 하려면 퀀텀 접지 상태에 대 한 적절 한 근사값을 준비 해야 합니다. 이러한 근사치에 대 한 제안은 스키마에 제공 됩니다 [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) . 그러나 이러한 제안이 없는 경우에는 기본 방법으로 `hamiltonian.NElectrons` 적극적 대각선 파괴을 최소화 하기 위해 여러 개의를 추가 합니다. 단계 예측 함수 및 작업은 Microsoft. n a m [. 특성화](xref:Microsoft.Quantum.Characterization) 네임 스페이스의 docfx 표기법으로 제공 됩니다.

다음 코드 조각에서는 화학 시뮬레이션 라이브러리의 실시간 진화 출력이 퀀텀 단계 예측과 통합 되는 방식을 보여 줍니다.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // Using a Product formula, also known as `Trotterization`, to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined here.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // Using the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // Now, obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // Return both the estimated phase and the estimated energy.
    return (estPhase, estEnergy);
}
```

이제 Q# 호스트 프로그램에서 코드를 호출할 수 있습니다. 다음 c # 코드는 전체 상태 시뮬레이터를 만들고를 실행 `GetEnergyByTrotterization` 하 여 그라운드 상태 에너지를 가져옵니다.

```csharp
using (var qsim = new QuantumSimulator())
{
    // Specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // Specify the step size of the simulated time evolution. The step size needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

작업은 두 개의 매개 변수를 반환 합니다. 

- `energyEst` 는 그라운드 상태 에너지 추정치 이며 평균에 가까워야 합니다 `-1.137` . 
- `phaseEst` 단계 추정 알고리즘에서 반환 하는 원시 단계입니다. 이는 너무 커서 값으로 인해 발생 하는 별칭을 진단 하는 데 유용 `trotterStep` 합니다.
