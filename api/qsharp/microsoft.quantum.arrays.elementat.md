---
uid: Microsoft.Quantum.Arrays.ElementAt
title: ElementAt 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementAt
qsharp.summary: Returns the at the given index of an array.
ms.openlocfilehash: 2d31c62a4a5ba3b273e7440b5dfe4482b47e3a8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842812"
---
# <a name="elementat-function"></a>ElementAt 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 지정 된 인덱스에 있는를 반환 합니다.

```qsharp
function ElementAt<'T> (index : Int, array : 'T[]) : 'T
```


## <a name="input"></a>입력

### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)

요소의 인덱스


### <a name="array--t"></a>배열: ' t []

인덱싱되는 배열입니다.



## <a name="output--t"></a>출력: ' '



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="example"></a>예

네 가지 유명한 정수 시퀀스에서 세 번째 숫자를 가져옵니다. 0 인덱스는 시퀀스의 _첫 번째_ 값에 해당 합니다.

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famous2 = Mapped(ElementAt<Int>(2, _), [lucas, prime, fibonacci, catalan]);
// same as: famous2 = [3, 5, 1, 2]
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 함수](xref:Microsoft.Quantum.Arrays.LookupFunction)
- [Microsoft 양자.](xref:Microsoft.Quantum.Arrays.ElementsAt)