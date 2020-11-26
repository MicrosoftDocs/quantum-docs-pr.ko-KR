---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: CategoricalDistribution 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210253"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="6db7a-102">CategoricalDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="6db7a-102">CategoricalDistribution function</span></span>

<span data-ttu-id="6db7a-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="6db7a-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="6db7a-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6db7a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6db7a-105">지정 된 결과의 각 한정 된 목록에 대 한 확률이 명시적으로 지정 된 불연속 범주 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db7a-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="6db7a-106">입력</span><span class="sxs-lookup"><span data-stu-id="6db7a-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="6db7a-107">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6db7a-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6db7a-108">범주 분포의 각 결과에 대 한 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="6db7a-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="6db7a-109">이러한 확률은 정규화 되지 않을 수 있지만 모두 음수가 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db7a-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="6db7a-110">출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="6db7a-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="6db7a-111">확률을 포함 하는 인덱스입니다 `i` `probs[i] / sum` `sum` . 여기서는에 지정 된의 합계입니다 `probs` `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="6db7a-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>