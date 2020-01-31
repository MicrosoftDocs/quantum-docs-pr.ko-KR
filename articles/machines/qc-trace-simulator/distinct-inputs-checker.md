---
title: 고유 입력 검사기 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 양자 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 3c21a54f5da83bf1ea0792e79cc773be5fba71e8
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820966"
---
# <a name="distinct-inputs-checker"></a><span data-ttu-id="40f5e-103">고유 입력 검사기</span><span class="sxs-lookup"><span data-stu-id="40f5e-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="40f5e-104">`Distinct Inputs Checker`는 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="40f5e-105">코드에서 잠재적 버그를 검색 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="40f5e-106">이 패키지에서 발견 된 문제를 설명 하는 Q # 코드의 다음 부분을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

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

<span data-ttu-id="40f5e-107">사용자가이 프로그램을 볼 때 `q1`와 `q2`는 서로 다른 commute에서 작동 하는 다른 `op1` 및 `op2`이 호출 되는 순서는 중요 하지 않다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="40f5e-108">이제이 작업을 사용 하는 예를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="40f5e-109">이제 부분 응용 프로그램을 사용 하 여 `op1` 및 `op2`를 가져오고,이를 사용 하 여 응용 프로그램을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="40f5e-110">사용자가 위의 예제에서 `ApplyBoth`를 호출 하는 경우 작업의 결과는 `op1` 순서와 `ApplyBoth`내 `op2`에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-110">When the user calls `ApplyBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `ApplyBoth`.</span></span> <span data-ttu-id="40f5e-111">이는 사용자가 수행 해야 하는 작업은 명확 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="40f5e-112">`Distinct Inputs Checker` 사용 하도록 설정 하 고 `DistinctInputsCheckerException`을 throw 하는 경우 이러한 상황을 감지 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="40f5e-113">자세한 내용은 [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40f5e-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="40f5e-114">C# 프로그램에서 고유한 입력 검사기 사용</span><span class="sxs-lookup"><span data-stu-id="40f5e-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="40f5e-115">다음은 `Distinct Inputs Checker` 사용 하도록 설정 C# 된 퀀텀 컴퓨터 추적 시뮬레이터를 사용 하는 드라이버 코드의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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

<span data-ttu-id="40f5e-116">클래스 `QCTraceSimulatorConfiguration`는 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 `QCTraceSimulator` 생성자에 대 한 인수로 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="40f5e-117">`useDistinctInputsChecker` true로 설정 되 면 `Distinct Inputs Checker` 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="40f5e-118">자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40f5e-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="40f5e-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="40f5e-119">See also</span></span>

- <span data-ttu-id="40f5e-120">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5e-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
