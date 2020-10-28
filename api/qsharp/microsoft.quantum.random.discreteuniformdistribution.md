---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: DiscreteUniformDistribution 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720296"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="31786-102">DiscreteUniformDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="31786-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="31786-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="31786-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="31786-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="31786-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="31786-105">지정 된 포괄 범위에 대해 균일 한 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="31786-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="31786-106">입력</span><span class="sxs-lookup"><span data-stu-id="31786-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="31786-107">min: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31786-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31786-108">그릴 가장 작은 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="31786-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="31786-109">최대: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31786-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31786-110">그릴 가장 큰 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="31786-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="31786-111">출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="31786-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="31786-112">난수를 생성 하는 분포는의 포괄 범위에서 `min` `max` 단일 확률을 가진 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="31786-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="31786-113">설명</span><span class="sxs-lookup"><span data-stu-id="31786-113">Remarks</span></span>

<span data-ttu-id="31786-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="31786-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="31786-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="31786-115">See Also</span></span>

- [<span data-ttu-id="31786-116">DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="31786-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)