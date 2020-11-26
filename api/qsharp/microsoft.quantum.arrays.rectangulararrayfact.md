---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: RectangularArrayFact 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220419"
---
# <a name="rectangulararrayfact-function"></a>RectangularArrayFact 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


2 차원 배열에 사각형 모양이 있는 상태를 나타냅니다.

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>Description

이 함수는 배열의 각 행 길이가 동일 함을 어설션 합니다.

## <a name="input"></a>입력

### <a name="array--t"></a>배열: ' t [] []

요소의 2 차원 배열입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

배열이 사각형 배열이 아닌 경우 인쇄 될 메시지입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="see-also"></a>참고 항목

- [SquareArrayFact.](xref:Microsoft.Quantum.Arrays.SquareArrayFact)