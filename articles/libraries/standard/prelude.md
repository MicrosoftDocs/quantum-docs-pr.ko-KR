---
title: 'Q # 표준 라이브러리-prelude | Microsoft Docs'
description: 'Q # 표준 라이브러리-prelude'
author: QuantumWriter
uid: microsoft.quantum.libraries.standard.prelude
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: dddb3d4a5ebcdca16da41a5ae5520d98ea900a7f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73183236"
---
# <a name="the-prelude"></a>Prelude #

Q # 컴파일러 및 퀀텀 개발 키트에 포함 된 대상 컴퓨터는 Q #에서 퀀텀 프로그램을 작성할 때 사용할 수 있는 내장 함수 및 작업 집합을 제공 합니다.

## <a name="intrinsic-operations-and-functions"></a>내장 작업 및 함수 ##

표준 라이브러리에 정의 된 기본 작업은 다음과 같은 몇 가지 범주 중 하나에 해당 합니다.

- <xref:microsoft.quantum.core> 네임 스페이스에 수집 된 필수 클래식 함수
- [Clifford 및 $T $ 게이트](xref:microsoft.quantum.concepts.qubit)로 구성 된 unitaries를 나타내는 작업입니다.
- 다양 한 연산자에 대 한 회전을 나타내는 작업입니다.
- 측정을 구현 하는 작업입니다.

Clifford + $T $ gate 집합은 퀀텀 컴퓨팅을 위한 [유니버설](xref:microsoft.quantum.concepts.multiple-qubits) 이므로 negligibly 작은 오류 내에서 임의 퀀텀 알고리즘을 구현 하는 데에는 충분 합니다.
Q #은 회전도 제공 하 여 프로그래머는 단일의 단일 기능 및 CNOT gate 라이브러리 내에서 작업을 수행할 수 있습니다. 이 라이브러리는 프로그래머가 Clifford + $T $ 분해를 직접 표현할 필요가 없으며, 단일 highbit unitaries를 Clifford 및 $T $ 게이트로 컴파일하기 위한 매우 효율적인 메서드가 필요 하지 않기 때문에 훨씬 더 쉽습니다. ( [여기](xref:microsoft.quantum.more-information) 참조 추가 정보).

가능 하면, prelude에서 정의 된 작업을 수행 하 여 대상 컴퓨터에서 적절 한 분해를 수행 하는 등의 작업을 수행할 `Controlled` 수 있습니다.

Prelude의이 부분에 정의 된 대부분의 함수 및 작업은 @"microsoft.quantum.intrinsic" 네임 스페이스에 있습니다. 즉, 대부분의 Q # 소스 파일은 초기 네임 스페이스 선언 바로 뒤에 `open Microsoft.Quantum.Intrinsic;` 지시문을 포함 합니다.
<xref:microsoft.quantum.core> 네임 스페이스는 자동으로 열리므로 <xref:microsoft.quantum.core.length>와 같은 함수를 `open` 문 없이 사용할 수 있습니다.

### <a name="common-single-qubit-unitary-operations"></a>일반적인 단일 기능 비트 단일 작업 ###

또한 prelude는 여러 일반적인 [단일 기능 비트 작업](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)을 정의 합니다.
이러한 모든 작업은 `Controlled` 및 `Adjoint` 함수를 모두 허용 합니다.

#### <a name="pauli-operators"></a>Pauli 연산자 ####

<xref:microsoft.quantum.intrinsic.x> 작업은 Pauli $X $ 연산자를 구현 합니다.
이를 `NOT` 게이트 라고도 합니다.
`(Qubit => Unit is Adj + Ctl)`시그니처가 있습니다.
단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 0 & 1 \\\\% FIXME: 현재는 quadwhack hack를 사용 합니다.
1 & 0 \end{bmatrix} \end{ation}

