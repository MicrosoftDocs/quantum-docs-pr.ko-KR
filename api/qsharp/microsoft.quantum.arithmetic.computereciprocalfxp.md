---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: ComputeReciprocalFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: db7425f1a8a9b5ddfdc6b123dad003298e3670e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843255"
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

