---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: PrepareQubit 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 84674d70d6a038ceaf1c637b22afa1b724d90795
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193525"
---
# <a name="preparequbit-operation"></a>PrepareQubit 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> PrepareQubit는 더 이상 사용 되지 않습니다. 대신 <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate>를 사용하십시오.

`Zero`지정 된 Pauli 연산자의 + 1 () eigenstate에서 eibit를 준비 합니다.
Id 연산자가 지정 된 경우에는 최대 혼합 된 상태에서 해당 비트를 준비 합니다.

이 작업은 처음에 $ \ket $ 상태에 있는 경우 {0} 이 작업을 통해 지정 된 Pauli 연산자의 $ + $1 eigenstate 또는의 최대 mixed 상태 ()에 대 한 추가 비트를 준비 `PauliI` 합니다 (참조 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).

이 연산은 $ \ket $ 이외의 상태에 있는 경우 {0} 다음 게이트를 적용 합니다. $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` 및 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> `PauliI`

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a>입력

### <a name="basis--pauli"></a>기준: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Pauli 연산자 $P $.


### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

준비할 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

