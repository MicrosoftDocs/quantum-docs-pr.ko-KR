---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: RobustPhaseEstimation 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: d04ee578c0e6f916e9a4da451075b79e0630c70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714939"
---
# <a name="robustphaseestimation-operation"></a>RobustPhaseEstimation 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지 [](https://nuget.org/packages/)


지정 된 oracle 및 eigenstate에 대 한 강력한 비 반복적인 퀀텀 단계 예측 알고리즘 `U` 을 수행 하 고 Heisenberg 한도에 분산 배율이 지정 된 단계의 단일 실제 값을 제공 합니다.

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>입력

### <a name="bitsprecision--int"></a>bitsPrecision: [Int](xref:microsoft.quantum.lang-ref.int)

이는 $ \phi \phi 10.7 \phi/\texts {queries} $와 같이 많은 수의 쿼리를 사용 하는 $ \a$의 추정치를 제공 합니다.


### <a name="oracle--discreteoracle"></a>oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

지정 된 정수에 대 한 ^ m $ $U를 구현 하는 작업은 $ $m.


### <a name="targetstate--qubit"></a>targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]

$ $U 하는 퀀텀 레지스터가 작동 합니다. $U $의 eigenstate $ \ket{\phi} $ $U를 저장 하는 경우 $ \phi\in (-\pi, \pi] $의 \ket{\phi} = e ^ {i\phi} \ket{\phi} $에 대해 알 수 없는 단계가 발생 합니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>설명

많은 수의 쿼리를 제한 하는 경우 $ \\a$의 예상 값에 대 한 표준 편차에 대 한 낮은 범위를 Cramer-Rao 합니다.

## <a name="references"></a>참조

- 강력한 단계 추정 Shelby Kimmel, Guang Jia-hao Low, (Yoder를 통한 범용 Single-Qubit Gate-Set의 강력한 보정 https://arxiv.org/abs/1502.02677