---
제목: 여러 기능에 대 한 설명: 둘 이상의 이상에서 작업을 수행 하는 방법을 알아봅니다.
만든이: QuantumWriter uid:: nawiebe@microsoft.com 12/11/2017: 밀리초. 토픽: 문서 번호-다음이 아닙니다.
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

# <a name="multiple-qubits"></a>여러 비트

단일 기능 비트 게이트는 지정 된 시간에 둘 이상의 상태에 있을 수 있는 기능과 같은 몇 가지 카운터 직관적인 기능을 보유 하 고 있지만, 퀀텀 컴퓨터에 있는 모든 것이 단일 기능 비트 게이트가 었으 면 계산기로만 고전 고성능 컴퓨터을 dwarfed 계산 능력을 갖춘 장치를 갖게 됩니다.
퀀텀 계산의 진정한 힘은 성능 수가 증가 하는 것 처럼 분명 하 게 드러납니다.
이는 일부 경우에는 퀀텀 상태 벡터의 벡터 공간 차원이 지 수의 수를 사용 하 여 급격 하 게 증가 하기 때문입니다.
즉, 단일 기능을 모델링 하는 것이 일반적으로 수 있지만, 50-슈퍼 컴퓨터 퀀텀 계산을 시뮬레이션 하는 것은 기존의 제한을 거의 푸시하는 것을 의미 합니다.
하나 이상의 추가 비트를 기준으로 계산 크기를 늘리면 상태를 저장 하는 데 필요한 메모리가 *두 배가* 되며 약 *두* 배가 계산 시간이 됩니다.
계산 능력의 급속 한 배가 되는 이유는 상대적으로 적은 수의 초과할를 가진 퀀텀 컴퓨터가 일부 계산 작업에 대해 미래의 슈퍼 컴퓨터 가장 강력한 기능을 사용할 수 있는 것입니다.

퀀텀 상태 벡터에 대해 지 수 증가가 있는 이유는 무엇 인가요?  이 섹션의 목표는 단일가 나 비트 상태에서 다 수의 비트 상태를 빌드하는 데 사용 되는 규칙을 검토 하는 것이 고, 전 세계의 뛰어난 비트 퀀텀 컴퓨터를 형성 하기 위해 게이트 집합에 포함 해야 하는 게이트 작업에 대해 설명 하는 것입니다.
이러한 도구는 일반적으로 코드에 사용 되는 게이트 집합을 이해 하는 데 필요 Q# 하며, 되거나 얽 히 또는 간섭 같은 퀀텀 효과가 기존 컴퓨팅 보다 더 강력한 성능을 intuition 수 있는 이유에 대 한 정보를 얻을 수 있습니다.

## <a name="representing-two-qubits"></a>두 개의 비트를 나타내는
1 ~ 2의 비트 상태 간의 주요 차이점은 두 번째 비트 상태는 2 차원이 아닌 4 차원 이라는 것입니다.
이는 두 번째 비트 상태에 대 한 계산 기준이 한 수준 비트 상태의 텐서 products로 구성 되기 때문입니다.  예를 들어\begin{align}
00 \equiv \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} & = \begin{bmatrix} 1 \\\\ 0 0 0 \\\\ \\\\ \end{bmatrix} , \qquad 01 \equiv \begin{bmatrix} 1 \\\\ 0 0 \end{bmatrix} \otimes \begin{bmatrix} \\\\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \\\\ \\\\ \end{bmatrix} 0 0,\\\\
10 \equiv \begin{bmatrix} 0 \\\\ 1 1 0 0 0 0 \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} & = \begin{bmatrix} \\\\ \\\\ 1 \\\\ \end{bmatrix} , \qquad 11 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ \\\\ \\\\ \end{bmatrix} 0 0 1.
\end{align}

$이 구성을 사용 하 여 보다 일반적으로 n 비트의 퀀텀 상태를 $ 차원 2 ^ n의 단위 벡터로 표시 한다는 것을 쉽게 확인할 수 $ $ 있습니다.  벡터입니다.

