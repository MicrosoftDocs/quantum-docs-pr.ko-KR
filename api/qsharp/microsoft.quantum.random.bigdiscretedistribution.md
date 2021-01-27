---
uid: Microsoft.Quantum.Random.BigDiscreteDistribution
title: BigDiscreteDistribution 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: BigDiscreteDistribution
qsharp.summary: Represents a univariate probability distribution over integers of arbitrary size.
ms.openlocfilehash: de33b458b63a8c1f2c4af28dbb7db0b97367ce98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855803"
---
# <a name="bigdiscretedistribution-user-defined-type"></a><span data-ttu-id="0c877-102">BigDiscreteDistribution 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="0c877-102">BigDiscreteDistribution user defined type</span></span>

<span data-ttu-id="0c877-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="0c877-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="0c877-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0c877-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0c877-105">임의 크기의 정수에 대 한 확률 분포를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c877-105">Represents a univariate probability distribution over integers of arbitrary size.</span></span>

```qsharp

newtype BigDiscreteDistribution = (Sample : (Unit => BigInt));
```



## <a name="named-items"></a><span data-ttu-id="0c877-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="0c877-106">Named Items</span></span>

### <a name="sample--unit--bigint"></a><span data-ttu-id="0c877-107">샘플: [유닛](xref:microsoft.quantum.lang-ref.unit) => [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0c877-107">Sample : [Unit](xref:microsoft.quantum.lang-ref.unit) => [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span> 



## <a name="see-also"></a><span data-ttu-id="0c877-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0c877-108">See Also</span></span>

- [<span data-ttu-id="0c877-109">ContinuousDistribution.</span><span class="sxs-lookup"><span data-stu-id="0c877-109">Microsoft.Quantum.Random.ContinuousDistribution</span></span>](xref:Microsoft.Quantum.Random.ContinuousDistribution)
- [<span data-ttu-id="0c877-110">Microsoft 양자 배포</span><span class="sxs-lookup"><span data-stu-id="0c877-110">Microsoft.Quantum.Random.ComplexDistribution</span></span>](xref:Microsoft.Quantum.Random.ComplexDistribution)
- [<span data-ttu-id="0c877-111">DiscreteDistribution.</span><span class="sxs-lookup"><span data-stu-id="0c877-111">Microsoft.Quantum.Random.DiscreteDistribution</span></span>](xref:Microsoft.Quantum.Random.DiscreteDistribution)