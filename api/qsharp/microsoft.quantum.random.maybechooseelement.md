---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: MaybeChooseElement 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192862"
---
# <a name="maybechooseelement-operation"></a>MaybeChooseElement 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


데이터 배열 및 해당 인덱스에 대 한 분포를 지정 하는 경우에서 임의로 요소를 선택 하려고 시도 합니다.

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a>입력

### <a name="data--t"></a>데이터: ' t []

요소를 선택 해야 하는 배열입니다.


### <a name="indexdistribution--discretedistribution"></a>indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

의 인덱스에 대 한 분포 `data` 입니다.



## <a name="output--boolt"></a>Output: ([Bool](xref:microsoft.quantum.lang-ref.bool), ' t)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

