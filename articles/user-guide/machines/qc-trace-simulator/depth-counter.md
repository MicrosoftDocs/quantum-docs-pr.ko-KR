---
title: 깊이 카운터-퀀텀 개발 키트
description: 퀀텀 추적 시뮬레이터를 사용 하 여 프로그램에서 호출 된 모든 작업의 깊이 수를 수집 하는 Microsoft QDK depth 카운터에 대해 알아봅니다 Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8280783adfcc2867c3a598a6f57d827125aadcfd
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833445"
---
# <a name="quantum-trace-simulator-depth-counter"></a>퀀텀 추적 시뮬레이터: 깊이 카운터

Depth 카운터는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다.
이를 사용 하 여 퀀텀 프로그램에서 호출 된 모든 작업의 깊이 상한을 나타내는 개수를 수집할 수 있습니다. 

## <a name="depth-values"></a>깊이 값

기본적으로 모든 작업은 깊이가 1 인 작업을 제외 하 고 깊이가 **0** 입니다 `T` . **1** 즉, 기본적으로 `T` 작업 수준도 계산 됩니다 (종종 바람직한 경우). 수준 카운터는 작업 [호출 그래프](https://en.wikipedia.org/wiki/Call_graph)의 모든 가장자리에 대 한 통계를 집계 하 고 수집 합니다.

모든 <xref:microsoft.quantum.intrinsic> 연산은 단일 비트 회전, <xref:microsoft.quantum.intrinsic.t> 작업, 단일가 Clifford 작업, <xref:microsoft.quantum.intrinsic.cnot> 작업 및 다중 기능 비트 pauli 관찰 가능 개체의 측정값으로 표현 됩니다. 사용자는의 필드를 통해 각 기본 작업에 대 한 깊이를 설정할 수 있습니다 `gateTimes` <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>수준 카운터 호출

Depth 카운터를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> 해당 `UseDepthCounter` 속성을 **true**로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` . 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a>C # 호스트 프로그램에서 depth 카운터 사용

이 단원의 뒷부분에 나오는 c # 예제에서는 `T` `CCNOT` 다음 샘플 코드에 따라 작업의 깊이를 계산 합니다 Q# .

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

에 `CCNOT` `T` 깊이 **5** 가 있고 `ApplySampleWithCCNOT` 깊이 6이 있는지 확인 하려면 `T` 다음 c # 코드를 사용 합니다. **6**

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

프로그램의 첫 번째 부분을 실행 `ApplySampleWithCCNOT` 합니다. 두 번째 부분에서는 메서드를 사용 하 여 [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) `T` 및의 깊이를 검색 합니다 `CCNOT` `ApplySampleWithCCNOT` . 

마지막으로, 다음을 사용 하 여 깊이 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력할 수 있습니다.
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>참고 항목

- 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter>API 참조입니다.
