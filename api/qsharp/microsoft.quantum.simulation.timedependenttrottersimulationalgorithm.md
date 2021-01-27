---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: TimeDependentTrotterSimulationAlgorithm 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: c827dd79af6f4b745adf8903ed2664d9e8255785
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858367"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a>TimeDependentTrotterSimulationAlgorithm 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`TimeDependentSimulationAlgorithm` Trotter – Suzuki 분해를 사용 하 여 시간 종속 Schrodinger 수식을 해결 하는 단일 연산자를 대략적으로 계산 하는 함수입니다.

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a>입력

### <a name="trotterstepsize--double"></a>trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)

시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.


### <a name="trotterorder--int"></a>trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)

Trotter 통합자의 순서입니다. 이 값은 1 또는 짝수 여야 합니다.



## <a name="output--timedependentsimulationalgorithm"></a>출력: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

`TimeDependentSimulationAlgorithm` 형식입니다.