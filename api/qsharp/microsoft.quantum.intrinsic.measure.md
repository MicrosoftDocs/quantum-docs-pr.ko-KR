---
uid: Microsoft.Quantum.Intrinsic.Measure
title: 측정 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: 804ae72ed2d5302b14011b737b7ed3ad2b9a14ca
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212293"
---
# <a name="measure-operation"></a>측정 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 Pauli 기반에서 하나 이상의 값에 대 한 공동 측정을 수행 합니다.

출력 결과는 배포에 의해 제공 됩니다. \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \frac12 \braket{\pr \pr | \pr (\boldone + P_0 \otime P_1 \ost\oatimes P_ {N-1} \pr) \pr | \pr}, \end{align} 여기서 $P _i $은의 $i $ th 요소이 `bases` 고 where $N = \texttt{Length} (\texttt{bases}) $입니다.
즉, 측정값은 `Result` 관찰 된 측정 효과의 eigenvalue가 $ (-1) ^ d $ 인 $d $를 반환 합니다.

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a>입력

### <a name="bases--pauli"></a>기본: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

각 텐서에 대 한 제품 요소를 나타내는 단일 값의 배열입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

측정할 비트의 레지스터입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`Zero` $ + $1 eigenvalue가 관찰 되 면이 고, `One` $-$1 eigenvalue가 관찰 되 면입니다.

## <a name="remarks"></a>설명

기본 배열 및 기본 비트 배열의 길이가 다른 경우 작업이 실패 합니다.