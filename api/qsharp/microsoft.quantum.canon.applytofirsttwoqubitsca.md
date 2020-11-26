---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA
title: ApplyToFirstTwoQubitsCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsCA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: a2281776b617d5c3f8cc706ea09d14995fce4a27
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208655"
---
# <a name="applytofirsttwoqubitsca-operation"></a>ApplyToFirstTwoQubitsCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 처음 두 비트에 작업을 적용 합니다.
한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.

```qsharp
operation ApplyToFirstTwoQubitsCA (op : ((Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="op--qubitqubit--unit--is-adj--ctl"></a>op: (Adj[bit](xref:microsoft.quantum.lang-ref.qubit),[?](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl

처음 두 개의 작업에 적용 되는 작업입니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

연산이 적용 되는 처음 두 개의 비트에 대 한 기본 비트 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음 코드와 동일합니다.

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a>참고 항목

- [ApplyToFirstTwoQubits입니다.](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)