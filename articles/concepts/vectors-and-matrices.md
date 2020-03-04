---
title: 퀀텀 컴퓨팅의 벡터 및 행렬
description: 벡터 및 매트릭스를 사용 하는 방법에 대 한 기본 사항을 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 076ab6242b7ae31d4936ae8505034f1f13fa4727
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904913"
---
# <a name="vectors-and-matrices"></a>벡터 및 행렬

몇 가지 벡터와 행렬에 대해 잘 알고 있는 것은 퀀텀 컴퓨팅을 이해 하는 데 필수적입니다. 아래에서 간략하게 소개 하 고 관심 있는 독자는 *Strang, G와 같은 선형 대 수 표준 참조를 읽는 것이 좋습니다. (1993). 선형 대 수 (Vol. 3)에 대해 소개 합니다. Wellesley, MA: Wellesley-캠브리지* 또는 [Linear 대 수](http://joshua.smcvt.edu/linearalgebra/)와 같은 온라인 참조를 누릅니다.

차원 (또는 크기 $n)의 열 벡터 (또는 간단히 [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $는 열로 정렬 된 $n $ 복소수 $ (v_1, v_2, \ldots, v_n) $의 컬렉션입니다.

$ $v = \begin{bmatrix} v_1\\\\ v_2\\\\ \vdots\\\\ v_n \end{bmatrix} $ $

벡터 $v $은 $ \sqrt{\sum\_i | v\_i | ^ 2} $로 정의 됩니다. 벡터가 $1 $ 인 경우 벡터는 unit (또는 [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)라고 함) 이라고 합니다. Vector $v $ [*의 adjoint*](https://en.wikipedia.org/wiki/Adjoint_matrix) 는 $v ^ \aate$로 표시 되며 $\*$에서 복소수 복소수를 나타내는 다음 행 벡터로 정의 됩니다.

$ $ \begin{bmatrix} v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \\end{bmatrix} = \begin{bmatrix} v_1 ^ * & \cs& v_n ^ * $ $

두 벡터를 하나로 곱하는 가장 일반적인 방법은 점 제품이 라고도 하는 [*내부 제품*](https://en.wikipedia.org/wiki/Inner_product_space)을 통하는 것입니다.  내부 제품은 한 벡터의 프로젝션을 다른 벡터에 제공 하며, 한 벡터를 다른 간단한 벡터의 합계로 표현 하는 방법을 설명 하는 데 유용 합니다.  $ \Left\langle u, v\right\rangle $로 표시 되는 $u $ 및 $v $ 사이의 내부 곱은로 정의 됩니다.

$ $ \langle u, v\rangle = u ^ \langle = u\_1 ^ {\*} v_1 + \langle + u\_n ^ {\*} v\_n.
$$

이 표기법을 사용 하면 vector $v $를 $ \sqrt{\langle v, v\rangle} $로 작성할 수도 있습니다.

벡터를 숫자 $c $로 곱하여 해당 항목에 $c $로 곱하는 새 벡터를 만들 수 있습니다. $ 및 $v $ $u 두 개의 벡터를 추가 하 여 항목이 $u $ 및 $v $ 인 항목의 합계인 새 벡터를 만들 수도 있습니다. 이러한 작업은 다음과 같습니다.

$ $ \mathrm{If} ~ u = \begin{bmatrix} u_1\\\\ u_2\\\\ \vdots\\\\ u_n \end{bmatrix} ~ \mathrm{and} ~ v = \begin{bmatrix} v_1\\\\ v_2\\\\ \vdots\\\\ v_n \end{bmatrix}, ~ \mathrm{then} ~ au + bv = \begin{bmatrix} au_1 + bv_1\\\\ au_2 + bv_2\\\\ \vdots\\\\ au_n + bv_n \end{bmatrix}.
$$

$M \times n $ 크기의 [*행렬*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) 은 아래와 같이 $ rows 및 $n $ columns $m 정렬 된 $mn $ 복소수의 컬렉션입니다.

$ $M = \begin{bmatrix} M_{11} ~ ~ M_{12} ~ ~ \cstii~ ~ M_ {1n}\\\\ M_{21} ~ ~ M_{22} M_ ~ ~ \cdots ~ ~\\{2n} \\\\\\ d도트 M_ M_ M_ {m1} ~ ~\\{m2} ~ ~ \cstii~ ~ \\ {mn} $ $

차원 $n $의 벡터는 단순히 크기 $n \times $1에 해당 하는 행렬입니다. 벡터를 사용할 때와 마찬가지로 행렬을 숫자 $c $로 곱하여 모든 항목에 $c $가 곱해집니다. 그러면 동일한 크기의 두 행렬을 추가 하 여 해당 항목이 두 행렬의 각 항목의 합계인 새 행렬을 생성할 수 있습니다. 

## <a name="matrix-multiplication-and-tensor-products"></a>행렬 곱하기 및 텐서 제품

또한 다음과 같이 dimension $m \times n $ 및 dimension $n \times p $의 $N $ 라는 두 행렬 $M $ $P를 곱합니다.

\begin{align} & \begin{bmatrix} M_{11} ~ ~ M_{12} ~ ~ \comi~ ~ M_ {1n}\\\\ M_{21} ~ ~ M_{22} M_ ~ \cdots ~ ~\\{2n} \\\\\\ d도트 M_ M_ M_ {m1} ~ ~ {m2} ~ ~ \csti~ ~ {} \end{bmatrix} \begin{bmatrix} N_{11} ~ ~ N_{12} ~ ~ \cdots ~ ~ N_ {1 p}\\\\ N_{21} ~ ~ N_{22} N_ ~ \cstii~ ~\\{2p} \\\\\\ N_ N_ N_ P_ {n1} ~ ~ {n2} ~ ~ \cdots = \begin{bmatrix} {np} ={11} ~ ~ P_{12} ~ ~ \cdots ~ ~ P_ {1 p}\\\\ P_{21} ~ ~ P_{22} ~ ~ \csti~ ~ P_ {2p}\\\\\\\\ P_ \end{align} P_ P_ {m1} ~ ~ {m2} ~ ~ \csta~ ~ {mp} \end{bmatrix}

$P $의 항목이 $P _ {ik} = \ sum_j M_ {ij} N_ {jk} $입니다. 예를 들어 $P _{11}$ 항목은 $ $N의 첫 번째 열과 $M $의 첫 번째 행에 대 한 내부 곱입니다. 벡터는 단순히 행렬의 특별 한 사례 이므로이 정의는 행렬-벡터 곱셈으로 확장 됩니다. 

이를 고려 하는 모든 행렬은 행과 열의 수가 같거나 $1 $ 열에 해당 하는 벡터 인 정사각형 행렬입니다. 하나의 특수 사각형 행렬은 [*id 매트릭스*](https://en.wikipedia.org/wiki/Identity_matrix)이며, $ \boldone $는 모든 대각선 요소가 $1 $이 고 나머지 요소는 $0 $와 동일 합니다.

$ $ \boldone = \begin{bmatrix} 1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\ 0 ~ ~ 1 ~ ~ \coml ~ 0\\\\ ~ ~ \dst\\\\ 0 ~ ~ 0 ~ ~ \cdots $ $

사각형 행렬 $A $의 경우 행렬 $B $는 $AB = BA = \boldone $ 인 경우에는 [*역행렬*](https://en.wikipedia.org/wiki/Invertible_matrix) 을 말합니다. 행렬의 역함수는 존재 하지 않아도 되지만, 존재 하는 경우에는 고유 하 고 ^{-1}$ $A 나타냅니다. 

행렬 $M $의 경우 $M $의 adjoint 또는 켤레 ji은 _ {ij} = M_ {} ^\*$와 $N 같은 행렬 $N $입니다. $M $의 adjoint는 일반적으로 $M ^ \aa$로 표시 됩니다. $UU ^ \a턴 = U ^ \dagger $ 또는 같은 경우에는 $U ^{-1} = U ^ \dagger $와 같이 행렬 $U $가 [*단일*](https://en.wikipedia.org/wiki/Unitary_matrix) 것으로 가정 합니다.  단일 매트릭스의 가장 중요 한 속성은 벡터의 표준을 유지 한다는 것입니다.  이는 다음과 같은 경우에 발생 합니다. 

$ $ \langle v, v \rangle = v ^ \aav = v ^ \langle U ^{-1} U v = v ^ \l n u ^ \v\rangle. $ $  

$M = M ^ \dagger $ 인 경우 행렬 $M $은 (는) [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) 라고 합니다.

마지막으로 두 행렬의 [*텐서 product*](https://en.wikipedia.org/wiki/Tensor_product) (또는 Kronecker) $M $ size $m \times n $ $N 및 size $p \times) q $는 크기가 더 큰 행렬 $P = M\otimes n $ 이며 크기는 $mp \times nq $ 이며 다음과 같이 $M $ 및 $N $에서 가져옵니다.

\begin{align} M \otimes N & = \begin{bmatrix} M_{11} ~ ~ \otimes ~ ~ M_ {1n} \\\\\\d도트 \\ M_ M_ {m1} ~ ~ \comi~ ~ N_ {mn} \end{bmatrix} \otimes \begin{bmatrix}{11} N_ ~ ~ \cs ~\\{1n} \\ d도트\\\\ N_ {p1} ~ ~ \otimes ~ ~ N_ {pq} \end{bmatrix}\\\\ & = \begin{bmatrix} M_{11} \begin{bmatrix} N_{11}-~ \com~ ~ N_ {1n}\\\\\\d도트 \\ N_ N_ {p1} ~ ~ \cstii~ ~ {pq} \end{bmatrix} ~ ~ \comi~ ~ M_ {1n} \begin{bmatrix} N_{11} ~ \cs~ ~ N_ {1n}\\\\ \dst\begin{bmatrix}\\\\ {p1} ~ ~ \cdots ~ ~ N_ {pq} N_\\\\ \dst\\\\ {m1} M_ N_{11} ~ \cdots\\\\ \cdots\\\\ N_ {p1} ~ ~ \cdots ~ ~ N_ {pq} \end{bmatrix} ~ ~ \csta~ ~ M_ {mn} \begin{bmatrix} N_{11}-~ \cdots ~ ~ N_ {1n}\\\\\\d도트 \\ N_ N_ bmatrix} \end{bmatrix}.
\end{align}

몇 가지 예제를 통해이를 보다 잘 이해할 수 있습니다.

$ $ \begin{bmatrix} a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix} a \begin{bmatrix} c \\\\ \\\\ e \end{bmatrix} \\\\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ \\e\end {bmatrix} \end{bmatrix} = \begin{bmatrix} a c \\ \\a d \\ \\a e \\ b c \\\\ b d \\\\ be\end {bmatrix} $ $

및

$ $ \begin{bmatrix} a \ b \\\\ c\ d \end{bmatrix} \otimes \begin{bmatrix} e\ f\\\\e\ h \end{bmatrix} = \begin{bmatrix} a\begin {bmatrix} e \ f\\\\ \end{bmatrix} b\ams {bmatrix} e \ f\\\\ g \ h \end{bmatrix} \\\\[1em] c\begin {bmatrix} e \ f\\\\ e\ h \end{bmatrix} d\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} \end{bmatrix} = \begin{bmatrix} or\ af \ n o \\\\@no__ t_15_ ag \ ah \ bg \ bh \\\\ ce \ cf \ de \ df \\\\ cg \ ch \ dg \ dh \end{bmatrix}.
$$

텐서 제품에 대 한 최종 유용한 표기법 밑수 규칙은 모든 vector $v $ 또는 matrix $M $, $v ^ {\otimes n} $ 또는 $M ^ {\otimes n} $가 $n $-접기 반복 텐서 제품에 대 한 짧은 손 임을 나타내는 것입니다.  예를 들어 다음과 같은 가치를 제공해야 합니다.

\begin{align} & \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ {\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\-1 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 1 \\\\-1 \\\\-1 \\\\1 \otimes bmatrix}, \\\\ & \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ {\otimes 1} = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} \qquad\begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0\\\\ 1 & 0 & 0 & 0 \ 끝 { bmatrix}.
\end{align}
