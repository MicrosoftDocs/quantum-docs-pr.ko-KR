---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: SampleTransformedContinuousDistribution 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: f9f2b3cbbb4423f267758976cd066abbfec93a77
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192692"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="da681-102">SampleTransformedContinuousDistribution 작업</span><span class="sxs-lookup"><span data-stu-id="da681-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="da681-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="da681-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="da681-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="da681-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="da681-105">변환 된 분포에서 샘플링 하기 위한 내부 전용 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="da681-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="da681-106">부분 응용 프로그램을 통해서만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da681-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="da681-107">입력</span><span class="sxs-lookup"><span data-stu-id="da681-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="da681-108">변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="da681-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="da681-109">배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="da681-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="da681-110">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="da681-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

