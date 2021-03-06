---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: PreparePauliEigenstate 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: 473bb2fa4429a14f69bcae4573354aad87dc37df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854351"
---
# <a name="preparepaulieigenstate-operation"></a>PreparePauliEigenstate 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 Pauli 연산자의 긍정 eigenstate에서 원하는 비트를 준비 합니다.
Id 연산자가 지정 된 경우에는 최대 혼합 된 상태에서 해당 비트를 준비 합니다.

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a>설명

이 작업은 처음에 $ \ket $ 상태에 있는 경우 {0} 이 작업을 통해 지정 된 Pauli 연산자의 $ + $1 eigenstate 또는의 최대 mixed 상태 ()에 대 한 추가 비트를 준비 `PauliI` 합니다 (참조 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).

이 연산은 $ \ket $ 이외의 상태에 있는 경우 {0} 다음 게이트를 적용 합니다. $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` 및 <xref:microsoft.quantum.preparation.preparesinglequbitidentity> `PauliI`

## <a name="input"></a>입력

### <a name="basis--pauli"></a>기준: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Pauli 연산자 $P $.


### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

준비할 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

$ \Ket{+} $ 상태에서이를 준비 하려면 다음을 수행 합니다.

```qsharp
using (q = Qubit()) {
    PreparePauliEigenstate(PauliX, qubit);
    // ...
}
```