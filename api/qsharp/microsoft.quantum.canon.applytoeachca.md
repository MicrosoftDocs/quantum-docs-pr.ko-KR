---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: ApplyToEachCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841484"
---
# <a name="applytoeachca-operation"></a>ApplyToEachCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.
한정자는 `CA` 단일의 비트 작업을 제어 하 고 adjointable 나타냅니다.

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a>singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

각 고 비트에 적용할 연산입니다.


### <a name="register--t"></a>등록: ' t []

지정 된 작업을 적용할 대상 비트의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

작업이 수행 되는 대상입니다.

## <a name="example"></a>예

3-이상 비트 $ \ket{+} $ 상태 준비:

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a>참고 항목

- [각각의 Microsoft 양자](xref:Microsoft.Quantum.Canon.ApplyToEach)