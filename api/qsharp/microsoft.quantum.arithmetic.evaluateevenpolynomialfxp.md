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
# <a name="evaluateevenpolynomialfxp-operation"></a><span data-ttu-id="0beeb-102">EvaluateEvenPolynomialFxP 작업</span><span class="sxs-lookup"><span data-stu-id="0beeb-102">EvaluateEvenPolynomialFxP operation</span></span>

<span data-ttu-id="0beeb-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0beeb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0beeb-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0beeb-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0beeb-105">고정 소수점 표현에서 짝수 다항식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0beeb-105">Evaluates an even polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0beeb-106">입력</span><span class="sxs-lookup"><span data-stu-id="0beeb-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="0beeb-107">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="0beeb-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="0beeb-108">더블 배열인 짝수 다항식의 계수입니다. 즉, 짝수 다항식 $P (x) = a_0 + a_1 x ^ 2 + \cs+ a_k x ^ {2k} $에 대 한 배열 $ [a_0, a_1, ..., a_k] $입니다.</span><span class="sxs-lookup"><span data-stu-id="0beeb-108">Coefficients of the even polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the even polynomial $P(x) = a_0 + a_1 x^2 + \cdots + a_k x^{2k}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="0beeb-109">fpx: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0beeb-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0beeb-110">다항식을 계산할 입력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="0beeb-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="0beeb-111">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0beeb-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0beeb-112">$P (x) $를 포함 하는 출력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="0beeb-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="0beeb-113">처음에는 state $ \ket {0} $ 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0beeb-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0beeb-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0beeb-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

