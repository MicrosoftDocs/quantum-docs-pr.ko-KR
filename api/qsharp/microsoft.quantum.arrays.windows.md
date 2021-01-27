---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: adfea2b9a2f6c22446817538d29586284dba723e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842205"
---
# <a name="windows-function"></a>Windows 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


길이의 연속 subarrays 모두 반환 합니다 `size` .

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a>설명

이 함수는의 길이에 대 한 모든 `n - size + 1` subarrays을 순서 대로 반환 합니다 `size` `n` . 여기서은의 길이입니다 `arr` .
첫 번째 subarrays는 `arr[0..size - 1], arr[1..size], arr[2..size + 1]` 마지막 하위 배열까지 `arr[n - size..n - 1]` 입니다.

또는 인 경우 `size <= 0` `size > n` 빈 배열이 반환 됩니다.

## <a name="input"></a>입력

### <a name="size--int"></a>크기: [Int](xref:microsoft.quantum.lang-ref.int)

Subarrays의 길이입니다.


### <a name="array--t"></a>배열: ' t []

요소의 배열입니다.



## <a name="output--t"></a>출력: ' t [] []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
// same as [[1, 2, 3], [2, 3, 4], [3, 4, 5]]
let windows = Windows(3, [1, 2, 3, 4, 5]);
```