---
uid: Microsoft.Quantum.Intrinsic.M
title: M 연산
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 0037d7f5ad060857c6ca2c863b1d24aca3e338cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818866"
---
# <a name="m-operation"></a>M 연산

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Pauli $Z $ 기준에서 단일 고 비트를 측정 합니다.

출력 결과는 배포 \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.에 의해 제공 됩니다.
\end{align}

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a>입력

### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

측정할 비트입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`Zero` $ + $1 eigenvalue가 관찰 되 면이 고, `One` $-$1 eigenvalue가 관찰 되 면입니다.

## <a name="remarks"></a>설명

다음에 해당 합니다.

```qsharp
Measure([PauliZ], [qubit]);
```