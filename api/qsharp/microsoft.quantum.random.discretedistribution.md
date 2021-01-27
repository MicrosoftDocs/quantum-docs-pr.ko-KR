---
uid: Microsoft.Quantum.Random.DiscreteDistribution
title: DiscreteDistribution 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteDistribution
qsharp.summary: Represents a univariate probability distribution over integers.
ms.openlocfilehash: a3278d03dee9b30acd6fc6b61b94267adb4ae44f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851166"
---
# <a name="discretedistribution-user-defined-type"></a>DiscreteDistribution 사용자 정의 형식

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


정수에 대 한 확률 분포를 나타냅니다.

```qsharp

newtype DiscreteDistribution = (Sample : (Unit => Int));
```



## <a name="named-items"></a>명명 된 항목

### <a name="sample--unit--int"></a>샘플: [단위](xref:microsoft.quantum.lang-ref.unit) => [Int](xref:microsoft.quantum.lang-ref.int) 



## <a name="see-also"></a>참고 항목

- [ContinuousDistribution.](xref:Microsoft.Quantum.Random.ContinuousDistribution)
- [Microsoft 양자 배포](xref:Microsoft.Quantum.Random.ComplexDistribution)
- [BigDiscreteDistribution.](xref:Microsoft.Quantum.Random.BigDiscreteDistribution)