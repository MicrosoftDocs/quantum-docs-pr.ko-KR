---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: MaybeChooseElement 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856121"
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



## <a name="example"></a>예

다음 Q # 코드 조각은 배열에서 임의로 요소를 선택 합니다.

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```