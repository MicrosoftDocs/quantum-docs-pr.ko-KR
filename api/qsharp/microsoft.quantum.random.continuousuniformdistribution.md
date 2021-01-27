---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: ContinuousUniformDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: c81eb433f50277c677756ee70d916f4856260c6d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842310"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="1e5d0-102">ContinuousUniformDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="1e5d0-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="1e5d0-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="1e5d0-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="1e5d0-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1e5d0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1e5d0-105">지정 된 포함 간격에 대해 균일 한 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e5d0-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="1e5d0-106">입력</span><span class="sxs-lookup"><span data-stu-id="1e5d0-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="1e5d0-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1e5d0-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1e5d0-108">그릴 최소 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e5d0-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="1e5d0-109">최대값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1e5d0-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1e5d0-110">그릴 최대 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e5d0-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="1e5d0-111">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="1e5d0-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="1e5d0-112">난수를 생성 하는 분포는의 포괄 간격에서 단일 확률을 갖는 실제 숫자입니다 `min` `max` .</span><span class="sxs-lookup"><span data-stu-id="1e5d0-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="1e5d0-113">예</span><span class="sxs-lookup"><span data-stu-id="1e5d0-113">Example</span></span>

<span data-ttu-id="1e5d0-114">다음 Q # 코드 조각은 임의로 $0 $과 $2 \pi $ 사이의 각도를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="1e5d0-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angleDistribution = ContinuousUniformDistribution(0.0, 2.0 * PI());
let angle = angleDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="1e5d0-115">설명</span><span class="sxs-lookup"><span data-stu-id="1e5d0-115">Remarks</span></span>

<span data-ttu-id="1e5d0-116">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e5d0-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e5d0-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1e5d0-117">See Also</span></span>

- [<span data-ttu-id="1e5d0-118">DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="1e5d0-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)