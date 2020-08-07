---
제목: Pauli 측정 설명: 단일 및 다중 값 비트를 사용 하는 방법에 대해 알아봅니다.
작성자: QuantumWriter uid: microsoft..:. nawiebe@microsoft.com 날짜: 12/11/2017 밀리초. 토픽: 문서 번호-loc:
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

# <a name="pauli-measurements"></a>Pauli 측정

위의 논의에서 계산 기준 측정에 중점을 두었습니다.
사실, 표기법 밑수 관점에서 계산 기준 측정 측면에서 편리 하 게 사용할 수 있는 퀀텀 컴퓨팅에서 발생 하는 다른 일반적인 측정이 있습니다.
로 작업할 때 Q# 가장 일반적인 측정 종류는 다른 기본에 대 한 측정치를 포함 하는 계산 기준 측정을 일반화 하 고 다양 한 비트 간의 패리티를 포함 하는 *Pauli 측정이*될 가능성이 높습니다.
이 경우 일반적으로 $ x, Y, z $ 또는 $ z \otimes z, x \otimes x, x \otimes Y $ 등의 연산자를 통해 pauli 연산자를 측정 하는 방법을 설명 하는 것이 일반적입니다.

> [!TIP]
>에서 Q# 다기능 비트 Pauli 연산자는 일반적으로 형식의 배열로 표시 됩니다 `Pauli[]` .
>예를 들어 $ X \otimes Z Y를 \otimes 나타내려면 $ 배열을 사용할 수 있습니다 `[PauliX, PauliZ, PauliY]` .

Pauli 연산자를 기준으로 측정값을 논의 하는 것은 퀀텀 오류 수정의 하위 필드에서 특히 일반적입니다.
에서는 Q# 비슷한 규칙을 따르고 있습니다. 이제 이러한 대체 측정값에 대해 설명 합니다.

Pauli를 측정 하는 방법에 대 한 세부 정보를 살펴보기 하기 전에 퀀텀 컴퓨터 내의 단일 요소를 퀀텀 상태로 측정 하는 것을 고려 하는 것이 유용 합니다.
N bit 퀀텀 상태를 보유 하 고 있다고 가정 $ $ 합니다. 그런 다음, $ $ 해당 상태가 될 수 있는 2 ^ n의 절반에 해당 하는 규칙을 즉시 측정 한 것입니다.
즉, 측정은 퀀텀 상태를 두 개의 반 공간 중 하나로 프로젝션 합니다.
이 intuition을 반영 하기 위해 측정 하는 방식을 일반화할 수 있습니다.

이러한 하위 공간을 간결 하 게 식별 하기 위해 설명을 위한 언어가 필요 합니다.
두 개의 하위 공간을 설명 하는 한 가지 방법은 규칙에 따라 \pm 1을 사용 하 여 두 개의 고유한 eigenvalues만 있는 행렬을 통해 지정 하는 것입니다 $ $ .
이러한 방식으로 하위 공간을 설명 하는 간단한 예제를 보려면 Z를 고려 하십시오 $ $ .

$$
\begin{align}
  Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} .
\end{align}
$$

Pauli-z 행렬의 대각선 요소를 읽으면 $ $ $ z $ 에 $ \ket { } $ $ \ket { } $ 해당 고유 값이 $ \pm 1 인 $ 두 개의 고유 벡터 0과 1이 있음을 알 수 있습니다.
따라서, (상태 0에 해당 하는 경우)를 측정 하 고 가져오는 경우 `Zero` $ \ket { } $ 이의 상태는 $ $ Z 연산자의 + 1 eigenstate 임을 알 수 $ $ 있습니다.
마찬가지로,를 얻을 경우 `One` 이의 상태는 $ z의-1 eigenstate 임을 알 수 $ $ $ 있습니다. 이 프로세스는 "측정값을 측정 합니다." 라고 하는 Pauli 측정 언어에서 $ $ 계산 기준 측정을 수행 하는 것과 완전히 동일 합니다.

