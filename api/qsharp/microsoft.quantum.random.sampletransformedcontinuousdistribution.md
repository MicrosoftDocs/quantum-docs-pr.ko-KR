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
# <a name="sampletransformedcontinuousdistribution-operation"></a>SampleTransformedContinuousDistribution 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


변환 된 분포에서 샘플링 하기 위한 내부 전용 작업입니다.
부분 응용 프로그램을 통해서만 사용 해야 합니다.

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a>입력

### <a name="transform--double---double"></a>변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)




### <a name="distribution--continuousdistribution"></a>배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)





## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

