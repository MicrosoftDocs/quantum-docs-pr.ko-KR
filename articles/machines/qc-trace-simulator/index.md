---
title: 양자 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 양자 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 929745a6da6034599e97d2f573190308fde6eb75
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820439"
---
# <a name="quantum-trace-simulator"></a><span data-ttu-id="c2b8d-103">양자 추적 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="c2b8d-103">Quantum Trace Simulator</span></span>

<span data-ttu-id="c2b8d-104">Microsoft 양자 컴퓨터 추적 시뮬레이터는 실제로 양자 컴퓨터의 상태를 시뮬레이트하지 않고 양자 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-104">The Microsoft quantum computer trace simulator executes a quantum program without actually simulating the state of a quantum computer.</span></span>  <span data-ttu-id="c2b8d-105">이러한 이유로 추적 시뮬레이터는 수천 큐비트를 사용하는 양자 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-105">For this reason, the trace simulator can execute quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="c2b8d-106">이러한 방식은 다음 두 가지 주요 목적에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="c2b8d-107">양자 프로그램에 속하는 클래식 코드 디버그</span><span class="sxs-lookup"><span data-stu-id="c2b8d-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="c2b8d-108">양자 컴퓨터에서 지정된 양자 프로그램 인스턴스를 실행하는 데 필요한 리소스 예측</span><span class="sxs-lookup"><span data-stu-id="c2b8d-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span>

<span data-ttu-id="c2b8d-109">추적 시뮬레이터는 측정을 수행해야 할 때 사용자가 제공하는 추가 정보에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-109">The trace simulator relies on additional information provided by the user when measurements must be performed.</span></span> <span data-ttu-id="c2b8d-110">이에 대한 자세한 내용은 [측정 결과의 확률 제공](#providing-the-probability-of-measurement-outcomes)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-110">See Section [Providing the probability of measurement outcomes](#providing-the-probability-of-measurement-outcomes) for more details on this.</span></span> 

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="c2b8d-111">측정 결과의 확률 제공</span><span class="sxs-lookup"><span data-stu-id="c2b8d-111">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="c2b8d-112">양자 알고리즘에는 두 가지 종류의 측정값이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-112">There are two kinds of measurements that appear in quantum algorithms.</span></span> <span data-ttu-id="c2b8d-113">첫 번째 종류는 사용자가 일반적으로 결과의 확률을 알고 있는 경우에 보조적 역할을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-113">The first kind plays an auxiliary role where the user usually knows the probability of the outcomes.</span></span> <span data-ttu-id="c2b8d-114">이 경우 사용자는 이 정보를 나타내기 위해 <xref:microsoft.quantum.intrinsic> 네임스페이스의 <xref:microsoft.quantum.intrinsic.assertprob>을 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-114">In this case the user can write <xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace to express this knowledge.</span></span> <span data-ttu-id="c2b8d-115">다음 예제에서는 이에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-115">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="c2b8d-116">추적 시뮬레이터가 `AssertProb`를 실행할 때 `source` 및 `q`에 대해 `PauliZ`를 측정하면 확률이 0.5일 때 `Zero` 결과가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-116">When the trace simulator executes `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="c2b8d-117">시뮬레이터는 나중에 `M`을 실행할 경우 기록된 결과 확률 값을 찾을 수 있으며 `M`은 확률이 0.5일 때 `Zero` 또는 `One`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-117">When the simulator executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span> <span data-ttu-id="c2b8d-118">양자 상태를 추적하는 동일한 코드를 시뮬레이터에서 실행하는 경우 이러한 시뮬레이터는 `AssertProb`의 제공된 확률이 올바른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-118">When the same code is executed on a simulator that keeps track of the quantum state, such a simulator will check that the provided probabilities in `AssertProb` are correct.</span></span>

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a><span data-ttu-id="c2b8d-119">양자 컴퓨터 추적 시뮬레이터를 사용하여 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="c2b8d-119">Running your Program with the Quantum Computer Trace Simulator</span></span> 

<span data-ttu-id="c2b8d-120">양자 컴퓨터 추적 시뮬레이터는 단지 다른 대상 컴퓨터로 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-120">The quantum computer trace simulator may be viewed as just another target machine.</span></span> <span data-ttu-id="c2b8d-121">이를 사용하기 위한 C# 드라이버 프로그램은 다른 양자 시뮬레이터용 드라이버 프로그램과 매우 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-121">The C# driver program for using it is very similar to the one for any other quantum Simulator:</span></span> 

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="c2b8d-122">`AssertProb`을 사용하여 주석이 추가되지 않은 측정값이 하나 이상 있는 경우 시뮬레이터는 `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` 네임스페이스에서 `UnconstrainedMeasurementException`을 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-122">Note that if there is at least one measurement not annotated using `AssertProb`, the simulator will throw `UnconstrainedMeasurementException` from the `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` namespace.</span></span> <span data-ttu-id="c2b8d-123">자세한 내용은 [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException)에 대한 API 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-123">See the API documentation on [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) for more details.</span></span>

<span data-ttu-id="c2b8d-124">추적 시뮬레이터는 양자 프로그램을 실행하는 것 외에도, 프로그램의 버그를 감지하고, 양자 프로그램 리소스 예측을 수행하기 위한 5가지 구성 요소를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-124">In addition to running quantum programs, the trace simulator comes with five components for detecting bugs in programs and performing quantum program resource estimates:</span></span> 

* [<span data-ttu-id="c2b8d-125">고유 입력 검사기</span><span class="sxs-lookup"><span data-stu-id="c2b8d-125">Distinct Inputs Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [<span data-ttu-id="c2b8d-126">무효화된 큐비트 사용 검사기</span><span class="sxs-lookup"><span data-stu-id="c2b8d-126">Invalidated Qubits Use Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [<span data-ttu-id="c2b8d-127">기본 연산 카운터</span><span class="sxs-lookup"><span data-stu-id="c2b8d-127">Primitive Operations Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [<span data-ttu-id="c2b8d-128">회로 깊이 카운터</span><span class="sxs-lookup"><span data-stu-id="c2b8d-128">Circuit Depth Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [<span data-ttu-id="c2b8d-129">회로 너비 카운터</span><span class="sxs-lookup"><span data-stu-id="c2b8d-129">Circuit Width Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

<span data-ttu-id="c2b8d-130">이러한 각 구성 요소는 `QCTraceSimulatorConfiguration`에서 적절한 플래그를 설정하여 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-130">Each of these components may be enabled by setting appropriate flags in `QCTraceSimulatorConfiguration`.</span></span> <span data-ttu-id="c2b8d-131">이러한 각 구성 요소를 사용하는 방법에 대한 자세한 내용은 해당 참조 파일에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-131">More details about using each of these components are provided in the corresponding reference files.</span></span> <span data-ttu-id="c2b8d-132">구체적인 세부 정보는 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration)에 대한 API 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2b8d-132">See the API documentation on [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for specific details.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2b8d-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c2b8d-133">See also</span></span>
<span data-ttu-id="c2b8d-134">양자 컴퓨터 [추적 시뮬레이터](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# 참조</span><span class="sxs-lookup"><span data-stu-id="c2b8d-134">The quantum computer [trace simulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# reference</span></span> 

