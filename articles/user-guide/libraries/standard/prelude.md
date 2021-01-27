---
title: QDK의 내장 작업 및 함수
description: 클래식 함수 및 단일 함수, 회전 및 측정 작업을 포함 하 여 QDK의 내장 작업 및 함수에 대해 알아봅니다.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
uid: microsoft.quantum.libraries.standard.prelude
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6ed5b1677a204b9425f229a3ea0855bb789f3f75
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857197"
---
# <a name="the-prelude"></a>Prelude #

Q#퀀텀 개발 키트에 포함 된 컴파일러 및 대상 컴퓨터는에서 퀀텀 프로그램을 작성할 때 사용할 수 있는 내장 함수 및 작업 집합을 제공 합니다 Q# .

## <a name="intrinsic-operations-and-functions"></a>내장 작업 및 함수 ##

표준 라이브러리에 정의 된 기본 작업은 다음과 같은 몇 가지 범주 중 하나에 해당 합니다.

- 네임 스페이스에 수집 된 필수 기존 함수 <xref:Microsoft.Quantum.Core>
- [Clifford 및 $T $ 게이트](xref:microsoft.quantum.concepts.qubit)로 구성 된 unitaries를 나타내는 작업입니다.
- 다양 한 연산자에 대 한 회전을 나타내는 작업입니다.
- 측정을 구현 하는 작업입니다.

Clifford + $T $ gate 집합은 퀀텀 컴퓨팅을 위한 [유니버설](xref:microsoft.quantum.concepts.multiple-qubits) 이므로 negligibly 작은 오류 내에서 임의 퀀텀 알고리즘을 구현 하는 데에는 충분 합니다.
또한 회전을 제공 하 여 Q# 프로그래머는 단일의 단일 기능 및 CNOT gate 라이브러리 내에서 작업할 수 있습니다. 이 라이브러리는 프로그래머가 Clifford + $T $ 분해를 직접 표현할 필요가 없으며, 단일 highbit unitaries를 Clifford 및 $T $ 게이트로 컴파일하기 위한 매우 효율적인 메서드가 필요 하지 않기 때문에 훨씬 더 쉽습니다. 자세한 내용은 [여기](xref:microsoft.quantum.more-information) 를 참조 하세요.

가능 하면, prelude에서 정의 된 작업은 `Controlled` 대상 컴퓨터에서 적절 한 분해를 수행 하는 등의 작업을 수행 하 여 variant를 적용할 수 있습니다.

Prelude의이 부분에 정의 된 대부분의 함수 및 작업은 @"microsoft.quantum.intrinsic" 네임 스페이스에 있습니다. 즉, 대부분의 Q# 소스 파일에는 `open Microsoft.Quantum.Intrinsic;` 초기 네임 스페이스 선언 바로 뒤에 지시문이 있습니다.
<xref:Microsoft.Quantum.Core>네임 스페이스는 자동으로 열리므로와 같은 함수를 <xref:Microsoft.Quantum.Core.Length> 문 없이 사용할 수 있습니다 `open` .

### <a name="common-single-qubit-unitary-operations"></a>공통 Single-Qubit 단일 작업 ###

또한 prelude는 여러 일반적인 [단일 기능 비트 작업](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)을 정의 합니다.
이러한 모든 작업은 및 함수를 모두 허용 `Controlled` `Adjoint` 합니다.

#### <a name="pauli-operators"></a>Pauli 연산자 ####

<xref:Microsoft.Quantum.Intrinsic.X>작업은 Pauli $X $ 연산자를 구현 합니다.
이를 `NOT` 게이트 라고도 합니다.
시그니처가 `(Qubit => Unit is Adj + Ctl)` 있습니다.
단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 0 & 1 \\ \\ % fixme: 현재 quadwhack hack를 사용 합니다.
1 & 0 \end{bmatrix} \end{ation}

<xref:Microsoft.Quantum.Intrinsic.Y>작업은 Pauli $Y $ 연산자를 구현 합니다.
시그니처가 `(Qubit => Unit is Adj + Ctl)` 있습니다.
단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 0 &-i \\ \\ % fixme: 현재 quadwhack hack를 사용 합니다.
i & 0 \end{bmatrix} \end{ation}

