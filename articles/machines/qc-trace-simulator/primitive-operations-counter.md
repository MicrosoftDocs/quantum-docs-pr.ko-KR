---
title: 기본 작업 카운터 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 퀀텀 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: b7ec8b0d7a713051e36cb778c087050f0257710f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184885"
---
# <a name="primitive-operations-counter"></a><span data-ttu-id="50783-103">기본 작업 카운터</span><span class="sxs-lookup"><span data-stu-id="50783-103">Primitive Operations Counter</span></span>  

<span data-ttu-id="50783-104">`Primitive Operations Counter`는 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="50783-104">The `Primitive Operations Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="50783-105">퀀텀 프로그램에서 호출 된 모든 작업에서 사용 되는 기본 실행 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="50783-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> <span data-ttu-id="50783-106">`Microsoft.Quantum.Primitive`의 모든 작업은 단일 고 비트 회전, T 게이트, 단일 관찰 가능 개체 게이트, CNOT 게이트 및 여러의 측정값으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50783-106">All operations from `Microsoft.Quantum.Primitive` are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="50783-107">수집 된 통계는 작업 호출 그래프의 가장자리에 걸쳐 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50783-107">Collected statistics are aggregated over the edges of the operations call graph.</span></span> <span data-ttu-id="50783-108">이제 `CCNOT` 작업을 구현 하는 데 필요한 `T` 게이트 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="50783-108">Let us now count how many `T` gates are needed to implement the `CCNOT` operation.</span></span> 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a><span data-ttu-id="50783-109">C# 프로그램 내에서 기본 작업 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="50783-109">Using the Primitive Operations Counter within a C# Program</span></span>

<span data-ttu-id="50783-110">`CCNOT` 실제로 7 개의 `T` 게이트가 필요 하 고 `CCNOTDriver` 8 `T` 게이트를 실행 하는 것을 확인 하려면 C# 다음 코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50783-110">To check that `CCNOT` indeed requires 7 `T` gates and that `CCNOTDriver` executes 8 `T` gates we can use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="50783-111">프로그램의 첫 번째 부분은 `CCNOTDriver`를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="50783-111">The first part of the program executes `CCNOTDriver`.</span></span> <span data-ttu-id="50783-112">두 번째 부분에서는 메서드 `QCTraceSimulator.GetMetric`를 사용 하 여 `CCNOTDriver`에서 실행 되는 T 게이트 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50783-112">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the number of T gates executed by `CCNOTDriver`:</span></span> 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="50783-113">두 개의 형식 매개 변수를 사용 하 여 `GetMetric`를 호출 하면 지정 된 호출 그래프 가장자리와 연결 된 메트릭의 값이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50783-113">When `GetMetric` is called with two type parameters it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="50783-114">이 예제에서는 `Primitive.CCNOT` 작업을 `CCNOTDriver` 내에서 호출 하므로 호출 그래프에는에 지 `<Primitive.CCNOT,CCNOTDriver>`가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50783-114">In our example operation `Primitive.CCNOT` is called within `CCNOTDriver` and therefore the call graph contains the edge `<Primitive.CCNOT,CCNOTDriver>`.</span></span> 

<span data-ttu-id="50783-115">사용 되는 `CNOT` 게이트 수를 얻기 위해 다음 줄을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50783-115">To get the number of `CNOT` gates used, we can add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="50783-116">마지막으로 게이트 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력 하려면 다음을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50783-116">Finally, to output all the statistics collected by the gate counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="50783-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="50783-117">See also</span></span> ##

- <span data-ttu-id="50783-118">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="50783-118">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