$ \times $ Z의 단일 변환 인 2 2 행렬 $ $ 도이 조건을 충족 합니다.
즉, u $ = ^ \dagger Z u를 사용할 수도 있습니다 $ $ . 여기서 u $ 는 다른 단일 행렬을 사용 하 여 \pm 1 고유 벡터에서 측정의 두 가지 결과를 정의 하는 행렬을 제공 $ $ 합니다.
Pauli 측정의 표기법은 $ X, Y, Z $ 측정을 동일한 측정으로 식별 하 여이 단일 동등성을 참조 합니다.
이러한 측정은 편의를 위해 아래에 제공 됩니다.


|Pauli 측정 | 단일 변환|
|-------------------|------------------------|
|$ $ Z |               $\boldone$             |
|$ $ X | $H               $                    |
|$ $ Y | $HS ^               {\dagger}$         |

즉,이 언어를 사용 하는 경우 "measure $ Y $ "는 HS ^를 적용 한 다음 계산 단위로 측정 하는 것과 같습니다. $ \dagger $ 여기서 [`S`](xref:microsoft.quantum.intrinsic.s) 는 "단계 게이트" 라고도 하는 내장 퀀텀 연산이 며 단일 행렬에 의해 시뮬레이션 될 수 있습니다.

$$
\begin{align}
    S =\begin{bmatrix}
        1 & 0 \\\\ 0 & i \end{bmatrix} .
\end{align}
$$

다음 작업을 수행 하는 경우 $ 에도 HS ^ \dagger $ 를 퀀텀 상태 벡터에 적용 한 다음 $ Z를 측정 $ `Measure([PauliY], [q])` 하는 것과 같습니다.

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

그런 다음 계산 기준으로 다시 변환 하 여 올바른 상태를 확인할 수 있습니다 $ .이는 SH를 $ 퀀텀 상태 벡터에 적용 하는 것입니다. 위의 코드 조각에서 계산 기준으로 다시 변환 하는 것은 블록을 사용 하 여 자동으로 처리 됩니다 `within … apply` .

에서는 결과 Q# ---, 상태---와 상호 작용 하 여 추출 된 클래식 정보를 값 j 0으로 지정 합니다 .이 정보는 결과가 지정 된 `Result` $ \in \\ { \texttt { } \texttt { } \\ } $ $ (-1) ^ j # 연산자의 (-1) ^ j $ eigenspace에 있음을 나타냅니다.


## <a name="multiple-qubit-measurements"></a>여러 비트 측정

다음에서 볼 수 있듯이 다중 기능 비트 Pauli 연산자의 측정은 유사 하 게 정의 됩니다.

$$
Z \otimes z 1 0 0 0 0 = \begin{bmatrix} & & -1 0 0 0 0 & \\\\ & & & \\\\ & & -1 & 0 \\\\ & & & \end{bmatrix} 0 0 0 0 1.
$$

따라서 두 개의 Pauli-Z 연산자의 텐서 제품은 $ $ $ + 1 $ 및 $ -1 $ eigenvalues로 구성 된 두 개의 공백으로 구성 된 행렬을 형성 합니다.
단일 고 비트 사례와 마찬가지로 두 가지 모두 반 공간을 구성 합니다 .이는 액세스 가능한 벡터 공간의 절반이 $ + 1 $ eigenspace에 속하고 나머지는 $ -1 $ eigenspace를 나타냅니다.
일반적으로 텐서 제품의 정의에서 쉽게 확인할 수 있습니다 .이는 Pauli-Z 연산자의 텐서 제품이 $ $ 고이를 따르는 합니다.
예를 들면 다음과 같습니다.

$$
\begin{align}
    \otimes \boldone Z =\begin{bmatrix}
        1 & 0 & 0 0 &\\\\
        0 & 1 & 0 & 0\\\\
        0 & 0 & -1 & 0\\\\
        0 & 0 & & -1 \end{bmatrix} .
\end{align}
$$

