---
title: 수준 카운터
description: 퀀텀 프로그램에서 호출 된 모든 작업의 깊이 수를 수집 하는 Microsoft QDK Depth 카운터에 대해 알아봅니다.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: d532a9f512b8c87d83d62ed26e3bb67e1b6f668b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275625"
---
# <a name="depth-counter"></a>수준 카운터

는 `Depth Counter` 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.
퀀텀 프로그램에서 호출 된 모든 작업의 깊이 수를 수집 하는 데 사용 됩니다. 의 모든 작업 <xref:microsoft.quantum.intrinsic> 은 단일 비트 회전, T 게이트, 단일 고 비트 Clifford 게이트, CNOT 게이트 및 여러 가지 관찰 가능 개체의 측정으로 표현 됩니다. 사용자는의 필드를 통해 각 기본 작업에 대 한 깊이를 설정할 수 있습니다 `gateTimes` <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

기본적으로 모든 작업에는 깊이 1이 있는 T 게이트를 제외 하 고 깊이 0이 있습니다. 즉, 기본적으로 작업의 T 수준만 계산 됩니다 (종종 바람직한 경우). 수집 된 통계는 작업 호출 그래프의 모든 가장자리에 걸쳐 집계 됩니다. 

이제 <xref:microsoft.quantum.intrinsic.t> 작업의 깊이를 계산 해 보세요 <xref:microsoft.quantum.intrinsic.ccnot> . 다음 Q # 샘플 코드를 사용 합니다.

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>C # 프로그램 내에서 Depth 카운터 사용

에 `CCNOT` `T` 깊이 5가 있고 `ApplySampleWithCCNOT` 깊이 6이 있는지 확인 하려면 `T` 다음 c # 코드를 사용할 수 있습니다.

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

프로그램의 첫 번째 부분이 실행 `ApplySampleWithCCNOT` 됩니다. 두 번째 부분에서는 메서드를 사용 하 여 `QCTraceSimulator.GetMetric` `T` 및의 깊이를 가져옵니다 `CCNOT` `ApplySampleWithCCNOT` . 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

마지막으로에서 수집한 모든 통계를 CSV 형식으로 출력 하려면 `Depth Counter` 다음을 사용할 수 있습니다.
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>참조 ##

- 퀀텀 컴퓨터 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요입니다.
