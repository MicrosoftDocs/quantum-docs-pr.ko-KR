---
uid: Microsoft.Quantum.Arrays.Zipped
title: 압축 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 5177ab0ade5a9ad7788e60c1028befb84b0191d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845342"
---
# <a name="zipped-function"></a>압축 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 배열이 지정 된 경우 각 쌍은 각 원래 배열의 요소를 포함 하도록 쌍의 새 배열을 반환 합니다.

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a>입력

### <a name="left--t"></a>left: ' t []

각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.


### <a name="right--u"></a>right: ' U []

각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.



## <a name="output--tu"></a>출력: (' t ', ' U) []

각에 대 한 폼의 쌍을 포함 하는 배열 `(left[idx], right[idx])` `idx` 입니다. 두 배열의 길이가 같지 않은 경우에는 입력 중 짧은 값 만큼 출력 됩니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

왼쪽 배열 요소의 형식입니다.
### <a name="u"></a>' U

오른쪽 배열 요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zipped(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a>참고 항목

- [Microsoft.Quantum.Arrays.Zipped3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Microsoft 양자. 배열 압축 해제](xref:Microsoft.Quantum.Arrays.Unzipped)