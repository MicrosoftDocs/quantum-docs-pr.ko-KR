---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: DiscreteUniformDistribution 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720296"
---
# <a name="discreteuniformdistribution-function"></a>DiscreteUniformDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


지정 된 포괄 범위에 대해 균일 한 분포를 반환 합니다.

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>입력

### <a name="min--int"></a>min: [Int](xref:microsoft.quantum.lang-ref.int)

그릴 가장 작은 정수입니다.


### <a name="max--int"></a>최대: [Int](xref:microsoft.quantum.lang-ref.int)

그릴 가장 큰 정수입니다.



## <a name="output--discretedistribution"></a>출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

난수를 생성 하는 분포는의 포괄 범위에서 `min` `max` 단일 확률을 가진 정수입니다.

## <a name="remarks"></a>설명

인 경우 실패 `max <= min` 합니다.

## <a name="see-also"></a>참고 항목

- [DrawRandomDouble](xref:Microsoft.Quantum.DrawRandomDouble)