---
uid: Microsoft.Quantum.Random.NormalDistribution
title: NormalDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814177"
---
# <a name="normaldistribution-function"></a>NormalDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 평균과 분산이 있는 정규 분포를 반환 합니다.

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>입력

### <a name="mean--double"></a>평균: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="variance--double"></a>분산: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--continuousdistribution"></a>출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>예

다음은 평균 2와 표준 편차 0.1를 사용 하 여 정규 분포에서 10 개의 샘플을 그립니다.

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. StandardNormalDistribution](xref:Microsoft.Quantum.Random.StandardNormalDistribution)