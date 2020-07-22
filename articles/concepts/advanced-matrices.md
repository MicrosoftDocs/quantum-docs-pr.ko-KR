---
제목: 고급 행렬 개념 설명: 퀀텀 알고리즘을 설명 하 고 시뮬레이트하는 데 사용 되는 기본 도구인 고유 벡터, eigenvalues 및 matrix 지 수에 대해 알아봅니다.
작성자: QuantumWriter uid:-advanced ms. author: nawiebe@microsoft.com ms. 날짜: 12/11/2017. 토픽: 문서 번호-loc:
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "$$$"
- "$$$"
- "$$$"
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
# <a name="advanced-matrix-concepts"></a>고급 행렬 개념 #

이제 [*고유 벡터*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 및 [*지 수*](https://en.wikipedia.org/wiki/Matrix_exponential) 에 대 한 행렬 조작을 확장 하 여 퀀텀 알고리즘을 설명 하 고 구현 하는 데 필요한 기본적인 도구 집합을 형성 합니다.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenvalues 및 고유 벡터 ##

$M을 $ 사각형 행렬로 $ , v를 $ 모두 0 벡터가 아닌 벡터 (즉, 모든 항목이 0 인 벡터 $ $ )로 지정 합니다.

$ $ [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $ M은 $ $ = $ 일부 숫자 c에 대해 Mv cv 인 $ 경우 M은 eigenvector입니다 $ . $ $ Eigenvector v에 해당 하는 [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 를 c 라고 $ 합니다 $ . 일반적으로 행렬과 $ M은 $ 벡터를 다른 벡터로 변환할 수 있지만 eigenvector는 숫자를 곱하는 경우를 제외 하 고는 변경 되지 않은 상태로 유지 되기 때문에 특수 합니다. $V $ 가 eigenvalue c를 사용 하는 eigenvector $ 경우 $ $ av $ 는 $ $ 동일한 eigenvalue를 사용 하는 eigenvector (0이 아닌 경우) 이기도 합니다.

예를 들어 id 매트릭스의 경우 모든 벡터 $ v $ 는 eigenvalue 1을 사용 하는 eigenvector입니다 $ $ .

또 다른 예로 [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ $ 대각선에 0이 아닌 항목을 포함 하는 대각선 행렬 D를 생각해 보겠습니다.

$$
\begin{bmatrix}
d_1 & 0 0 0 & d_2 0 0 0 \\\\ & & \\\\ & & d_3 \end{bmatrix} .
$$

벡터입니다.

$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} 및 \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$

는이 행렬에서 고유 값 $ d_1 $ , $ d_2 $ 및 $ d_3 $ 를 각각 고유 벡터 합니다. $D_1 $ , $ d_2 $ 및 $ d_3 $ 고유한 숫자인 경우 이러한 벡터 (및 해당)는 행렬 d의 유일한 고유 벡터입니다 $ $ . 일반적으로 대각선 행렬의 경우 고유 값 및 고유 벡터를 쉽게 읽을 수 있습니다. 고유 값는 대각선에 표시 되는 모든 숫자이 고 각 고유 벡터는 1과 동일한 항목이 $ 1이 $ 고 나머지 항목이 0 인 단위 벡터입니다 $ $ .

위의 예제에서 고유 벡터 $ D는 $ $ 3 차원 벡터의 기반을 형성 합니다 $ . 기반은 벡터를 선형 조합으로 작성할 수 있도록 벡터 집합입니다. 더 명시적, $ v_1 $ , $ v_2 $ 및 $ v_3 $ v_1 a_2 $ $ $ = $ $ $ , $ v_2 $ 및 $ a_3 $ 일부 숫자에 대 한 v a_1 v_3 + a_1 a_2 + a_3에 대 한 모든 벡터 v를 작성할 수 있습니다.

Hermitian 매트릭스 (자체 adjoint 라고도 함)는 자체의 복소수 복소수와 동일한 복잡 한 정사각형 행렬 이지만, 단일 행렬은 해당 하는가 adjoint 또는 복소수 복소수와 동일한 복잡 한 사각형 행렬입니다.
기본적으로 퀀텀 컴퓨팅에서 발생 하는 유일한 행렬 인 Hermitian 및 단일 매트릭스의 경우 [*spectral 정리*](https://en.wikipedia.org/wiki/Spectral_theorem)라고 하는 일반적인 결과가 있습니다. 즉, 모든 Hermitian 또는 단일 매트릭스 m의 경우 $ $ $ $ $ = \dagger $ 일부 대각선 행렬 d에 대 한 M u ^ d u $ 와 같은 단일 U $ 가 있습니다. 또한 D의 대각선 항목은 $ $ M의 고유 값가 됩니다 $ $ .

대각선 행렬 D의 고유 값 및 고유 벡터를 계산 하는 방법을 이미 알고 $ $ 있습니다. 이 정리를 사용 하 여 $ v $ 가 $ eigenvalue c를 포함 하는 D의 eigenvector (예 $ : Dv cv) 인 경우 $ $ $ = $ $ U ^ \dagger v는 $ $ $ eigenvalue c가 있는 eigenvector의입니다 $ $ . 그 이유는 다음과 같습니다.

$$M (U ^ \dagger v) = u ^ \dagger d u (u ^ \dagger v) = U ^ \dagger d (u u ^ \dagger ) v = u ^ \dagger d v = c u ^ \dagger v.$$

## <a name="matrix-exponentials"></a>행렬 지 수
[*행렬 지*](https://en.wikipedia.org/wiki/Matrix_exponential) 수는 지 수 함수를 정확 하 게 유추 하 여 정의할 수도 있습니다.  행렬 a의 행렬 지 $ 수는 $ 로 표현 될 수 있습니다.

$$
e ^ A = \boldone + a + \frac { a ^ 2 } { 2! } + \frac { ^ 3 } { 3!}+\cdots
$$

이는 퀀텀 기계 시간 진화는 $ e ^ { IB } $ for Hermitian matrix $ B $ 형식의 단일 행렬에서 설명 하기 때문에 중요 합니다.  이러한 이유로 matrix 지 수를 수행 하는 것은 퀀텀 컴퓨팅의 기본 부분이 며, 이러한 Q #은 이러한 작업을 설명 하는 기본 루틴을 제공 합니다.
기존 컴퓨터에서 행렬 지 수를 계산 하는 방법에는 여러 가지가 있습니다. 일반적으로 이러한 지 수는 점이로 위험이 크기 합니다.  [*Cleve Moler 및 Charles Van 대출을 참조 하세요. "천구 수상한는 행렬의 지 수를 계산 하는 방법" SIAM 리뷰 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) 은 관련 된 문제에 대 한 자세한 정보를 확인 합니다.

행렬의 지 수를 계산 하는 방법을 이해 하는 가장 쉬운 방법은 해당 행렬의 고유 값 및 고유 벡터를 통하는 것입니다.  특히 위에 설명 된 spectral 정리는 모든 Hermitian 또는 단일 행렬에 대 한 $ 단일 $ 매트릭스 $ u $ 와 대각선 행렬 $ d ( $ $ = u ^ \dagger d u $ )가 존재 한다는 것을 의미 합니다.  단위 인자의 속성 때문에 $ ^ 2 = u ^ \dagger d ^ 2 u $ 및 이와 유사한 모든 전원 $ p $ $ a ^ p = u ^ \dagger d ^ p u $ 를 사용할 수 있습니다.  이를 연산자 지 수의 연산자 정의로 대체 하는 경우 다음을 가져옵니다.

$$
e ^ A = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \exp (D_ { 11 } ) & 0 0 0 & \cdots & \\\\ 0 & \exp (D_ { 22 } ) & \cdots & 0 \\\\ \vst\vst\v도트 & & \ddots & \\\\ 0 & 0 & \cdots & \exp (D_ { NN } ) \end{bmatrix} U.$$

즉, 행렬 A의 eigenbasis으로 변환 하는 경우 행렬 $ $ 의 지 수를 계산 하는 것은 행렬의 eigenbasis의 일반 지 수를 계산 하는 것과 같습니다.  퀀텀 컴퓨팅의 많은 작업에는 matrix 지 수 수행이 포함 되어 있으므로, 연산자 지 수를 단순화 하기 위해 행렬의 eigenbasis으로 변환 하는이 트릭은 자주 나타나고이 가이드의 뒷부분에서 설명 하는 Trotter – Suzuki 퀀텀 시뮬레이션 방법과 같은 여러 퀀텀 알고리즘의 기반이 됩니다.

또 다른 유용한 속성은 $ b $ 가 단일 and Hermitian 경우입니다 (예: $ b = b ^ { -1 } = b ^ \dagger $ then $ b ^ 2 = \boldone $ ). 이러한 행렬 지 수의 위 확장에이 규칙을 적용 하 고 $ \boldone $ 및 $ B 용어를 함께 그룹화 하면 $ 모든 실수 값 $ x에서 id를 볼 수 있습니다 $ .

$$e ^ { ibx } = \boldone \cos (x) + iB\sin (x)$$


갖고. 이 트릭은 b의 차원이 $ $ $ 단일 및 Hermitian 경우의 특수 한 경우에도 b의 차원이 수많은 지 수 작업 행렬에 대 한 이유를 허용 하기 때문에 특히 유용 합니다 $ .
