---
title: 에너지 수준 추정치 얻기
description: '분자 hydrogen의 에너지 수준 값을 예측 하는 샘플 Q # 프로그램을 안내 합니다.'
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: b26538980366cf4cbe01fc2ef59580ae182f1e8a
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871571"
---
# <a name="obtaining-energy-level-estimates"></a><span data-ttu-id="69300-103">에너지 수준 추정치 얻기</span><span class="sxs-lookup"><span data-stu-id="69300-103">Obtaining energy level estimates</span></span>
<span data-ttu-id="69300-104">에너지 수준의 값을 예측 하는 것은 퀀텀 화학의 주요 응용 프로그램 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="69300-104">Estimating the values of energy levels is one of the principal applications of quantum chemistry.</span></span> <span data-ttu-id="69300-105">이 문서에서는 분자 hydrogen의 정식 예제에 대해이를 수행 하는 방법을 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-105">This article outlines how you can perform this for the canonical example of molecular hydrogen.</span></span> <span data-ttu-id="69300-106">이 섹션에서 참조 하는 샘플은 [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) 화학 샘플 리포지토리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69300-106">The sample referenced in this section is [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) in the chemistry samples repository.</span></span> <span data-ttu-id="69300-107">출력을 그리는 시각적 예제는 [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogenGUI) 데모입니다.</span><span class="sxs-lookup"><span data-stu-id="69300-107">A more visual example that plots the output is the [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogenGUI) demo.</span></span>

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a><span data-ttu-id="69300-108">분자 hydrogen의 에너지 값 추정</span><span class="sxs-lookup"><span data-stu-id="69300-108">Estimating the energy values of molecular hydrogen</span></span>

<span data-ttu-id="69300-109">첫 번째 단계는 분자 hydrogen를 나타내는 Hamiltonian를 생성 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="69300-109">The first step is to construct the Hamiltonian representing molecular hydrogen.</span></span> <span data-ttu-id="69300-110">NWChem 도구를 사용 하 여이를 생성할 수 있지만, 간단히 하기 위해이 샘플에서는 Hamiltonian 용어를 수동으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-110">Although you can construct this using the NWChem tool, for brevity, this sample adds the Hamiltonian terms manually.</span></span>

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

<span data-ttu-id="69300-111">Hamiltonian를 시뮬레이션 하려면 fermion 연산자를 연산자로 변환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-111">Simulating the Hamiltonian requires converting the fermion operators to qubit operators.</span></span> <span data-ttu-id="69300-112">이러한 변환은 다음과 같이 Wigner 인코딩을 통해 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69300-112">This conversion is performed through the Jordan-Wigner encoding as follows:</span></span>

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

<span data-ttu-id="69300-113">그런 다음 `qSharpData` Hamiltonian를 나타내는을 함수에 전달 `TrotterStepOracle` 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-113">Next, pass `qSharpData`, which represents the Hamiltonian, to the `TrotterStepOracle` function.</span></span> <span data-ttu-id="69300-114">`TrotterStepOracle`Hamiltonian의 실시간 진화에 근사치를 주는 퀀텀 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-114">`TrotterStepOracle` returns a quantum operation that approximates the real-time evolution of the Hamiltonian.</span></span> <span data-ttu-id="69300-115">자세한 내용은 [Hamiltonian Dynamics 시뮬레이션](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69300-115">For more information, see [Simulating Hamiltonian dynamics](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms).</span></span>

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

<span data-ttu-id="69300-116">이제 표준 라이브러리의 [단계 추정 알고리즘](xref:microsoft.quantum.libraries.characterization) 을 사용 하 여 이전 시뮬레이션을 통해 그라운드 상태 에너지를 배울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69300-116">At this point, you can use the standard library's [phase estimation algorithms](xref:microsoft.quantum.libraries.characterization) to learn the ground state energy using the previous simulation.</span></span> <span data-ttu-id="69300-117">이렇게 하려면 퀀텀 접지 상태에 대 한 적절 한 근사값을 준비 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-117">This requires preparing a good approximation to the quantum ground state.</span></span> <span data-ttu-id="69300-118">이러한 근사치에 대 한 제안은 스키마에 제공 됩니다 [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) .</span><span class="sxs-lookup"><span data-stu-id="69300-118">Suggestions for such approximations are provided in the [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) schema.</span></span> <span data-ttu-id="69300-119">그러나 이러한 제안이 없는 경우에는 기본 방법으로 `hamiltonian.NElectrons` 적극적 대각선 파괴을 최소화 하기 위해 여러 개의를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-119">However, absent these suggestions, the default approach adds a number of `hamiltonian.NElectrons` electrons to greedily minimize the diagonal one-electron term energies.</span></span> <span data-ttu-id="69300-120">단계 예측 함수 및 작업은 Microsoft. n a m [. 특성화](xref:microsoft.quantum.characterization) 네임 스페이스의 docfx 표기법으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69300-120">The phase estimation functions and operations are provided in DocFX notation in the [Microsoft.Quantum.Characterization](xref:microsoft.quantum.characterization) namespace.</span></span>

<span data-ttu-id="69300-121">다음 코드 조각에서는 화학 시뮬레이션 라이브러리의 실시간 진화 출력이 퀀텀 단계 예측과 통합 되는 방식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69300-121">The following snippet shows how the real-time evolution output by the chemistry simulation library integrates with quantum phase estimation.</span></span>

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

<span data-ttu-id="69300-122">이제 호스트 프로그램에서 Q # 코드를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69300-122">You can now invoke the Q# code from the host program.</span></span> <span data-ttu-id="69300-123">다음 c # 코드는 전체 상태 시뮬레이터를 만들고를 실행 `GetEnergyByTrotterization` 하 여 그라운드 상태 에너지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69300-123">The following C# code creates a full-state simulator and runs `GetEnergyByTrotterization` to obtain the ground state energy.</span></span>

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

<span data-ttu-id="69300-124">작업은 두 개의 매개 변수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-124">The operation returns two parameters:</span></span> 

- <span data-ttu-id="69300-125">`energyEst`는 그라운드 상태 에너지 추정치 이며 평균에 가까워야 합니다 `-1.137` .</span><span class="sxs-lookup"><span data-stu-id="69300-125">`energyEst` is the estimate of the ground state energy and should be close to `-1.137` on average.</span></span> 
- <span data-ttu-id="69300-126">`phaseEst`단계 추정 알고리즘에서 반환 하는 원시 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="69300-126">`phaseEst` is the raw phase returned by the phase estimation algorithm.</span></span> <span data-ttu-id="69300-127">이는 너무 커서 값으로 인해 발생 하는 별칭을 진단 하는 데 유용 `trotterStep` 합니다.</span><span class="sxs-lookup"><span data-stu-id="69300-127">This useful for diagnosing aliasing when it occurs due to a `trotterStep` value that is too large.</span></span>
