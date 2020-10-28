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
# <a name="transformedcontinuousdistribution-function"></a>TransformedContinuousDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


연속 분포가 지정 된 경우 지정 된 함수를 통해 원래를 변환 하는 새 분포를 반환 합니다.

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>입력

### <a name="transform--double---double"></a>변환: [이중](xref:microsoft.quantum.lang-ref.double) -> [double](xref:microsoft.quantum.lang-ref.double)

원래 분포의 변형 된 분포를 변환 하는 함수입니다.


### <a name="distribution--continuousdistribution"></a>배포: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

변환할 원래 분포입니다.



## <a name="output--continuousdistribution"></a>출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

에서 제공 하는 변환과 관련 된 새 분포 `distribution` `transform` 입니다.