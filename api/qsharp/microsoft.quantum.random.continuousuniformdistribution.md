---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: ContinuousUniformDistribution 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709430"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="cbbdd-102">ContinuousUniformDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="cbbdd-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="cbbdd-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="cbbdd-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="cbbdd-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cbbdd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cbbdd-105">지정 된 포함 간격에 대해 균일 한 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbbdd-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="cbbdd-106">입력</span><span class="sxs-lookup"><span data-stu-id="cbbdd-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="cbbdd-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cbbdd-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cbbdd-108">그릴 최소 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="cbbdd-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="cbbdd-109">최대값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cbbdd-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cbbdd-110">그릴 최대 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="cbbdd-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="cbbdd-111">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="cbbdd-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="cbbdd-112">난수를 생성 하는 분포는의 포괄 간격에서 단일 확률을 갖는 실제 숫자입니다 `min` `max` .</span><span class="sxs-lookup"><span data-stu-id="cbbdd-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbbdd-113">설명</span><span class="sxs-lookup"><span data-stu-id="cbbdd-113">Remarks</span></span>

<span data-ttu-id="cbbdd-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbbdd-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbbdd-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cbbdd-115">See Also</span></span>

- [<span data-ttu-id="cbbdd-116">DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="cbbdd-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)