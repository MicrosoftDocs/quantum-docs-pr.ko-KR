---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Exp 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 7aa6974e83e917125b63ef91fb5c3b1238f6e856
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819004"
---
# <a name="exp-operation"></a>Exp 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


다중값 비트 Pauli 연산자의 지 수를 적용 합니다.

\begin{align} e ^ {i \theta [P_0 \otime P_1 \coP_ {N-1}]}, \end{align} $P _i $은의 $i $ th 요소 `paulis` 이며 where $N = $입니다 `Length(paulis)` .

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="paulis--pauli"></a>paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]

각 텐서에 대 한 제품 요소를 나타내는 단일 값의 배열입니다.


### <a name="theta--double"></a>테타: [Double](xref:microsoft.quantum.lang-ref.double)

대상 레지스터를 회전 하는 데 사용한 지정 된 다중 기능 비트 Pauli 연산자의 각도입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

지정 된 회전을에 적용 하려면 등록 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

