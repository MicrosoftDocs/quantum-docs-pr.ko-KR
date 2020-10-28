---
title: 퀀텀 추적 시뮬레이터 - Quantum Development Kit
description: 'Microsoft 양자 컴퓨터 추적 시뮬레이터를 사용하여 클래식 코드를 디버그하고 :::no-loc(Q#)::: 프로그램의 리소스 요구 사항을 예측하는 방법을 알아봅니다.'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 2e2d9f8494d8709fba34123793cecce4011b609a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690830"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a><span data-ttu-id="93268-103">Microsoft QDK(Quantum Development Kit) 퀀텀 추적 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="93268-103">Microsoft Quantum Development Kit (QDK) quantum trace simulator</span></span>

<span data-ttu-id="93268-104">QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 클래스는 실제로 양자 컴퓨터의 상태를 시뮬레이션하지 않고 양자 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-104">The QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> class runs a quantum program without actually simulating the state of a quantum computer.</span></span> <span data-ttu-id="93268-105">이러한 이유로 퀀텀 추적 시뮬레이터는 수천 큐비트를 사용하는 양자 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-105">For this reason, the quantum trace simulator is able to run quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="93268-106">이러한 방식은 다음 두 가지 주요 목적에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="93268-107">양자 프로그램에 속하는 클래식 코드 디버그</span><span class="sxs-lookup"><span data-stu-id="93268-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="93268-108">양자 컴퓨터에서 지정된 양자 프로그램 인스턴스를 실행하는 데 필요한 리소스 예측</span><span class="sxs-lookup"><span data-stu-id="93268-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span> <span data-ttu-id="93268-109">실제로 더 제한적인 메트릭 집합을 제공하는 [리소스 예측 도구](xref:microsoft.quantum.machines.resources-estimator)는 추적 시뮬레이터를 기반으로 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="93268-109">In fact, the [Resources estimator](xref:microsoft.quantum.machines.resources-estimator), which provides a more limited set of metrics, is built upon the trace simulator.</span></span>

## <a name="invoking-the-quantum-trace-simulator"></a><span data-ttu-id="93268-110">퀀텀 추적 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="93268-110">Invoking the quantum trace simulator</span></span>

