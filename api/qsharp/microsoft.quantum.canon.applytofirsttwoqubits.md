---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: ApplyToFirstTwoQubits 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: e4f1eb396efb390c7470ea2aaf5c3b5be60b8c1b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217410"
---
# <a name="applytofirsttwoqubits-operation"></a>ApplyToFirstTwoQubits 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터의 처음 두 비트에 작업을 적용 합니다.

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubitqubit--unit"></a>op: ([(고](xref:microsoft.quantum.lang-ref.qubit)[비트](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

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

- [ApplyToFirstTwoQubitsA입니다.](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [ApplyToFirstTwoQubitsC입니다.](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [ApplyToFirstTwoQubitsCA입니다.](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)