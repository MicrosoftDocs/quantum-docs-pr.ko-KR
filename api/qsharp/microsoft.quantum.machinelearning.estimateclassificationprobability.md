---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: EstimateClassificationProbability 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853950"
---
# <a name="estimateclassificationprobability-operation"></a>EstimateClassificationProbability 작업

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


샘플 및 순차 분류자가 지정 된 경우 지정 된 샘플에서 분류자의 출력을 반복적으로 측정 하 여 해당 샘플에 대 한 분류 확률을 예측 합니다.

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a>입력

### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

샘플을 상태 준비 작업으로 인코딩할 수 있는 허용 오차입니다.


### <a name="model--sequentialmodel"></a>모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

지정 된 샘플의 분류 확률을 예측 하는 데 사용할 순차 모델입니다.


### <a name="sample--double"></a>샘플: [Double](xref:microsoft.quantum.lang-ref.double)[]

분류할 샘플의 기능 벡터입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

분류 확률을 예측 하는 데 사용할 측정 수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

지정 된 샘플에 대 한 예상 분류 확률입니다.