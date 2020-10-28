---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: TrotterStepImpl 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: 1ddd7ab33df243d729b5b48cba393d976bfd3640
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725324"
---
# <a name="trotterstepimpl-operation"></a>TrotterStepImpl 작업

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지 [](https://nuget.org/packages/)


에 포함 된 용어에의 한 시간 혁신을 구현 `GeneratorSystem` 합니다.

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="evolutiongenerator--evolutiongenerator"></a>evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

시뮬레이트할 시스템에 대 한 전체 설명입니다.


### <a name="idx--int"></a>idx: [Int](xref:microsoft.quantum.lang-ref.int)

설명 된 시스템의 용어에 대 한 정수 인덱스입니다.


### <a name="stepsize--double"></a>stsize: [Double](xref:microsoft.quantum.lang-ref.double)

시간 (시간)에 대 한 승수-로 인덱싱된 용어로 진화 `idx` 합니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

이벤트가 시뮬레이션에 의해 처리 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