<xref:Microsoft.Quantum.Intrinsic.Z>작업은 Pauli $Z $ 연산자를 구현 합니다.
시그니처가 `(Qubit => Unit is Adj + Ctl)` 있습니다.
단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 1 & 0 \\ \\ % fixme: 현재 quadwhack hack를 사용 합니다.
0 &-1 \end{bmatrix} \end{ation}

아래에는 [Bloch 구에](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) 매핑되는 이러한 변환이 표시 됩니다 (각 사례의 회전 축은 빨간색으로 강조 표시 됨).

![Bloch 구에 매핑된 pauli 작업](~/media/prelude_pauliBloch.png)

동일한 이상 비트에 동일한 Pauli 게이트를 두 번 적용 하면 작업을 취소 합니다. 이제 Bloch 구에 대 한 2π (360 °)의 전체 회전을 수행 했으므로 시작 지점에서 다시 도착 하 게 됩니다. 그러면 다음 id가 제공 됩니다.

$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \boldone $ $

Bloch 구에 visualised 수 있습니다.

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a>기타 Single-Qubit Cliffords ####

<xref:Microsoft.Quantum.Intrinsic.H>작업은 Hadamard gate를 구현 합니다.
이는 \ket {0} = \ket{+} \mathrel{: =} (\ket {0} + \ket {1} )/\sqrt {2} $ 및 $H \ket{+} = \ket $와 $H 같은 대상의 pauli $X $ 및 $Z $ 축을 교환 {0} 합니다.
이 파일은 시그니처를 포함 하 `(Qubit => Unit is Adj + Ctl)` 고 다음과 같은 단일 기능에 해당 합니다.

\begin{equation} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ % fixme: 현재 quadwhack hack를 사용 합니다.
1 &-1 \end{bmatrix} \end{ation}

Hadamard gate는 $ \ket {0} $ 및 $ \ket $ 상태의 superposition을 만드는 데 사용할 수 있으므로 특히 중요 합니다 {1} . Bloch 구의 표현은 $ \pi $ radians ($ 180 ^ \pi $)에 의해 x 축 주위에 $ \ket{\psi} $를 회전 하 고, $ \ pi/2 $ radians ($ 90 ^ \pi $)로 y 축을 중심으로 (시계 방향) 회전으로 생각 하는 것이 가장 쉽습니다.

![Bloch 구에 매핑된 Hadamard 작업](~/media/prelude_hadamardBloch.png)

<xref:Microsoft.Quantum.Intrinsic.S>작업은 단계 게이트 $S $을 구현 합니다.
이는 Pauli $Z $ operation의 매트릭스 제곱근입니다.
즉, $S ^ 2 = Z $입니다.
이 파일은 시그니처를 포함 하 `(Qubit => Unit is Adj + Ctl)` 고 다음과 같은 단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 1 & 0 \\ \\ % fixme: 현재 quadwhack hack를 사용 합니다.
0 & i \end{bmatrix} \end{ation}

#### <a name="rotations"></a>교대 ####

위의 Pauli 및 Clifford 작업 외에도 prelude는 회전을 표현 하는 Q# 다양 한 방법을 제공 합니다.
[단일 기능 비트 작업](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)에 설명 된 대로,이를 회전 하는 기능은 퀀텀 알고리즘에 매우 중요 합니다.

먼저 $H $ 및 $T $ 게이트를 사용 하 여 단일 기능 비트 작업을 표현할 수 있습니다. 여기서 $H $은 Hadamard 연산이 고, 여기서 \begin{equation} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ % fixme: 현재는 쿼드 백 whack hack를 사용 합니다.
0 & e ^ {i \pi/4} \end{bmatrix} \end{cation}이는 <xref:Microsoft.Quantum.Intrinsic.S> $T ^ 2 = S $와 같은 작업의 제곱근입니다.
$T $ gate는 작업에 의해 구현 되 <xref:Microsoft.Quantum.Intrinsic.T> 고, 시그니처가 있으므로 `(Qubit => Unit is Adj + Ctl)` 단일 기능 비트에서 단일 작업 임을 나타냅니다.

