---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: DrawRandomDouble 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 6c0558ded2bd018afad84c42c2d15fc029ac0d44
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723987"
---
# <a name="drawrandomdouble-operation"></a>DrawRandomDouble 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


지정 된 포함 간격으로 임의의 실수를 그립니다.

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a>입력

### <a name="min--double"></a>min: [Double](xref:microsoft.quantum.lang-ref.double)

그릴 최소 실수입니다.


### <a name="max--double"></a>최대값: [Double](xref:microsoft.quantum.lang-ref.double)

그릴 최대 실수입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

에서로의 포괄 간격의 임의의 실수 `min` `max` 입니다.

## <a name="remarks"></a>설명

인 경우 실패 `max <= min` 합니다.

## <a name="see-also"></a>참고 항목

- [ContinuousUniformDistribution](xref:Microsoft.Quantum.ContinuousUniformDistribution)