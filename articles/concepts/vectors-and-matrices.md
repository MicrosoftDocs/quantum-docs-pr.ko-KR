---
title: 양자 컴퓨팅의 벡터 및 행렬
description: 벡터 및 매트릭스를 사용 하는 방법에 대 한 기본 사항을 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: f9d4e14742b7d06a6e90af0902b31fbdf17aedab
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269544"
---
# <a name="vectors-and-matrices"></a>벡터 및 행렬

몇 가지 벡터와 행렬에 대해 잘 알고 있는 것은 퀀텀 컴퓨팅을 이해 하는 데 필수적입니다. 아래에서 간략하게 소개 하 고 관심 있는 독자는 *Strang, G. (1993)와 같은 선형 대 수 표준 참조를 읽는 것이 좋습니다. 선형 대 수 (Vol. 3)에 대해 소개 합니다. Wellesley, MA: Wellesley-캠브리지* 또는 [Linear 대 수](http://joshua.smcvt.edu/linearalgebra/)같은 온라인 참조를 누릅니다.

차원 (또는 크기 $n)의 열 벡터 (또는 단순한 [*벡터*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v는 $ $ $ 열로 정렬 된 $n 복소수 $ (v_1, v_2, \ldots, v_n) $의 컬렉션입니다.

$ $v = \begin{bmatrix}
v_1\\\\
v_2\\\\
\vdots\\\\
v_n \end{bmatrix}$$

벡터 $v의 일반은 $ $ \sqrt { \sqrt \_ i | v \_ i | ^ 2 } $로 정의 됩니다. 벡터가 $1 인 경우 벡터는 unit (또는 [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)라고 함) 이라고 합니다 $ . [*벡터 $v의 adjoint*](https://en.wikipedia.org/wiki/Adjoint_matrix) 는 $ $v ^ \a와 같이 표시 되며 $ $ \* $가 복소수 복소수를 나타내는 다음 행 벡터로 정의 됩니다.

$ $ \begin{ bmatrix } v_1 \\ \\ \vsts \\ \\ v_n \begin{ bmatrix } ^ \aate= \begin{ bmatrix } v_1 ^ * & \cs& v_n ^ * \begin{bmatrix}$$

두 벡터를 하나로 곱하는 가장 일반적인 방법은 점 제품이 라고도 하는 [*내부 제품*](https://en.wikipedia.org/wiki/Inner_product_space)을 통하는 것입니다.  내부 제품은 한 벡터의 프로젝션을 다른 벡터에 제공 하며, 한 벡터를 다른 간단한 벡터의 합계로 표현 하는 방법을 설명 하는 데 유용 합니다.  $U와 $v 사이의 내부 곱 ( $ $ $ \left \langle u, v \right \rangle $ 는로 정의 됨)

$ $ \langle u, v \rangle = u ^ \langle = u \_ 1 ^ { \* } v_1 + \langle + u \_ n ^ { \* } v \_ n.
$$

이 표기법을 사용 하면 벡터 $v를 $ $ \sqrt { \larv, v $로 작성할 수도 있습니다 \rangle } .

벡터를 숫자 $c와 곱하여 $ 해당 항목에 $c를 곱한 새 벡터를 만들 수 있습니다 $ . $U 두 개의 벡터를 추가 $ 하 고 $v $ $u 및 $v 항목의 합 인 새 벡터를 형성할 수 있습니다 $ $ . 이러한 작업은 다음과 같습니다.

$ $ \mathrm{If } ~ u = \begin{bmatrix}
u_1\\\\
u_2\\\\
\vdots\\\\
u_n \end{ bmatrix } ~ \mathrm{and } ~ v = \end{bmatrix}
    v_1\\\\
    v_2\\\\
    \vdots\\\\
    v_n \end{ bmatrix } , ~ \mathrm{then } ~ au + bv = \end{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\vdots\\\\
au_n + bv_n \end{ bmatrix } .
$$

$M \times n 크기의 [*행렬*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) $ 은 아래와 $ $ 같이 $m 행과 $n 열에 정렬 된 $mn 복소수 모음입니다 $ .

$ $M = \begin{bmatrix}
M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1n } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \cdots\\\\
M_ {m1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {mn } \\ \\ \cdots bmatrix } . $ $

차원 $n 벡터는 $ 단순히 \times 1 $n 크기의 행렬입니다 $ . 벡터를 사용 하는 것 처럼 행렬을 숫자 $c와 곱하여 $ 모든 항목에 $c를 곱하는 새 행렬을 얻을 수 $ 있으며, 동일한 크기의 두 행렬을 추가 하 여 항목이 두 행렬의 각 항목의 합계인 새 행렬을 생성할 수 있습니다. 

## <a name="matrix-multiplication-and-tensor-products"></a>행렬 곱하기 및 텐서 제품

또한 다음과 $ 같이 차원 $m \times n 및 차원 $n \times p $N의 두 행렬 $M 곱하여 n $ $ $ $ 차원에 대 한 새 행렬 $P을 얻을 $ 수 있습니다.

\begin{align}
& \begin{bmatrix}
    M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1n } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \cdots\\\\
    M_ {m1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {mn}
종단bmatrix}
시작bmatrix}
N_ {11 } ~ ~ N_ {12 } ~ ~ \cdots ~ ~ N_ {1 p } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \cdots ~ ~ N_ {2p } \\ \\ \cdots\\\\
N_ {n1 } ~ ~ N_ {n2 } ~ ~ \comi~ ~ N_ {np}
\end{ bmatrix } = \end{bmatrix}
P_ {11 } ~ ~ P_ {12 } ~ ~ \cdots ~ ~ P_ {1 p } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \cdots ~ ~ P_ {2p } \\ \\ \cdots\\\\
P_ {m1 } ~ ~ P_ {m2 } ~ ~ \cdots ~ ~ P_ {mp}
종단bmatrix}
\end{align}

$P의 항목은 $ $P _ {ik } = \ sum_j M_ {ij} N_ {jk } $입니다. 예를 들어 $P _ {11 $ 항목은 } $ $N의 첫 번째 열에 $M 첫 번째 행의 내부 곱입니다 $ . 벡터는 단순히 행렬의 특별 한 사례 이므로이 정의는 행렬-벡터 곱셈으로 확장 됩니다. 

이를 고려 하는 모든 행렬은 행과 열 수가 같거나 $1 열에 해당 하는 벡터입니다 $ . 하나의 특수 사각형 행렬은 [*id 매트릭스*](https://en.wikipedia.org/wiki/Identity_matrix)이며, $ \boldone는 $ 모든 대각선 요소가 $1이 $ 고 나머지 요소는 $0와 동일 합니다 $ .

$ $ \boldone = \begin{bmatrix}
1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\
0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\
~ ~ \ddots\\\\
0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \cdots bmatrix } . $ $

사각형 행렬 $A의 $ $ 경우 $AB = BA = \boldone 인 경우 행렬 $B [*역행렬*](https://en.wikipedia.org/wiki/Invertible_matrix) 이라고 $ 합니다. 행렬의 역함수는 존재 하지 않아도 되지만,이 경우에는 고유 하 고 ^ {-1 $ $A를 나타냅니다 } . 

행렬 $M의 경우 $ $M의 adjoint 또는 복소수는 $ $ _ {ij } = M_ {ji $ $N 하는 행렬 $N입니다 } ^ \* . $M의 adjoint는 $ 일반적으로 $M ^ \aatea로 표시 됩니다 $ . $$UU ^ \a턴 = [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) u ^ \dagger; $ $U ^ {-1 } = u ^ \dagger 인 경우 행렬 $U는 단일 인 것으로 가정 $ 합니다.  단일 매트릭스의 가장 중요 한 속성은 벡터의 표준을 유지 한다는 것입니다.  이는 다음과 같은 경우에 발생 합니다. 

$ $ \langle v, v \rangle = v ^ \aav = v ^ \langle U ^ {-1 } U v = v ^ \aau ^ \aau v = \laru v, U v \rangle . $ $  

$$M = M ^ [*\dagger*](https://en.wikipedia.org/wiki/Hermitian_matrix) 인 경우 행렬 $M는 라고 $ 합니다.

마지막으로 크기가 $m n 인 두 $M 행렬의 [*텐서 product*](https://en.wikipedia.org/wiki/Tensor_product) (또는 Kronecker product) $ \times $ $N와 크기 $ $p \times q는 크기가 $ 더 큰 행렬 $P = M n n a M e \otimes $ nq, $mp $ 에서 얻은 것 이며 다음과 같이 $M에서 가져옵니다 $ $ .

\begin{align}
    M \otimes N &= \otimesbmatrix}
        M_ {11 } ~ ~ \cdots ~ ~ M_ {1n } \\ \\ \cdots\\\\
        M_ {m1 } ~ ~ \cdots ~ ~ M_ {mn}
    종단bmatrix}
    \otimes \otimesbmatrix}
        N_ {11 } ~ ~ \cdots ~ ~ N_ {1q } \\ \\ \cdots\\\\
        N_ {p1 } ~ ~ \csti~ ~ N_ {pq}
    \end{ bmatrix } \\ \\ &= \end{bmatrix}
        M_ { } 11\begin{ bmatrix } N_ {11 } ~ ~ \cststii~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{ bmatrix } ~ ~ \cf~ ~ M_ {1q } \begin{ bmatrix } N_ {11 } ~ ~ \begin{~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{ bmatrix } \\ \\ \begin{\\\\
        M_ {m1 } \begin{ bmatrix } N_ {11 } ~ ~ \begin{~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{ bmatrix } ~ \begin{점 ~ ~ M_ {mn } \begin{ bmatrix } N_ {11 } ~ ~ \begin{~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{bmatrix}
    \end{ bmatrix } .
\end{align}

몇 가지 예제를 통해이를 보다 잘 이해할 수 있습니다.

$ $ \begin{bmatrix}
        a \\ \\ b \end{ bmatrix } \end{\end{ bmatrix } c \\ \\ d \\ \\ e \end{ bmatrix } = \end{bmatrix}
        a \begin{ bmatrix } c \\ \\ d \\ \\ e \begin{bmatrix}
        \\\\[1.5 em] b \begin{ bmatrix } c \\ \\ d \\ \\ e\end{bmatrix}
    종단bmatrix}
    = \begin{ bmatrix } a c a \\ \\ d \\ \\ a e \\ \\ b c \\ \\ b d \\ \\\end{bmatrix}
$$

및

$ $ \begin{bmatrix}
        a \ b \\ \\ c \ d \end{bmatrix}
    \otimes \otimesbmatrix}
        e \ f \\ \\ g \ h \end{bmatrix}
     = \begin{bmatrix}
    은\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    b\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    2\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    종단bmatrix}
    = \begin{bmatrix}
    ae \ n a m e \ n a m e \ i n \ \\ \\ bg \ bh \\ \\ w\ f\ de \ df \\ \\ cg \ ch \ bmatrix }
$$

텐서 제품에 대 한 최종 유용한 표기법 밑수 규칙은 모든 벡터 $v $ 또는 행렬 $v $M에 대해 $ ^ {\otimes n } $ 또는 $M ^ {\otimes n } $은 $n $ 접기 반복 텐서 제품에 대 한 짧은 손입니다.  예를 들어:

\begin{align}
& \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } ^ {\begin{1 } = \begin{1 0 \begin{, bmatrix } \\ \\ bmatrix } \qquad \begin{bmatrix} 1 \\ \\ 0\end{ bmatrix } ^ {\begin{2 } = \begin{ bmatrix } 1 \\ \\ 0 0 \\ \\ \\ \\ 0 \begin{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ -1 \begin{ bmatrix } ^ {\begin{2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \begin{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 1 & 0 \begin{ bmatrix } ^ {\begin{1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \begin{ bmatrix } , \qquad \begin{bmatrix} 0 & 1 \\ \\ 1 0&& end{ bmatrix } ^ {\begin{2 } = \begin{ bmatrix } 0 &0&0 &1 0 \\ \\ \\ \\ \\\\ \end{bmatrix}&0&1 &0 0&1&0 &0&0&0 0
\end{align}
