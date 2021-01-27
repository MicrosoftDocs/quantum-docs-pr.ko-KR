---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: R1Frac 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfae01d11524f64ceebd53aa8544d7ea48c40f31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818681"
---
# <a name="r1frac-operation"></a>R1Frac 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Dyadic 분수로 지정 된 각도로 $ \ket $ 상태에 대 한 회전을 적용 {1} 합니다.

\begin{align} R_1 (n, k) \mathrel{: =} \operatorname{diag} (1, e ^ {i \pi k/2 ^ n}).
\end{align}

> [!WARNING]
> 이 작업은에서 **반대** 부호 규칙을 사용 @"microsoft.quantum.intrinsic.r" 하며에 포함 된 $1/2 $의 요소를 포함 하지 않습니다 @"microsoft.quantum.intrinsic.r1" .

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

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
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```