---
uid: Microsoft.Quantum.Random.NormalDistribution
title: NormalDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814177"
---
# <a name="normaldistribution-function"></a><span data-ttu-id="cda25-102">NormalDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="cda25-102">NormalDistribution function</span></span>

<span data-ttu-id="cda25-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="cda25-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="cda25-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cda25-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="cda25-105">지정 된 평균과 분산이 있는 정규 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda25-105">Returns a normal distribution with a given mean and variance.</span></span>

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="cda25-106">입력</span><span class="sxs-lookup"><span data-stu-id="cda25-106">Input</span></span>

### <a name="mean--double"></a><span data-ttu-id="cda25-107">평균: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cda25-107">mean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="variance--double"></a><span data-ttu-id="cda25-108">분산: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cda25-108">variance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--continuousdistribution"></a><span data-ttu-id="cda25-109">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="cda25-109">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="cda25-110">예</span><span class="sxs-lookup"><span data-stu-id="cda25-110">Example</span></span>

<span data-ttu-id="cda25-111">다음은 평균 2와 표준 편차 0.1를 사용 하 여 정규 분포에서 10 개의 샘플을 그립니다.</span><span class="sxs-lookup"><span data-stu-id="cda25-111">The following draws 10 samples from the normal distribution with mean 2 and standard deviation 0.1:</span></span>

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a><span data-ttu-id="cda25-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cda25-112">See Also</span></span>

- [<span data-ttu-id="cda25-113">Microsoft 양자. StandardNormalDistribution</span><span class="sxs-lookup"><span data-stu-id="cda25-113">Microsoft.Quantum.Random.StandardNormalDistribution</span></span>](xref:Microsoft.Quantum.Random.StandardNormalDistribution)