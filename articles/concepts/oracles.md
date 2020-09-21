---
제목: 퀀텀 oracles 설명: 다른 알고리즘에 대 한 입력으로 사용 되는 퀀텀 oracles 및 블랙 박스 작업을 사용 하 고 정의 하는 방법을 알아봅니다.
작성자: cgranade uid: oracles. author: chgranad: 07/11/2018 밀리초. 토픽: 문서 번호:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---
# <a name="quantum-oracles"></a>퀀텀 Oracles

Oracle $ O는 $ 다른 알고리즘에 대 한 입력으로 사용 되는 "블랙 박스" 작업입니다.
이러한 작업은 일반적으로 $ f: \\ { 0, 1 \\ } ^ n 0, 1 ^ m을 사용 하 여 정의 되며 \to \\ { \\ } $ $ n $ 비트 이진 입력을 사용 하 고 $ m $ 비트 이진 출력을 생성 합니다.
이렇게 하려면 특정 이진 입력 $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1)를 고려 } $ 합니다.
$ \ket { \vec { } } = \ket { X_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 } } $ 을 x로 지정할 수 있습니다.

처음에 $ $ 는 $ o \ket { x f (x)로 o를 정의 하려고 시도할 수 } = \ket { } $ 있지만 여기에는 몇 가지 문제가 있습니다.
첫째, $ f에 $ 는 다른 크기의 입력 및 출력 (n m)이 있을 수 있습니다 $ \ne $ .이 경우 O를 적용 하면 $ $ 레지스터의 원하는 비트 수가 변경 됩니다.
둘째, n m 인 경우에도 $ = $ 함수는 반전할 수 없습니다. $ x (x) = f (y) $ 가 일부 $ x y 이면 \ne $ $ o x o y는 o ^ \ket o { } = \ket { } $ $ \dagger \ket { } \ne \dagger \ket { } $ x o ^ o y입니다.
즉, adjoint 작업 $ O ^를 생성할 수 \dagger $ 없고 oracles에 대해 adjoint가 정의 되어 있어야 합니다.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>계산 기준 상태에 영향을 미치는 oracle 정의
$ $ 답변을 유지 하기 위해 두 번째 레지스터를 도입 하 여 이러한 문제를 모두 처리할 수 있습니다.
그런 다음 모든 계산 기반 상태에 oracle의 효과를 정의 합니다. 모든 $ x \in \\ { 0, 1 \\ } ^ n $ 및 $ y \in \\ { 0, 1 \\ } ^ m $ ,

$$
\begin{align}
    O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .
\end{align}
$$

이제 $ = 생성을 통해 o o ^ ^ ^ \dagger $ 이 (가) 이전 문제를 모두 해결 했습니다.

> [!TIP]
>$O = o ^ ^ ^ 2를 확인 하려면 { \dagger } $ $ = \boldone $ $ 모든 a에 대해 \oplus b \oplus a와 b a를 모두 포함 하 여 o ^ 2를 확인 = $ $ 합니다. b \in \: :: 비 loc ({)::: 0, 1 \: :: no loc (})::: $
>결과적으로 $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ 입니다.

중요 한 점은 각 계산 기준 상태에 대해 oracle을 정의 $ \ket { } \ket { } $ 하는 것은 $ $ 다른 모든 상태에 대해 O가 작동 하는 방식도 정의 합니다.
이는 $ $ 모든 퀀텀 작업과 같이 O가 작동 하는 상태에서 선형 이라는 점에서 즉시 수행 됩니다.
예를 들어 $ h \ket { 0 } = \ket { + } $ 및 $ h \ket { 1 } = \ket { - } $ 로 정의 되는 Hadamard 작업을 고려 합니다.
H가 어떻게 작동 하는지 알고 $ 싶으면 $ h를 $ \ket { + } $ $ $ 선형으로 사용할 수 있습니다.

$$
\begin{align}
H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\
           &= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .
\end{align}
$$

Oracle O를 정의 하는 경우에는 $ $ $ \ket { \psi } $ n + m의 모든 상태를 $ $ 로 작성할 수 있습니다.

$$
\begin{align}
\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}
\end{align}
$$

where $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C는 } $ 상태의 계수를 나타냅니다 $ \ket { \psi } $ . 그러므로

$$
\begin{align}
O \ket { \psi } & = o \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) o \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\
             &= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .
\end{align}
$$

## <a name="phase-oracles"></a>Oracles 단계
또는 O에 대 한 $ $ $ $ 입력에 따라 _단계_ 를 적용 하 여 f를 oracle O로 $ $ 인코딩할 수 있습니다. 예를 들어, $ $$$
\begin{align}
    O \ket { x } = (-1) ^ { f (x) } \ket { x } .
\end{align}
$$
Oracle 단계가 초기에 계산 기준 상태 x로 작동 하는 경우 $ \ket { } $ 이 단계는 글로벌 단계 이므로 관찰 가능 하지 않습니다.
그러나 이러한 oracle은 superposition에 적용 되거나 제어 된 작업으로 적용 되는 경우 매우 강력한 리소스가 될 수 있습니다.
예를 들어 $ $ 단일 기능 비트 함수 f의 oracle O_f 단계를 살펴보겠습니다 $ $ .
다음 $$
\begin{align}
    O_f \ket{+}
        &=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\
        &=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } z ^ { f (0)-f (1) } \ket { + } .
\end{align}
$$

보다 일반적으로는 oracles의 두 뷰를 넓혔습니다 하 여 단일 비트만이 아닌 실수를 반환 하는 클래식 함수를 나타낼 수 있습니다.

Oracle을 구현 하는 가장 좋은 방법은 지정 된 알고리즘 내에서이 oracle을 사용 하는 방법에 따라 크게 달라 집니다.
예를 들어 [Deutsch-Jozsa 알고리즘](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) 은 첫 번째 방법으로 구현 된 oracle을 사용 하는 반면 [Grover의 알고리즘](https://en.wikipedia.org/wiki/Grover's_algorithm) 은 두 번째 방법으로 구현 된 oracle에 의존 합니다.


자세한 내용은 [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465)에 설명 되어 있습니다.
