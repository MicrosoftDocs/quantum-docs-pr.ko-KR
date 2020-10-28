---
title: 깊이 카운터-퀀텀 개발 키트
description: '퀀텀 추적 시뮬레이터를 사용 하 여 프로그램에서 호출 된 모든 작업의 깊이 수를 수집 하는 Microsoft QDK depth 카운터에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 89d8a2c9f2ecd5c5332215cd4307bcf4a6422036
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692100"
---
# <a name="quantum-trace-simulator-depth-counter"></a><span data-ttu-id="48fcd-103">퀀텀 추적 시뮬레이터: 깊이 카운터</span><span class="sxs-lookup"><span data-stu-id="48fcd-103">Quantum trace simulator: depth counter</span></span>

<span data-ttu-id="48fcd-104">Depth 카운터는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-104">The depth counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="48fcd-105">이를 사용 하 여 퀀텀 프로그램에서 호출 된 모든 작업의 깊이 상한을 나타내는 개수를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-105">You can use it to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> 

## <a name="depth-values"></a><span data-ttu-id="48fcd-106">깊이 값</span><span class="sxs-lookup"><span data-stu-id="48fcd-106">Depth values</span></span>

<span data-ttu-id="48fcd-107">기본적으로 모든 작업은 깊이가 1 인 작업을 제외 하 고 깊이가 **0** 입니다 `T` . **1**</span><span class="sxs-lookup"><span data-stu-id="48fcd-107">By default, all operations have a depth of **0** except the `T` operation, which has a depth of **1** .</span></span> <span data-ttu-id="48fcd-108">즉, 기본적으로 `T` 작업 수준도 계산 됩니다 (종종 바람직한 경우).</span><span class="sxs-lookup"><span data-stu-id="48fcd-108">This means that by default, only the `T` depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="48fcd-109">수준 카운터는 작업 [호출 그래프](https://en.wikipedia.org/wiki/Call_graph)의 모든 가장자리에 대 한 통계를 집계 하 고 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-109">The depth counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

<span data-ttu-id="48fcd-110">모든 <xref:Microsoft.Quantum.Intrinsic> 연산은 단일 비트 회전, <xref:Microsoft.Quantum.Intrinsic.T> 작업, 단일가 Clifford 작업, <xref:Microsoft.Quantum.Intrinsic.CNOT> 작업 및 다중 기능 비트 pauli 관찰 가능 개체의 측정값으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-110">All <xref:Microsoft.Quantum.Intrinsic> operations are expressed in terms of single-qubit rotations, <xref:Microsoft.Quantum.Intrinsic.T> operations, single-qubit Clifford operations, <xref:Microsoft.Quantum.Intrinsic.CNOT> operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="48fcd-111">사용자는의 필드를 통해 각 기본 작업에 대 한 깊이를 설정할 수 있습니다 `gateTimes` <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="48fcd-111">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

## <a name="invoking-the-depth-counter"></a><span data-ttu-id="48fcd-112">수준 카운터 호출</span><span class="sxs-lookup"><span data-stu-id="48fcd-112">Invoking the depth counter</span></span>

<span data-ttu-id="48fcd-113">Depth 카운터를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> 해당 `UseDepthCounter` 속성을 **true** 로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="48fcd-113">To run the quantum trace simulator with the depth counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set its `UseDepthCounter` property to **true** , and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a><span data-ttu-id="48fcd-114">C # 호스트 프로그램에서 depth 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="48fcd-114">Using the depth counter in a C# host program</span></span>

<span data-ttu-id="48fcd-115">이 단원의 뒷부분에 나오는 c # 예제에서는 `T` `CCNOT` 다음 샘플 코드에 따라 작업의 깊이를 계산 합니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="48fcd-115">The C# example that follows in this section computes the `T` depth of the `CCNOT` operation, based on the following :::no-loc(Q#)::: sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="48fcd-116">에 `CCNOT` `T` 깊이 **5** 가 있고 `ApplySampleWithCCNOT` 깊이 6이 있는지 확인 하려면 `T` 다음 c # 코드를 사용 합니다. **6**</span><span class="sxs-lookup"><span data-stu-id="48fcd-116">To check that `CCNOT` has `T` depth **5** and `ApplySampleWithCCNOT` has `T` depth **6** , use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="48fcd-117">프로그램의 첫 번째 부분을 실행 `ApplySampleWithCCNOT` 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-117">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="48fcd-118">두 번째 부분에서는 메서드를 사용 하 여 [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) `T` 및의 깊이를 검색 합니다 `CCNOT` `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="48fcd-118">The second part uses the [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`.</span></span> 

<span data-ttu-id="48fcd-119">마지막으로, 다음을 사용 하 여 깊이 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-119">Finally, you can output all the statistics collected by the depth counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="48fcd-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="48fcd-120">See also</span></span>

- <span data-ttu-id="48fcd-121">퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.</span><span class="sxs-lookup"><span data-stu-id="48fcd-121">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="48fcd-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="48fcd-123"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="48fcd-124"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="48fcd-124">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API reference.</span></span>
