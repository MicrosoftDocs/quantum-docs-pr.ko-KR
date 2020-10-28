---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: EstimateClassificationProbabilities 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 2b7845d39256f718cc3e415207b8a47b24620bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709787"
---
# <a name="estimateclassificationprobabilities-operation"></a>EstimateClassificationProbabilities 작업

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지 [](https://nuget.org/packages/)


샘플 집합과 순차 분류자가 지정 된 경우 각 샘플에서 분류자의 출력을 반복적으로 측정 하 여 해당 샘플에 대 한 분류 확률을 예측 합니다.

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a>입력

### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

샘플을 상태 준비 작업으로 인코딩할 수 있는 허용 오차입니다.


### <a name="model--sequentialmodel"></a>모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

지정 된 샘플에 대 한 분류 확률을 예측 하는 데 사용할 순차 모델입니다.


### <a name="samples--double"></a>샘플: [Double](xref:microsoft.quantum.lang-ref.double)[] []

분류할 각 샘플에 대 한 기능 벡터의 배열입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

분류 확률을 예측 하는 데 사용할 측정 수입니다.



## <a name="output--double"></a>Output: [Double](xref:microsoft.quantum.lang-ref.double)[]

지정 된 각 샘플에 대 한 분류 확률의 예상 배열입니다.