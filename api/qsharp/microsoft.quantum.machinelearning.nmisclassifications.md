---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: NMisclassifications 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 30d049ba54630cd2f5f350280bad7f587599f459
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196313"
---
# <a name="nmisclassifications-function"></a>NMisclassifications 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


유추 된 레이블 집합과 올바른 레이블 집합을 지정 하면 각 레이블 집합이 다른 인덱스 수를 반환 합니다.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>입력

### <a name="proposed--int"></a>제안 됨: [Int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>actual: [Int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

이에 해당 하는 인덱스 수입니다 `idx` `inferredLabels[idx] != actualLabels[idx]` .