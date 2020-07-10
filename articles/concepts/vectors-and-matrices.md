---
제목: 퀀텀 계산의 벡터 및 행렬 설명: 벡터 및 매트릭스를 사용 하는 방법에 대 한 기본 사항을 알아봅니다.
작성자: QuantumWriter uid:: nawiebe@microsoft.com 12/11/2017: ms. 날짜:. 토픽: 문서 번호:
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

# <a name="vectors-and-matrices"></a>벡터 및 행렬

몇 가지 벡터와 행렬에 대해 잘 알고 있는 것은 퀀텀 컴퓨팅을 이해 하는 데 필수적입니다. 아래에서 간략하게 소개 하 고 관심 있는 독자는 *Strang, G. (1993)와 같은 선형 대 수 표준 참조를 읽는 것이 좋습니다. 선형 대 수 (Vol. 3)에 대해 소개 합니다. Wellesley, MA: Wellesley-캠브리지* 또는 [Linear 대 수](http://joshua.smcvt.edu/linearalgebra/)같은 온라인 참조를 누릅니다.

차원 (또는 크기)의 열 벡터 (또는 단순한 [*벡터*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ v는 $ $ $ $ $ $ $ 열로 정렬 된 n 복소수 (v_1, v_2, \ldots, v_n)의 컬렉션입니다.

$$hyper-v=\begin{bmatrix}
v_1\\\\
v_2\\\\
\vdots\\\\
v_n\end{bmatrix}$$

벡터 $ v는 $ $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $ 로 정의 됩니다. 벡터가 1 인 경우 벡터는 unit (또는 [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)라고 함) 이라고 합니다 $ $ . [*벡터 v의 adjoint*](https://en.wikipedia.org/wiki/Adjoint_matrix) 는 $ $ $ v ^로 표시 되며 \dagger $ 은 $ \* $ 복소수 복소수를 나타내는 다음 행 벡터로 정의 됩니다.

$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ * & \cdots & v_n ^ *\end{bmatrix}$$

두 벡터를 하나로 곱하는 가장 일반적인 방법은 점 제품이 라고도 하는 [*내부 제품*](https://en.wikipedia.org/wiki/Inner_product_space)을 통하는 것입니다.  내부 제품은 한 벡터의 프로젝션을 다른 벡터에 제공 하며, 한 벡터를 다른 간단한 벡터의 합계로 표현 하는 방법을 설명 하는 데 유용 합니다.  U $ , v를 표시 하는 u와 v 사이의 내부 곱 $ $ $ $ \left \langle \right \rangle $ 은로 정의 됩니다.

$$
\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.
$$

이 표기법을 사용 하면 벡터 $ v를 $ $ \sqrt { \langle v, v \rangle } $ 로 작성할 수도 있습니다.

벡터와 숫자 c를 곱하여 $ $ 해당 항목에 c를 곱한 새 벡터를 만들 수 있습니다 $ $ . U 및 v 라는 두 개의 $ 벡터 $ 를 추가 하 여 $ $ 항목이 $ u 및 v 항목의 합계인 새 벡터를 $ $ $ 만들 수도 있습니다. 이러한 작업은 다음과 같습니다.

$$\mathrm{U 인 경우 } ~=\begin{bmatrix}
u_1\\\\
u_2\\\\
\vdots\\\\
u_n \end{bmatrix} ~ \mathrm { 및}~
hyper-v=\begin{bmatrix}
    v_1\\\\
    v_2\\\\
    \vdots\\\\
    v_n \end{bmatrix} ~ \mathrm { 다음}~
오스트레일리아 + bv=\begin{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\vdots\\\\
au_n + bv_n \end{bmatrix} .
$$

크기 [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) $ m n의 행렬 \times $ 은 아래와 $ $ $ $ 같이 m 행과 $ n 개의 $ 열로 정렬 된 mn 복소수의 컬렉션입니다.

$$매= 
\begin{bmatrix}
M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1n}\\\\
M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\
\ddots\\\\
M_ { m1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { mn}\\\\
\end{bmatrix}.$$

차원 n의 벡터는 $ $ 단순히 n 1 크기의 행렬입니다 $ \times $ . 벡터와 마찬가지로 행렬을 숫자 c와 곱하여 $ $ 모든 항목에 c를 곱한 새 행렬을 얻을 수 $ 있으며, $ 동일한 크기의 두 행렬을 추가 하 여 해당 항목이 두 행렬의 각 항목의 합계인 새 행렬을 생성할 수 있습니다. 

## <a name="matrix-multiplication-and-tensor-products"></a>행렬 곱하기 및 텐서 제품

또한 다음과 같이 dimension m n 및 n 차원의 두 행렬 m을 곱하여 $ $ $ \times $ $ $ $ n \times p 차원의 $ 새 매트릭스 p를 $ 가져올 $ $ \times $ 수 있습니다.

\begin{align}
&\begin{bmatrix}
    M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1n}\\\\
    M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\
    \ddots\\\\
    M_ { m1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { mn}
\end{bmatrix}
\begin{bmatrix}
N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1 p}\\\\
N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2p}\\\\
\ddots\\\\
N_ { n1 } ~~ N_ { n2 } ~~ \cdots ~~ N_ { np}
\end{bmatrix}=\begin{bmatrix}
P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1 p}\\\\
P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2p}\\\\
\ddots\\\\
P_ { m1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { mp}
\end{bmatrix}
\end{align}

여기서 P의 항목 $ 은 $ $ { ik } = \sum _j M_ { ij } N_ jk P_ { } $ . 예를 들어 $ P_ 11 항목 { 은 } $ $ $ N의 첫 번째 열을 가진 M의 첫 번째 행의 내부 곱 $ 입니다 $ . 벡터는 단순히 행렬의 특별 한 사례 이므로이 정의는 행렬-벡터 곱셈으로 확장 됩니다. 

이를 고려 하는 모든 행렬은 행과 열 수가 같거나 벡터 (1 개 열에만 해당) 인 정사각형 행렬입니다 $ $ . 하나의 특수 사각형 행렬은 [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix) $ \boldone $ 모든 대각선 요소를 1로, $ $ 나머지 요소를 0으로 $ $ 유지 하는 id 매트릭스입니다.

$$\boldone=\begin{bmatrix}
1 ~~ 0 ~~ \cdots ~~ 0\\\\
0 ~~ 1 ~~ \cdots ~~ 0\\\\
~~ \ddots\\\\
0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$

사각형 행렬 a의 $ $ $ 경우 B 행렬은 $ AB BA 인 경우 [*역*](https://en.wikipedia.org/wiki/Invertible_matrix) 이라고 $ = = \boldone $ 합니다. 행렬의 역은 존재 하지 않아도 되지만, 존재 하는 경우에는 고유 하 고 $ ^ { -1을 나타냅니다 } $ . 

모든 matrix $ m $ 에서 m의 adjoint 또는 복소수는 $ $ $ $ $ N_ { ij } = M_ { ji } ^ \* $ 하는 행렬 N입니다. M의 adjoint $ 는 $ 보통 m ^로 표시 됩니다 $ \dagger $ . $ $ [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) $ UU ^ u \dagger = ^ \dagger u = \boldone $ 또는 동등 ( $ u ^ { -1 } = u ^ \dagger $ ) 인 경우에는 행렬 u가 단일 것으로 가정 합니다.  단일 매트릭스의 가장 중요 한 속성은 벡터의 표준을 유지 한다는 것입니다.  이는 다음과 같은 경우에 발생 합니다. 

$$\langlev, v v \rangle = ^ \dagger v = v ^ \dagger u ^ { -1 } u v = v ^ u ^ u v \dagger \dagger = \langle , u v \rangle .$$  

$ $ M m ^ 인 경우 행렬 m은 [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) 라고 $ = \dagger $ 합니다.

마지막으로, 크기가 m n 및 n 인 두 행렬 m의 [*텐서 product*](https://en.wikipedia.org/wiki/Tensor_product) (또는 Kronecker product)는 $ $ $ \times $ $ $ $ \times $ $ 크기 mp nq의 더 큰 행렬 p = m n 이며 다음과 \otimes $ $ \times $ $ $ 같이 m과 n에서 가져옵니다 $ $ .

\begin{align}
    M \otimes N&=
    \begin{bmatrix}
        M_ { 11 } ~~ \cdots ~~ M_ { 1n }\\\\
        \ddots\\\\
        M_ { m1 } ~~ \cdots ~~ M_ { mn  }
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        N_ { 11 } ~~ \cdots ~~ N_ { 1q  }\\\\
        \ddots\\\\
        N_ { p1 } ~~ \cdots ~~ N_ { pq}
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1q } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { 1n } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1n } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}\\\\
        \ddots\\\\
        M_ { m1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1q } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { mn } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1q } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}
    \end{bmatrix}.
