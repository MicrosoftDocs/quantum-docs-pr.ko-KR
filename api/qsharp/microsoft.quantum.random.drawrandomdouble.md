---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: DrawRandomDouble 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192947"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="460d8-102">DrawRandomDouble 작업</span><span class="sxs-lookup"><span data-stu-id="460d8-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="460d8-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="460d8-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="460d8-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="460d8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="460d8-105">지정 된 포함 간격으로 임의의 실수를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="460d8-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="460d8-106">입력</span><span class="sxs-lookup"><span data-stu-id="460d8-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="460d8-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="460d8-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="460d8-108">그릴 최소 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="460d8-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="460d8-109">최대값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="460d8-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="460d8-110">그릴 최대 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="460d8-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="460d8-111">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="460d8-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="460d8-112">에서로의 포괄 간격의 임의의 실수 `min` `max` 입니다.</span><span class="sxs-lookup"><span data-stu-id="460d8-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="460d8-113">설명</span><span class="sxs-lookup"><span data-stu-id="460d8-113">Remarks</span></span>

<span data-ttu-id="460d8-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="460d8-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="460d8-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="460d8-115">See Also</span></span>

- [<span data-ttu-id="460d8-116">ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="460d8-116">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)