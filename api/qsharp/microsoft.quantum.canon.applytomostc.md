---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: ApplyToMostC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 14de9f367aa7d19f64f13186d402239ae1fef3c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850568"
---
# <a name="applytomostc-operation"></a>ApplyToMostC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 마지막 요소를 제외한 모든 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>설명

작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Most(targets))` .

## <a name="input"></a>입력

### <a name="op--t--unit--is-ctl"></a>op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.

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
- [Microsoft. 양자. ApplyToMostCA](xref:Microsoft.Quantum.Canon.ApplyToMostCA)