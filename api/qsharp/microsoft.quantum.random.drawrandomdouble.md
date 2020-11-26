---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: DrawRandomDouble 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192947"
---
# <a name="drawrandomdouble-operation"></a>DrawRandomDouble 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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