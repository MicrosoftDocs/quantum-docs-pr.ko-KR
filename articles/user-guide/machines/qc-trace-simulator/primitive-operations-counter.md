---
title: 기본 작업 카운터
description: 퀀텀 프로그램에서 작업에 사용 되는 기본 실행 수를 추적 하는 Microsoft QDK 기본 작업 카운터에 대해 알아봅니다.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 8bdb0aed370e72b58b23025f1685ad7ce1a77a43
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275558"
---
# <a name="primitive-operations-counter"></a>기본 작업 카운터  

는 `Primitive Operations Counter` 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다. 퀀텀 프로그램에서 호출 된 모든 작업에서 사용 되는 기본 실행 수를 계산 합니다. 의 모든 작업 `Microsoft.Quantum.Intrinsic` 은 단일 비트 회전, T 게이트, 단일 고 비트 Clifford 게이트, CNOT 게이트 및 여러 가지 관찰 가능 개체의 측정으로 표현 됩니다. 수집 된 통계는 작업 호출 그래프의 가장자리에 걸쳐 집계 됩니다. 이제 `T` 작업을 구현 하는 데 필요한 게이트 수를 계산 `CCNOT` 합니다. 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>C # 프로그램에서 기본 작업 카운터 사용

실제로 7 개의 게이트가 필요 하 고 8 게이트를 실행 하는 것을 확인 하기 위해 `CCNOT` `T` `ApplySampleWithCCNOT` `T` 다음 c # 코드를 사용할 수 있습니다.

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

프로그램의 첫 번째 부분이 실행 `ApplySampleWithCCNOT` 됩니다. 두 번째 부분에서는 메서드를 사용 `QCTraceSimulator.GetMetric` 하 여에서 실행 하는 T 게이트 수를 가져옵니다 `ApplySampleWithCCNOT` . 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

`GetMetric`두 개의 형식 매개 변수를 사용 하 여를 호출 하면 지정 된 호출 그래프 가장자리와 연결 된 메트릭의 값이 반환 됩니다. 이 예제에서는 `Primitive.CCNOT` 내에서 작업을 호출 `ApplySampleWithCCNOT` 하므로 호출 그래프에 가장자리가 포함 됩니다 `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

사용 되는 게이트 수를 얻기 위해 `CNOT` 다음 줄을 추가할 수 있습니다.
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

마지막으로 게이트 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력 하려면 다음을 사용할 수 있습니다.
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>참조 ##

- 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.
