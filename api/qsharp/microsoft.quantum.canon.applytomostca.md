---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: ApplyToMostCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 797cbd835446f31b2df60dbb184f888e6d0356aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717165"
---
# <a name="applytomostca-operation"></a>ApplyToMostCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


배열의 마지막 요소를 제외한 모든 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a>Description

작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Most(targets))` .

## <a name="input"></a>입력

### <a name="op--t--unit-adj--ctl"></a>op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl

적용 될 작업입니다.


### <a name="targets--t"></a>대상: ' t []

마지막가 적용 되는 대상의 배열입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToMost](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [Microsoft. 양자. ApplyToMostA](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [Microsoft. 양자. ApplyToMostC](xref:Microsoft.Quantum.Canon.ApplyToMostC)