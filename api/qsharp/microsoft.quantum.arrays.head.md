---
uid: Microsoft.Quantum.Arrays.Head
title: Head 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 6dd181914b5ed3ef16a02b31cb6131daf2a34e19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848563"
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