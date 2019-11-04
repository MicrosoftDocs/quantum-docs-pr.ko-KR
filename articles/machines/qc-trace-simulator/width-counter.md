---
title: Width 카운터 | 퀀텀 컴퓨터 추적 시뮬레이터 | Microsoft Docs
description: 퀀텀 컴퓨터 추적 시뮬레이터 개요
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: e202c527e7e26751361e0c46355ffcefa9c95091
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184919"
---
# <a name="width-counter"></a>Width 카운터

`Width Counter`은 각 작업에 의해 할당 되 고 가져온 것과 같은 수를 계산 합니다.
`Microsoft.Quantum.Primitive` 네임 스페이스의 모든 작업은 단일의 비트 회전, T 게이트, 단일 관찰 가능 개체 게이트, CNOT 게이트 및 여러의 측정을 기준으로 표현 됩니다. 일부 기본 작업에서는 추가 비트를 할당할 수 있습니다. 예를 들어 제어 `X` 게이트 또는 제어 된 `T` 게이트를 곱합니다. 곱하기 제어 `X` 게이트의 구현에 의해 할당 된 추가 된 추가 비트 수를 계산 해 보겠습니다.

```qsharp
open Microsoft.Quantum.Primitive;
open Microsoft.Quantum.Arrays;
operation MultiControlledXDriver( numberOfQubits : Int ) : Unit {

    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

# <a name="using-width-counter-within-a-c-program"></a>C# 프로그램 내에서 Width 카운터 사용

총 5 개에 대해 작동 하는 곱하기 제어 `X`는 2 개의 보조 비트를 할당 하 고 입력 너비가 5가 됩니다. 이 경우에 해당 하는지 확인 하려면 다음 C# 프로그램을 사용할 수 있습니다.

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = MultiControlledXDriver.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

프로그램의 첫 번째 부분은 `MultiControlledXDriver`를 실행 합니다. 두 번째 부분에서는 `QCTraceSimulator.GetMetric` 메서드를 사용 하 여 할당 된 요소 수 뿐만 아니라 입력으로 받은 `X` 제어 되는 값을 가져옵니다. 

마지막으로 width 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력 하려면 다음을 사용할 수 있습니다.
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>참고 항목 ##

- 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.
