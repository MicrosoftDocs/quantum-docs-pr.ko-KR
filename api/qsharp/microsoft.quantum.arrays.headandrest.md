---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: 헤드 Andrest 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221082"
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