이전과 마찬가지로 이러한 매트릭스의 모든 단일 변환은 $ \pm 1 eigenvalues로 레이블이 지정 된 두 개의 반 공간에 대해서도 설명 $ 합니다.
예를 들어 $ \otimes = z HXH id의 x x h \otimes h (z \otimes z) h \otimes h입니다 $ $ = $ .
1 ~ 2 비트의 경우와 마찬가지로, $ \dagger 4 개의 \otimes \id $ $ \times $ 단일 행렬 $ u $ 에 대해 모든 2-수준 pauli 측정값을 u ^ (Z) u로 작성할 수 있습니다. 다음 표에서는 변환을 열거 합니다.

> [!NOTE]
>아래 표에서는 전환을 사용 하 여 $ \operatorname { } $ 행렬 > 을 표시 합니다.$$
> \begin{align}
>     \operatorname{교환 } &=
>     \left( \begin { 행렬}
>1 & 0 & 0 0 &\\\\
>0 & 0 & 1 & 0\\\\
>0 & 1 & 0 & 0\\\\
>0 0 0 & & & 1 > \end { 행렬 } \right ) >     \end{align}
> $$
>내장 작업을 시뮬레이션 하는 데 사용 [`SWAP`](xref:microsoft.quantum.intrinsic) 됩니다.

|Pauli 측정 | 단일 변환|
|----------------------|------------------------|
|$ \otimes \boldone Z $ | $\boldone \otimes \boldone$|
|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|
|$ \otimes \boldone X $ | $ \otimes \boldone H $|
|$ \otimes \boldone Y $ | $ HS \dagger \otimes \boldone ^ $|
|$\boldone \otimes Z $ | $ \operatorname { 교환 } $|
|$\boldone \otimes X $ | $ (H \otimes \boldone ) \operatorname { 교환 } $|
|$\boldone \otimes Y $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { 교환 } $|
|$Z \otimes Z $ | $ \operatorname { cnot } \_ { 10 } $|
|$X \otimes Z 시간 $ | $ \operatorname { } \_ { 10 } (H \otimes \boldone ) $|
|$Y \otimes Z $ | $ \operatorname { cnot } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|
|$Z \otimes X $ | $ \operatorname { cnot } \_ { 10 } ( \boldone \otimes H) $|
|$X \otimes X $ | $ \operatorname { cnot } \_ { 10 } (h \otimes h) $|
|$Y \otimes X $ | $ \operatorname { cnot } \_ { 10 } (HS ^ \dagger \otimes H) $|
|$Z \otimes Y $ | $ \operatorname { cnot } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|
|$X \otimes Y $ | $ \operatorname { cnot } \_ { 10 } (H \otimes HS ^ \dagger ) $|
|$Y \otimes Y $ | $ \operatorname { cnot } \_ { 10 } (hs ^ \dagger \otimes hs ^ \dagger ) $|

여기에서 [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) 다음과 같은 이유로 작업이 표시 됩니다.
행렬을 포함 하지 않는 각 pauli 측정값 $ \boldone $ 은 $ 위의 추론에 의해 단일에서 z z까지 동일 \otimes $ 합니다.
Z z의 고유 값는 $ \otimes $ 각 계산 기준 벡터를 구성 하는 eibit의 패리티에만 의존 하며 제어 되지 않는 연산은이 패리티를 계산 하 여 첫 번째 비트에 저장 하는 데 사용 됩니다.
그런 다음 첫 번째 비트를 측정 한 후에는 Pauli 연산자를 측정 하는 것과 동일한 결과의 절반 공간 id를 복구할 수 있습니다.

