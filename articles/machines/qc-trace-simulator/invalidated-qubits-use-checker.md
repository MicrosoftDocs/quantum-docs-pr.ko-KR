---
title: 무효화 되는 사용 검사기 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 퀀텀 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 7403381b995ab660aa5cbc5a52b1e12c5c9ce442
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184970"
---
# <a name="invalidated-qubits-use-checker"></a>무효화 되는 사용 검사기

`Invalidated Qubits Use Checker`은 코드에서 잠재적 버그를 검색 하기 위해 설계 된 퀀텀 컴퓨터 [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 의 일부입니다. `Invalidated Qubits Use Checker`에서 검색 된 문제를 설명 하는 다음의 Q # 코드 부분을 고려 합니다.

```qsharp
operation UseReleasedQubitTest () : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

`H` 적용 되 `q[0]`에 적용 되는 경우에는 이미 출시 된 요소를 가리킵니다. 이로 인해 정의 되지 않은 동작이 발생할 수 있습니다. `Invalidated Qubits Use Checker` 사용 하도록 설정 된 경우에는 작업이 이미 릴리스된의에 적용 되는 경우 예외가 throw 됩니다 `InvalidatedQubitsUseCheckerException`. 자세한 내용은 [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) 에 대 한 API 설명서를 참조 하세요.

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>C# 프로그램에서 무효화 된 기능이 사용 되는 검사기 사용

다음은 `Invalidated Qubits Use Checker` 사용 하도록 설정 C# 된 상태에서 퀀텀 컴퓨터 `Trace
Simulator`를 사용 하는 드라이버 코드의 예입니다. 

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

클래스 `QCTraceSimulatorConfiguration`는 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 `QCTraceSimulator` 생성자에 대 한 인수로 제공 될 수 있습니다. `useInvalidatedQubitsUseChecker` true로 설정 되 면 `Invalidated Qubits Use Checker` 사용 됩니다. 자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) 에 대 한 API 설명서를 참조 하세요.

## <a name="see-also"></a>참고 항목 ##

- 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.