이 원칙은 임의의 단일 기능 비트 작업을 설명 하는 데 충분 하지만, 서로 다른 대상 컴퓨터는 prelude에 대 한 회전을 보다 효율적으로 표현할 수 있습니다 .이에 따라 이러한 회전을 convienently 하는 다양 한 방법이 포함 되어 있습니다.
이러한 작업의 가장 기본적인 기능은 <xref:Microsoft.Quantum.Intrinsic.R> 지정 된 Pauli 축을 중심으로 회전을 구현 하는 작업입니다. \begin{equation} R (\시그마, \>) \mathrel{: =} \exp (-i \begin{equation}/2), \begin{equation} 여기서 $ \\bn\a\a는 Pauli, $ \\a$는 각도 이며 여기서 $ \exp $는 행렬 지 수를 나타냅니다.
이 파일에는 시그니처가 있습니다 `((Pauli, Double, Qubit) => Unit is Adj + Ctl)` . 여기서 입력의 처음 두 부분은 기존 인수인 $ \sigma $ 및 $ \\? $를 나타내며 단일 연산자 $R (\sigma, \\as) $를 지정 하는 데 필요 합니다.
$ \Sigma $ 및 $ \\s$를 부분적으로 적용 하 여 해당 형식이 단일의 단일 비트를 포함 하는 작업을 가져올 수 있습니다.
예를 들어,에 `R(PauliZ, PI() / 4, _)` 는 형식이 `(Qubit => Unit is Adj + Ctl)` 있습니다.

