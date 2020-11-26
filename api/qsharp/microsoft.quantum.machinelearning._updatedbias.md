---
uid: Microsoft.Quantum.MachineLearning._UpdatedBias
title: _UpdatedBias 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _UpdatedBias
qsharp.summary: Returns a bias value that leads to near-minimum misclassification score.
ms.openlocfilehash: 141edf6e425a060a995bfc181aefb1bcffdb128b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196704"
---
# <a name="_updatedbias-function"></a>_UpdatedBias 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


가장 낮은 최소 분류 점수를 초래 하는 편차 값을 반환 합니다.

```qsharp
function _UpdatedBias (labeledProbabilities : (Double, Int)[], bias : Double, tolerance : Double) : Double
```


## <a name="input"></a>입력

### <a name="labeledprobabilities--doubleint"></a>labeledProbabilities: ([Double](xref:microsoft.quantum.lang-ref.double),[Int](xref:microsoft.quantum.lang-ref.int)) []




### <a name="bias--double"></a>바이어스: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

