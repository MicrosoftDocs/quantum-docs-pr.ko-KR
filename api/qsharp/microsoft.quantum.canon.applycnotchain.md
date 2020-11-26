---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: ApplyCNOTChain 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: e237e4424661de816e73b0c78523180b41190cf9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219144"
---
# <a name="applycnotchain-operation"></a>ApplyCNOTChain 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


내부에서의 레지스터 패리티를 계산 합니다.

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

이 작업을 수행 하면 해당 입력의 상태가 $ $ \begin{align} \ket{q_0} \ket{q_1} \cdots} q_ {n-1}} & \maps\ket{q_0} \ket{q_0 \cdots} \ket{q_1 \cdots q_0 \cdots q_1} \cdots q_2 \cdots \co\o {n-1}}로 변환 됩니다.
\end{align} $ $

## <a name="input"></a>입력

### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

패리티를 계산 하 고 저장 하는 데 사용할 수 있는 비트의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

