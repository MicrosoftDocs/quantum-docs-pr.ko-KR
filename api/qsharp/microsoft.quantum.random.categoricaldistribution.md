---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: CategoricalDistribution 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210253"
---
# <a name="categoricaldistribution-function"></a>CategoricalDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 결과의 각 한정 된 목록에 대 한 확률이 명시적으로 지정 된 불연속 범주 분포를 반환 합니다.

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>입력

### <a name="probs--double"></a>probs: [Double](xref:microsoft.quantum.lang-ref.double)[]

범주 분포의 각 결과에 대 한 확률입니다.
이러한 확률은 정규화 되지 않을 수 있지만 모두 음수가 아니어야 합니다.



## <a name="output--discretedistribution"></a>출력: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

확률을 포함 하는 인덱스입니다 `i` `probs[i] / sum` `sum` . 여기서는에 지정 된의 합계입니다 `probs` `Fold(PlusD, 0.0, probs)` .