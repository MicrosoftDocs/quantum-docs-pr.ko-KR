---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: InferredLabels 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 874d1a2f7cc6d67567e0d2baa70b0d26b639a029
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722482"
---
# <a name="inferredlabels-function"></a>InferredLabels 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지 [](https://nuget.org/packages/)


분류 확률 및 바이어스의 배열이 지정 된 경우 각 확률에서 유추 된 레이블을 반환 합니다.

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a>입력

### <a name="bias--double"></a>바이어스: [Double](xref:microsoft.quantum.lang-ref.double)

두 클래스 간의 편차 (일반적으로 분류자 학습의 결과)입니다.


### <a name="probabilities--double"></a>확률: [Double](xref:microsoft.quantum.lang-ref.double)[]

일반적으로 분류 빈도를 추정 하 여 얻은 샘플 집합에 대 한 분류 확률의 배열입니다.



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

각 분류 확률에서 유추 된 레이블입니다.