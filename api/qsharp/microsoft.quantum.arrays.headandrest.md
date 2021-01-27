---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: 헤드 Andrest 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848554"
---
# <a name="headandrest-function"></a>헤드 Andrest 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 첫 번째 및 나머지 모든 요소에 대 한 튜플을 반환 합니다.

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a>입력

### <a name="array--a"></a>array: ' A []

요소가 하나 이상 포함 된 배열입니다.



## <a name="output--aa"></a>Output: (' A, ' A [])

배열의 첫 번째 및 나머지 모든 요소에 대 한 튜플입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="a"></a>' A

배열 요소의 형식입니다.