$$
\begin{bmatrix}\alpha _ { 00 } 01 \\\\ 10 \alpha   _ { } \\\\ \alpha _ { 11 } \\\\ \alpha   _ { }  \end{bmatrix}
$$

$ | \alpha _ { 00 } | ^ 2 | + \alpha _ { 01 } | ^ 2 + | \alpha _ { 10 } | ^ 2 | + \alpha _ { 11 } | ^ 2 = 1 $ 인 경우 두 가지 비트의 퀀텀 상태를 나타냅니다. 단일 기능을 사용 하는 것과 마찬가지로, 여러 기능에 대 한 퀀텀 상태 벡터는 시스템의 동작을 설명 하는 데 필요한 모든 정보를 포함 합니다.

상태에서 두 개의 별도 비트가 지정 된 경우, 상태에서 두 $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ 번째 고 비트는 해당 하는 $ \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $ 두 번째 비트 상태입니다.    

$$
\begin{bmatrix} \alpha \\\\  \beta \end{bmatrix} \otimes \begin{bmatrix} \gamma \\\\  \delta \end{bmatrix} 
=\begin{bmatrix} \alpha \begin{bmatrix} \gamma \\\\  \delta \end{bmatrix} \\\\ \beta \begin{bmatrix}\gamma \\\\  \delta \end{bmatrix} \end{bmatrix}
= \begin{bmatrix} \alpha\gamma \\\\  \alpha\delta \\\\  \beta\gamma \\\\  \beta\delta \end{bmatrix}, $$

여기서 작업을 $ \otimes $ 벡터의 텐서 product (또는 Kronecker product) 라고 합니다. 항상 두 개의 단일 수준 비트 상태를 텐서 제품을 사용 하 여 두 개의 단일 비트 상태를 텐서 곱으로 작성할 수 있는 것은 아니지만 두 개의 단일 비트 양자 상태를 작성할 수 있습니다.
예를 들어 상태는 없으며 $ \psi = \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ $ \phi = \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $ 해당 텐서 제품이 상태입니다.     

$$\psi\otimes\phi = \begin{bmatrix} 1/ \sqrt { 2 } \\\\ 0 \\\\ 0 \\\\ 1/ \sqrt { 2 } \end{bmatrix} .$$ 

