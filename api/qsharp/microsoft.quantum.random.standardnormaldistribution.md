---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: StandardNormalDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857806"
---
# <a name="standardnormaldistribution-function"></a><span data-ttu-id="43694-102">StandardNormalDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="43694-102">StandardNormalDistribution function</span></span>

<span data-ttu-id="43694-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="43694-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="43694-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="43694-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="43694-105">평균 0과 분산이 1 인 정규 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43694-105">Returns a normal distribution with mean 0 and variance 1.</span></span>

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a><span data-ttu-id="43694-106">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="43694-106">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="43694-107">예</span><span class="sxs-lookup"><span data-stu-id="43694-107">Example</span></span>

<span data-ttu-id="43694-108">다음은 표준 정규 분포에서 10 개의 샘플을 그립니다.</span><span class="sxs-lookup"><span data-stu-id="43694-108">The following draws 10 samples from the standard normal distribution:</span></span>

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a><span data-ttu-id="43694-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="43694-109">See Also</span></span>

- [<span data-ttu-id="43694-110">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="43694-110">Microsoft.Quantum.Random.NormalDistribution</span></span>](xref:Microsoft.Quantum.Random.NormalDistribution)