---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: TrotterStep 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 7a1a27ba4dc4b8b7bbc4da6a378d4a1494bc9415
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725352"
---
# <a name="trotterstep-function"></a>TrotterStep 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지 [](https://nuget.org/packages/)


`EvolutionGenerator`Trotter – Suzuki 분해를 사용 하 여에 설명 된 시스템의 시간 진화의 단일 시간 단계를 구현 합니다.

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="evolutiongenerator--evolutiongenerator"></a>evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

시뮬레이트할 시스템에 대 한 전체 설명입니다.


### <a name="trotterorder--int"></a>trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)

Trotter 통합자의 순서입니다. 이 값은 1 또는 짝수 여야 합니다.


### <a name="trotterstepsize--double"></a>trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)

시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.



## <a name="output--qubit--unit-adj--ctl"></a>출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl

기간에 대 한 단일 시간 진화의 단일 단계를 대략적으로 나타내는 단일 작업입니다 `trotterStepSize` .

## <a name="remarks"></a>설명

Trotter – Suzuki 분해에 대 한 자세한 내용은 [시간이 지정 된 컴퍼지션](/quantum/libraries/control-flow#time-ordered-composition)을 참조 하세요.