단일 수준 비트 상태의 텐서 곱으로 작성할 수 없는 두 번째 비트 상태를 "entangled 상태" 라고 합니다. 두 개의이 두 비트는 [*entangled*](https://en.wikipedia.org/wiki/Quantum_entanglement)이라고 합니다.  느슨하게 말하면 퀀텀 상태를 단일 텐서의 곱으로 간주할 수 없기 때문에 상태가 보유 한 정보는 개별적 비트 중 하나로 제한 되지 않습니다.  대신이 정보는 두 상태 간의 상관 관계에서 로컬로 저장 되지 않습니다.  이러한 정보가 아닌 이러한 정보는 기존 컴퓨팅에 대 한 퀀텀 컴퓨팅의 주요 기능 중 하나 이며, [퀀텀 teleportation](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/teleportation) 및 [퀀텀 오류 수정](xref:microsoft.quantum.libraries.error-correction)사항을 비롯 한 다양 한 퀀텀 프로토콜에 필수적입니다.

## <a name="measuring-two-qubit-states"></a>두 수준 비트 상태 측정 ##
두 번째 비트 상태 측정은 단일 수준 비트 측정과 매우 유사 합니다. 상태 측정

$$
    \begin{bmatrix}
        \alpha_ { 00 } 01 \\\\ \alpha _ { }\\\\ 
        \alpha_ { 10 } 11 \\\\ \alpha _ {}
    \end{bmatrix}
$$

확률은 00 $ $ $ | \alpha _ { } | ^ 2 $ , $ 01 $ 은 확률 01 ^ 2, 10은 확률 10 ^ 2, 10은 확률 11 ^ 2 인 00을 산출 합니다. $ | \alpha _ { } | $ $ $ $ | \alpha _ { } | $ $ $ $ | \alpha _ { } | $ 변수 $ \alpha _ { 00 } , \alpha _ { 01 } , \alpha _ { 10 } $ 및 $ 11은이 연결을 명확 하 게 하기 위해 의도적으로 이름이 지정 되었습니다 \alpha _ { } $ . 측정 후 결과가 00 인 경우 두 번째 $ $ 비트 시스템의 퀀텀 상태는 축소 되어 이제

$$
    00\equiv
    \begin{bmatrix}
        1(sp1)\\\\ 
        0 \\\\ 
        0 \\\\ 
        0 \end{bmatrix} .
$$

또한 두 번째 비트율의 퀀텀 상태를 한 번만 측정할 수 있습니다. 원하는 비트 중 하나만 측정 하는 경우 전체 상태가 계산 기준 상태로 축소 되지 않고 하나의 하위 시스템 으로만 축소 되므로 측정의 영향은 약간 다릅니다.  즉, 이러한 경우에는 하나의 요소를 측정 하는 경우에만 하위 시스템 중 하나만 축소할 수 있습니다.  

이를 확인 하려면 $ $ 처음에 "0" 상태로 설정 된 두 개의 Hadamard transform H를 적용 하 여 형성 된 다음 상태의 첫 번째 비트를 측정 합니다.$$
H ^ { \otimes 2 } \left ( \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \right ) = \frac { 1 2 1 1 1 1 } { } \begin{bmatrix} & & & \\\\ & -1 1 & & -1 \\\\ 1 & & - & \\\\ & & & \end{bmatrix} \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} = \frac { } { } \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \mapsto \begin{cases} \text { } = & \frac { } { \sqrt { } } \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \\\\ \text { } = & \frac { } { \sqrt { } } \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \\\\ \end{cases} 1-1 1-1-1-1-1-1-1-1-1-1-1 1 1 1 0 0 0 1 2 1 1 1  
$$
두 결과 모두 50% 발생 확률이 있습니다.  50% 확률에 대 한 결과는 초기 퀀텀 상태 벡터가 고정 임을 intuited 수 있습니다 $ $ $ $ . 첫 번째 비트의 0을 1로 바꾸면 됩니다.

첫 번째 또는 두 번째 비트를 측정 하는 수학적 규칙은 간단 합니다.  E_k 수 있는 $ 경우 $ $ k ^ { \rm의 계산 기준 벡터를 사용 하 여 } $ $ $ $ $ $ $ 해당 값에 대해 값 1을 사용 하 $ $ 는 모든 e_k 집합을 사용할 수 있도록 합니다.  예를 들어 첫 번째 비트를 측정 하는 데 관심이 있는 경우 $ 는 $ $ e_1 \equiv 10 $ 및 $ e_3 \equiv 11 $ 로 구성 됩니다.  마찬가지로 두 번째는 $ $ $ e_2 \equiv 01 $ 및 $ e_3 \equiv 11 $ 로 구성 됩니다.  그런 다음 선택한의 비트를 1로 측정할 확률은 $ $ 상태 벡터에 대해입니다.$\psi$

$$
P ( \text { 결과 } = 1) = \sum _ { e_k \text { 집합 } S } \psi ^ \dagger e_k e_k ^에 \dagger \psi 있습니다.
$$

> [!NOTE]
>이 문서에서는 작은 endian 형식을 사용 하 여 계산 기준에 레이블을 지정 합니다. Little endian 형식에서 최하위 비트가 먼저 나옵니다. 예를 들어, 작은 endian 형식의 숫자 4는 비트 001의 문자열로 표시 됩니다.

각의 비트 측정은 $ 0 또는 1만 생성할 수 있으므로 $ 0으로 $ $ 측정 되는 $ 확률 $ 은 단순히 $ 1-P ( \text { 결과 } = 1)입니다 $ .  이것은 측정의 확률에 대 한 수식을 명시적으로 제공 하는 이유입니다 $ $ .

