---
uid: Microsoft.Quantum.Arrays.Head
title: Head 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 834cbe2384122463be6a0efcb6e09785aae9c092
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221116"
---
# <a name="head-function"></a>Head 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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