---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: DrawRandomDouble 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 6c0558ded2bd018afad84c42c2d15fc029ac0d44
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723987"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="934b9-102">DrawRandomDouble 작업</span><span class="sxs-lookup"><span data-stu-id="934b9-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="934b9-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="934b9-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="934b9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="934b9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="934b9-105">지정 된 포함 간격으로 임의의 실수를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="934b9-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="934b9-106">입력</span><span class="sxs-lookup"><span data-stu-id="934b9-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="934b9-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="934b9-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="934b9-108">그릴 최소 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="934b9-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="934b9-109">최대값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="934b9-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="934b9-110">그릴 최대 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="934b9-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="934b9-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="934b9-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="934b9-112">에서로의 포괄 간격의 임의의 실수 `min` `max` 입니다.</span><span class="sxs-lookup"><span data-stu-id="934b9-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="934b9-113">설명</span><span class="sxs-lookup"><span data-stu-id="934b9-113">Remarks</span></span>

<span data-ttu-id="934b9-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="934b9-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="934b9-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="934b9-115">See Also</span></span>

- [<span data-ttu-id="934b9-116">ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="934b9-116">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)