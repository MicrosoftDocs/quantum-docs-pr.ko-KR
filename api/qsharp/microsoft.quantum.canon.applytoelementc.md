---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: ApplyToElementC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: c8d7841e3846ab435671f7959c724f987d8ad5a0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217580"
---
# <a name="applytoelementc-operation"></a>ApplyToElementC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 지정 된 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Description

작업 `op` , 인덱스 `index` 및 대상의 배열이 지정 된 `targets` 경우 적용 됩니다 `op(targets[index])` .

## <a name="input"></a>입력

### <a name="op--t--unit--is-ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.

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
- [Microsoft. 양자. ApplyToElementA](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [Microsoft. 양자. ApplyToElementCA](xref:Microsoft.Quantum.Canon.ApplyToElementCA)