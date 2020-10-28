---
uid: Microsoft.Quantum.Arrays.Head
title: Head 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 7b26a9c414ab2caad70f96f3c26c2d1cf0b03e95
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719185"
---
# <a name="head-function"></a>Head 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


배열의 첫 번째 요소를 반환 합니다.

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a>입력

### <a name="array--a"></a>array: ' A []

첫 번째 요소를 가져올 배열입니다. 배열의 길이는 1 이상 이어야 합니다.



## <a name="output--a"></a>출력: ' A

배열의 첫 번째 요소입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="a"></a>' A

배열 요소의 형식입니다.