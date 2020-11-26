---
uid: Microsoft.Quantum.Canon.ApplyToHeadA
title: Applyto헤드 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3397c059706c48ff8ca47dd2312cfa9565aacaba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208638"
---
# <a name="applytoheada-operation"></a>Applyto헤드 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 첫 번째 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToHeadA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a>설명

작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Head(targets))` .

## <a name="input"></a>입력

### <a name="op--t--unit--is-adj"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

적용 될 작업입니다.


### <a name="targets--t"></a>대상: ' t []

첫 번째가 적용 될 대상의 배열입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToHead](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [Microsoft. 양자. Applyto헤드 c](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [Microsoft 양자. Applyto헤드 Ca](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)