---
uid: Microsoft.Quantum.Arrays.Zipped
title: 압축 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 67170fa005675f0e5d788c9c3b350fb9a961a597
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718712"
---
# <a name="zipped-function"></a>압축 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


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

## <a name="see-also"></a>참고 항목

- [Microsoft.Quantum.Arrays.Zipped3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Microsoft 양자. 배열 압축 해제](xref:Microsoft.Quantum.Arrays.Unzipped)