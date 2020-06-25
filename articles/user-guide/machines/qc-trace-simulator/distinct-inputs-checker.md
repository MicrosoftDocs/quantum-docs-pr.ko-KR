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
# <a name="distinct-inputs-checker"></a>고유 입력 검사기

는 `Distinct Inputs Checker` 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다. 코드에서 잠재적 버그를 검색 하도록 설계 되었습니다. 이 패키지에서 발견 된 문제를 설명 하는 Q # 코드의 다음 부분을 고려 합니다.

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

사용자가이 프로그램을 살펴보면와가 서로 다른 `op1` `op2` commute에서 작동 하는 다른 작업을 수행 하기 때문에 및가 호출 되는 순서는 중요 하지 않다고 가정 `q1` `q2` 합니다. 이제이 작업을 사용 하는 예를 살펴보겠습니다.

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

이제 `op1` 및 `op2` 은 모두 부분 응용 프로그램을 사용 하 여 얻고, 위의 예에서 사용자가 작업 결과를 호출 하는 경우 `ApplyBoth` 의 순서와의 순서에 따라 달라 `op1` 집니다 `op2` `ApplyBoth` . 이는 사용자가 수행 해야 하는 작업은 명확 하지 않습니다. 는 `Distinct Inputs Checker` 사용 하도록 설정 되 고가 throw 될 때 이러한 상황을 감지 합니다 `DistinctInputsCheckerException` . 자세한 내용은 [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) 에 대 한 API 설명서를 참조 하세요.

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>C # 프로그램에서 고유 입력 검사기 사용

다음은 사용 하도록 설정 된 퀀텀 컴퓨터 추적 시뮬레이터를 사용 하는 c # 드라이버 코드의 예입니다 `Distinct Inputs Checker` .

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

클래스는 `QCTraceSimulatorConfiguration` 퀀텀 컴퓨터 추적 시뮬레이터의 구성을 저장 하 고 생성자에 대 한 인수로 제공 될 수 있습니다 `QCTraceSimulator` . `useDistinctInputsChecker`가 true로 설정 되 면 `Distinct Inputs Checker` 이 사용 됩니다. 자세한 내용은 [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) 및 [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) 에 대 한 API 설명서를 참조 하세요.

## <a name="see-also"></a>참조

- 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.
