---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: EstimateGradient 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 79f4abdf131509d4948a3c114e631118329f88d8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211851"
---
# <a name="estimategradient-operation"></a>EstimateGradient 작업

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


특정 모델 및 지정 된 인코딩된 입력에 대 한 순차 분류자의 학습 그라데이션을 추정 합니다.

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a>입력

### <a name="model--sequentialmodel"></a>모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

그라데이션을 예상할 순차 모델입니다.


### <a name="encodedinput--stategenerator"></a>encodedInput: [Stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

상태 준비 작업으로 인코딩된 순차 분류자에 대 한 입력입니다.


### <a name="nmeasurements--int"></a>n 측정값: [Int](xref:microsoft.quantum.lang-ref.int)

그라데이션을 예측 하는 데 사용할 측정 수입니다.



## <a name="output--double"></a>Output: [Double](xref:microsoft.quantum.lang-ref.double)[]

지정 된 입력 및 모델 매개 변수에 대 한 예상 학습 그라데이션입니다.

## <a name="remarks"></a>설명

이 작업에서는 Hadamard 테스트를 사용 하 고 매개 변수를 함께 사용 하 여 그라데이션을 계산 합니다.