---
title: 무효화된 큐비트 사용 검사기
description: 'Microsoft QDK 무효화 된의 사용 검사기에 대해 알아봅니다 .이 검사기는 Q # 코드에서 잠재적으로 잘못 된 수 비트를 확인 합니다.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: e2bbb12448e27f28db030a0084302fb24f46f26b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275574"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="8d2eb-103">무효화 되는 사용 검사기</span><span class="sxs-lookup"><span data-stu-id="8d2eb-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="8d2eb-104">는 `Invalidated Qubits Use Checker` 코드에서 잠재적 버그를 검색 하기 위해 설계 된 퀀텀 컴퓨터 [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="8d2eb-105">에서 검색 된 문제를 설명 하는 다음의 Q # 코드 부분을 고려 합니다 `Invalidated Qubits Use Checker` .</span><span class="sxs-lookup"><span data-stu-id="8d2eb-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="8d2eb-106">`H`가 적용 되는 경우는 `q[0]` 이미 릴리스된 요소를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="8d2eb-107">이로 인해 정의 되지 않은 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-107">This can cause undefined behavior.</span></span> <span data-ttu-id="8d2eb-108">를 `Invalidated Qubits Use Checker` 사용 하도록 설정 하면 `InvalidatedQubitsUseCheckerException` 작업이 이미 릴리스된의에 적용 되는 경우 예외가 throw 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="8d2eb-109">자세한 내용은 [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="8d2eb-110">C # 프로그램에서 무효화 된 기능이 사용 되는 검사기 사용</span><span class="sxs-lookup"><span data-stu-id="8d2eb-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="8d2eb-111">다음은 `Trace
Simulator` 사용 하도록 설정 된 퀀텀 컴퓨터를 사용 하는 c # 드라이버 코드의 예입니다 `Invalidated Qubits Use Checker` .</span><span class="sxs-lookup"><span data-stu-id="8d2eb-111">The following is an example of C# driver code for using the quantum computer `Trace
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

<span data-ttu-id="8d2eb-112">클래스는 `QCTraceSimulatorConfiguration` 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 생성자에 대 한 인수로 제공 될 수 있습니다 `QCTraceSimulator` .</span><span class="sxs-lookup"><span data-stu-id="8d2eb-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="8d2eb-113">`useInvalidatedQubitsUseChecker`가 true로 설정 되 면 `Invalidated Qubits Use Checker` 이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="8d2eb-114">자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) 에 대 한 API 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d2eb-115">참조</span><span class="sxs-lookup"><span data-stu-id="8d2eb-115">See also</span></span> ##

- <span data-ttu-id="8d2eb-116">퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>