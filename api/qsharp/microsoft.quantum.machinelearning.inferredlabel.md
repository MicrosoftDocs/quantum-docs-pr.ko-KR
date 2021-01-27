---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: InferredLabel 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848412"
---
# <a name="inferredlabel-function"></a>InferredLabel 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


분류 확률 및 바이어스가 지정 된 경우 해당 확률에서 유추 된 레이블을 반환 합니다.

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a>입력

### <a name="bias--double"></a>바이어스: [Double](xref:microsoft.quantum.lang-ref.double)

두 클래스 간의 편차 (일반적으로 분류자 학습의 결과)입니다.


### <a name="probability--double"></a>확률: [Double](xref:microsoft.quantum.lang-ref.double)

특정 샘플에 대 한 분류 확률입니다. 일반적으로 분류 빈도를 예측 한 결과입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 분류 확률에서 유추 된 레이블입니다.