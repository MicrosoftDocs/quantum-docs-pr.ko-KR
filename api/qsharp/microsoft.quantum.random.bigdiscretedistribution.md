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