<xref:microsoft.quantum.intrinsic.y> 작업은 Pauli $Y $ 연산자를 구현 합니다.
`(Qubit => Unit is Adj + Ctl)`시그니처가 있습니다.
단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 0 &-i \\\\% FIXME: 현재는 quadwhack hack를 사용 합니다.
i & 0 \end{bmatrix} \end{ation}

<xref:microsoft.quantum.intrinsic.z> 작업은 Pauli $Z $ 연산자를 구현 합니다.
`(Qubit => Unit is Adj + Ctl)`시그니처가 있습니다.
단일 기능에 해당 합니다.

\begin{equation} \begin{bmatrix} 1 & 0 \\\\% FIXME: 현재는 quadwhack hack를 사용 합니다.
0 &-1 \end{bmatrix} \end{ation}

아래에는 [Bloch 구에](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) 매핑되는 이러한 변환이 표시 됩니다 (각 사례의 회전 축은 빨간색으로 강조 표시 됨).

![Bloch 구에 매핑된 pauli 작업](~/media/prelude_pauliBloch.png)

동일한 이상 비트에 동일한 Pauli 게이트를 두 번 적용 하면 작업을 취소 합니다. 이제 Bloch 구에 대 한 2π (360 °)의 전체 회전을 수행 했으므로 시작 지점에서 다시 도착 하 게 됩니다. 그러면 다음 id가 제공 됩니다.

$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \boldone $ $

Bloch 구에 visualised 수 있습니다.

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a>다른 단일 수준 비트 Cliffords ####

<xref:microsoft.quantum.intrinsic.h> 작업은 Hadamard gate를 구현 합니다.
이는 \ket{0} = \ket{+} \mathrel{: =} (\ket{0} + \ket{1})/\sqrt{2}$ 및 $H \ket{+} = \ket{0}$와 $H 같은 대상의 Pauli $X $ 및 $Z $ 축을 교환 합니다.
이 파일에는 `(Qubit => Unit is Adj + Ctl)`시그니처와 해당 하는 단일 고 비트에 해당 합니다.

\begin{equation} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\% FIXME: 현재 quadwhack 해킹을 사용 합니다.
1 &-1 \end{bmatrix} \end{ation}

Hadamard gate는 $ \ket{0}$ 및 $ \ket{1}$ states의 superposition를 만드는 데 사용할 수 있으므로 특히 중요 합니다. Bloch 구의 표현은 $ \pi $ radians ($ 180 ^ \pi $)에 의해 x 축 주위에 $ \ket{\psi} $를 회전 하 고, $ \ pi/2 $ radians ($ 90 ^ \pi $)로 y 축을 중심으로 (시계 방향) 회전으로 생각 하는 것이 가장 쉽습니다.

![Bloch 구에 매핑된 Hadamard 작업](~/media/prelude_hadamardBloch.png)

<xref:microsoft.quantum.intrinsic.s> 작업은 단계 게이트 $S $을 구현 합니다.
이는 Pauli $Z $ operation의 매트릭스 제곱근입니다.
즉, $S ^ 2 = Z $입니다.
이 파일에는 `(Qubit => Unit is Adj + Ctl)`시그니처와 해당 하는 단일 고 비트에 해당 합니다.

\begin{equation} \begin{bmatrix} 1 & 0 \\\\% FIXME: 현재는 quadwhack hack를 사용 합니다.
0 & i \end{bmatrix} \end{ation}

#### <a name="rotations"></a>회전 ####

위의 Pauli 및 Clifford 작업 외에도 Q # prelude는 회전을 표현 하는 다양 한 방법을 제공 합니다.
[단일 기능 비트 작업](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)에 설명 된 대로,이를 회전 하는 기능은 퀀텀 알고리즘에 매우 중요 합니다.