> [!NOTE]
> <xref:Microsoft.Quantum.Intrinsic.R>작업은 입력 각도를 2로 나누고-1을 곱합니다.
> $Z $ 회전의 경우 $ \ket {0} $ eigenstate가 $-\\a/$2에 의해 회전 되 고 $ \ket $ eigenstate가 $ \\a/$2에 의해 회전 되며 $ \ket $ eigenstate가 $ {1} {1} \aa$에서 $ \ket $ eigenstate를 기준으로 회전 합니다 {0} .
>
> 특히, 및은 관련이 없는 `T` `R(PauliZ, PI() / 8, _)` [전역 단계](xref:microsoft.quantum.glossary#global-phase)에 의해서만 차이가 있습니다.
> 따라서 $ \frac{\pi} $-gate 라고도 하는 $T $를 사용할 수 있습니다 {8} .
>
> 또한를 중심으로 회전 해도 `PauliI` $ \a/$2의 글로벌 단계를 적용 합니다. 이러한 단계는 [개념 문서](xref:microsoft.quantum.concepts.qubit)에서 주장해와는 관련이 없지만 제어 되는 회전과 관련이 있습니다 `PauliI` .

퀀텀 알고리즘 내에서 dyadic로 회전을 표현 하는 것이 유용한 경우가 종종 있습니다. 예를 들어 \mathbb{Z} $ 및 $n \bin \mathbb{N} $의 일부 $k \phi = \phi k/2 ^ n $입니다.
<xref:Microsoft.Quantum.Intrinsic.RFrac>작업은이 규칙을 사용 하 여 지정 된 Pauli 축을 중심으로 회전을 구현 합니다.
<xref:Microsoft.Quantum.Intrinsic.R>회전 각도는 형식의 두 입력으로 지정 되 `Int` 고 dyadic 분수로 해석 된다는 점에서와는 다릅니다.
따라서에 `RFrac` 는 시그니처가 `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)` 있습니다.
단일 기능을 구현 합니다. 여기서 $ \b\시그마 $는 첫 번째 인수에 해당 하는 Pauli 매트릭스이 고 $k $은 두 번째 인수 이며 $n $는 세 번째 인수입니다.
`RFrac(_,k,n,_)` 는와 동일 합니다. `R(_,-πk/2^n,_)` 각도는 분수의 *음수* 입니다.

<xref:Microsoft.Quantum.Intrinsic.Rx>작업은 Pauli $X $ axis를 중심으로 회전을 구현 합니다.
시그니처가 `((Double, Qubit) => Unit is Adj + Ctl)` 있습니다.
`Rx(_, _)`이 `R(PauliX, _, _)`와 같은 경우

<xref:Microsoft.Quantum.Intrinsic.Ry>작업은 Pauli $Y $ axis를 중심으로 회전을 구현 합니다.
시그니처가 `((Double, Qubit) => Unit is Adj + Ctl)` 있습니다.
`Ry(_, _)`이 `R(PauliY,_ , _)`와 같은 경우

<xref:Microsoft.Quantum.Intrinsic.Rz>작업은 Pauli $Z $ axis를 중심으로 회전을 구현 합니다.
시그니처가 `((Double, Qubit) => Unit is Adj + Ctl)` 있습니다.
`Rz(_, _)`이 `R(PauliZ, _, _)`와 같은 경우

작업은 $ <xref:Microsoft.Quantum.Intrinsic.R1> \ket $ 주위의 지정 된 양만큼 회전을 구현 합니다 {1} . $-$1 eigenstate $Z $입니다.
시그니처가 `((Double, Qubit) => Unit is Adj + Ctl)` 있습니다.
`R1(phi,_)` 는 뒤에와 동일 합니다 `R(PauliZ,phi,_)` `R(PauliI,-phi,_)` .

<xref:Microsoft.Quantum.Intrinsic.R1Frac>연산은 Z = 1 eigenstate를 기준으로 지정 된 양만큼 소수 순환을 구현 합니다.
시그니처가 `((Int,Int, Qubit) => Unit is Adj + Ctl)` 있습니다.
`R1Frac(k,n,_)` 는 뒤에와 동일 합니다 `RFrac(PauliZ,-k.n+1,_)` `RFrac(PauliI,k,n+1,_)` .

Bloch 구에 매핑된이 인스턴스에서 Pauli $Z $ 축에 대 한 회전 작업의 예는 다음과 같습니다.

![회전 작업이 Bloch 구에 매핑됨](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a>다중 기능 비트 작업 ####

Prelude는 위의 단일 비트 작업 외에도 여러 가지 다중 기능 비트 작업을 정의 합니다.

먼저 작업에서 <xref:Microsoft.Quantum.Intrinsic.CNOT> 표준 제어- `NOT` 게이트를 수행 합니다. \begin{equation} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 0 & 0 & 0 & \\ \\ 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}.
\end{equation} `((Qubit, Qubit) => Unit is Adj + Ctl)` 는 $ \operatorname{CNOT} $가 두 개의 개별의 unitarily에서 작동 한다는 것을 나타내는 시그니처를 포함 합니다.
`CNOT(q1, q2)`이 `(Controlled X)([q1], q2)`와 같은 경우
함수는 `Controlled` 레지스터에 대 한 제어를 허용 하므로 배열 리터럴을 사용 하 여 `[q1]` 한 개의 컨트롤을 원하는 것으로 표시 합니다.

<xref:Microsoft.Quantum.Intrinsic.CCNOT>연산은 이중 제어 되지 않는 게이트 (Toffoli gate 라고도 함)를 수행 합니다.
시그니처가 `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)` 있습니다.
`CCNOT(q1, q2, q3)`이 `(Controlled X)([q1, q2], q3)`와 같은 경우

<xref:Microsoft.Quantum.Intrinsic.SWAP>작업은 두 가지 비트의 퀀텀 상태를 바꿉니다.
즉, 단일 행렬을 구현 합니다. \begin{\operatorname{SWAP} ation} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 0 & 1 & 0 & 0 0 & 0 & 0 & \\ \\ \\ \\ 1 \end{bmatrix}.
\end{equation}에 시그니처가 `((Qubit, Qubit) => Unit is Adj + Ctl)` 있습니다.
`SWAP(q1,q2)` 는와 동일 `CNOT(q1, q2)` `CNOT(q2, q1)` `CNOT(q1, q2)` 합니다.

> [!NOTE]
> 스왑 게이트는 형식의 변수 요소를 다시 정렬 하는 것 *과는 다릅니다* `Qubit[]` .
> 를 적용 `SWAP(q1, q2)` 하면 및에서 참조 하는 원하는 비트의 상태가 변경 `q1` 되 고 `q2` ,는 `let swappedRegister = [q2, q1];` 해당 하는 비트를 참조 하는 방법에만 영향을 줍니다.
> 또한을 `(Controlled SWAP)([q0], (q1, q2))` 사용 하면 `SWAP` 요소를 다시 정렬 하 여 나타낼 수 없는 세 번째 조건 화 된의 상태를 확인할 수 있습니다.
> Fredkin gate 라고도 하는 제어 교환 게이트는 모든 클래식 계산을 포함 하기에 충분히 강력한 기능입니다.

마지막으로 prelude는 여러 가지 지 수 연산자를 나타내는 두 가지 작업을 제공 합니다.
<xref:Microsoft.Quantum.Intrinsic.Exp>작업은 다기능 비트 단일 \begin{equation} \operatorname{Exp} (\vec{\sigma}, \aas) \mathrel{: =} \a\left (, \\텐서): =} \a\left (i sigma_n sigma_1 sigma_0 \sa\o\o\o\ost\ost\o\o\o\o\o\o\o\o\o\o\end{station} 여기서 $ \vec{\sigma} = (\ sigma_0, \ sigma_1, \점선이, \ sigma_n) $는 단일 stbit Pauli 연산자의 시퀀스이 고, 여기서 $ \\a$는 각도입니다.
`Exp`회전은 `Pauli` 시그니처를 포함 하는 요소의 배열로 $ \vec{\sigma} $를 나타냅니다 `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` .

<xref:Microsoft.Quantum.Intrinsic.ExpFrac>작업은 위에서 설명한 dyadic 분수 표기법을 사용 하 여 동일한 회전을 수행 합니다.
시그니처가 `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)` 있습니다.

> [!WARNING]
> Pauli 연산자의 텐서 제품 지 수은 Pauli 연산자 지 수의 텐서 제품과 동일 하지 않습니다.
> 즉, $e ^ {i (Z \otimes Z)는 \phi} \ne e ^ {i Z \phi} \otimes e ^ {i Z \phi} $입니다.

### <a name="measurements"></a>측정 ###

측정 시 측정 되는 연산자의 + 1 eigenvalue는 결과에 해당 하 `Zero` 고-1 eigenvalue는 결과에 해당 `One` 합니다.

> [!NOTE]
> 이 규칙은 이상한 것 처럼 보일 수 있지만 두 가지 매우 좋은 이점이 있습니다.
> 첫째, $ \ket $ 결과를 관찰 하는 {0} 것은 값으로 표시 되는 `Result` `Zero` 반면 $ \ket {1} $는에 해당 `One` 합니다.
> 둘째, $ \lambda = (-1) ^ r $ $r 결과에 해당 하는 eigenvalue $ \lambda $를 작성할 수 있습니다.

측정 연산은 또는 함수를 지원 하지 않습니다 `Adjoint` `Controlled` .

<xref:Microsoft.Quantum.Intrinsic.Measure>작업은 지정 된 Pauli 연산자 제품에서 하나 이상의에 대 한 공동 측정을 수행 합니다.
Pauli 배열 및 원하는 비트 배열의 길이가 다른 경우 작업이 실패 합니다.
`Measure` 에 시그니처가 `((Pauli[], Qubit[]) => Result)` 있습니다.

조인트 측정은 각 비트를 개별적으로 측정 하는 것과는 다릅니다.
예를 들어 $ \ket {11} = \ket {1} \otimes \Ket {1} = X\otimes X \ket $ 상태를 고려해 보세요 {00} .
$Z _0 $ 및 $Z _1 $를 개별적으로 측정 하 여 _0 = $1 및 $r _1 = $1 $r 결과를 가져옵니다.
$Z _0 Z_1 $를 측정 하는 중입니다. _ {\textrm{joint}} = $0의 단일 $r 결과가 pairity $ \ket $의 {11} 가 긍정적 임을 나타냅니다.
다른 방법으로 $ (-1) ^ {r_0 + r_1} = (-1) ^ r_ {\textrm{joint}}) $입니다.
이 측정을 통해 패리티 *를 알아보는 것* 이기 때문에 superposition에서 긍정 패리티의 2 2-\ket {00} $ 및 $ \ket $와 같은 모든 퀀텀 정보를 {11} 유지 합니다.
오류 수정에 대해 설명 하는 것 처럼이 속성은 나중에 필요 합니다.

