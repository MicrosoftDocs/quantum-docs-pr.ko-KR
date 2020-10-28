---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: ApplyToEachCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: b24fbb8c7a1a55c0a7750c5d096a61f4824dadfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717550"
---
# <a name="applytoeachca-operation"></a>ApplyToEachCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


레지스터의 각 요소에 단일 수준 비트 작업을 적용 합니다.
한정자는 `CA` 단일의 비트 작업을 제어 하 고 adjointable 나타냅니다.

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a>입력

### <a name="singleelementoperation--t--unit-adj--ctl"></a>singleElementOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl

각 고 비트에 적용할 연산입니다.


### <a name="register--t"></a>등록: ' t []

지정 된 작업을 적용할 대상 비트의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

작업이 수행 되는 대상입니다.

## <a name="see-also"></a>참고 항목

- [각각의 Microsoft 양자](xref:Microsoft.Quantum.Canon.ApplyToEach)