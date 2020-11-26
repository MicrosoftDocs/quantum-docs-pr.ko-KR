---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: ComputeReciprocalFxP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: 3ca050d6ce9daaa10e14c2f12dd571398cf436b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223394"
---
# <a name="computereciprocalfxp-operation"></a>ComputeReciprocalFxP 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


고정 소수점 숫자 $x $에 대해 $1/x $를 계산 합니다.

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="x--fixedpoint"></a>x: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

반전 시킬 고정 소수점 숫자입니다.


### <a name="result--fixedpoint"></a>결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

결과를 보관할 고정 소수점 숫자입니다. $ \Ket{0.0} $로 초기화 해야 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

