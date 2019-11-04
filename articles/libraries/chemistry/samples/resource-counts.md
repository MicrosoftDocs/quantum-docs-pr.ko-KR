---
title: 리소스 개수 가져오기 | Microsoft Docs
description: 리소스 개수 문서 가져오기
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.resourcecounts
ms.openlocfilehash: f9311c1987ced4336c4e98bdb984fbee009e9acc
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442464"
---
# <a name="obtaining-resource-counts"></a><span data-ttu-id="9238f-103">리소스 개수 가져오기</span><span class="sxs-lookup"><span data-stu-id="9238f-103">Obtaining resource counts</span></span>

<span data-ttu-id="9238f-104">기존 컴퓨터에서 $ 이상 비트 $n 시뮬레이트하는 비용은 $n $로 확대 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-104">The cost of simulating $n$ qubits on classical computers scales exponentially with $n$.</span></span> <span data-ttu-id="9238f-105">이는 전체 상태 시뮬레이터로 수행할 수 있는 퀀텀 화학 시뮬레이션의 크기를 크게 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-105">This greatly limits the size of a quantum chemistry simulation we may perform with the full-state simulator.</span></span> <span data-ttu-id="9238f-106">대량 화학 인스턴스의 경우에도 유용한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-106">For large instances of chemistry, we may nevertheless obtain useful information.</span></span> <span data-ttu-id="9238f-107">여기서는 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 사용 하 여 자동화 된 방식으로 연금술 시뮬레이션에 대 한 T 게이트 또는 cnot 게이트 수와 같은 리소스 비용을 얻을 수 있는 방법을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-107">Here, we examine how resource costs, such as the number of T-gates or CNOT gates, for simulating chemistry may be obtained in an automated fashion using the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="9238f-108">이러한 정보는 퀀텀 컴퓨터가 이러한 퀀텀 화학 알고리즘을 실행 하기에 충분히 큰 경우에 대해 알립니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-108">Such information informs us of when quantum computers might be large enough to run these quantum chemistry algorithms.</span></span> <span data-ttu-id="9238f-109">참조는 제공 된 `GetGateCount` 샘플을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9238f-109">For reference, see the provided `GetGateCount` sample.</span></span>

<span data-ttu-id="9238f-110">[파일 로드](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) 예제에서 설명한 대로 Broombridge 스키마에서 로드 한 `FermionHamiltonian` 인스턴스가 이미 있다고 가정 하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-110">Let us assume that we already have a `FermionHamiltonian` instance, say, loaded from the Broombridge schema as discussed in the [loading-from-file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) example.</span></span> 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

<span data-ttu-id="9238f-111">리소스 예상치를 얻기 위한 구문은 전체 상태 시뮬레이터에서 알고리즘을 실행 하는 것과 거의 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-111">The syntax for obtaining resource estimates is almost identical to running the algorithm on the full-state simulator.</span></span> <span data-ttu-id="9238f-112">다른 대상 컴퓨터를 선택 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-112">We simply choose a different target machine.</span></span> <span data-ttu-id="9238f-113">리소스 추정치의 목적을 위해이는 단일 Trotter 단계의 비용 또는 접미사 기술을 통해 만든 퀀텀 워크를 평가 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-113">For the purposes of resource estimates, it suffices to evaluate the cost of a single Trotter step, or a quantum walk created by the Qubitization technique.</span></span> <span data-ttu-id="9238f-114">이러한 알고리즘을 호출 하는 상용구는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-114">The boilerplate for invoking these algorithms is as follows.</span></span>

```qsharp
//////////////////////////////////////////////////////////////////////////
// Using Trotterization //////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single Trotter step.
operation RunTrotterStep (qSharpData: JordanWignerEncodingData) : Unit {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    // The integrator step size does not affect the gate cost of a single step.
    let trotterStepSize = 1.0;
    
    // Order of integrator
    let trotterOrder = 1;
    let (nQubits, (rescaleFactor, oracle)) = TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // We not allocate qubits an run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
}


//////////////////////////////////////////////////////////////////////////
// Using Qubitization ////////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single qubitization step.
operation RunQubitizationStep (qSharpData: JordanWignerEncodingData) : Double {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nQubits, (l1Norm, oracle)) = QubitizationOracle(qSharpData);
    
    // We now allocate qubits and run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
    
    return l1Norm;
}
```

<span data-ttu-id="9238f-115">이제 원하는 리소스를 추적 하도록 추적 시뮬레이터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-115">We now configure the trace simulator to track the resources we are interested in.</span></span> <span data-ttu-id="9238f-116">이 경우 `usePrimitiveOperationsCounter` 플래그를 `true`설정 하 여 기본 퀀텀 작업의 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-116">In this case, we count primitive quantum operations by setting the `usePrimitiveOperationsCounter` flag to `true`.</span></span> <span data-ttu-id="9238f-117">Q # 코드가 측정 결과의 확률 (있는 경우)을 올바르게 어설션 하지 않는 경우 예외를 방지 하려면 기술 정보 `throwOnUnconstraintMeasurement` `false`로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-117">A technical detail `throwOnUnconstraintMeasurement` is set to `false` to avoid exceptions in cases where the Q# code does not correctly assert of probability of measurement outcomes, if any are performed.</span></span>

```csharp
private static QCTraceSimulator CreateAndConfigureTraceSim()
{
    // Create and configure Trace Simulator
    var config = new QCTraceSimulatorConfiguration()
    {
        usePrimitiveOperationsCounter = true,
        throwOnUnconstraintMeasurement = false
    };

    return new QCTraceSimulator(config);
}
```

<span data-ttu-id="9238f-118">이제 다음과 같이 드라이버 프로그램에서 퀀텀 알고리즘을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9238f-118">We now run the quantum algorithm from the driver program as follows.</span></span>

```csharp
// Instantiate a trace simulator instance
QCTraceSimulator sim = CreateAndConfigureTraceSim();

// Run the quantum algorithm on the trace simulator.
RunQubitizationStep.Run(sim, qSharpData);

// Print all resource counts to file.
var gateStats = sim.ToCSV();
foreach (var x in gateStats)
{
    System.IO.File.WriteAllLines($"QubitizationGateCountEstimates.{x.Key}.csv", new string[] { x.Value });
}
```