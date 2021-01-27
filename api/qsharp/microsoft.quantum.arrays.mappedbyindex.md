---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: MappedByIndex 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845660"
---
# <a name="mappedbyindex-function"></a>MappedByIndex 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 인덱싱된 요소에 대해 정의 된 배열과 함수가 지정 된 경우 함수에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>입력

### <a name="mapper--intt---u"></a>매퍼: ([Int](xref:microsoft.quantum.lang-ref.int), ' t)-> ' U

`(Int, 'T)` `'U` 요소와 해당 인덱스를 매핑하는 데 사용 되는의 함수입니다.


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--u"></a>출력: ' U []

`'U[]`함수로 매핑되는 요소의 배열입니다 `mapper` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.
### <a name="u"></a>' U

함수의 결과 형식 `mapper` 입니다.

## <a name="example"></a>예

다음 두 줄은 동일 합니다.

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

및

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. 배열 매핑](xref:Microsoft.Quantum.Arrays.Mapped)