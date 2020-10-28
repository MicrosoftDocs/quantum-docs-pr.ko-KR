---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC
title: ApplyToFirstThreeQubitsC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsC
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 9450b084cd77f75511fe631cda9a4f9fc426142d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717375"
---
# <a name="applytofirstthreequbitsc-operation"></a>ApplyToFirstThreeQubitsC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


레지스터의 처음 3 개 비트에 작업을 적용 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
operation ApplyToFirstThreeQubitsC (op : ((Qubit, Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubitqubitqubit--unit-ctl"></a>op[: (이상 비트](xref:microsoft.quantum.lang-ref.qubit),[고 비트, 고](xref:microsoft.quantum.lang-ref.qubit)[비트](xref:microsoft.quantum.lang-ref.qubit)) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

처음 세 개의에 적용 되는 작업입니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

연산이 적용 되는 처음 세 개의 비트에 대 한 기본 비트 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음 코드와 동일합니다.

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a>참고 항목

- [ApplyToFirstThreeQubits입니다.](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)