---
uid: Microsoft.Quantum.Arrays.IndexRange
title: IndexRange 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220946"
---
# <a name="indexrange-function"></a>IndexRange 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


배열이 지정 된 경우 for 루프에서 사용 하기에 적합 한 해당 배열의 인덱스에 대해 범위를 반환 합니다.

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a>입력

### <a name="array--telement"></a>배열: ' TElement []

인덱스 범위가 반환 되어야 하는 배열입니다.



## <a name="output--range"></a>출력: [범위](xref:microsoft.quantum.lang-ref.range)

배열의 모든 인덱스에 대 한 범위입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="telement"></a>' TElement

배열의 요소 형식입니다.