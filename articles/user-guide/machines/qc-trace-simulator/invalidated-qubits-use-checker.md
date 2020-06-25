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
# <a name="invalidated-qubits-use-checker"></a>무효화 되는 사용 검사기

는 `Invalidated Qubits Use Checker` 코드에서 잠재적 버그를 검색 하기 위해 설계 된 퀀텀 컴퓨터 [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 의 일부입니다. 에서 검색 된 문제를 설명 하는 다음의 Q # 코드 부분을 고려 합니다 `Invalidated Qubits Use Checker` .

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

`H`가 적용 되는 경우는 `q[0]` 이미 릴리스된 요소를 가리킵니다. 이로 인해 정의 되지 않은 동작이 발생할 수 있습니다. 를 `Invalidated Qubits Use Checker` 사용 하도록 설정 하면 `InvalidatedQubitsUseCheckerException` 작업이 이미 릴리스된의에 적용 되는 경우 예외가 throw 됩니다. 자세한 내용은 [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) 에 대 한 API 설명서를 참조 하세요.

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>C # 프로그램에서 무효화 된 기능이 사용 되는 검사기 사용

다음은 `Trace
Simulator` 사용 하도록 설정 된 퀀텀 컴퓨터를 사용 하는 c # 드라이버 코드의 예입니다 `Invalidated Qubits Use Checker` . 

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

클래스는 `QCTraceSimulatorConfiguration` 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 생성자에 대 한 인수로 제공 될 수 있습니다 `QCTraceSimulator` . `useInvalidatedQubitsUseChecker`가 true로 설정 되 면 `Invalidated Qubits Use Checker` 이 사용 됩니다. 자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) 에 대 한 API 설명서를 참조 하세요.

## <a name="see-also"></a>참조 ##

- 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.
