---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: ApplyToRestA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 69001f6c8d65806e7259f2d2f2741d48866daa84
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841258"
---
# <a name="applytoresta-operation"></a>ApplyToRestA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 첫 번째 요소를 제외한 모든 요소에 작업을 적용 합니다.

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a>설명

작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Rest(targets))` .

## <a name="input"></a>입력

### <a name="op--t--unit--is-adj"></a>op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj

적용 될 작업입니다.


### <a name="targets--t"></a>대상: ' t []

첫 번째가 적용 되는 대상의 배열입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 작업의 입력 형식입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyToRest](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [Microsoft. 양자. ApplyToRestC](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [Microsoft 양자. ApplyToRestCA](xref:Microsoft.Quantum.Canon.ApplyToRestCA)