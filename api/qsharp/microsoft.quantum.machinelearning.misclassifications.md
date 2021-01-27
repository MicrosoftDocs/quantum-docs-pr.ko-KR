---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: 잘못 분류 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 3913395fbd9f7cf96732c17ca0c726289e5087ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853920"
---
# <a name="misclassifications-function"></a>잘못 분류 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


유추 된 레이블 집합과 올바른 레이블 집합을 지정 하면 각 레이블 집합이 다른에 대 한 인덱스를 반환 합니다.

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a>입력

### <a name="inferredlabels--int"></a>inferredLabels: [Int](xref:microsoft.quantum.lang-ref.int)[]

지정 된 학습 또는 유효성 검사 집합에 대해 유추 된 레이블입니다.


### <a name="actuallabels--int"></a>actualLabels: [Int](xref:microsoft.quantum.lang-ref.int)[]

지정 된 학습 또는 유효성 검사 집합의 실제 레이블입니다.



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

`idx`이에 해당 하는 인덱스의 배열입니다 `inferredLabels[idx] != actualLabels[idx]` .

## <a name="example"></a>예제

```qsharp
let misclassifications = Misclassifications([0, 1, 0, 0], [0, 1, 1, 0]);
Message($"{misclassifications}"); // Will print [2].
```