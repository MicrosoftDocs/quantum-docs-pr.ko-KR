---
uid: Microsoft.Quantum.Random.DrawCategorical
title: DrawCategorical 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: fdc5ae3a9341cb11e8fda129bdd030289b6c99c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720284"
---
# <a name="drawcategorical-operation"></a>DrawCategorical 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


Probablities 목록에 지정 된 범주 분포의 무작위 샘플을 그립니다.

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a>Description

특정 인덱스를 선택할 확률은 해당 인덱스에 있는 배열 요소의 값에 비례 합니다.
0과 같은 배열 요소는 무시 되 고 해당 인덱스는 반환 되지 않습니다. 배열 요소가 0 보다 작거나 0 보다 큰 배열 요소가 없으면 작업이 실패 합니다.

## <a name="input"></a>입력

### <a name="probs--double"></a>probs: [Double](xref:microsoft.quantum.lang-ref.double)[]

각 인덱스를 선택할 확률에 비례 하는 부동 소수점 숫자의 배열입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

$ \Pr (i) = p_i/\ sum_i p_i $와 같은 정수 $i $입니다. 여기서 $p _i $은의 $i $ th 요소입니다 `probs` .

## <a name="see-also"></a>참고 항목

- [CategoricalDistribution.](xref:Microsoft.Quantum.Random.CategoricalDistribution)