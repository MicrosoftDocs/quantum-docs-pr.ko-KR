---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: TransformedContinuousDistribution 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226267"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="8e6cf-102">TransformedContinuousDistribution 함수</span><span class="sxs-lookup"><span data-stu-id="8e6cf-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="8e6cf-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="8e6cf-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="8e6cf-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="8e6cf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="8e6cf-105">연속 분포가 지정 된 경우 지정 된 함수를 통해 원래를 변환 하는 새 분포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="8e6cf-106">입력</span><span class="sxs-lookup"><span data-stu-id="8e6cf-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="8e6cf-107">변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8e6cf-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8e6cf-108">원래 분포의 변형 된 분포를 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="8e6cf-109">배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="8e6cf-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="8e6cf-110">변환할 원래 분포입니다.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="8e6cf-111">출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="8e6cf-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="8e6cf-112">에서 제공 하는 변환과 관련 된 새 분포 `distribution` `transform` 입니다.</span><span class="sxs-lookup"><span data-stu-id="8e6cf-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>