---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: DiscreteUniformDistribution 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 08a62805f59df339ef6b91dff802c40c407808f4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193015"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="486c3-102">DiscreteUniformDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="486c3-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="486c3-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="486c3-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="486c3-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="486c3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="486c3-105">지정 된 포괄 범위에 대해 균일 한 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="486c3-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="486c3-106">입력</span><span class="sxs-lookup"><span data-stu-id="486c3-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="486c3-107">min: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="486c3-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="486c3-108">그릴 가장 작은 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="486c3-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="486c3-109">최대: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="486c3-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="486c3-110">그릴 가장 큰 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="486c3-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="486c3-111">출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="486c3-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="486c3-112">난수를 생성 하는 분포는의 포괄 범위에서 `min` `max` 단일 확률을 가진 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="486c3-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="486c3-113">설명</span><span class="sxs-lookup"><span data-stu-id="486c3-113">Remarks</span></span>

<span data-ttu-id="486c3-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="486c3-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="486c3-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="486c3-115">See Also</span></span>

- [<span data-ttu-id="486c3-116">DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="486c3-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)