먼저 $H $ 및 $T $ 게이트를 사용 하 여 단일 기능 비트 작업을 표현할 수 있습니다. 여기서 $H $은 Hadamard 연산이 고, 여기서 \begin{equation} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\\\% FIXME: 현재는 쿼드 back을 사용 합니다. whack hack.
0 & e ^ {i \pi/4} \end{bmatrix} \end{cation}이는 $T ^ 2 = S $와 같이 <xref:microsoft.quantum.intrinsic.s> 작업의 제곱근입니다.
$T $ gate는 <xref:microsoft.quantum.intrinsic.t> 작업에 의해 구현 되 고, `(Qubit => Unit is Adj + Ctl)`시그니처를 포함 하 여 단일의 단일 작업 임을 나타냅니다.

이 경우 임의의 단일 기능 비트 작업을 설명 하는 데에는 충분 하지만, prelude에는 다양 한 방법이 포함 되어 있기 때문에 다른 대상 컴퓨터에서 Pauli 연산자에 대 한 회전을 보다 효율적으로 표현할 수 있습니다. 이러한 회전을 표현 합니다.
이러한 작업의 가장 기본적인 <xref:microsoft.quantum.intrinsic.r> 작업입니다. 지정 된 Pauli 축을 중심으로 하는 회전을 구현 하는 것입니다. \begin{equation} R (\시그마, \\as) \mathrel{: =} \exp (-i \\a\aa\시그마/2), \begin{equation} 여기서 $ \b\시그마 $은 \exp $는 행렬 지 수를 나타냅니다.
이 클래스에는 서명 `((Pauli, Double, Qubit) => Unit is Adj + Ctl)`있습니다. 여기서 입력의 처음 두 부분은 n\시그마 $ 및 $ \\\\\\\\\\\\a>를 $R 지정 하는 데 필요한 기존 인수인 $ \sigma $ 및 $ \\? $를 나타냅니다.
$ \Sigma $ 및 $ \\s$를 부분적으로 적용 하 여 해당 형식이 단일의 단일 비트를 포함 하는 작업을 가져올 수 있습니다.
예를 들어 `R(PauliZ, PI() / 4, _)`에는 `(Qubit => Unit is Adj + Ctl)`형식이 있습니다.