한 가지 추가 참고 사항: z z 측정 $ \otimes $ 은 z 1을 순차적으로 측정 하는 것과 동일한 것으로 간주 될 수 있지만 $ \otimes \mathbb { } $ $ \mathbb { } \otimes $ 이 가정은 false가 됩니다.
그 이유는 $ z z 측정 \otimes $ 에서 $ $ $ 이러한 연산자의 + 1 또는-1 $ eigenstate로 퀀텀 상태를 프로젝션 하기 때문입니다.
$Z \otimes \mathbb { 1을 측정 한 } $ 다음 $ \mathbb { 1 } \otimes z는 $ 퀀텀 상태 벡터를 z 1의 절반 공간에 먼저 투영 $ \otimes \mathbb { } $ 하 고 그 다음에 $ \mathbb { 1 } \otimes z $ 의 반쪽 공간으로 투영 합니다. 네 가지 계산 기준 벡터가 있으므로 두 측정값을 모두 수행 하면 상태가 1/4로 줄어들고 단일 계산 기준 벡터로 줄어듭니다.

## <a name="correlations-between-qubits"></a>이상 비트 간의 상관 관계
X x 또는 Z z와 같은 Pauli 매트릭스의 텐서 곱을 측정 하는 또 다른 방법은 $ \otimes $ $ \otimes $ 이러한 측정을 사용 하 여 두 개의 두 비트 간 상관 관계에 저장 된 정보를 확인할 수 있다는 것입니다.
X를 측정 $ \otimes \id $ 하면 첫 번째 비트에 로컬로 저장 된 정보를 볼 수 있습니다.
두 유형의 측정은 모두 퀀텀 컴퓨팅에서 동일 하 게 중요 하지만, 이전에는 퀀텀 컴퓨팅의 기능을 비춥니다.
이는 퀀텀 컴퓨팅에서 배워야 하는 정보가 단일의 모든 비트에 저장 되지 않고 한 번에 모든 모든 기능에 로컬로 저장 되는 것이 아니라 공동 측정 (예: z z)을 통해 확인 하는 경우에만 $ \otimes $ 이 정보가 매니페스트가 됨을 나타냅니다.

예를 들어 오류 수정에서는 보호 하려는 상태에 대 한 정보를 확인 하는 동안 발생 한 오류를 배우는 경우가 많습니다.
[비트 대칭 코드 샘플](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) 에서는 $ z \otimes z \otimes \id $ 및 $ \id \otimes z \otimes z $ < 와 같은 측정을 사용 하 여이 작업을 수행할 수 있는 방법의 예를 보여 줍니다. --TODO: 비트 대칭 코드 샘플이 온-등록 인 경우 바로 샘플 브라우저에 대 한 링크를 변경 합니다. -->

X Y Z와 같은 임의 pauli 연산자를 $ \otimes \otimes \otimes \boldone $ 측정할 수도 있습니다.
이러한 모든 텐서 제품의 pauli 연산자에는 두 개의 고유 값 $ \pm 1만 있고 $ 고유 값는 전체 벡터 공간의 반 공간을 구성 합니다.
따라서 위에 명시 된 요구 사항과 일치 합니다.

에서 Q# $ $ 측정이 기호 $ (-1) ^ j의 결과를 생성 하는 경우 이러한 측정값은 j를 반환 합니다 $ .
의 기본 제공 기능으로 Pauli를 측정 하 Q# 는 것은 이러한 연산자를 측정 하는 데 시간이 오래 걸릴 수 $ $ $ $ $ \id $ 있습니다 .이는 Z 및의 텐서 곱으로 작업을 표현 하는 데 필요한 diagonalizing U 게이트를 설명 하기 위해 이러한 연산자를 측정 하는 데 필요 합니다.
이러한 미리 정의 된 측정값 중 하나를 수행 하도록 지정할 수 있으므로 계산 기준 측정이 필요한 정보를 제공 하도록를 변환 하는 방법을 걱정 하지 않아도 됩니다.
Q#자동으로 필요한 모든 기본 변환을 처리 합니다.
자세한 내용은 및 작업을 참조 [`Measure`](xref:microsoft.quantum.intrinsic.measure) 하세요 [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) .

## <a name="the-no-cloning-theorem"></a>복제 안 함 정리

