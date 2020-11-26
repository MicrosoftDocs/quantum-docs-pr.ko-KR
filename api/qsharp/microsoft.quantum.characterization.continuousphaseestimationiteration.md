---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: ContinuousPhaseEstimationIteration 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 3c0f6cf084311598346b25dd7028e290946cd87f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216288"
---
# <a name="continuousphaseestimationiteration-operation"></a>ContinuousPhaseEstimationIteration 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 oracle의 임의의 실제 성능을 사용 하 여 반복적인 (일반적으로 제어) 단계 추정 알고리즘의 단일 반복을 수행 합니다.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="oracle--continuousoracle"></a>oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

$U ^ t $가 지정 된 레지스터에 적용 되는 작업 (예: "^ t $")이 지정 된 레지스터에 적용 되는 $t 작업입니다. 여기서 $U $은 단계가 예상 되는 단일이 고, $t 여기서 $는 oracle에 지정 된 정수 거듭제곱입니다.


### <a name="time--double"></a>시간: [Double](xref:microsoft.quantum.lang-ref.double)

지정 된 단일 oracle을 적용 하는 횟수입니다.


### <a name="theta--double"></a>테타: [Double](xref:microsoft.quantum.lang-ref.double)

대상 상태에 대해 동작 하기 전에 컨트롤의 단계를 반전 하는 각도입니다.


### <a name="targetstate--qubit"></a>targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]

지정 된 단일 oracle에 의해 처리 되는 상태 등록입니다.


### <a name="controlqubit--qubit"></a>Control의 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

