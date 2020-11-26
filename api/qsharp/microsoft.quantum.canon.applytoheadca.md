---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Applyto헤드 Ca 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: f28cff599e06090145fac860dbaf8274c966f80a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208553"
---
# <a name="applytoheadca-operation"></a>Applyto헤드 Ca 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 첫 번째 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Head(targets))` .

## <a name="input"></a>입력

### <a name="op--t--unit--is-adj--ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

적용 될 작업입니다.


### <a name="targets--t"></a>대상: ' t []

첫 번째가 적용 될 대상의 배열입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToHead](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [Microsoft. 양자..](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [Microsoft. 양자. Applyto헤드 c](xref:Microsoft.Quantum.Canon.ApplyToHeadC)