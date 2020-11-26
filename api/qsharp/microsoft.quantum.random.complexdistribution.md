---
uid: Microsoft.Quantum.Random.ComplexDistribution
title: ComplexDistribution 사용자 정의 유형
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ComplexDistribution
qsharp.summary: Represents a univariate probability distribution over complex numbers.
ms.openlocfilehash: 660ebd43ffc1ce25f070716c936ec15ed54bd5dc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193151"
---
# <a name="complexdistribution-user-defined-type"></a><span data-ttu-id="1a7a1-102">ComplexDistribution 사용자 정의 유형</span><span class="sxs-lookup"><span data-stu-id="1a7a1-102">ComplexDistribution user defined type</span></span>

<span data-ttu-id="1a7a1-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="1a7a1-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="1a7a1-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1a7a1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1a7a1-105">복소수를 넘는 확률 분포를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a7a1-105">Represents a univariate probability distribution over complex numbers.</span></span>

```qsharp

newtype ComplexDistribution = (Sample : (Unit => Microsoft.Quantum.Math.Complex));
```



## <a name="named-items"></a><span data-ttu-id="1a7a1-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="1a7a1-106">Named Items</span></span>

### <a name="sample--unit--complex"></a><span data-ttu-id="1a7a1-107">샘플: [단위](xref:microsoft.quantum.lang-ref.unit) => [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="1a7a1-107">Sample : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span> 



## <a name="see-also"></a><span data-ttu-id="1a7a1-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1a7a1-108">See Also</span></span>

- [<span data-ttu-id="1a7a1-109">ContinuousDistribution.</span><span class="sxs-lookup"><span data-stu-id="1a7a1-109">Microsoft.Quantum.Random.ContinuousDistribution</span></span>](xref:Microsoft.Quantum.Random.ContinuousDistribution)
- [<span data-ttu-id="1a7a1-110">DiscreteDistribution.</span><span class="sxs-lookup"><span data-stu-id="1a7a1-110">Microsoft.Quantum.Random.DiscreteDistribution</span></span>](xref:Microsoft.Quantum.Random.DiscreteDistribution)
- [<span data-ttu-id="1a7a1-111">BigDiscreteDistribution.</span><span class="sxs-lookup"><span data-stu-id="1a7a1-111">Microsoft.Quantum.Random.BigDiscreteDistribution</span></span>](xref:Microsoft.Quantum.Random.BigDiscreteDistribution)