---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Motail 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845599"
---
# <a name="mostandtail-function"></a>Motail 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 모든 및 마지막 요소에 대 한 튜플을 반환 합니다.

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a>입력

### <a name="array--a"></a>array: ' A []

요소가 하나 이상 포함 된 배열입니다.



## <a name="output--aa"></a>Output: (' A [], ' A)

배열의 모든 및 마지막 요소에 대 한 튜플

## <a name="type-parameters"></a>형식 매개 변수

### <a name="a"></a>' A

배열 요소의 형식입니다.