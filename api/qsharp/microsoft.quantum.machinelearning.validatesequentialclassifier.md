---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: ValidateSequentialClassifier 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 5174085edbfd846e8f6649f33e325fd1979ae6a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196109"
---
# <a name="validatesequentialclassifier-operation"></a>ValidateSequentialClassifier 작업

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


지정 된 미리 레이블이 지정 된 샘플 집합에 대해 지정 된 순차 분류자의 유효성을 검사 합니다.

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a>입력

### <a name="model--sequentialmodel"></a>모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

유효성을 검사할 순차 모델입니다.


### <a name="samples--labeledsample"></a>샘플: [Labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

지정 된 모델의 유효성을 검사 하는 데 사용할 샘플입니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

각 샘플을 순차 분류자에 대 한 입력으로 인코딩할 때 사용 하는 근사 허용 오차입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

각 샘플을 분류 하는 데 사용할 측정 수입니다.


### <a name="validationschedule--samplingschedule"></a>validationSchedule: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

유효성 검사 집합에서 샘플을 그려야 하는 일정입니다.



## <a name="output--validationresults"></a>출력: [Validationresults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)

지정 된 유효성 검사의 결과입니다.