퀀텀 정보는 강력 합니다.
이를 통해 가장 잘 알려진 기존 알고리즘 보다 많은 수치를 지 원하는 것과 같은 놀라운 작업을 수행할 수 있습니다.
그러나 퀀텀 컴퓨팅의 기능에는 제한이 있습니다.
이러한 제한 사항 중 하나는 *복제 안 함 정리*에서 제공 됩니다.

복제 안 함 정리의 이름은 무엇입니다.
퀀텀 컴퓨터에의 한 일반 퀀텀 상태 복제를 허용 하지 않습니다.
정리 증명은 매우 간단 합니다.
이에 대 한 설명에는 복제 안 함 정리의 전체 증명을 사용 하는 것이 약간 기술적 이지만 추가 보조 기능을 사용 하지 않는 경우에는이 범위 내에 포함 됩니다 (보조 비트는 계산 중에는 스크래치 공간에 사용 되 고, 사용 되 고 관리 되는에는 사용 되 고 관리 됩니다 Q# . [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)

이러한 퀀텀 컴퓨터의 경우 단일 행렬에서 복제 작업을 설명 해야 합니다.
복제 하려고 하는 퀀텀 상태를 손상 시킬 수 있으므로 측정이 허용 되지 않습니다.
복제 작업을 시뮬레이션 하기 위해 속성을 사용 하는 데 사용 되는 단일 행렬을 원합니다.$$
  U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}
$$
모든 상태에 대해 $ \ket { \psi } $ 입니다.
행렬 곱셈의 선형 속성은 두 번째 $ 퀀텀 상태의 선형 속성을 의미 \ket 합니다. { \phi } $

$$
\begin{align}
    U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}
    &= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}
      + \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\
    &= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}
        \right) \\\\
    &\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ).
\end{align}
$$

이는 복제 안 함 정리의 기본적인 intuition을 제공 합니다. 알 수 없는 퀀텀 상태를 복사 하는 모든 장치는 복사 하는 일부 상태에서 오류를 유도 해야 합니다.
Cloner는 입력 상태에서 선형으로 작동 하는 주요 가정을 추가 하 고 보조 비트를 측정 하 여 위반할 수 있지만 이러한 상호 작용은 측정 통계를 통해 시스템에 대 한 정보를 누출 하 고 이러한 경우에도 정확한 복제를 방지 합니다.
복제 안 함 정리에 대 한 자세한 [내용은](xref:microsoft.quantum.more-information)을 참조 하십시오.

퀀텀 상태 저렴를 복제할 수 있는 경우 퀀텀 상태를 정리 하는 근거리 및 마법 기능을 제공 하기 때문에 복제 안 함은 퀀텀 컴퓨팅에 대 한 정 성적을 이해 하는 데 중요 합니다.
정말 Heisenberg의 vaunted 불확실성 원칙을 위반할 수 있습니다.
또는 최적의 cloner를 사용 하 여 복잡 한 퀀텀 배포에서 단일 샘플을 가져오고 한 샘플에서 해당 배포에 대해 알아볼 수 있는 모든 것을 알아볼 수 있습니다.
이는 동전 및 관찰 헤드를 대칭 이동 하는 것과 마찬가지로 "Ah가 해당 동전의 분포는 $ p = 0.512643 \ ldots!"를 통해 베르누이 되어야 합니다 $ .  한 가지 정보 (헤드 결과)가 상당한 이전 정보 없이 배포를 인코딩하는 데 필요한 많은 양의 정보를 제공할 수 없기 때문에 이러한 문은 sensical 되지 않습니다.
마찬가지로, 이전 정보가 없으면 p를 몰라도 이러한 동전의 앙상블를 준비할 수 없기 때문에 퀀텀 상태를 완벽 하 게 복제할 수 없습니다 $ $ .

정보는 퀀텀 컴퓨팅에서 무료로 제공 됩니다.
측정 된 각는 단일 비트 정보를 제공 하 고, 복제 안 함 정리는 시스템 및 해당 시스템에 대해 발생 하는 파업에 대 한 정보 간의 기본적인 균형을 유지 하기 위해 악용할 수 있는 백도어가 없음을 보여 줍니다.
