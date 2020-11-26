---
uid: Microsoft.Quantum.Arrays.Unzipped
title: 압축이 풀린 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: aee1d48c9e0a1f104040bc56c78fdbb8bc4d34ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219960"
---
# <a name="unzipped-function"></a>압축이 풀린 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


2 튜플 배열이 지정 된 경우 각각 입력 배열의 튜플 요소를 포함 하는 두 배열의 튜플을 반환 합니다.

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a>입력

### <a name="arr--tu"></a>arr: (' t ', ' U) []

2 개의 튜플을 포함 하는 배열입니다.



## <a name="output--tu"></a>Output: (' ' ', ' U [])

첫 번째 배열은 입력 튜플의 모든 첫 번째 요소를 포함 하 고 두 번째 배열은 입력 튜플의 두 번째 요소를 모두 포함 하는 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

각 튜플에 있는 첫 번째 요소의 형식입니다.
### <a name="u"></a>' U

각 튜플에서 두 번째 요소의 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft.Quantum.Arrays.Zip예: ped](xref:Microsoft.Quantum.Arrays.Zipped)