\end{align}

몇 가지 예제를 통해이를 보다 잘 이해할 수 있습니다.

$$
    \begin{bmatrix}
        a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=
    \begin{bmatrix}
        a \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
        \\\\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
    \end{bmatrix}
    =\begin{bmatrix}a \\\\ ca d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}
$$

and

$$
    \begin{bmatrix}
        a \ b \\\\ c \ d\end{bmatrix}
    \otimes 
    \begin{bmatrix}
        e \ f \\\\ g \ h\end{bmatrix}
     =
    \begin{bmatrix}
    은\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    b\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    2\begin{bmatrix}
    e \ f \\\\ g \ h\end{bmatrix}
    \end{bmatrix}
    =
    \begin{bmatrix}
    ns\\\\\
    ag \ ah \ bg \ bh\\\\
    ce \ cf \ de \ df\\\\
    cg \ ch \ dg \ dh \end{bmatrix} .
$$

텐서 제품에 대 한 최종 유용한 표기법 밑수 규칙은 모든 벡터 $ v $ 또는 매트릭스 M의 $ 경우 $ $ v ^ { \otimes n } $ 또는 $ M ^ { \otimes n } $ 은 $ n $ 접기 반복 텐서 제품에 대 한 짧은 손입니다.  예를 들면 다음과 같습니다.

\begin{align}
&\begin{bmatrix}1 \\\\ 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 0 0 \\\\ \\\\ \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1 \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\
  &\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & 0 0 1 0 0 & & \\\\ & & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 1 & 0 & & \end{bmatrix} 0 0.
\end{align}
