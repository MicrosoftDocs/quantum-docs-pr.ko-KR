---
title: Width 카운터
description: 퀀텀 프로그램에서 각 작업에 의해 할당 되 고 빌려 온 것과 같은 수를 계산 하는 Microsoft QDK Width 카운터에 대해 알아봅니다.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275561"
---
# <a name="width-counter"></a><span data-ttu-id="04d52-103">Width 카운터</span><span class="sxs-lookup"><span data-stu-id="04d52-103">Width Counter</span></span>

<span data-ttu-id="04d52-104">는 `Width Counter` 각 작업에서 할당 및 빌려 온의 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="04d52-105">네임 스페이스의 모든 작업 `Microsoft.Quantum.Intrinsic` 은 단일의 비트 회전, T 게이트, 단일 Clifford 게이트, CNOT 게이트 및 여러 관찰 가능 개체의 측정값으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="04d52-106">일부 기본 작업에서는 추가 비트를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="04d52-107">예를 들어 제어 되는 `X` 게이트 또는 제어 되는 게이트를 곱합니다 `T` .</span><span class="sxs-lookup"><span data-stu-id="04d52-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="04d52-108">곱셈 제어 되는 게이트 구현에 의해 할당 된 추가 된 추가 비트 수를 계산 해 보겠습니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="04d52-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="04d52-109">C # 프로그램에서 Width 카운터 사용</span><span class="sxs-lookup"><span data-stu-id="04d52-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="04d52-110">`X`총 55fbits에 대해 제어 되는 곱하기는 2 개의 보조 비트를 할당 하 고 입력 너비는 5가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="04d52-111">이 경우에 해당 하는지 확인 하려면 다음 c # 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-111">To check that this is the case, we can use the following C# program:</span></span>

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

<span data-ttu-id="04d52-112">프로그램의 첫 번째 부분이 실행 `ApplyMultiControlledX` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="04d52-113">두 번째 부분에서는 메서드를 사용 `QCTraceSimulator.GetMetric` 하 여 할당 된 요소 수 뿐만 아니라 수신으로 제어 된 제어 비트 수를 가져옵니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="04d52-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="04d52-114">마지막으로 width 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력 하려면 다음을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="04d52-115">참조</span><span class="sxs-lookup"><span data-stu-id="04d52-115">See also</span></span> ##

- <span data-ttu-id="04d52-116">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="04d52-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