편의를 위해 prelude는 두 가지 다른 작업을 제공 하 여이를 측정 합니다.
첫째, 단일 수준 측정을 수행 하는 것이 매우 일반적 이기 때문에 prelude은이 경우의 약어를 정의 합니다.
<xref:Microsoft.Quantum.Intrinsic.M>작업은 단일의 비트에 대해 Pauli $Z $ 연산자를 측정 하 고 서명을 갖습니다 `(Qubit => Result)` .
`M(q)`은 `Measure([PauliZ], [q])`와 동등합니다.

는 <xref:Microsoft.Quantum.Measurement.MultiM> 각 고 비트에 대해 얻은 값의 *배열을* 반환 하 여 각 값의 배열에 대해 *별도로* pauli $Z $ 연산자를 측정 합니다 `Result` .
일부 경우에는이를 최적화할 수 있습니다. 서명 ()이 있습니다 `Qubit[] => Result[])` .
`MultiM(qs)` 는 다음과 같습니다.

```qsharp
mutable rs = new Result[Length(qs)];
for (index in 0..Length(qs)-1)
{
    set rs[index] = M(qs[index]);
}
return rs;
```

## <a name="extension-functions-and-operations"></a>확장 함수 및 작업 ##

또한 prelude는 코드 내에서 사용 하기 위해 .NET 수준에서 다양 한 수학적 및 형식 변환 함수 집합을 정의 합니다 Q# .
예를 들어, <xref:Microsoft.Quantum.Math> 네임 스페이스는 및와 같은 유용한 작업을 정의 합니다 <xref:Microsoft.Quantum.Math.Sin> <xref:Microsoft.Quantum.Math.Log> .
퀀텀 개발 키트에서 제공 하는 구현에서는 기존 .NET 기본 클래스 라이브러리를 사용 하므로 퀀텀 프로그램 및 해당 클래식 드라이버 사이에 추가 통신 왕복이 포함 될 수 있습니다.
이는 로컬 시뮬레이터에 대 한 문제를 제공 하지 않지만 원격 시뮬레이터 또는 실제 하드웨어를 대상 컴퓨터로 사용 하는 경우 성능 문제가 발생할 수 있습니다.
즉, 개별 대상 컴퓨터는 특정 시스템에 보다 효율적인 버전으로 이러한 작업을 재정의 하 여 이러한 성능 영향을 완화할 수 있습니다.

### <a name="math"></a>수식 ###

<xref:Microsoft.Quantum.Math>네임 스페이스는 .net 기본 클래스 라이브러리의 [ `System.Math` 클래스](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1&preserve-view=true)에서 많은 유용한 함수를 제공 합니다.
이러한 함수는 다른 함수와 동일한 방식으로 사용할 수 있습니다 Q# .

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

해당 인수의 형식에 따라 .NET 정적 메서드가 오버 로드 된 경우 해당 함수에는 해당 Q# 입력의 형식을 나타내는 접미사로 주석이 추가 됩니다.

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a>비트 연산 ###

마지막으로, <xref:Microsoft.Quantum.Bitwise> 네임 스페이스는 비트 연산자를 통해 정수 조작을 위한 몇 가지 유용한 함수를 제공 합니다.
예를 들어은 <xref:Microsoft.Quantum.Bitwise.Parity> 정수의 비트 패리티를 다른 정수로 반환 합니다.
