---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: DrawRandomInt 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192913"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="244b6-102">DrawRandomInt 작업</span><span class="sxs-lookup"><span data-stu-id="244b6-102">DrawRandomInt operation</span></span>

<span data-ttu-id="244b6-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="244b6-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="244b6-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="244b6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="244b6-105">지정 된 포함 범위에서 임의의 정수를 그립니다.</span><span class="sxs-lookup"><span data-stu-id="244b6-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="244b6-106">입력</span><span class="sxs-lookup"><span data-stu-id="244b6-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="244b6-107">min: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="244b6-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="244b6-108">그릴 가장 작은 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="244b6-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="244b6-109">최대: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="244b6-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="244b6-110">그릴 가장 큰 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="244b6-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="244b6-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="244b6-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="244b6-112">의 포함 범위에서에 해당 하는 정수 `min` `max` 입니다.</span><span class="sxs-lookup"><span data-stu-id="244b6-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="244b6-113">설명</span><span class="sxs-lookup"><span data-stu-id="244b6-113">Remarks</span></span>

<span data-ttu-id="244b6-114">인 경우 실패 `max <= min` 합니다.</span><span class="sxs-lookup"><span data-stu-id="244b6-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="244b6-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="244b6-115">See Also</span></span>

- [<span data-ttu-id="244b6-116">DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="244b6-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)