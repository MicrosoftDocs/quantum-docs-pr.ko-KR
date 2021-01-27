---
uid: Microsoft.Quantum.Arrays.ElementsAt
title: ElementsAt 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementsAt
qsharp.summary: Returns the array's elements at a given range of indices.
ms.openlocfilehash: 295aa4e2d79857405186b835d9788f59db83d1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842786"
---
# <a name="elementsat-function"></a>ElementsAt 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 인덱스 범위에서 배열의 요소를 반환 합니다.

```qsharp
function ElementsAt<'T> (range : Range, array : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="range--range"></a>범위: [범위](xref:microsoft.quantum.lang-ref.range)

배열 인덱스의 범위


### <a name="array--t"></a>배열: ' t []

Array



## <a name="output--t"></a>출력: ' t []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="example"></a>예

유명한 정수 시퀀스에서 홀수 인덱스를 가져옵니다. 0 인덱스는 시퀀스의 _첫 번째_ 값에 해당 합니다.

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famousOdd = Mapped(ElementsAt<Int>(0..2..9, _), [lucas, prime, fibonacci, catalan]);
// same as: famousOdd = [[2, 3, 7, 18, 47], [2, 5, 11, 17, 23], [0, 1, 3, 8, 21], [1, 2, 14, 132, 1430]]
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자.](xref:Microsoft.Quantum.Arrays.ElementAt)
- [Microsoft 양자 함수](xref:Microsoft.Quantum.Arrays.LookupFunction)