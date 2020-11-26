---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: MappedOverRange 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: b1d73c2503e63ed09a3d6a56421760ca29eb0c3f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220691"
---
# <a name="mappedoverrange-function"></a>MappedOverRange 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


정수를 입력으로 사용 하는 범위와 함수가 지정 된 경우 함수 아래 범위 값의 이미지로 구성 된 새 배열을 반환 합니다.

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a>입력

### <a name="mapper--int---t"></a>매퍼: [Int](xref:microsoft.quantum.lang-ref.int) -> ' t

범위 값을 매핑하는 데 사용 되는의 함수입니다 `Int` `'T` .


### <a name="range--range"></a>범위: [범위](xref:microsoft.quantum.lang-ref.range)

정수 범위입니다.



## <a name="output--t"></a>출력: ' t []

`'T[]`함수로 매핑되는 요소의 배열입니다 `mapper` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

함수의 결과 형식 `mapper` 입니다.

## <a name="remarks"></a>설명

함수는 제네릭 형식에 대해 정의 됩니다. 즉, 함수가 있을 때마다 `mapper: Int -> 'T` 범위의 값을 매핑하고 형식의 배열을 생성할 수 있습니다 `'T[]` .

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. 배열 매핑](xref:Microsoft.Quantum.Arrays.Mapped)