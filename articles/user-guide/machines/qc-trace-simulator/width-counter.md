---
title: Width 카운터-퀀텀 개발 키트
description: '퀀텀 추적 시뮬레이터를 사용 하 여 프로그램의 작업에 의해 할당 되 고 사용 되는 수를 계산 하는 Microsoft QDK width 카운터에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: e54e92cc4a76ce9f9c5aead84f2b64320d6b4f1c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691122"
---
# <a name="quantum-trace-simulator-width-counter"></a><span data-ttu-id="b41aa-103">퀀텀 추적 시뮬레이터: width 카운터</span><span class="sxs-lookup"><span data-stu-id="b41aa-103">Quantum trace simulator: width counter</span></span>

<span data-ttu-id="b41aa-104">Width 카운터는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-104">The width counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="b41aa-105">이를 사용 하 여 프로그램의 각 작업에서 할당 되 고 사용 되는 것과 같은 수를 계산할 수 있습니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="b41aa-105">You can use it to count the number of qubits allocated and borrowed by each operation in a :::no-loc(Q#)::: program.</span></span> <span data-ttu-id="b41aa-106">일부 기본 작업에서는 제어 되는 작업 또는 제어 된 작업을 곱하는 등의 추가 기능을 할당할 수 있습니다 `X` `T` .</span><span class="sxs-lookup"><span data-stu-id="b41aa-106">Some primitive operations can allocate extra qubits, for example, multiply controlled `X` operations or controlled `T` operations.</span></span>

## <a name="invoking-the-width-counter"></a><span data-ttu-id="b41aa-107">Width 카운터 호출</span><span class="sxs-lookup"><span data-stu-id="b41aa-107">Invoking the width counter</span></span>

<span data-ttu-id="b41aa-108">Width 카운터를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UseWidthCounter` 속성을 **true** 로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="b41aa-108">To run the quantum trace simulator with the width counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseWidthCounter` property to **true** , and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a><span data-ttu-id="b41aa-109">C # 호스트 프로그램에서 width 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="b41aa-109">Using the width counter in a C# host program</span></span>

<span data-ttu-id="b41aa-110">이 단원의 뒷부분에 나오는 c # 예제에서는 <xref:Microsoft.Quantum.Intrinsic.X> 다음 샘플 코드에 따라 곱하기 제어 작업의 구현에 의해 할당 된 추가 작업의 수를 계산 합니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="b41aa-110">The C# example that follows in this section computes the number of extra qubits allocated by the implementation of a multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation, based on the following :::no-loc(Q#)::: sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

<span data-ttu-id="b41aa-111">곱하기 제어 <xref:Microsoft.Quantum.Intrinsic.X> 연산은 총 5 개에 해당 하는 작업을 수행 하 고 두 [보조](xref:microsoft.quantum.glossary#ancilla)비트를 할당 하며 입력 너비가 **5** 입니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-111">The multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation acts on a total of five qubits, allocates two [ancillary qubits](xref:microsoft.quantum.glossary#ancilla), and has an input width of **5** .</span></span> <span data-ttu-id="b41aa-112">다음 c # 프로그램을 사용 하 여 개수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-112">Use the following C# program to verify the counts:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="b41aa-113">프로그램의 첫 번째 부분에서 작업을 실행 합니다 `ApplyMultiControlledX` .</span><span class="sxs-lookup"><span data-stu-id="b41aa-113">The first part of the program runs the `ApplyMultiControlledX` operation.</span></span> <span data-ttu-id="b41aa-114">두 번째 부분에서는 메서드를 사용 하 여 [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) 할당 된 값을 검색 하 고 `Controlled X` 작업에서 입력으로 받은 원하는 비트 수를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of allocated qubits as well as the number of qubits that the `Controlled X` operation received as input.</span></span> 

<span data-ttu-id="b41aa-115">마지막으로 다음을 사용 하 여 width 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-115">Finally, you can output all the statistics collected by the width counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="b41aa-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b41aa-116">See also</span></span>

- <span data-ttu-id="b41aa-117">퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.</span><span class="sxs-lookup"><span data-stu-id="b41aa-117">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="b41aa-118"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="b41aa-119"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="b41aa-120"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="b41aa-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API reference.</span></span>
