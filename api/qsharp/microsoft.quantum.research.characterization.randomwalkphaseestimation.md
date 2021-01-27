---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: RandomWalkPhaseEstimation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: f9edafcce62c8b30a6bd52b7dbaa2df2c50c920d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846012"
---
# <a name="randomwalkphaseestimation-operation"></a>RandomWalkPhaseEstimation 작업

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Characterization) .

패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization) .


임의 워크를 사용 하 여 반복 단계 예측을 수행 하 여 지정 된 oracle 및 eigenstate에서 얻은 기존 측정 결과에 대 한 Bayesian 유추를 대략적으로 수행 합니다.

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>입력

### <a name="initialmean--double"></a>initialMean: [Double](xref:microsoft.quantum.lang-ref.double)

$ \\A$를 통한 초기 정규 이전 배포의 평균입니다.


### <a name="initialstddev--double"></a>initialStdDev: [Double](xref:microsoft.quantum.lang-ref.double)

$ \Phi $를 통한 초기 표준 이전 배포의 표준 편차입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

최종 사후 예상치에 허용할 측정 수입니다.


### <a name="maxmeasurements--int"></a>maxMeasurements: [Int](xref:microsoft.quantum.lang-ref.int)

작업을 실패 한 것으로 간주 하기 전에 수행할 수 있는 총 측정 수입니다.


### <a name="unwind--int"></a>해제: [Int](xref:microsoft.quantum.lang-ref.int)

일관성 확인에 실패할 경우 잊어버릴 결과의 수입니다.


### <a name="oracle--continuousoracle"></a>oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

\Ket{\phi} (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ for eigenstates $ $ (\mathbb{R} ^ + $에서 알 수 없는 단계 $ \emin) 인 단일 $U $를 나타내는 작업 $U입니다.


### <a name="targetstate--qubit"></a>targetState: [[](xref:microsoft.quantum.lang-ref.qubit)]

$U $가 작동 하는 레지스터입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

최종 예상 $ \hat{\phi} \mathrel{: =} \은 (는) 허용 되는 모든 데이터를 제공 하는 사후에 대 한 기대를 예상 합니다.

## <a name="remarks"></a>설명

### <a name="iterative-phase-estimation-and-eigenstates"></a>반복 단계 예측 및 Eigenstates

일반적으로 입력 레지스터는 `eigenstate` $U $의 eigenstate $ \ket{\phi} $ 일 필요가 없지만 eigenstate에 superposition 수 있습니다. 입력 상태가 \begin{align} \ket{\psi} & = \sum \_ {j} \sum \_ j \ket{\phi j}에서 제공 된다고 가정 합니다 \_ . 여기서 $ \{ \sum \_ j \} $는 $ \sum \_ j | \sum \_ j | ^ 2 = $1 및 where $U \ket{\phi \_ j} = \aj\ket \_ {\ l \_ j} $와 같이 복잡 한 계수입니다.

그런 다음 [개발 가이드](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates)에 설명 된 대로 반복적인 단계 예측을 수행 하면 궁극적으로 단일 eigenstate로 수렴 됩니다.

### <a name="experiment-design"></a>실험 디자인

에 전달 되는 $t $ 및 역 각도 $ \theta $의 측정 시간은 `oracle` *파티클 추측 추론*, \begin{align} \stc\\\ac\\\\variance{\phi}}., \aa\ca\a\a\ca\ca\ {1}
\end{align}이 추론은 이전의 표준에 대 한 가정 하에 반복 단계 추정에서 예상 되는 사후 분산을 줄이는 데 가장 적합 합니다.

### <a name="optimality"></a>Optimality

이 작업은 평가기 (\phi,) \mathrel{: =} (\a\hat{\phi}) ^ 2 $를 사용 $L 하 여 계산한 $ \\a$ 단계에 대 한 최적의 근사치를 계산 합니다.

반복 단계 예측의 통계에 대 한 자세한 내용은 [Bayesian 단계 예측](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) 을 참조 하세요.

## <a name="references"></a>참조

- Ferrie *et al.* 2011 [doi: 10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arxiv: 1110.3067](https://arxiv.org/abs/1110.3067).
- Wiebe *et al.* 2013 [doi: 10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arxiv: 1309.0876](https://arxiv.org/abs/1309.0876)
- Wiebe 및 Granade 2018 *(준비)*.