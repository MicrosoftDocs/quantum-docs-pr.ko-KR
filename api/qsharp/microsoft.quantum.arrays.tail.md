---
uid: Microsoft.Quantum.Arrays.Tail
title: Tail 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 680562228a39263ef87ba053e6b7683412947e46
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845403"
---
# <a name="tail-function"></a>Tail 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 마지막 요소를 반환합니다.

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a>입력

### <a name="array--a"></a>array: ' A []

마지막 요소를 가져올 배열입니다. 배열의 길이는 1 이상 이어야 합니다.



## <a name="output--a"></a>출력: ' A

배열의 마지막 요소입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="a"></a>' A

배열 요소의 형식입니다.