---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: DrawRandomInt 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724659"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="877c4-102">DrawRandomInt 작업</span><span class="sxs-lookup"><span data-stu-id="877c4-102">DrawRandomInt operation</span></span>

<span data-ttu-id="877c4-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="877c4-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="877c4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="877c4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="877c4-105">지정 된 포함 범위에서 임의의 정수를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="877c4-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="877c4-106">입력</span><span class="sxs-lookup"><span data-stu-id="877c4-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="877c4-107">min: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="877c4-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="877c4-108">그릴 가장 작은 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="877c4-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="877c4-109">최대: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="877c4-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="877c4-110">그릴 가장 큰 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="877c4-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="877c4-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="877c4-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="877c4-112">의 포함 범위에서에 해당 하는 정수 `min` `max` 입니다.</span><span class="sxs-lookup"><span data-stu-id="877c4-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="877c4-113">설명</span><span class="sxs-lookup"><span data-stu-id="877c4-113">Remarks</span></span>

<span data-ttu-id="877c4-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="877c4-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="877c4-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="877c4-115">See Also</span></span>

- [<span data-ttu-id="877c4-116">DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="877c4-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)