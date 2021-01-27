---
title: 무효화 되는 ombits 사용 검사기-퀀텀 개발 키트
description: 퀀텀 추적 시뮬레이터를 사용 하 여 코드에서 잠재적으로 잘못 된 수를 확인 하는 Microsoft QDK 무효화 된 사용 검사기에 대해 알아봅니다 Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9014097ace7c9f19d93a92372da40f71fa7f87ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858613"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>퀀텀 추적 시뮬레이터: 무효화 되는 사용 검사기

무효화 된 ombits 사용 검사기는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다. 이를 사용 하 여 잘못 된 비트로 인해 발생 하는 코드에서 잠재적 버그를 검색할 수 있습니다. 

## <a name="invalid-qubits"></a>잘못 된 비트

Q#무효화 된 작업에서 발견 된 문제를 설명 하는 다음 코드를 고려 합니다.

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

작업을에 적용 하는 경우 `H` 이 작업은 `q[0]` 이미 릴리스된 (정의 되지 않은 동작을 발생 시킬 수 있음)를 가리킵니다. 무효화 된 기능을 사용 하는 경우 `InvalidatedQubitsUseCheckerException` 프로그램이 이미 릴리스된의 작업을 적용 하는 경우 예외를 throw 합니다. 자세한 내용은 <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>를 참조하세요.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>무효화 된의 사용 검사를 호출 합니다.

무효화 된 인스턴스를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UseInvalidatedQubitsUseChecker` 속성을 **true** 로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` . 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a>C # 호스트 프로그램에서 무효화 된 사용 검사 사용

다음은 무효화 된 기능 사용 검사기를 사용 하는 퀀텀 추적 시뮬레이터를 사용 하는 c # 호스트 프로그램의 예입니다. 

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

## <a name="see-also"></a>참고 항목

- 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>API 참조입니다.