이러한 측정이 상태에 주는 동작은 수학적으로로 표현 될 수 있습니다.

$$
\psi\mapsto \frac{\sum _ { e_k \text { 집합 } S } e_k e_k ^ \dagger \psi } { \sqrt { P ( \text { 결과 } = 1) } } .
$$

주의 대상 독자는 측정 확률이 0 인 경우 발생 하는 상황에 대해 걱정할 수 있습니다.  이 경우 결과 상태는 기술적으로 정의 되지 않지만 확률은 0 이기 때문에 이러한 eventualities에 대해 걱정 하지 않아도 됩니다.


$ \psi $ 위에서 제공 된 균일 한 상태 벡터로 사용 되며, 첫 번째 비트를 측정 하는 데 관심이 있는 경우 

$$
P ( \text { 첫 번째 비트 1의 측정 } = ) = ( \psi ^ \dagger e_1) (e_1 ^ \dagger \psi ) + ( \psi ^ \dagger e_3) (e_3 ^ \dagger \psi ) = | e_1 ^ \dagger \psi | ^ 2 + | e_3 ^ \dagger \psi | ^ 2.
$$

이는 결과를 측정 하는 데 예상 되는 두 확률의 합계입니다 $ $ . 10과 11은 $ $ 모두 측정할 비트입니다.
이 예에서는 다음으로 평가 됩니다.

$$
\frac{1 } { 4 } \left | \begin{bmatrix} 0 & 0 1 0 1 1 1 1 & & \end{bmatrix} \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \right | ^ 2 + 1 4 0 0 0 0 1 1 1 1 \frac { } { } \left | \begin{bmatrix} & & & \end{bmatrix} \begin{bmatrix} \\\\ \\\\ \\\\ 1 \end{bmatrix} \right | ^ 2 = \frac { 1 } { 2 } .
$$

intuition가 확률을 나타내는 것과 정확히 일치 하는 것입니다.  마찬가지로 상태를로 작성할 수 있습니다.

$$
\frac{\frac{e_1 } { 2 } + \frac { e_3 } { 2 } } { \sqrt { \frac { 1 } { 2 } } } = \frac { 1 } { \sqrt { 2 } } \begin{bmatrix} 0 \\\\ 0 \\\\ 1 \\\\ 1\end{bmatrix}
$$

intuition에 따라 다시 합니다.

## <a name="two-qubit-operations"></a>두 가지 비트 작업
단일 비트의 경우 처럼 모든 단일 변환은 원하는 비트의 유효한 작업입니다. 일반적으로 n의 단일 변환은 $ 크기 2 $ ^ n $ $ 2 ^ n의 행렬 u로 $ \times $ $ $ , $ U ^ { -1 } = u ^ \dagger $ 와 같이 크기 2 ^ n의 벡터에서 작동 합니다.
예를 들어 CNOT (제어 되지 않음) 게이트는 일반적으로 사용 되는 두 번째 비트 게이트 이며 다음과 같은 단일 행렬로 표시 됩니다.

$$
\operatorname{CNOT } = \begin{bmatrix} 1 \ 0 \ 0 \ 0 \\\\ 0 \ 1 \ 0 \ 0 \\\\ 0 \ 0 \ 0 \ 1 \\\\ 0 \ 0 \ 1 \ 0\end{bmatrix}
$$

또한 두 가지 기능에 단일 고 비트 게이트를 적용 하 여 두 가지 비트 게이트를 형성할 수 있습니다. 예를 들어 게이트를 적용 하는 경우 

$$
\begin{bmatrix}
a \ b \\\\ c \ d\end{bmatrix}
$$

and

$$\begin{bmatrix}
e \ f \\\\ g \ h\end{bmatrix}
$$

