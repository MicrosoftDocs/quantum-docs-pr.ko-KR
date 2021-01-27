---
uid: Microsoft.Quantum.Arrays.Where
title: Where 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 4a938114689177f7a9ee182e6e5f36debe4edac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842210"
---
# <a name="where-function"></a>Where 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


조건자와 배열이 지정 된 경우 조건자가 true 인 배열의 인덱스를 반환 합니다.

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a>입력

### <a name="predicate--t---bool"></a>조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)

에서 요소를 `'T` 필터링 하는 데 사용 되는 부울로의 함수입니다.


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

이 true 인 인덱스의 배열입니다 `predicate` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.