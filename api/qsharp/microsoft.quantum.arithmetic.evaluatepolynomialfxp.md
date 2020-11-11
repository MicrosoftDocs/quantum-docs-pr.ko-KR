---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: EvaluatePolynomialFxP 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 3903bf69d5b0a6e57530f2c6a44e1d351c8a605f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721184"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="0312c-102">EvaluatePolynomialFxP 작업</span><span class="sxs-lookup"><span data-stu-id="0312c-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="0312c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0312c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0312c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0312c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0312c-105">고정 소수점 표현에서 다항식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0312c-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="0312c-106">입력</span><span class="sxs-lookup"><span data-stu-id="0312c-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="0312c-107">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="0312c-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="0312c-108">이중 배열로 된 다항식의 계수입니다. 즉, 다항식 $P (x) = a_0 + a_1 x + \cdots + a_d x ^ d $의 배열 $ [a_0, a_1, ..., a_d] $입니다.</span><span class="sxs-lookup"><span data-stu-id="0312c-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="0312c-109">fpx: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0312c-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0312c-110">다항식을 계산할 입력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="0312c-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="0312c-111">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="0312c-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="0312c-112">$P (x) $를 포함 하는 출력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="0312c-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="0312c-113">처음에는 state $ \ket {0} $ 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0312c-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0312c-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0312c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
