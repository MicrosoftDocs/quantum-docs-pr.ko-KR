---
uid: Microsoft.Quantum.Random.BigDiscreteDistribution
title: BigDiscreteDistribution 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: BigDiscreteDistribution
qsharp.summary: Represents a univariate probability distribution over integers of arbitrary size.
ms.openlocfilehash: add39f057b209bb19336a2af3d08aefcf8e1e11e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193202"
---
# <a name="bigdiscretedistribution-user-defined-type"></a>BigDiscreteDistribution 사용자 정의 형식

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


임의 크기의 정수에 대 한 확률 분포를 나타냅니다.

```qsharp

newtype BigDiscreteDistribution = (Sample : (Unit => BigInt));
```



## <a name="named-items"></a>명명 된 항목

### <a name="sample--unit--bigint"></a>샘플: [유닛](xref:microsoft.quantum.lang-ref.unit) => [BigInt](xref:microsoft.quantum.lang-ref.bigint) 



## <a name="see-also"></a>참고 항목

- [ContinuousDistribution.](xref:Microsoft.Quantum.Random.ContinuousDistribution)
- [Microsoft 양자 배포](xref:Microsoft.Quantum.Random.ComplexDistribution)
- [DiscreteDistribution.](xref:Microsoft.Quantum.Random.DiscreteDistribution)