---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: DiscretePhaseEstimationIteration 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 8ce1e1a2bda6507285f055c87619a8760c891082
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204388"
---
# <a name="discretephaseestimationiteration-operation"></a>DiscretePhaseEstimationIteration 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 oracle의 정수 제곱을 사용 하 여 반복적인 (일반적으로 제어) 단계 예측 알고리즘의 단일 반복을 수행 합니다.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="oracle--discreteoracle"></a>oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

$U ^ m $이 지정 된 레지스터에 적용 되는 작업 (예: ^ m $이 지정 된 레지스터에 적용 됨). 여기서 $U $은 단계가 예상 되는 단일이 고, 여기서 $m $은 oracle에 지정 된 정수 거듭제곱입니다.


### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 단일 oracle을 적용 하는 횟수입니다.


### <a name="theta--double"></a>테타: [Double](xref:microsoft.quantum.lang-ref.double)

대상 상태에 대해 동작 하기 전에 컨트롤의 단계를 반전 하는 각도입니다.


### <a name="targetstate--qubit"></a>targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]

지정 된 단일 oracle에 의해 처리 되는 상태 등록입니다.


### <a name="controlqubit--qubit"></a>Control의 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

지정 된 oracle의 응용 프로그램을 제어 하는 데 사용 되는 보조 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

