---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: TrainSequentialClassifier 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: 97865965bef831eeb53245ba0c23d6bce54643ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847701"
---
# <a name="trainsequentialclassifier-operation"></a>TrainSequentialClassifier 작업

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


순차 분류자의 구조가 지정 된 경우 지정 된 레이블이 지정 된 학습 집합에 분류자를 학습 합니다.

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>입력

### <a name="models--sequentialmodel"></a>모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]

학습 중에 시작 점으로 사용할 모델의 배열입니다.


### <a name="samples--labeledsample"></a>샘플: [Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

학습을 수행 하는 데 사용 되는 레이블이 지정 된 학습 데이터의 집합입니다.


### <a name="options--trainingoptions"></a>옵션: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

학습 시 사용할 구성 @"microsoft.quantum.machinelearning.trainingoptions" 자세한 내용은 및 @"microsoft.quantum.machinelearning.defaulttrainingoptions" 를 참조 하세요.


### <a name="trainingschedule--samplingschedule"></a>trainingSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

학습 단계 중 학습 데이터에서 샘플을 선택할 때 사용할 샘플링 일정입니다.


### <a name="validationschedule--samplingschedule"></a>validationSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

최상의 분류자 점수를 발생 시킨 시작점을 선택할 때 학습 데이터에서 샘플을 선택 하는 경우 사용할 샘플링 일정입니다.



## <a name="output--sequentialmodelint"></a>출력: ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))

- 지정 된 분류자의 매개 변수화 및 두 클래스 간의 바이어스는 각각의 지정 된 시작점에서 최상의 결과에 해당 합니다.
- 최상의 분류자 모델에서 관찰 된 누락 수입니다.

## <a name="see-also"></a>참고 항목

- [MachineLearning. TrainSequentialClassifierAtModel](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [MachineLearning. ValidateSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)