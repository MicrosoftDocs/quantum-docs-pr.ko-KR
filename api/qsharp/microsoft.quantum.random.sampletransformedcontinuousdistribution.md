---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: SampleTransformedContinuousDistribution 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: dc93022e53199cd8ef794da9c1590d6997a0fda1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723973"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="d946c-102">SampleTransformedContinuousDistribution 작업</span><span class="sxs-lookup"><span data-stu-id="d946c-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="d946c-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d946c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d946c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d946c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d946c-105">변환 된 분포에서 샘플링 하기 위한 내부 전용 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d946c-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="d946c-106">부분 응용 프로그램을 통해서만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d946c-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="d946c-107">입력</span><span class="sxs-lookup"><span data-stu-id="d946c-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="d946c-108">변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d946c-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="d946c-109">배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="d946c-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="d946c-110">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d946c-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

