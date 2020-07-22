---
title: 무효화 되는 ombits 사용 검사기-퀀텀 개발 키트
description: '퀀텀 추적 시뮬레이터를 사용 하 여 Q # 코드에서 잠재적으로 잘못 된 기능이 있는지 확인 하는 Microsoft QDK 무효화 된 사용 검사기에 대해 알아봅니다.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: fccf6d5784b587f4ad9b659e23027619acd06ffa
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871096"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a><span data-ttu-id="72de5-103">퀀텀 추적 시뮬레이터: 무효화 되는 사용 검사기</span><span class="sxs-lookup"><span data-stu-id="72de5-103">Quantum trace simulator: invalidated qubits use checker</span></span>

<span data-ttu-id="72de5-104">무효화 된 ombits 사용 검사기는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-104">The invalidated qubits use checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="72de5-105">이를 사용 하 여 잘못 된 비트로 인해 발생 하는 코드에서 잠재적 버그를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-105">You can use it to detect potential bugs in the code caused by invalid qubits.</span></span> 

## <a name="invalid-qubits"></a><span data-ttu-id="72de5-106">잘못 된 비트</span><span class="sxs-lookup"><span data-stu-id="72de5-106">Invalid qubits</span></span>

<span data-ttu-id="72de5-107">무효화 된 작업에서 검색 된 문제를 설명 하는 Q # 코드의 다음 부분을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-107">Consider the following piece of Q# code to illustrate the issues detected by the invalidated qubits use checker:</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="72de5-108">작업을에 적용 하는 경우 `H` 이 작업은 `q[0]` 이미 릴리스된 (정의 되지 않은 동작을 발생 시킬 수 있음)를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-108">When you apply the `H` operation to `q[0]`, it points to an already released qubit, which can cause undefined behavior.</span></span> <span data-ttu-id="72de5-109">무효화 된 기능을 사용 하는 경우 `InvalidatedQubitsUseCheckerException` 프로그램이 이미 릴리스된의 작업을 적용 하는 경우 예외를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-109">When the Invalidated Qubits Use Checker is enabled, it throws the exception `InvalidatedQubitsUseCheckerException` if the program applies an operation to an already released qubit.</span></span> <span data-ttu-id="72de5-110">자세한 내용은 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="72de5-110">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span></span>

## <a name="invoking-the-invalidated-qubits-use-checker"></a><span data-ttu-id="72de5-111">무효화 된의 사용 검사를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-111">Invoking the invalidated qubits use checker</span></span>

<span data-ttu-id="72de5-112">무효화 된 인스턴스를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UseInvalidatedQubitsUseChecker` 속성을 **true**로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="72de5-112">To run the quantum trace simulator with the invalidated qubits use checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseInvalidatedQubitsUseChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a><span data-ttu-id="72de5-113">C # 호스트 프로그램에서 무효화 된 사용 검사 사용</span><span class="sxs-lookup"><span data-stu-id="72de5-113">Using the invalidated qubits use checker in a C# host program</span></span>

<span data-ttu-id="72de5-114">다음은 무효화 된 기능 사용 검사기를 사용 하는 퀀텀 추적 시뮬레이터를 사용 하는 c # 호스트 프로그램의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-114">The following is an example of C# host programs that uses the quantum trace simulator with the invalidated qubits use checker enabled:</span></span> 

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
            traceSimCfg.UseInvalidatedQubitsUseChecker = true; // enables UseInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="72de5-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="72de5-115">See also</span></span>

- <span data-ttu-id="72de5-116">퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.</span><span class="sxs-lookup"><span data-stu-id="72de5-116">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="72de5-117"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-117">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="72de5-118"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="72de5-119"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>API 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="72de5-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API reference.</span></span>