---
uid: Microsoft.Quantum.Arrays.Reversed
title: 반전 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 50699465711de45ff994095e6c098550d637d608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845467"
---
# <a name="reversed-function"></a>반전 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


입력 배열과 동일한 요소가 포함 된 배열을 역순으로 만듭니다.

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="array--t"></a>배열: ' t []

요소가 역순으로 복사 될 배열입니다.



## <a name="output--t"></a>출력: ' t []

요소가 포함 된 배열입니다 `array[Length(array) - 1]` . `array[0]`.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

배열 요소의 형식입니다.