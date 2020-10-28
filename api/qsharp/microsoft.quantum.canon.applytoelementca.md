---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: ApplyToElementCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 599a8afe1ab97b0ab0d6621cabd7707faaeddda3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717445"
---
# <a name="applytoelementca-operation"></a>ApplyToElementCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


배열의 지정 된 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a>Description

작업 `op` , 인덱스 `index` 및 대상의 배열이 지정 된 `targets` 경우 적용 됩니다 `op(targets[index])` .

## <a name="input"></a>입력

### <a name="op--t--unit-adj--ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl

적용 될 작업입니다.


### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)

대상 배열의 인덱스입니다.


### <a name="targets--t"></a>대상: ' t []

에 대해 가능한 대상의 배열입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToElement](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [Microsoft. 양자. ApplyToElementC](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Microsoft. 양자. ApplyToElementA](xref:Microsoft.Quantum.Canon.ApplyToElementA)