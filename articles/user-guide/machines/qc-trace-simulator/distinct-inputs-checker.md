---
title: 고유 입력 검사기-퀀텀 개발 키트
description: 퀀텀 추적 시뮬레이터를 사용 하 여 코드에서 공유 하는 경우의 잠재적 충돌을 확인 하는 Microsoft QDK 고유 입력 검사기에 대해 알아봅니다 Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
no-loc:
- Q#
- $$v
ms.openlocfilehash: bcb0bc92a546279496d27ad9b8c5f943ac133e2a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833469"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a><span data-ttu-id="2e38d-103">퀀텀 추적 시뮬레이터: 고유 입력 검사기</span><span class="sxs-lookup"><span data-stu-id="2e38d-103">Quantum trace simulator: distinct inputs checker</span></span>

<span data-ttu-id="2e38d-104">고유 입력 검사기는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-104">The distinct inputs checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="2e38d-105">이를 사용 하 여 공유의 충돌로 인해 발생 하는 코드에서 잠재적 버그를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-105">You can use it to detect potential bugs in the code caused by conflicts with shared qubits.</span></span> 

## <a name="conflicts-with-shared-qubits"></a><span data-ttu-id="2e38d-106">공유 된 비트와 충돌</span><span class="sxs-lookup"><span data-stu-id="2e38d-106">Conflicts with shared qubits</span></span>

<span data-ttu-id="2e38d-107">다음 코드를 고려 Q# 하 여 고유한 입력 검사기에서 발견 된 문제를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-107">Consider the following piece of Q# code to illustrate the issues detected by the distinct inputs checker:</span></span>

```qsharp
operation ApplyBoth(
    q1 : Qubit,
    q2 : Qubit,
    op1 : (Qubit => Unit),
    op2 : (Qubit => Unit))
: Unit {
    op1(q1);
    op2(q2);
}
```

<span data-ttu-id="2e38d-108">이 프로그램을 살펴보면 `op1` `op2` 및가 서로 다른 `q1` commute에서 작동 하는 다른 기능을 수행 하기 때문에이 프로그램을 호출 하는 순서는 중요 하지 않을 수 있습니다 `q2` .</span><span class="sxs-lookup"><span data-stu-id="2e38d-108">When you look at this program, you can assume that the order in which it calls `op1` and `op2` does not matter, because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> 

<span data-ttu-id="2e38d-109">이제 다음 예제를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-109">Now, consider this example:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="2e38d-110">및는 `op1` `op2` 모두 부분 응용 프로그램을 사용 하 여 가져오고,</span><span class="sxs-lookup"><span data-stu-id="2e38d-110">Note that `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="2e38d-111">`ApplyBoth`이 예제에서를 호출 하는 경우 작업의 결과는 `op1` 발생 하는 것 `op2` 으로 간주 되는 및의 순서에 따라 달라 집니다 `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="2e38d-111">When you call `ApplyBoth` in this example, the result of the operation depends on the order of `op1` and `op2` inside `ApplyBoth` - not what you would expect to happen.</span></span> <span data-ttu-id="2e38d-112">고유 입력 검사기를 사용 하도록 설정 하면 이러한 상황을 감지 하 고을 throw `DistinctInputsCheckerException` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-112">When you enable the distinct inputs checker, it detects such situations and throws a `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="2e38d-113">자세한 내용은 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API 라이브러리에서을 참조 하세요 Q# .</span><span class="sxs-lookup"><span data-stu-id="2e38d-113">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in the Q# API library.</span></span>

## <a name="invoking-the-distinct-inputs-checker"></a><span data-ttu-id="2e38d-114">고유 입력 검사기 호출</span><span class="sxs-lookup"><span data-stu-id="2e38d-114">Invoking the distinct inputs checker</span></span>

<span data-ttu-id="2e38d-115">고유 입력 검사기를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UseDistinctInputsChecker` 속성을 **true**로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="2e38d-115">To run the quantum trace simulator with the distinct inputs checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseDistinctInputsChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a><span data-ttu-id="2e38d-116">C # 호스트 프로그램에서 고유 입력 검사기 사용</span><span class="sxs-lookup"><span data-stu-id="2e38d-116">Using the distinct inputs checker in a C# host program</span></span>

<span data-ttu-id="2e38d-117">다음은 고유한 입력 검사기를 사용 하는 퀀텀 추적 시뮬레이터를 사용 하는 c # 호스트 프로그램의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-117">The following is an example of C# host program that uses the quantum trace simulator with the distinct inputs checker enabled:</span></span>

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
            var traceSimCfg = new QCTraceSimulatorConfiguration();
            traceSimCfg.UseDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2e38d-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2e38d-118">See also</span></span>

- <span data-ttu-id="2e38d-119">퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.</span><span class="sxs-lookup"><span data-stu-id="2e38d-119">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="2e38d-120"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="2e38d-121"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="2e38d-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="2e38d-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API reference.</span></span>
