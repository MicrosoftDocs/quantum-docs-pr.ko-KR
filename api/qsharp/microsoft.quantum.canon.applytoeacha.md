---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: ApplyToEachA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844612"
---
# <a name="applytoeacha-operation"></a>ApplyToEachA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.
한정자는 `A` 단일의 비트 연산이 adjointable을 나타냅니다.

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="singleelementoperation--t--unit--is-adj"></a>singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

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