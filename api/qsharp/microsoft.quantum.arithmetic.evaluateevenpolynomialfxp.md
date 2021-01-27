---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: EvaluateEvenPolynomialFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: c3129cb796a344f7ad38a585183db285d48892bf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843242"
---
# <a name="evaluateevenpolynomialfxp-operation"></a><span data-ttu-id="c4533-102">EvaluateEvenPolynomialFxP 작업</span><span class="sxs-lookup"><span data-stu-id="c4533-102">EvaluateEvenPolynomialFxP operation</span></span>

<span data-ttu-id="c4533-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c4533-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c4533-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="c4533-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="c4533-105">고정 소수점 표현에서 짝수 다항식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4533-105">Evaluates an even polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c4533-106">입력</span><span class="sxs-lookup"><span data-stu-id="c4533-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="c4533-107">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c4533-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c4533-108">더블 배열인 짝수 다항식의 계수입니다. 즉, 짝수 다항식 $P (x) = a_0 + a_1 x ^ 2 + \cs+ a_k x ^ {2k} $에 대 한 배열 $ [a_0, a_1, ..., a_k] $입니다.</span><span class="sxs-lookup"><span data-stu-id="c4533-108">Coefficients of the even polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the even polynomial $P(x) = a_0 + a_1 x^2 + \cdots + a_k x^{2k}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="c4533-109">fpx: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="c4533-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="c4533-110">다항식을 계산할 입력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c4533-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="c4533-111">결과: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="c4533-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="c4533-112">$P (x) $를 포함 하는 출력 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c4533-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="c4533-113">처음에는 state $ \ket {0} $ 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4533-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4533-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4533-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

