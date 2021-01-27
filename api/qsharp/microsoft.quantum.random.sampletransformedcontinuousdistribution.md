---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: SampleTransformedContinuousDistribution 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: 62f6f4ff372143228de007c98a23697022fcfd24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856097"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="f7d2c-102">SampleTransformedContinuousDistribution 작업</span><span class="sxs-lookup"><span data-stu-id="f7d2c-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="f7d2c-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="f7d2c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="f7d2c-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f7d2c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f7d2c-105">변환 된 분포에서 샘플링 하기 위한 내부 전용 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f7d2c-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="f7d2c-106">부분 응용 프로그램을 통해서만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7d2c-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="f7d2c-107">입력</span><span class="sxs-lookup"><span data-stu-id="f7d2c-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="f7d2c-108">변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f7d2c-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="f7d2c-109">배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="f7d2c-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="f7d2c-110">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f7d2c-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

