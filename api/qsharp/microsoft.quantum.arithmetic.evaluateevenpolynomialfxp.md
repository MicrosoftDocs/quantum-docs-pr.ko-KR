---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: EvaluateEvenPolynomialFxP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: 21c700ccb2b87b906fc4d8b65eddf962353948c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223258"
---
# <a name="evaluateevenpolynomialfxp-operation"></a>EvaluateEvenPolynomialFxP 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


고정 소수점 표현에서 짝수 다항식을 계산 합니다.

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="coefficients--double"></a>계수: [Double](xref:microsoft.quantum.lang-ref.double)[]

더블 배열인 짝수 다항식의 계수입니다. 즉, 짝수 다항식 $P (x) = a_0 + a_1 x ^ 2 + \cs+ a_k x ^ {2k} $에 대 한 배열 $ [a_0, a_1, ..., a_k] $입니다.


### <a name="fpx--fixedpoint"></a>fpx: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

다항식을 계산할 입력 고정 소수점 숫자입니다.


### <a name="result--fixedpoint"></a>결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

$P (x) $를 포함 하는 출력 고정 소수점 숫자입니다. 처음에는 state $ \ket {0} $ 여야 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

