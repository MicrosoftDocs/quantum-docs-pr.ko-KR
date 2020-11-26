---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: ApplyCCNOTChain 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: 275f31ea636d15eb0d78e5148e8af6b58d22729d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209658"
---
# <a name="applyccnotchain-operation"></a>ApplyCCNOTChain 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


레지스터 중 하나에 대 한 다음의 비트에서 작동 하는 두 개의 두 비트 레지스터의 해당 비트에서 제어 되는 CCNOT 게이트의 cascade를 구현 합니다.
두 레지스터의 위치 0에 있는 이상에서 시작 하 여, CCNOT은 대상 레지스터의 위치 1에 있는 나머지 비트에 적용 되 고, 대상 레지스터의 위치 2에 있는 두 번째 위치에 있는 두 번째 위치에 있는 나머지 비트에 의해 제어 `Length(nQubits)-1` 됩니다.

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

컨트롤에만 사용 되는  bit 레지스터입니다.


### <a name="targets--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

컨트롤 및 대상으로 사용 되는 및 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

대상의 비트 레지스터는 다른 레지스터 보다 하나 이상 커야 합니다.