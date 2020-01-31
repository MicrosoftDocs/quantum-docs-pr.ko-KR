---
title: 무효화 되는 사용 검사기 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 양자 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 093937346488725eacb69ef7da6affde764ec5c1
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820881"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="3cd04-103">무효화 되는 사용 검사기</span><span class="sxs-lookup"><span data-stu-id="3cd04-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="3cd04-104">`Invalidated Qubits Use Checker`은 코드에서 잠재적 버그를 검색 하기 위해 설계 된 퀀텀 컴퓨터 [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="3cd04-105">`Invalidated Qubits Use Checker`에서 검색 된 문제를 설명 하는 다음의 Q # 코드 부분을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="3cd04-106">`H` 적용 되 `q[0]`에 적용 되는 경우에는 이미 출시 된 요소를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="3cd04-107">이로 인해 정의 되지 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-107">This can cause undefined behavior.</span></span> <span data-ttu-id="3cd04-108">`Invalidated Qubits Use Checker` 사용 하도록 설정 된 경우에는 작업이 이미 릴리스된의에 적용 되는 경우 예외가 throw 됩니다 `InvalidatedQubitsUseCheckerException`.</span><span class="sxs-lookup"><span data-stu-id="3cd04-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="3cd04-109">자세한 내용은 [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cd04-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="3cd04-110">C# 프로그램에서 무효화 된 기능이 사용 되는 검사기 사용</span><span class="sxs-lookup"><span data-stu-id="3cd04-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="3cd04-111">다음은 `Invalidated Qubits Use Checker` 사용 하도록 설정 C# 된 상태에서 퀀텀 컴퓨터 `Trace
Simulator`를 사용 하는 드라이버 코드의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-111">The following is an example of C# driver code for using the quantum computer `Trace
Simulator` with the `Invalidated Qubits Use Checker` enabled:</span></span> 

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
            traceSimCfg.useInvalidatedQubitsUseChecker = true; // enables useInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="3cd04-112">클래스 `QCTraceSimulatorConfiguration`는 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 `QCTraceSimulator` 생성자에 대 한 인수로 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="3cd04-113">`useInvalidatedQubitsUseChecker` true로 설정 되 면 `Invalidated Qubits Use Checker` 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="3cd04-114">자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cd04-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cd04-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3cd04-115">See also</span></span> ##

- <span data-ttu-id="3cd04-116">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd04-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
