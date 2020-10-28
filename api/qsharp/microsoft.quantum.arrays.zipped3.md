---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Zipped3 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: c0535ca4d6e0de13bf809a21e69d100dcb798d1f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718693"
---
# <a name="zipped3-function"></a>Zipped3 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


3 개의 배열이 지정 된 경우 각 3 튜플은 각 원래 배열의 요소를 포함 하도록 3 튜플의 새 배열을 반환 합니다.

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a>입력

### <a name="first--t1"></a>first: ' t 1 []

각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.


### <a name="second--t2"></a>second: ' 2 []

각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.


### <a name="third--t3"></a>세 번째: ' t 3 []

각 튜플의 세 번째 요소에 대 한 값을 포함 하는 배열입니다.



## <a name="output--t1t2t3"></a>출력: (' 0 ', ' 2 ', ' t 3) []

각각에 대 한 폼의 3 개 튜플을 포함 하는 배열 `(first[idx], second[idx], third[idx])` `idx` 입니다. 세 배열의 길이가 같지 않은 경우 출력은 입력 중 짧은 값 만큼 길어야 합니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t1"></a>' 1 '

첫 번째 배열 요소의 형식입니다.
### <a name="t2"></a>' 2 '

두 번째 배열 요소의 형식입니다.
### <a name="t3"></a>' T 3

세 번째 배열 요소의 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft.Quantum.Arrays.Zip예: ped](xref:Microsoft.Quantum.Arrays.Zipped)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)