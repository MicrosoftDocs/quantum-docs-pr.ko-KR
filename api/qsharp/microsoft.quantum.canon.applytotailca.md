---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: ApplyToTailCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 00755df80981a09ddfd8327ee9b35761d30af4f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716941"
---
# <a name="applytotailca-operation"></a>ApplyToTailCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


배열의 마지막 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a>Description

작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Tail(targets))` .

## <a name="input"></a>입력

### <a name="op--t--unit-adj--ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl

적용 될 작업입니다.


### <a name="targets--t"></a>대상: ' t []

마지막이 적용 될 대상의 배열입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToTail](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [ApplyToTailA입니다.](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [ApplyToTailC입니다.](xref:Microsoft.Quantum.Canon.ApplyToTailC)