첫 번째 및 두 번째 비트의 경우 각각 텐서 제품에서 제공 하는 두 번째 비트를 적용 하는 것과 같습니다.$$\begin{bmatrix}
a \ b \\\\ c \ d\end{bmatrix}
\otimes 
\begin{bmatrix}
e \ f \\\\ g \ h\end{bmatrix}=
    \begin{bmatrix}
    ns\\\\\
    ag \ ah \ bg \ bh\\\\
    ce \ cf \ de \ df\\\\
    cg \ ch \ dg \ dh \end{bmatrix} .$$
따라서 몇 가지 알려진 단일 고 비트 게이트의 텐서 제품을 활용 하 여 두 가지 비트 게이트를 형성할 수 있습니다. 2 배 비트 게이트의 몇 가지 예에는 $ h \otimes h $ , $ x \otimes \boldone $ 및 $ x \otimes Z가 $ 있습니다.

두 개의 단일 기능 비트 게이트가 텐서 제품을 가져와 두 번째 비트 게이트를 정의 하지만 반대의 경우는 그렇지 않습니다. 두 가지 모든 비트 게이트는 단일 고 비트 게이트의 텐서 곱으로 작성할 수 없습니다.  이러한 게이트를 *entangling* 게이트 라고 합니다. Entangling gate의 한 가지 예로 CNOT gate가 있습니다.

제어 되지 않는 게이트 intuition 뒤에 있는 경우 임의 게이트로 일반화 될 수 있습니다.  일반적으로 제어 되는 게이트는 특정 비트 비트가 1 인 경우를 제외 하 고 id 역할을 하는 게이트 (작업 없음)입니다 $ $ .  이 경우 x $ $ $ \Lambda \_ (U)를 사용 하 여 $ 레이블이 지정 된 x에 대 한 제어 된 단일를 나타냅니다.  예를 들어 $ \Lambda _0 (u) e \_ { 1 } \otimes { \psi } = e 1 \_ { } \otimes U { \psi } $ 및 $ \Lambda \_ 0 (u) e \_ { 0 } \otimes { \psi } = e \_ { 0 } \otimes { \psi } $ $ \_ 입니다. 여기서 e 0 $ 과 $ e \_ 1 $ 은 값 $ 0 $ 및 1에 해당 하는 단일 값에 대 한 계산 기준 벡터입니다 $ $ .  예를 들어 다음과 같은 제어-Z 게이트를 고려 하 여 $ $ 이를 표현할 수 있습니다.$$
\Lambda\_0 (Z) 1 0 0 0 0 0 0 0 0 0 = \begin{bmatrix} & 1 0 0 0 & & \\\\ & & & \\\\ & & & \\\\ & & & -1 \end{bmatrix} = ( \boldone \otimes h) \operatorname { cnot } ( \boldone \otimes h).
$$

효율적인 방식으로 제어 되는 unitaries을 빌드하는 것은 중요 한 문제입니다.  이를 구현 하는 가장 간단한 방법은 제어 되는 기본 게이트 버전의 데이터베이스를 형성 하 고 원래 단일 작업의 모든 기본 게이트를 제어 된 해당 작업으로 바꾸는 것입니다.  이는 종종 매우 불필요 한 정보를 사용 하 여 동일한 영향을 얻기 위해 몇 가지 게이트를 제어 된 버전으로 바꾸는 것입니다.  이러한 이유로, 최적화 된 손으로 조정 된 버전이 알려진 경우 사용자가 제어 하는 naive 메서드를 수행 하거나 제어 되는 버전의 사용자를 정의할 수 있도록 하는 기능을 프레임 워크에 제공 합니다.

클래식 정보를 사용 하 여 게이트를 제어할 수도 있습니다.  예를 들어 일반적으로 제어 되는 게이트는 일반적인 비 게이트 이지만, 기존 비트가 $ 퀀텀 비트가 아닌 1 인 경우에만 적용 됩니다 $ .  이러한 점에서 일반적으로 제어 되는 게이트는 코드의 한 분기에만 게이트가 적용 되는 퀀텀 코드의 if 문으로 간주할 수 있습니다.


