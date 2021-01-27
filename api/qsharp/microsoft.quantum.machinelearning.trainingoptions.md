---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: TrainingOptions 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 762d6853910832c6d4cda522c0c5df706d1ed195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842775"
---
# <a name="trainingoptions-user-defined-type"></a>TrainingOptions 사용자 정의 형식

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


퀀텀 분류자 학습에 사용할 옵션의 컬렉션입니다.

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a>명명 된 항목

### <a name="learningrate--double"></a>LearningRate: [Double](xref:microsoft.quantum.lang-ref.double)

학습 단계에서 모델 매개 변수를 업데이트할 때 그라데이션을 재조정 하는 학습 률입니다.
### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

샘플을 퀀텀 상태로 준비할 때 사용할 근사 허용 오차입니다.
### <a name="minibatchsize--int"></a>미니 Batchsize: [Int](xref:microsoft.quantum.lang-ref.int)

각 학습 미니 배치에서 사용할 샘플의 수입니다.
### <a name="nmeasurements--int"></a>N 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

분류 확률을 예측 하기 위해 각 분류 결과를 측정 하는 횟수입니다.
### <a name="maxepochs--int"></a>MaxEpochs: [Int](xref:microsoft.quantum.lang-ref.int)

각 모델을 학습 하는 최대 epoch 수입니다.
### <a name="maxstalls--int"></a>MaxStalls: [Int](xref:microsoft.quantum.lang-ref.int)

학습 epoch가 실패 하기 전까지 정지 (약 0 그라데이션) 할 수 있는 최대 횟수입니다.
### <a name="stochasticrescalefactor--double"></a>StochasticRescaleFactor: [Double](xref:microsoft.quantum.lang-ref.double)

업데이트를 다시 시도 하기 전에 지연 된 모델의 크기를 조정 하는 크기입니다.
### <a name="scoringperiod--int"></a>ScoringPeriod: [Int](xref:microsoft.quantum.lang-ref.int)

점수 매기기 점수 사이에 수행할 그라데이션 단계 수입니다.
최상의 정확도를 위해를 1로 설정 합니다.
### <a name="verbosemessage--string---unit"></a>VerboseMessage: [문자열](xref:microsoft.quantum.lang-ref.string) -> [단위](xref:microsoft.quantum.lang-ref.unit)

자세한 피드백을 제공 하는 데 사용할 수 있는 함수입니다.

## <a name="remarks"></a>설명

이 UDT는 직접 만들 수 없습니다. 대신를 호출 하 @"microsoft.quantum.machinelearning.defaulttrainingoptions" 고 연산자를 사용 하 여 다른 기본값을 재정의 하 여 지정 해야 합니다 `w/` .

예를 들어 10만 측정치와 최대 8 교육 epoch를 사용 하려면 다음을 수행 합니다.

```qsharp
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a>참조

- [arXiv: 1804.00633](https://arxiv.org/abs/1804.00633)