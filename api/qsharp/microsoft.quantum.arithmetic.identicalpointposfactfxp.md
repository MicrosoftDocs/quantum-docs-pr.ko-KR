---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: IdenticalPointPosFactFxP 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 907e270e1c3710fb346044ad7757171c6d5f568d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223054"
---
# <a name="identicalpointposfactfxp-function"></a>IdenticalPointPosFactFxP 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


제공 된 배열의 모든 고정 소수점 숫자가 최하위 비트에서 계산 될 때 동일한 점 위치를 갖도록 어설션 합니다. 즉, 비트 수 빼기 point position은 배열의 모든 고정 소수점 숫자에 대해 상수 여야 합니다.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>입력

### <a name="fixedpoints--fixedpoint"></a>fixedPoints: [Fixedpoints](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

호환성을 검사 하는 퀀텀 고정 소수점 숫자 (어설션 사용)의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

