---
title: Width 카운터 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 양자 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: 9c3601e74eec17bd6b463e90f8f3085c959d6f95
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820371"
---
# <a name="width-counter"></a><span data-ttu-id="fdc9b-103">Width 카운터</span><span class="sxs-lookup"><span data-stu-id="fdc9b-103">Width Counter</span></span>

<span data-ttu-id="fdc9b-104">`Width Counter`은 각 작업에 의해 할당 되 고 가져온 것과 같은 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="fdc9b-105">`Microsoft.Quantum.Intrinsic` 네임 스페이스의 모든 작업은 단일의 비트 회전, T 게이트, 단일 관찰 가능 개체 게이트, CNOT 게이트 및 여러의 측정을 기준으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="fdc9b-106">일부 기본 작업에서는 추가 비트를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="fdc9b-107">예를 들어 제어 `X` 게이트 또는 제어 된 `T` 게이트를 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="fdc9b-108">곱하기 제어 `X` 게이트의 구현에 의해 할당 된 추가 된 추가 비트 수를 계산 해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="fdc9b-109">C# 프로그램 내에서 Width 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="fdc9b-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="fdc9b-110">총 5 개에 대해 작동 하는 곱하기 제어 `X`는 2 개의 보조 비트를 할당 하 고 입력 너비가 5가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="fdc9b-111">이 경우에 해당 하는지 확인 하려면 다음 C# 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-111">To check that this is the case, we can use the following C# program:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
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

<span data-ttu-id="fdc9b-112">프로그램의 첫 번째 부분은 `ApplyMultiControlledX`를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="fdc9b-113">두 번째 부분에서는 `QCTraceSimulator.GetMetric` 메서드를 사용 하 여 할당 된 요소 수 뿐만 아니라 입력으로 받은 `X` 제어 되는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="fdc9b-114">마지막으로 width 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력 하려면 다음을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="fdc9b-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fdc9b-115">See also</span></span> ##

- <span data-ttu-id="fdc9b-116">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
