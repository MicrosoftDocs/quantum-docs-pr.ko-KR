---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: ApplyPauliFromBitString 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: cf4c99ec5134fac788cdd4c8a057258790152a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209063"
---
# <a name="applypaulifrombitstring-operation"></a>ApplyPauliFromBitString 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부울 배열의 해당 비트가 지정 된 입력과 일치 하는 경우 배열의 각 비트에 Pauli 연산자를 적용 합니다.

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

에 적용할 pauli 연산자 `qubits[idx]``bitsApply == bits[idx]`


### <a name="bitapply--bool"></a>bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)

bit가이 값인 경우 Pauli 적용


### <a name="bits--bool"></a>bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

에서 작동 해야 하는 해당 고 비트를 지정 하는 부울 레지스터입니다. `qubits`


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

지정 된 Pauli 연산자를 선택적으로 적용할 퀀텀 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.