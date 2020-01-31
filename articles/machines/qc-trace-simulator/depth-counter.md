---
title: 깊이 카운터 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 양자 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 07f927c794e2c62e53e4e053b5bc683d24bbed8d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820473"
---
# <a name="depth-counter"></a><span data-ttu-id="cc24e-103">수준 카운터</span><span class="sxs-lookup"><span data-stu-id="cc24e-103">Depth Counter</span></span>

<span data-ttu-id="cc24e-104">`Depth Counter`는 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="cc24e-105">퀀텀 프로그램에서 호출 된 모든 작업의 깊이 수를 수집 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-105">It is used to gather counts of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="cc24e-106"><xref:microsoft.quantum.intrinsic>의 모든 작업은 단일 고 비트 회전, T 게이트, 단일 관찰 가능 개체 게이트, CNOT 게이트 및 여러의 측정값으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="cc24e-107">사용자는 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>의 `gateTimes` 필드를 통해 각 기본 작업에 대 한 깊이를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="cc24e-108">기본적으로 모든 작업에는 깊이 1이 있는 T 게이트를 제외 하 고 깊이 0이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="cc24e-109">즉, 기본적으로 작업의 T 수준만 계산 됩니다 (종종 바람직한 경우).</span><span class="sxs-lookup"><span data-stu-id="cc24e-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="cc24e-110">수집 된 통계는 작업 호출 그래프의 모든 가장자리에 걸쳐 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="cc24e-111">이제 <xref:microsoft.quantum.intrinsic.ccnot> 작업의 <xref:microsoft.quantum.intrinsic.t> 깊이를 계산 해 보세요.</span><span class="sxs-lookup"><span data-stu-id="cc24e-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="cc24e-112">다음 Q # 샘플 코드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-112">We will use the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="cc24e-113">C# 프로그램 내에서 Depth 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="cc24e-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="cc24e-114">`CCNOT`에 `T` 깊이가 5이 고 `ApplySampleWithCCNOT` `T` 깊이 6이 있는지 확인 하려면 다음 C# 코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-114">To check that `CCNOT` has `T` depth 5 and `ApplySampleWithCCNOT` has `T` depth 6 we can use the following C# code:</span></span>

```csharp 
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="cc24e-115">프로그램의 첫 번째 부분은 `ApplySampleWithCCNOT`를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-115">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="cc24e-116">두 번째 부분에서는 메서드 `QCTraceSimulator.GetMetric` 사용 하 여 `CCNOT` 및 `ApplySampleWithCCNOT`의 `T` 깊이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="cc24e-117">마지막으로 `Depth Counter` 여 수집 된 모든 통계를 CSV 형식으로 출력 하려면 다음을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="cc24e-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cc24e-118">See also</span></span> ##

- <span data-ttu-id="cc24e-119">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="cc24e-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
