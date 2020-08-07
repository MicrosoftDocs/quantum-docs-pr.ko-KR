---
title: 고유 입력 검사기-퀀텀 개발 키트
description: 퀀텀 추적 시뮬레이터를 사용 하 여 코드에서 공유 하는 경우의 잠재적 충돌을 확인 하는 Microsoft QDK 고유 입력 검사기에 대해 알아봅니다 Q# .
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 750c94e7f861678d37f051619ff5b29bf4fd3d3e
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868273"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a>퀀텀 추적 시뮬레이터: 고유 입력 검사기

고유 입력 검사기는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다. 이를 사용 하 여 공유의 충돌로 인해 발생 하는 코드에서 잠재적 버그를 검색할 수 있습니다. 

## <a name="conflicts-with-shared-qubits"></a>공유 된 비트와 충돌

다음 코드를 고려 Q# 하 여 고유한 입력 검사기에서 발견 된 문제를 설명 합니다.

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

이 프로그램을 살펴보면 `op1` `op2` 및가 서로 다른 `q1` commute에서 작동 하는 다른 기능을 수행 하기 때문에이 프로그램을 호출 하는 순서는 중요 하지 않을 수 있습니다 `q2` . 

이제 다음 예제를 살펴보겠습니다.

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

및는 `op1` `op2` 모두 부분 응용 프로그램을 사용 하 여 가져오고, `ApplyBoth`이 예제에서를 호출 하는 경우 작업의 결과는 `op1` 발생 하는 것 `op2` 으로 간주 되는 및의 순서에 따라 달라 집니다 `ApplyBoth` . 고유 입력 검사기를 사용 하도록 설정 하면 이러한 상황을 감지 하 고을 throw `DistinctInputsCheckerException` 합니다. 자세한 내용은 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API 라이브러리에서을 참조 하세요 Q# .

## <a name="invoking-the-distinct-inputs-checker"></a>고유 입력 검사기 호출

고유 입력 검사기를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UseDistinctInputsChecker` 속성을 **true**로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` . 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a>C # 호스트 프로그램에서 고유 입력 검사기 사용

다음은 고유한 입력 검사기를 사용 하는 퀀텀 추적 시뮬레이터를 사용 하는 c # 호스트 프로그램의 예입니다.

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

## <a name="see-also"></a>참고 항목

- 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException>API 참조입니다.
