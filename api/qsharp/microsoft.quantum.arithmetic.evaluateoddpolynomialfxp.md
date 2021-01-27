---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: EvaluateOddPolynomialFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: 852e986cd09c3b2e31263f53e381d9da73298415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846674"
---
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="6dc3a-102">EvaluateOddPolynomialFxP 작업</span><span class="sxs-lookup"><span data-stu-id="6dc3a-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="6dc3a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6dc3a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6dc3a-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="6dc3a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="6dc3a-105">고정 소수점 표현에서 홀수 다항식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dc3a-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6dc3a-106">입력</span><span class="sxs-lookup"><span data-stu-id="6dc3a-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="6dc3a-107">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6dc3a-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6dc3a-108">이중 배열인 홀수 다항식의 계수입니다. 즉, 홀수 다항식 $P (x) = a_0 x + a_1 x ^ 3 + \cdots + a_k x ^ {2k + 1} $에 대 한 배열 $ [a_0, a_1, ..., a_k] $입니다.</span><span class="sxs-lookup"><span data-stu-id="6dc3a-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="6dc3a-109">fpx: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="6dc3a-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="6dc3a-110">다항식을 계산할 입력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="6dc3a-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="6dc3a-111">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="6dc3a-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="6dc3a-112">P (x)를 포함 하는 출력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="6dc3a-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="6dc3a-113">처음에는 state $ \ket {0} $ 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dc3a-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6dc3a-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6dc3a-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

