---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: ExtendedGreatestCommonDivisorI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: e86237f39e696485a3496f1c6dd571cd516214ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857547"
---
# <a name="extendedgreatestcommondivisori-function"></a><span data-ttu-id="ebf81-102">ExtendedGreatestCommonDivisorI 함수</span><span class="sxs-lookup"><span data-stu-id="ebf81-102">ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="ebf81-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ebf81-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ebf81-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ebf81-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ebf81-105">$U \cdot a + v \cdot b = \operatorname{GCD} (a, b) $와 같이 튜플을 $ (u, v) $로 계산 합니다. 여기서 $ \operatorname{GCD} $은 $a $ $a $ 및 $b $의 최대 공약수입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf81-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="ebf81-106">GCD는 항상 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf81-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="ebf81-107">입력</span><span class="sxs-lookup"><span data-stu-id="ebf81-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="ebf81-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ebf81-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ebf81-109">확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf81-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="ebf81-110">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ebf81-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ebf81-111">확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf81-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--intint"></a><span data-ttu-id="ebf81-112">Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="ebf81-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="ebf81-113">튜플을 $ (u, v) $로, 속성 $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf81-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="ebf81-114">참조</span><span class="sxs-lookup"><span data-stu-id="ebf81-114">References</span></span>

- <span data-ttu-id="ebf81-115">이 구현은 다음에 따라 구현 됩니다. https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="ebf81-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>