> [!NOTE]
> <xref:microsoft.quantum.intrinsic.r> 연산은 입력 각도를 2로 나누고-1을 곱합니다.
> $Z $ 회전의 경우 $ \ket{0}$ eigenstate가 $-\\a/$2에 의해 회전 되 고 $ \ket{1}$ eigenstate가 $ \\a/$2에 의해 회전 되며 $ \ket{0}$ eigenstate에 상대적인 $ \\an$에서 $ \ket{1}$ eigenstate가 회전 됩니다.
>
> 특히 `T`와 `R(PauliZ, PI() / 8, _)`는 관련이 없는 [전역 단계](xref:microsoft.quantum.glossary#global-phase)에 의해서만 차이가 있습니다.
> 따라서 $ \frac{\pi}{8}$-gate 라고도 하는 $T $를 사용할 수도 있습니다.
>
> 또한 `PauliI`을 순환 하는 것은 $ \\a/$2의 글로벌 단계를 적용 합니다. 이러한 단계는 [개념 문서](xref:microsoft.quantum.concepts.qubit)에서 주장해와는 관련이 없지만 제어 되는 `PauliI` 회전과 관련이 있습니다.

퀀텀 알고리즘 내에서 dyadic로 회전을 표현 하는 것이 유용한 경우가 종종 있습니다. 예를 들어 \mathbb{Z} $ 및 $n \bin \mathbb{N} $의 일부 $k \phi = \phi k/2 ^ n $입니다.
<xref:microsoft.quantum.intrinsic.rfrac> 연산은이 규칙을 사용 하 여 지정 된 Pauli 축을 중심으로 회전을 구현 합니다.
회전 각도가 dyadic 분수로 해석 된 `Int`형식의 두 입력으로 지정 된다는 점에서 <xref:microsoft.quantum.intrinsic.r>와 다릅니다.
따라서 `RFrac`에는 `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
단일 기능을 구현 합니다. 여기서 $ \b\시그마 $는 첫 번째 인수에 해당 하는 Pauli 매트릭스이 고 $k $은 두 번째 인수 이며 $n $는 세 번째 인수입니다.
`RFrac(_,k,n,_)`은 `R(_,-πk/2^n,_)`와 동일 합니다. 각도는 분수의 *음수* 입니다.

<xref:microsoft.quantum.intrinsic.rx> 연산은 Pauli $X $ axis를 중심으로 회전을 구현 합니다.
`((Double, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
`Rx(_, _)`은 `R(PauliX, _, _)`와 동일 합니다.

<xref:microsoft.quantum.intrinsic.ry> 연산은 Pauli $Y $ axis를 중심으로 회전을 구현 합니다.
`((Double, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
`Ry(_, _)`은 `R(PauliY,_ , _)`와 동일 합니다.

<xref:microsoft.quantum.intrinsic.rz> 연산은 Pauli $Z $ axis를 중심으로 회전을 구현 합니다.
`((Double, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
`Rz(_, _)`은 `R(PauliZ, _, _)`와 동일 합니다.

<xref:microsoft.quantum.intrinsic.r1> 연산은 $ \ket{1}$ ($Z $의 $-$1 eigenstate)를 기준으로 지정 된 양만큼 회전을 구현 합니다.
`((Double, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
`R1(phi,_)`은 `R(PauliZ,phi,_)`와 동일 하며 `R(PauliI,-phi,_)`.

<xref:microsoft.quantum.intrinsic.r1frac> 연산은 Z = 1 eigenstate를 기준으로 지정 된 양만큼 소수 순환을 구현 합니다.
`((Int,Int, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
`R1Frac(k,n,_)`은 `RFrac(PauliZ,-k.n+1,_)`와 동일 하며 `RFrac(PauliI,k,n+1,_)`.

Bloch 구에 매핑된이 인스턴스에서 Pauli $Z $ 축에 대 한 회전 작업의 예는 다음과 같습니다.

![회전 작업이 Bloch 구에 매핑됨](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a>다중 기능 비트 작업 ####

Prelude는 위의 단일 비트 작업 외에도 여러 가지 다중 기능 비트 작업을 정의 합니다.

먼저 <xref:microsoft.quantum.intrinsic.cnot> 작업에서 표준 제어-`NOT` 게이트를 수행 합니다. \begin{equation} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}.
\end{equation} \operatorname{CNOT} $ unitarily이 두 개의 개별 비트에서 작동 함을 나타내는 시그니처 `((Qubit, Qubit) => Unit is Adj + Ctl)`있습니다.
`CNOT(q1, q2)`은 `(Controlled X)([q1], q2)`와 동일 합니다.
`Controlled` 함수를 사용 하 여 레지스터를 제어할 수 있으므로 `[q1]` 배열 리터럴을 사용 하 여 한 개의 컨트롤을 사용 한다고 표시 합니다.

<xref:microsoft.quantum.intrinsic.ccnot> 작업은 Toffoli 게이트가 라고도 하는 이중 제어 되지 않는 게이트를 수행 합니다.
`((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)`시그니처가 있습니다.
`CCNOT(q1, q2, q3)`은 `(Controlled X)([q1, q2], q3)`와 동일 합니다.

<xref:microsoft.quantum.intrinsic.swap> 작업은 두 가지 비트의 퀀텀 상태를 바꿉니다.
즉, 단일 행렬을 구현 합니다. \begin{equation} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}.
\end{equation} `((Qubit, Qubit) => Unit is Adj + Ctl)`시그니처를 포함 합니다.
`SWAP(q1,q2)`은 `CNOT(q1, q2)`와 같으며 `CNOT(q2, q1)` 다음에 `CNOT(q1, q2)`합니다.

> [!NOTE]
> 스왑 게이트는 `Qubit[]`형식의 변수 요소를 다시 정렬 하는 것 *과는 다릅니다* .
> `SWAP(q1, q2)`를 적용 하면 `q1` 및 `q2`에서 참조 하는 원하는 비트의 상태가 변경 됩니다. 반면 `let swappedRegister = [q2, q1];`은 이러한 것이 해당 하는 비트를 참조 하는 방법에만 영향을 줍니다.
> 또한 `(Controlled SWAP)([q0], (q1, q2))`를 사용 하면 요소를 다시 정렬 하 여 나타낼 수 없는 세 번째 조건 화 된의 상태를 `SWAP` 수 있습니다.
> Fredkin gate 라고도 하는 제어 교환 게이트는 모든 클래식 계산을 포함 하기에 충분히 강력한 기능입니다.

마지막으로 prelude는 여러 가지 지 수 연산자를 나타내는 두 가지 작업을 제공 합니다.
<xref:microsoft.quantum.intrinsic.exp> 작업은 여러 \operatorname{Exp} (\vec{\sigma}, \a\mathrel{): =} \a\left (i \\a\sigma_0 \otime \sigma_1 \os)로 표현 된 Pauli 행렬의 텐서 제품을 기반으로 하는 회전을 수행 합니다. cdots \otimes \sigma_n \right), \end{-ation} (여기서 $ \vec{\sigma} = (\sigma_0, \sigma_1, \도트, \sigma_n) $은 단일 = (,, \
`Exp` 회전은 $ \vec{\sigma} $를 `Pauli` 요소의 배열로 나타내며이를 통해 시그니처 `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)`을 포함 합니다.

<xref:microsoft.quantum.intrinsic.expfrac> 작업은 위에서 설명한 dyadic 분수 표기법을 사용 하 여 동일한 회전을 수행 합니다.
`((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)`시그니처가 있습니다.

> [!WARNING]
> Pauli 연산자의 텐서 제품 지 수은 Pauli 연산자 지 수의 텐서 제품과 동일 하지 않습니다.
> 즉, $e ^ {i (Z \otimes Z)는 \phi} \ne e ^ {i Z \phi} \otimes e ^ {i Z \phi} $입니다.

### <a name="measurements"></a>측정값 ###

측정할 때 측정 되는 연산자의 + 1 eigenvalue는 `Zero` 결과에 해당 하 고-1 eigenvalue는 `One` 결과에 해당 합니다.

> [!NOTE]
> 이 규칙은 이상한 것 처럼 보일 수 있지만 두 가지 매우 좋은 이점이 있습니다.
> 첫째, $ \ket{0}$ 결과를 관찰 하는 것은 `Result` 값 `Zero`으로 표시 되 고 $ \ket{1}$은 `One`에 해당 합니다.
> 둘째, $ \lambda = (-1) ^ r $ $r 결과에 해당 하는 eigenvalue $ \lambda $를 작성할 수 있습니다.

측정 연산은 `Adjoint`와 `Controlled` 함수를 모두 지원 하지 않습니다.

<xref:microsoft.quantum.intrinsic.measure> 작업은 지정 된 Pauli 연산자 제품에서 하나 이상의에 대 한 공동 측정을 수행 합니다.
Pauli 배열 및 원하는 비트 배열의 길이가 다른 경우 작업이 실패 합니다.
`Measure`에 `((Pauli[], Qubit[]) => Result)`시그니처가 있습니다.

조인트 측정은 각 비트를 개별적으로 측정 하는 것과는 다릅니다.
예를 들어 $ \ket{11} = \ket{1} \otimes \ket{1} = X\otimes X \ket{00}$ 상태를 살펴보겠습니다.
$Z _0 $ 및 $Z _1 $를 개별적으로 측정 하 여 _0 = $1 및 $r _1 = $1 $r 결과를 가져옵니다.
$Z _0 Z_1 $을 측정 $r _ {\textrm{joint}} = $0의 단일 결과는 $ \ket{11}$의 pairity가 양수인 것을 나타냅니다.
다른 방법으로 $ (-1) ^ {r_0 + r_1} = (-1) ^ r_ {\textrm{joint}}) $를 입력 합니다.
이 측정을 통해 패리티 *를 알아보는 것* 이기 때문에 superposition에서 긍정 패리티 2 2-\ket{00}$ 및 $ \ket{11}$와 같은에 표시 되는 퀀텀 정보는 그대로 유지 됩니다.
오류 수정에 대해 설명 하는 것 처럼이 속성은 나중에 필요 합니다.

편의를 위해 prelude는 두 가지 다른 작업을 제공 하 여이를 측정 합니다.
첫째, 단일 수준 측정을 수행 하는 것이 매우 일반적 이기 때문에 prelude은이 경우의 약어를 정의 합니다.
<xref:microsoft.quantum.intrinsic.m> 작업은 단일의 비트에서 Pauli $Z $ 연산자를 측정 하 고 시그니처 `(Qubit => Result)`를 포함 합니다.
`M(q)`은 `Measure([PauliZ], [q])`와 동등합니다.

<xref:microsoft.quantum.measurement.multim>는 각 고 비트에 대해 얻은 `Result` 값의 *배열을* 반환 하 여 각 값의 배열에 대해 Pauli $Z $ 연산자를 *별도로* 측정 합니다.
일부 경우에는이를 최적화할 수 있습니다. 서명 (`Qubit[] => Result[])`)이 있습니다.
`MultiM(qs)`는 다음과 같습니다.

```qsharp
mutable rs = new Result[Length(qs)];
for (index in 0..Length(qs)-1)
{
    set rs[index] = M(qs[index]);
}
return rs;
```

## <a name="extension-functions-and-operations"></a>확장 함수 및 작업 ##

또한 prelude는 Q # 코드 내에서 사용 하기 위해 .NET 수준에서 다양 한 수학적 및 형식 변환 함수 집합을 정의 합니다.
예를 들어 <xref:microsoft.quantum.extensions.math> 네임 스페이스는 <xref:microsoft.quantum.extensions.math.sin> 및 <xref:microsoft.quantum.extensions.math.log>와 같은 유용한 작업을 정의 합니다.
퀀텀 개발 키트에서 제공 하는 구현에서는 기존 .NET 기본 클래스 라이브러리를 사용 하므로 퀀텀 프로그램 및 해당 클래식 드라이버 사이에 추가 통신 왕복이 포함 될 수 있습니다.
이는 로컬 시뮬레이터에 대 한 문제를 제공 하지 않지만 원격 시뮬레이터 또는 실제 하드웨어를 대상 컴퓨터로 사용 하는 경우 성능 문제가 발생할 수 있습니다.
즉, 개별 대상 컴퓨터는 특정 시스템에 보다 효율적인 버전으로 이러한 작업을 재정의 하 여 이러한 성능 영향을 완화할 수 있습니다.

### <a name="math"></a>산 ###

<xref:microsoft.quantum.extensions.math> 네임 스페이스는 .NET 기본 클래스 라이브러리의 [`System.Math` 클래스](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1)에서 많은 유용한 함수를 제공 합니다.
이러한 함수는 다른 Q # 함수와 동일한 방식으로 사용할 수 있습니다.

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

.NET 정적 메서드가 인수의 형식에 따라 오버 로드 된 경우 해당 하는 Q # 함수는 해당 입력의 형식을 나타내는 접미사로 주석을 답니다.

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a>비트 연산 ###

마지막으로, <xref:microsoft.quantum.extensions.bitwise> 네임 스페이스는 비트 연산자를 통해 정수 조작을 위한 몇 가지 유용한 함수를 제공 합니다.
예를 들어 <xref:microsoft.quantum.extensions.bitwise.parity>은 정수의 비트 패리티를 다른 정수로 반환 합니다.
