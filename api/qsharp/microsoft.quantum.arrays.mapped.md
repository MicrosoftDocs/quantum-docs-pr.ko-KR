---
uid: Microsoft.Quantum.Arrays.Mapped
title: Mapped 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 9632b9f53ffad8ece958ab1dc9ad446c7dcb9e13
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220742"
---
# <a name="mapped-function"></a>Mapped 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 요소에 대해 정의 된 배열과 함수가 지정 된 경우 함수에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>입력

### <a name="mapper--t---u"></a>매퍼: ' t > ' U

요소를 매핑하는 데 사용 되는의 함수입니다 `'T` `'U` .


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--u"></a>출력: ' U []

`'U[]`함수로 매핑되는 요소의 배열입니다 `mapper` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.
### <a name="u"></a>' U

함수의 결과 형식 `mapper` 입니다.

## <a name="remarks"></a>설명

함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 함수가 있을 때마다 `'T[]` `mapper: 'T -> 'U` 배열의 요소를 매핑하고 형식의 새 배열을 생성할 수 있습니다 `'U[]` .