---
uid: Microsoft.Quantum.Arrays.IndexRange
title: IndexRange 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845789"
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

## <a name="example"></a>예

다음 `for` 루프는 동일 합니다.

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```