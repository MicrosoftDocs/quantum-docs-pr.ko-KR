---
uid: Microsoft.Quantum.Random.DrawCategorical
title: DrawCategorical 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: fdc5ae3a9341cb11e8fda129bdd030289b6c99c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720284"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="cf7fc-102">DrawCategorical 작업</span><span class="sxs-lookup"><span data-stu-id="cf7fc-102">DrawCategorical operation</span></span>

<span data-ttu-id="cf7fc-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="cf7fc-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="cf7fc-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cf7fc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cf7fc-105">Probablities 목록에 지정 된 범주 분포의 무작위 샘플을 그립니다.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="cf7fc-106">Description</span><span class="sxs-lookup"><span data-stu-id="cf7fc-106">Description</span></span>

<span data-ttu-id="cf7fc-107">특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="cf7fc-108">0과 같은 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="cf7fc-109">배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="cf7fc-110">입력</span><span class="sxs-lookup"><span data-stu-id="cf7fc-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="cf7fc-111">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="cf7fc-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="cf7fc-112">각 인덱스를 선택할 확률에 비례 하는 부동 소수점 숫자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="cf7fc-113">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cf7fc-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cf7fc-114">$ \Pr (i) = p_i/\ sum_i p_i $와 같은 정수 $i $입니다. 여기서 $p _i $은의 $i $ th 요소입니다 `probs` .</span><span class="sxs-lookup"><span data-stu-id="cf7fc-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf7fc-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cf7fc-115">See Also</span></span>

- [<span data-ttu-id="cf7fc-116">CategoricalDistribution.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)