---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: 교환 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: e93c976f2fdf02de77fafa4d22e95fe9a33a9ba6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198421"
---
# <a name="swap-operation"></a>교환 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


교환 게이트를 다양 한 쌍에 적용 합니다.

\begin{align} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 0 & 1 & 0 & \\ \\ 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

여기에서 행과 열은 퀀텀 개념 가이드에서로 정렬 됩니다.

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="qubit1--qubit"></a>qubit1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

교환할 첫 번째 비트입니다.


### <a name="qubit2--qubit"></a>qubit2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

스왑할 두 번째 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음에 해당 합니다.

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```