---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: ExtendedGreatestCommonDivisorL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: abbbd367859952180f181a245ca0754646529b18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210712"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="b9120-102">ExtendedGreatestCommonDivisorL 함수</span><span class="sxs-lookup"><span data-stu-id="b9120-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="b9120-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b9120-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b9120-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b9120-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b9120-105">$U \cdot a + v \cdot b = \operatorname{GCD} (a, b) $와 같이 튜플을 $ (u, v) $로 계산 합니다. 여기서 $ \operatorname{GCD} $은 $a $ $a $ 및 $b $의 최대 공약수입니다.</span><span class="sxs-lookup"><span data-stu-id="b9120-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="b9120-106">GCD는 항상 양수입니다.</span><span class="sxs-lookup"><span data-stu-id="b9120-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="b9120-107">입력</span><span class="sxs-lookup"><span data-stu-id="b9120-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="b9120-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b9120-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b9120-109">확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="b9120-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="b9120-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b9120-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b9120-111">확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="b9120-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="b9120-112">출력: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="b9120-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="b9120-113">튜플을 $ (u, v) $로, 속성 $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $입니다.</span><span class="sxs-lookup"><span data-stu-id="b9120-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="b9120-114">참조 항목</span><span class="sxs-lookup"><span data-stu-id="b9120-114">References</span></span>

- <span data-ttu-id="b9120-115">이 구현은 다음에 따라 구현 됩니다. https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="b9120-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>