단일 수준 비트의 경우 처럼 $ \times $ 이 집합에서 임의 전체 자릿수로 4 개의 단일 행렬의 게이트를 대략적으로 비교할 수 있는 경우 2 ~ 5 비트 게이트 집합이 유니버설입니다.
범용 게이트 집합의 한 가지 예는 Hadamard 게이트, T 게이트 및 CNOT 게이트입니다. 이러한 게이트의 제품을 활용 하 여 두 개의 모든 단일 행렬을 대략적으로 살펴볼 수 있습니다.

## <a name="many-qubit-systems"></a>수많은 비트 시스템
두 번째 수준에서 살펴본 것과 동일한 패턴을 따라 작은 시스템에서 다양 한 수준의 퀀텀 상태를 작성 합니다.  이러한 상태는 더 작은 상태의 텐서 제품을 형성 하 여 구축 됩니다.  예를 들어, $ 퀀텀 컴퓨터에서 1011001 비트 문자열을 인코딩합니다 $ .  이를 다음과 같이 인코딩할 수 있습니다.

$$
1011001 \equiv \begin{bmatrix} 0 1 1 0 0 1 0 1 1 0 1 0 0 \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ 1 \end{bmatrix} .
$$

퀀텀 게이트는 정확히 동일한 방식으로 작동 합니다.  예를 들어, $ $ 첫 번째 비트에 X 게이트를 적용 한 다음 두 번째와 세 번째 비트 간에 cnot을 수행 하려는 경우이 변환을 표현할 수 있습니다.

\begin{align}
&(X \otimes \operatorname { cnot } _ { 12 } \otimes \boldone \otimes \boldone \otimes \boldone \otimes \boldone ) \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} \\\\ 0 1\end{bmatrix}\\\\
&\qquad\qquad\equiv0011001.\end{align}

많은 수의 시스템에서 퀀텀 컴퓨터의 임시 메모리 역할을 하는 원하는 비트를 할당 하 고 할당을 취소 해야 하는 경우가 많습니다.  이러한 비트를 ancilla 라고 합니다.  기본적으로이 경우에는 $ 할당 될 때 e_0로 초기화 되는 것으로 가정 합니다 $ .  할당 취소 전에 e_0 하기 위해 다시 반환 되는 것으로 가정 $ $ 합니다.  이 가정은 ancilla가 할당 취소 될 때 다른의 비트 레지스터를 사용 하 여 점점 증가 하 게 되 면 할당 취소 프로세스에서 ancilla을 손상 시키기 때문에 중요 합니다.  이러한 이유로 항상 이러한 비트를 출시 되기 전의 초기 상태로 되돌리는 것으로 가정 합니다.

마지막으로, 새 게이트를 게이트 집합에 추가 하 여 두 개의 엔터프라이즈급 비트 퀀텀 컴퓨터에 대 한 범용 퀀텀 컴퓨팅을 구현 하는 경우에도 새 게이트를 여러 기능에서 도입 해야 하는 것은 아닙니다.  $ $ $ $ 일반적인 단일 변환은 두 개의 다양 한 비트 회전으로 분리 될 수 있기 때문에 게이트 H, T 및 cnot은 다양 한 세계에서 범용 게이트 집합을 형성 하지 않습니다.  그런 다음 두 번째 비트 사례에 대해 개발한 이론을 활용 하 고 다양 한 기능을 제공 하는 경우 여기에서 다시 사용할 수 있습니다.

지금까지 사용 하 던 선형 대 수 표기법은 매우 다양 한 비트 상태를 설명 하는 데 사용 될 수 있지만 상태 크기를 늘리면 점점 복잡해 집니다.  예를 들어 길이 7 비트 문자열에 대 한 결과 벡터는 $ 128 $ 차원입니다 .이를 통해 앞에서 설명한 표기법을 사용 하 여이를 표현할 수 있습니다.  이러한 이유로, 다음은 이러한 높은 차원 벡터를 간결 하 게 설명할 수 있도록 하는 퀀텀 컴퓨팅에 일반적인 표기법을 제시 하는 것입니다.
