---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: DiscreteUniformDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853729"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="1e921-102">DiscreteUniformDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="1e921-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="1e921-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="1e921-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="1e921-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1e921-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1e921-105">지정 된 포괄 범위에 대해 균일 한 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e921-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="1e921-106">입력</span><span class="sxs-lookup"><span data-stu-id="1e921-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="1e921-107">min: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1e921-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1e921-108">그릴 가장 작은 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e921-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="1e921-109">최대: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1e921-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1e921-110">그릴 가장 큰 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e921-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="1e921-111">출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="1e921-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="1e921-112">난수를 생성 하는 분포는의 포괄 범위에서 `min` `max` 단일 확률을 가진 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e921-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="1e921-113">예</span><span class="sxs-lookup"><span data-stu-id="1e921-113">Example</span></span>

<span data-ttu-id="1e921-114">다음 Q # 코드 조각은 임의로 6 면 주사위를 롤업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e921-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="1e921-115">설명</span><span class="sxs-lookup"><span data-stu-id="1e921-115">Remarks</span></span>

<span data-ttu-id="1e921-116">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e921-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e921-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1e921-117">See Also</span></span>

- [<span data-ttu-id="1e921-118">DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="1e921-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)