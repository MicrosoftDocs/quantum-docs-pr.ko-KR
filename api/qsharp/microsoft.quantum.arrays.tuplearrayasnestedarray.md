---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: TupleArrayAsNestedArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718808"
---
# <a name="tuplearrayasnestedarray-function"></a>TupleArrayAsNestedArray 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


2 튜플의 목록을 중첩 된 배열로 변환 합니다.

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a>입력

### <a name="tuplelist--tt"></a>tupleList: (' ' ') []

중첩 배열로 전환 될 2 튜플의 목록입니다.



## <a name="output--t"></a>출력: ' t [] []

길이가 tupleList와 일치 하는 중첩 된 배열입니다.

## <a name="example"></a>예제

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

