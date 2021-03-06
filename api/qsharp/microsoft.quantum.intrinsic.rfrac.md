---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: RFrac 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: c80bb2b394e83c1133ed6ddc1640a3d88563ca6e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818477"
---
# <a name="rfrac-operation"></a>RFrac 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dyadic 분수로 지정 된 각도 만큼 지정 된 Pauli 축에 대 한 회전을 적용 합니다.

\begin{align} R_ {\mu} (n, k) \mathrel{: =} e ^ {i \pi n \ sigma_ {\mu}/2 ^ k}, \end{align} where $ \pi \pi \{ i, X, Y, Z \} $.

> [!WARNING]
> 이 작업에서는의 **반대** 서명 규칙을 사용 @"microsoft.quantum.intrinsic.r" 합니다.

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

지수화 하 여 회전을 형성 하는 연산자입니다.


### <a name="numerator--int"></a>분자: [Int](xref:microsoft.quantum.lang-ref.int)

Dyadic 분수를 회전 하는 각도를 나타내는 분자입니다.


### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)

제곱 비트를 회전할 각도의 분모를 지정 하는 2의 거듭제곱입니다.


### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

게이트가 적용 되어야 하는의 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음에 해당 합니다.

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```