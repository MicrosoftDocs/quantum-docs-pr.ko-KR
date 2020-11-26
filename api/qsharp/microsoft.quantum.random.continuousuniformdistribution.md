---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: ContinuousUniformDistribution 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193083"
---
# <a name="continuousuniformdistribution-function"></a>ContinuousUniformDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 포함 간격에 대해 균일 한 분포를 반환 합니다.

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>입력

### <a name="min--double"></a>min: [Double](xref:microsoft.quantum.lang-ref.double)

그릴 최소 실수입니다.


### <a name="max--double"></a>최대값: [Double](xref:microsoft.quantum.lang-ref.double)

그릴 최대 실수입니다.



## <a name="output--continuousdistribution"></a>출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

난수를 생성 하는 분포는의 포괄 간격에서 단일 확률을 갖는 실제 숫자입니다 `min` `max` .

## <a name="remarks"></a>설명

인 경우 실패 `max <= min` 합니다.

## <a name="see-also"></a>참고 항목

- [DrawRandomDouble](xref:Microsoft.Quantum.DrawRandomDouble)