---
uid: Microsoft.Quantum.Arrays.Most
title: 대부분 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 2b212b38ec55f3798eb9397f03b842573173eb88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845571"
---
# <a name="most-function"></a>대부분 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


마지막 배열 요소가 삭제 된 경우를 제외 하 고 입력 배열과 같은 배열을 만듭니다.

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="array--t"></a>배열: ' t []

첫 번째-마지막 요소에 대 한 첫 번째 요소에서 출력 배열을 형성 하는 배열입니다.



## <a name="output--t"></a>출력: ' t []

요소를 포함 하는 배열 `array[0..Length(array) - 2]` 입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

배열 요소의 형식입니다.