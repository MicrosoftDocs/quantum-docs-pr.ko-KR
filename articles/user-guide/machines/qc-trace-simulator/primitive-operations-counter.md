---
title: 기본 작업 카운터-퀀텀 개발 키트
description: 퀀텀 추적 시뮬레이터를 사용 하 여 프로그램의 작업에서 사용 되는 기본 프로세스를 추적 하는 Microsoft QDK 기본 작업 카운터에 대해 알아봅니다 Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: bf75eb94696a489a587316928bc3f33baa4a1785
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690958"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a>퀀텀 추적 시뮬레이터: 기본 작업 카운터

기본 작업 카운터는 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)의 일부입니다. 퀀텀 프로그램에서 호출 된 모든 작업에서 사용 되는 기본 프로세스의 수를 계산 합니다. 

모든 <xref:Microsoft.Quantum.Intrinsic> 연산은 단일 비트 회전, T 작업, 단일가 Clifford 작업, CNOT 작업 및 여러 가지 관찰 가능 개체의 측정값으로 표현 됩니다. 기본 작업 카운터는 작업 [호출 그래프](https://en.wikipedia.org/wiki/Call_graph)의 모든 가장자리에 대 한 통계를 집계 하 고 수집 합니다.

## <a name="invoking-the-primitive-operation-counter"></a>기본 작업 카운터 호출

기본 작업 카운터를 사용 하 여 퀀텀 추적 시뮬레이터를 실행 하려면 인스턴스를 만들고 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> `UsePrimitiveOperationsCounter` 속성을 **true** 로 설정한 다음 <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> 를 매개 변수로 사용 하 여 새 인스턴스를 만들어야 합니다 `QCTraceSimulatorConfiguration` .

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a>C # 호스트 프로그램에서 기본 작업 카운터 사용

이 단원의 뒷부분에 나오는 c # 예제에서는 <xref:Microsoft.Quantum.Intrinsic.T> <xref:Microsoft.Quantum.Intrinsic.ccnot> 다음 샘플 코드를 기반으로 작업을 구현 하는 데 필요한 작업 수를 계산 합니다 Q# .

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

에서 일곱 개의 `CCNOT` 작업이 필요 하 `T` 고 `ApplySampleWithCCNOT` 8 개의 작업을 실행 하는지 확인 하려면 `T` 다음 c # 코드를 사용 합니다.

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

프로그램의 첫 번째 부분을 실행 `ApplySampleWithCCNOT` 합니다. 두 번째 부분에서는 메서드를 사용 하 [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) `T` 여에서 실행 되는 작업 수를 검색 합니다 `ApplySampleWithCCNOT` . 

`GetMetric`두 개의 형식 매개 변수를 사용 하 여를 호출 하면 지정 된 호출 그래프 가장자리와 연결 된 메트릭의 값이 반환 됩니다. 위의 예제에서 프로그램은 `Primitive.CCNOT` 내에서 작업을 호출 `ApplySampleWithCCNOT` 하므로 호출 그래프는에 지를 포함 합니다 `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

사용 된 작업 수를 검색 하려면 `CNOT` 다음 줄을 추가 합니다.
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

마지막으로, 다음을 사용 하 여 기본 작업 카운터에 의해 수집 된 모든 통계를 CSV 형식으로 출력할 수 있습니다.
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>참고 항목

- 퀀텀 개발 키트 [퀀텀 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro) 개요.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>API 참조입니다.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames>API 참조입니다.