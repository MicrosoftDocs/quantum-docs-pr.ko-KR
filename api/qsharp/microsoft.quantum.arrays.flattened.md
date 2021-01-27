---
uid: Microsoft.Quantum.Arrays.Flattened
title: 평면화 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848627"
---
# <a name="flattened-function"></a>평면화 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 배열이 지정 된 경우 모든 배열의 연결을 반환 합니다.

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a>입력

### <a name="arrays--t"></a>배열: ' t [] []

배열의 배열입니다.



## <a name="output--t"></a>출력: ' t []

모든 배열의 연결입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```