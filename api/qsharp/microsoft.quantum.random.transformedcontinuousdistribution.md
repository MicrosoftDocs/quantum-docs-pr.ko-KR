---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: TransformedContinuousDistribution 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710942"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="63462-102">TransformedContinuousDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="63462-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="63462-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="63462-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="63462-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="63462-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="63462-105">연속 분포가 지정 된 경우 지정 된 함수를 통해 원래를 변환 하는 새 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="63462-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="63462-106">입력</span><span class="sxs-lookup"><span data-stu-id="63462-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="63462-107">변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="63462-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="63462-108">원래 분포의 변형 된 분포를 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="63462-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="63462-109">배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="63462-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="63462-110">변환할 원래 분포입니다.</span><span class="sxs-lookup"><span data-stu-id="63462-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="63462-111">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="63462-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="63462-112">에서 제공 하는 변환과 관련 된 새 분포 `distribution` `transform` 입니다.</span><span class="sxs-lookup"><span data-stu-id="63462-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>