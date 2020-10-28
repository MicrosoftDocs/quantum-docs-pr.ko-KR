---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: ContinuousUniformDistribution 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709430"
---
# <a name="continuousuniformdistribution-function"></a>ContinuousUniformDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


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