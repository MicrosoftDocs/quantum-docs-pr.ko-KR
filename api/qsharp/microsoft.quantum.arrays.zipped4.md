---
uid: Microsoft.Quantum.Arrays.Zipped4
title: Zipped4 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d5ee10ac9776383e75bc16a5c003a8b1a65c5698
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219637"
---
# <a name="zipped4-function"></a>Zipped4 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


4 개의 배열이 지정 된 경우 각 4 튜플은 각 원래 배열의 요소를 포함 하도록 4 튜플의 새 배열을 반환 합니다.

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a>입력

### <a name="first--t1"></a>first: ' t 1 []

각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.


### <a name="second--t2"></a>second: ' 2 []

각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.


### <a name="third--t3"></a>세 번째: ' t 3 []

각 튜플의 세 번째 요소에 대 한 값을 포함 하는 배열입니다.


### <a name="fourth--t4"></a>네 번째: ' t 4 []

각 튜플의 네 번째 요소에 대 한 값을 포함 하는 배열입니다.



## <a name="output--t1t2t3t4"></a>출력: (' 0 ', ' 2 ', ' 2 ', 4) []

각에 대 한 형식의 4 개 튜플을 포함 하는 배열 `(first[idx], second[idx], third[idx], fourth[idx])` `idx` 입니다. 네 배열의 길이가 같지 않은 경우 출력은 입력 중 짧은 값 만큼 길어야 합니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t1"></a>' 1 '

첫 번째 배열 요소의 형식입니다.
### <a name="t2"></a>' 2 '

두 번째 배열 요소의 형식입니다.
### <a name="t3"></a>' T 3

세 번째 배열 요소의 형식입니다.
### <a name="t4"></a>' 4 '

네 번째 배열 요소의 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft.Quantum.Arrays.Zip예: ped](xref:Microsoft.Quantum.Arrays.Zipped)
- [Microsoft.Quantum.Arrays.Zipped3](xref:Microsoft.Quantum.Arrays.Zipped3)