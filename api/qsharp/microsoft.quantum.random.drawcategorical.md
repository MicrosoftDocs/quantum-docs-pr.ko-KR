---
uid: Microsoft.Quantum.Random.DrawCategorical
title: DrawCategorical 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a9fe1b08e80abc65a5c4b803f0cb8a5e7a62759c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851160"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="9838b-102">DrawCategorical 작업</span><span class="sxs-lookup"><span data-stu-id="9838b-102">DrawCategorical operation</span></span>

<span data-ttu-id="9838b-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="9838b-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="9838b-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9838b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9838b-105">Probablities 목록에 지정 된 범주 분포의 무작위 샘플을 그립니다.</span><span class="sxs-lookup"><span data-stu-id="9838b-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="9838b-106">설명</span><span class="sxs-lookup"><span data-stu-id="9838b-106">Description</span></span>

<span data-ttu-id="9838b-107">특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="9838b-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="9838b-108">0과 같은 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9838b-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="9838b-109">배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9838b-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="9838b-110">입력</span><span class="sxs-lookup"><span data-stu-id="9838b-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="9838b-111">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9838b-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9838b-112">각 인덱스를 선택할 확률에 비례 하는 부동 소수점 숫자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9838b-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="9838b-113">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9838b-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9838b-114">$ \Pr (i) = p_i/\ sum_i p_i $와 같은 정수 $i $입니다. 여기서 $p _i $은의 $i $ th 요소입니다 `probs` .</span><span class="sxs-lookup"><span data-stu-id="9838b-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9838b-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9838b-115">See Also</span></span>

- [<span data-ttu-id="9838b-116">CategoricalDistribution.</span><span class="sxs-lookup"><span data-stu-id="9838b-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)