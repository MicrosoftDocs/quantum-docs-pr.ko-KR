---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: NMisclassifications 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709738"
---
# <a name="nmisclassifications-function"></a>NMisclassifications 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지 [](https://nuget.org/packages/)


유추 된 레이블 집합과 올바른 레이블 집합을 지정 하면 각 레이블 집합이 다른 인덱스 수를 반환 합니다.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>입력

### <a name="proposed--int"></a>제안 됨: [Int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>actual: [Int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

이에 해당 하는 인덱스 수입니다 `idx` `inferredLabels[idx] != actualLabels[idx]` .