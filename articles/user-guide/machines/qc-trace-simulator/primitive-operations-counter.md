---
title: 기본 작업 카운터-퀀텀 개발 키트
description: 퀀텀 추적 시뮬레이터를 사용 하 여 프로그램의 작업에서 사용 되는 기본 프로세스를 추적 하는 Microsoft QDK 기본 작업 카운터에 대해 알아봅니다 Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 19ea3c1f5a91c00de4d3e435318bf4cf8cdd83be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858597"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a><span data-ttu-id="0649b-103">퀀텀 추적 시뮬레이터: 기본 작업 카운터</span><span class="sxs-lookup"><span data-stu-id="0649b-103">Quantum trace simulator: primitive operations counter</span></span>

<span data-ttu-id="0649b-104">기본 작업 카운터는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-104">The primitive operation counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="0649b-105">퀀텀 프로그램에서 호출 된 모든 작업에서 사용 되는 기본 프로세스의 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-105">It counts the number of primitive processes used by every operation invoked in a quantum program.</span></span> 

<span data-ttu-id="0649b-106">모든 <xref:Microsoft.Quantum.Intrinsic> 연산은 단일 비트 회전, T 작업, 단일가 Clifford 작업, CNOT 작업 및 여러 가지 관찰 가능 개체의 측정값으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-106">All <xref:Microsoft.Quantum.Intrinsic> operations are expressed in terms of single-qubit rotations, T operations, single-qubit Clifford operations, CNOT operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="0649b-107">기본 작업 카운터는 작업 [호출 그래프](https://en.wikipedia.org/wiki/Call_graph)의 모든 가장자리에 대 한 통계를 집계 하 고 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-107">The Primitive Operations Counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

## <a name="invoking-the-primitive-operation-counter"></a><span data-ttu-id="0649b-108">기본 작업 카운터 호출</span><span class="sxs-lookup"><span data-stu-id="0649b-108">Invoking the primitive operation counter</span></span>

<span data-ttu-id="0649b-109">기본 작업 카운터를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UsePrimitiveOperationsCounter` 속성을 **true** 로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="0649b-109">To run the quantum trace simulator with the primitive operation counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UsePrimitiveOperationsCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span>

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a><span data-ttu-id="0649b-110">C # 호스트 프로그램에서 기본 작업 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="0649b-110">Using the primitive operation counter in a C# host program</span></span>

<span data-ttu-id="0649b-111">이 단원의 뒷부분에 나오는 c # 예제에서는 <xref:Microsoft.Quantum.Intrinsic.T> <xref:Microsoft.Quantum.Intrinsic.CCNOT> 다음 샘플 코드를 기반으로 작업을 구현 하는 데 필요한 작업 수를 계산 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="0649b-111">The C# example that follows in this section counts how many <xref:Microsoft.Quantum.Intrinsic.T> operations are needed to implement the <xref:Microsoft.Quantum.Intrinsic.CCNOT> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="0649b-112">에서 일곱 개의 `CCNOT` 작업이 필요 하 `T` 고 `ApplySampleWithCCNOT` 8 개의 작업을 실행 하는지 확인 하려면 `T` 다음 c # 코드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-112">To check that `CCNOT` requires seven `T` operations and that `ApplySampleWithCCNOT` runs eight `T` operations, use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="0649b-113">프로그램의 첫 번째 부분을 실행 `ApplySampleWithCCNOT` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-113">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="0649b-114">두 번째 부분에서는 메서드를 사용 하 [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) `T` 여에서 실행 되는 작업 수를 검색 합니다 `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="0649b-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of `T` operations run by `ApplySampleWithCCNOT`:</span></span> 

<span data-ttu-id="0649b-115">`GetMetric`두 개의 형식 매개 변수를 사용 하 여를 호출 하면 지정 된 호출 그래프 가장자리와 연결 된 메트릭의 값이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-115">When you call `GetMetric` with two type parameters, it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="0649b-116">위의 예제에서 프로그램은 `Primitive.CCNOT` 내에서 작업을 호출 `ApplySampleWithCCNOT` 하므로 호출 그래프는에 지를 포함 합니다 `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="0649b-116">In the preceding example, the program calls the `Primitive.CCNOT` operation  within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="0649b-117">사용 된 작업 수를 검색 하려면 `CNOT` 다음 줄을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-117">To retrieve the number of `CNOT` operations used, add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="0649b-118">마지막으로, 다음을 사용 하 여 기본 작업 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-118">Finally, you can output all the statistics collected by the Primitive Operations Counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="0649b-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0649b-119">See also</span></span>

- <span data-ttu-id="0649b-120">퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.</span><span class="sxs-lookup"><span data-stu-id="0649b-120">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="0649b-121"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="0649b-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="0649b-123"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="0649b-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API reference.</span></span>