---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: CategoricalDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842358"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="c53e6-102">CategoricalDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="c53e6-102">CategoricalDistribution function</span></span>

<span data-ttu-id="c53e6-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="c53e6-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="c53e6-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c53e6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c53e6-105">지정 된 결과의 각 한정 된 목록에 대 한 확률이 명시적으로 지정 된 불연속 범주 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c53e6-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="c53e6-106">입력</span><span class="sxs-lookup"><span data-stu-id="c53e6-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="c53e6-107">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c53e6-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c53e6-108">범주 분포의 각 결과에 대 한 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="c53e6-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="c53e6-109">이러한 확률은 정규화 되지 않을 수 있지만 모두 음수가 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c53e6-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="c53e6-110">출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="c53e6-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="c53e6-111">확률을 포함 하는 인덱스입니다 `i` `probs[i] / sum` `sum` . 여기서는에 지정 된의 합계입니다 `probs` `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="c53e6-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>

## <a name="example"></a><span data-ttu-id="c53e6-112">예</span><span class="sxs-lookup"><span data-stu-id="c53e6-112">Example</span></span>

<span data-ttu-id="c53e6-113">다음 Q # 코드는 확률은 30%이 고 1은 확률 70% 인 경우 0을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c53e6-113">The following Q# code will display 0 with probability 30% and 1 with probability 70%:</span></span>

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```