---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: SquareArrayFact 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: a154e5becba4dae762596a3fc1b268855520fa1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850975"
---
# <a name="squarearrayfact-function"></a>SquareArrayFact 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


2 차원 배열에 사각형 모양의 조건을 나타냅니다.

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>설명

이 함수는 배열의 각 행에 배열에 있는 행 (요소) 만큼의 요소가 있음을 어설션 합니다.

## <a name="input"></a>입력

### <a name="array--t"></a>배열: ' t [] []

요소의 2 차원 배열입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

배열이 정사각형 배열이 아닌 경우 인쇄 될 메시지입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="example"></a>예제

```qsharp
SquareArrayFact([[1, 2], [3, 4]], "Array is not a square");       // okay
SquareArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not a square"); // will fail
SquareArrayFact([[1, 2], [3, 4, 5]], "Array is not a square");    // will fail
```

## <a name="see-also"></a>참고 항목

- [RectangularArrayFact.](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)