<span data-ttu-id="93268-111">퀀텀 추적 시뮬레이터를 사용하여 모든 :::no-loc(Q#)::: 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-111">You can use the quantum trace simulator to run any :::no-loc(Q#)::: operation.</span></span>

<span data-ttu-id="93268-112">다른 대상 컴퓨터와 마찬가지로 먼저 `QCTraceSimulator` 클래스의 인스턴스를 만든 다음, 이를 작업의 `Run` 메서드의 첫 번째 매개 변수로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-112">As with other target machines, you first create an instance of the `QCTraceSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="93268-113">`QuantumSimulator` 클래스와 달리 `QCTraceSimulator` 클래스는 <xref:System.IDisposable> 인터페이스를 구현하지 않으므로 `using` 문 내에 묶을 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-113">Note that, unlike the `QuantumSimulator` class, the `QCTraceSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="93268-114">측정 결과의 확률 제공</span><span class="sxs-lookup"><span data-stu-id="93268-114">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="93268-115">퀀텀 추적 시뮬레이터는 실제 퀀텀 상태를 시뮬레이션하지 않으므로 작업 내에서 측정 결과의 확률을 계산할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-115">Because the quantum trace simulator does not simulate the actual quantum state, it cannot calculate the probability of measurement outcomes within an operation.</span></span> 

<span data-ttu-id="93268-116">따라서 작업에 측정값이 포함된 경우 <xref:Microsoft.Quantum.Diagnostics> 네임스페이스의 <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> 작업을 사용하여 이러한 확률을 명시적으로 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-116">Therefore, if an operation includes measurements, you must explicitly provide these probabilities using the <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> operation from the <xref:Microsoft.Quantum.Diagnostics> namespace.</span></span> <span data-ttu-id="93268-117">다음 예제에서는 이에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-117">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="93268-118">퀀텀 추적 시뮬레이터가 `AssertMeasurementProbability`를 만날 때 `source` 및 `q`에서 `PauliZ`를 측정하면 **0.5** 의 확률로 `Zero`를 제공하는 것으로 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-118">When the quantum trace simulator encounters `AssertMeasurementProbability` it records that measuring `PauliZ` on `source` and `q` should give an outcome of `Zero`, with probability **0.5** .</span></span> <span data-ttu-id="93268-119">나중에 `M` 작업을 실행할 때, 결과 확률의 기록된 값을 찾고 `M`은 **0.5** 의 확률로 `Zero` 또는 `One`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-119">When it runs the `M` operation later, it finds the recorded values of the outcome probabilities, and `M` returns `Zero` or `One`, with probability **0.5** .</span></span> <span data-ttu-id="93268-120">퀀텀 상태를 추적하는 시뮬레이터에서 동일한 코드를 실행하는 경우, 해당 시뮬레이터는 `AssertMeasurementProbability`의 제공된 확률이 올바른지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-120">When the same code runs on a simulator that keeps track of the quantum state, that simulator checks that the provided probabilities in `AssertMeasurementProbability` are correct.</span></span>

<span data-ttu-id="93268-121">`AssertMeasurementProbability`를 사용하여 주석을 달지 않은 측정 작업이 하나 이상 있는 경우 시뮬레이터는 [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception)을 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="93268-121">Note that if there is at least one measurement operation that is not annotated using `AssertMeasurementProbability`, the simulator throws an [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span></span>

## <a name="quantum-trace-simulator-tools"></a><span data-ttu-id="93268-122">퀀텀 추적 시뮬레이터 도구</span><span class="sxs-lookup"><span data-stu-id="93268-122">Quantum trace simulator tools</span></span>

<span data-ttu-id="93268-123">QDK에는 퀀텀 추적 시뮬레이터에서 프로그램의 버그를 검색하고 양자 프로그램 리소스 예상치를 수행하는 데 사용할 수 있는 5가지 도구가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-123">The QDK includes five tools that you can use with the quantum trace simulator to detect bugs in your programs and perform quantum program resource estimates:</span></span> 

|<span data-ttu-id="93268-124">도구</span><span class="sxs-lookup"><span data-stu-id="93268-124">Tool</span></span> | <span data-ttu-id="93268-125">설명</span><span class="sxs-lookup"><span data-stu-id="93268-125">Description</span></span> |
|-----| -----|
|[<span data-ttu-id="93268-126">고유 입력 검사기</span><span class="sxs-lookup"><span data-stu-id="93268-126">Distinct inputs checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |<span data-ttu-id="93268-127">공유된 큐비트와의 충돌 가능성이 있는지 검사</span><span class="sxs-lookup"><span data-stu-id="93268-127">Checks for potential conflicts with shared qubits</span></span> |
|[<span data-ttu-id="93268-128">무효화된 큐비트 사용 검사기</span><span class="sxs-lookup"><span data-stu-id="93268-128">Invalidated qubits use checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |<span data-ttu-id="93268-129">프로그램이 이미 릴리스된 큐비트에 작업을 적용하는지 검사</span><span class="sxs-lookup"><span data-stu-id="93268-129">Checks if the program applies an operation to a qubit that is already released</span></span> |
|[<span data-ttu-id="93268-130">기본 연산 카운터</span><span class="sxs-lookup"><span data-stu-id="93268-130">Primitive operations counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | <span data-ttu-id="93268-131">퀀텀 프로그램에서 호출된 모든 작업에서 사용되는 기본 형식 수 계산</span><span class="sxs-lookup"><span data-stu-id="93268-131">Counts the number of primitives used by every operation invoked in a quantum program</span></span>  |
|[<span data-ttu-id="93268-132">깊이 카운터</span><span class="sxs-lookup"><span data-stu-id="93268-132">Depth counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |<span data-ttu-id="93268-133">양자 프로그램에서 호출된 모든 작업 깊이의 하한을 나타내는 개수를 수집</span><span class="sxs-lookup"><span data-stu-id="93268-133">Gathers counts that represent the lower bound of the depth of every operation invoked in a quantum program</span></span>   |
|[<span data-ttu-id="93268-134">너비 카운터</span><span class="sxs-lookup"><span data-stu-id="93268-134">Width counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |<span data-ttu-id="93268-135">양자 프로그램에서 각 작업에 의해 할당되고 빌린 큐비트 수를 계산</span><span class="sxs-lookup"><span data-stu-id="93268-135">Counts the number of qubits allocated and borrowed by each operation in a quantum program</span></span> |

<span data-ttu-id="93268-136">이러한 각 도구는 `QCTraceSimulatorConfiguration`에서 적절한 플래그를 설정한 다음, 구성을 `QCTraceSimulator` 선언에 전달하면 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-136">Each of these tools is enabled by setting appropriate flags in `QCTraceSimulatorConfiguration` and then passing the configuration to the `QCTraceSimulator` declaration.</span></span> <span data-ttu-id="93268-137">이러한 각 도구를 사용하는 방법에 대한 자세한 내용은 위의 목록에 있는 링크를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93268-137">For information on using each of these tools, see the links in the preceding list.</span></span> <span data-ttu-id="93268-138">`QCTraceSimulator`를 구성하는 방법에 대한 자세한 내용은 [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93268-138">For more information about configuring `QCTraceSimulator`, see [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span></span>

## <a name="qctracesimulator-methods"></a><span data-ttu-id="93268-139">QCTraceSimulator 메서드</span><span class="sxs-lookup"><span data-stu-id="93268-139">QCTraceSimulator methods</span></span>

<span data-ttu-id="93268-140">`QCTraceSimulator`에는 퀀텀 작업 중 추적된 메트릭의 값을 검색하는 몇 가지 기본 제공 메서드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-140">`QCTraceSimulator` has several built-in methods to retrieve the values of the metrics tracked during a quantum operation.</span></span> <span data-ttu-id="93268-141">[QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) 및 [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) 메서드의 예는 [기본 작업 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [깊이 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) 및 [너비 카운터](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) 문서에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93268-141">Examples of the [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) and the [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) methods can be found in the [Primitive operations counter](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter), and [Width counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) articles.</span></span> <span data-ttu-id="93268-142">사용 가능한 모든 메서드에 대한 자세한 내용은 :::no-loc(Q#)::: API 참조의 [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93268-142">For more information on all available methods, see [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in the :::no-loc(Q#)::: API reference.</span></span>  

## <a name="see-also"></a><span data-ttu-id="93268-143">참고 항목</span><span class="sxs-lookup"><span data-stu-id="93268-143">See also</span></span>

- [<span data-ttu-id="93268-144">퀀텀 리소스 예측 도구</span><span class="sxs-lookup"><span data-stu-id="93268-144">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="93268-145">퀀텀 Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="93268-145">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="93268-146">퀀텀 전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="93268-146">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 