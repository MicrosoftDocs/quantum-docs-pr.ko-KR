---
title: 고유 입력 검사기
description: 'Microsoft QDK Distinct 입력 검사기에 대해 알아보세요 .이를 통해 Q # 코드를 확인 하 여 공유 하는 데 문제가 발생할 수 있습니다.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 11a0573242c8afb12f242aa3be5f9cff18290452
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275622"
---
# <a name="distinct-inputs-checker"></a><span data-ttu-id="e484b-103">고유 입력 검사기</span><span class="sxs-lookup"><span data-stu-id="e484b-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="e484b-104">는 `Distinct Inputs Checker` 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="e484b-105">코드에서 잠재적 버그를 검색 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="e484b-106">이 패키지에서 발견 된 문제를 설명 하는 Q # 코드의 다음 부분을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

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

<span data-ttu-id="e484b-107">사용자가이 프로그램을 살펴보면와가 서로 다른 `op1` `op2` commute에서 작동 하는 다른 작업을 수행 하기 때문에 및가 호출 되는 순서는 중요 하지 않다고 가정 `q1` `q2` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="e484b-108">이제이 작업을 사용 하는 예를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="e484b-109">이제 `op1` 및 `op2` 은 모두 부분 응용 프로그램을 사용 하 여 얻고,</span><span class="sxs-lookup"><span data-stu-id="e484b-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="e484b-110">위의 예에서 사용자가 작업 결과를 호출 하는 경우 `ApplyBoth` 의 순서와의 순서에 따라 달라 `op1` 집니다 `op2` `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="e484b-110">When the user calls `ApplyBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `ApplyBoth`.</span></span> <span data-ttu-id="e484b-111">이는 사용자가 수행 해야 하는 작업은 명확 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="e484b-112">는 `Distinct Inputs Checker` 사용 하도록 설정 되 고가 throw 될 때 이러한 상황을 감지 합니다 `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="e484b-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="e484b-113">자세한 내용은 [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e484b-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="e484b-114">C # 프로그램에서 고유 입력 검사기 사용</span><span class="sxs-lookup"><span data-stu-id="e484b-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="e484b-115">다음은 사용 하도록 설정 된 퀀텀 컴퓨터 추적 시뮬레이터를 사용 하는 c # 드라이버 코드의 예입니다 `Distinct Inputs Checker` .</span><span class="sxs-lookup"><span data-stu-id="e484b-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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
            traceSimCfg.useDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="e484b-116">클래스는 `QCTraceSimulatorConfiguration` 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 생성자에 대 한 인수로 제공 될 수 있습니다 `QCTraceSimulator` .</span><span class="sxs-lookup"><span data-stu-id="e484b-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="e484b-117">`useDistinctInputsChecker`가 true로 설정 되 면 `Distinct Inputs Checker` 이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="e484b-118">자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e484b-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="e484b-119">참조</span><span class="sxs-lookup"><span data-stu-id="e484b-119">See also</span></span>

- <span data-ttu-id="e484b-120">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="e484b-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
