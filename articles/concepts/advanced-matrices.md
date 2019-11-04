---
title: 고급 행렬 개념 | Microsoft Docs
description: 고급 행렬 개념
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: f87b3bcd19d2f98fea2a9724a280781a78c4cbb9
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183763"
---
# <a name="advanced-matrix-concepts"></a>고급 행렬 개념 #

이제 [*고유 벡터*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 및 [*지 수*](https://en.wikipedia.org/wiki/Matrix_exponential) 에 대 한 행렬 조작을 확장 하 여 퀀텀 알고리즘을 설명 하 고 구현 하는 데 필요한 기본적인 도구 집합을 형성 합니다.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenvalues 및 고유 벡터 ##

$를 정사각형 행렬로 지정 하 고, $v $은 모든 0 벡터가 아닌 벡터 (즉, 모든 항목이 $0 $ 인 벡터)가 $M 수 있습니다.

$V $은 일부 숫자 $c $의 경우 $ is $Mv = cv $ $M [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 입니다. $C $은 eigenvector $v $에 해당 하는 [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 입니다. 일반적으로 행렬 $M $는 벡터를 다른 벡터로 변환할 수 있지만 eigenvector는 숫자로 곱할 때를 제외 하 고는 변경 되지 않은 상태로 유지 되기 때문에 특수 합니다. $V $가 eigenvalue를 사용 하는 eigenvector $c $ 이면 동일한 eigenvalue를 사용 하 여 $av $도 0이 아닌 $a $에 대 한 eigenvector입니다.

예를 들어 id 매트릭스의 경우 모든 vector $v $는 eigenvalue $1 $를 사용 하는 eigenvector입니다.

또 다른 예로, 대각선에 0이 아닌 항목을 포함 하는 [*대각선 행렬*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D $를 생각해 보겠습니다.

$ $ \begin{bmatrix} d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.
$$

벡터입니다.

$ $ \begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0 \ end {bmatrix} 및 \begin{bmatrix}0 \\\\ 0 \\\\ 1 \ end {bmatrix} $ $

는이 행렬에서 고유 값 $d _1 $, $d _2 $ 및 $d _3 $로 각각 고유 벡터 됩니다. $D _1 $, $d _2 $ 및 $d _3 $이 고유한 숫자인 경우 이러한 벡터 (및 해당)는 행렬 $D $의 유일한 고유 벡터입니다. 일반적으로 대각선 행렬의 경우 고유 값 및 고유 벡터를 쉽게 읽을 수 있습니다. 고유 값는 대각선에 표시 되는 모든 숫자이 고 각 고유 벡터는 $1 $와 같은 항목 1 개 및 $0 $와 같은 나머지 항목을 포함 하는 단위 벡터입니다.

위의 예에서는 $D $의 고유 벡터가 $3 $ 차원 벡터의 기반을 형성 합니다. 기반은 벡터를 선형 조합으로 작성할 수 있도록 벡터 집합입니다. 좀 더 명시적으로, $v _1 $, $v _2 $ 및 $v _3 $ $v 형식으로 작성할 수 있습니다. $v = a_1 v_1 + a_2 v_2 + a_3 v_3 $로 작성할 수 있습니다.

Hermitian 행렬 (자체 adjoint 라고도 함)은 해당 하는 복잡 한 켤레와 동일한 복잡 한 정사각형 행렬 이지만, 단일 행렬은 역행렬이 복소수와 동일한 복잡 한 사각형입니다.
기본적으로 퀀텀 컴퓨팅에서 발생 하는 유일한 행렬 인 Hermitian 및 단일 행렬의 경우 [*spectral 정리*](https://en.wikipedia.org/wiki/Spectral_theorem)라고 하는 일반적인 결과가 있습니다. 여기에는 Hermitian 또는 단일 행렬 $M $가 있습니다. 일부 대각선 행렬 $D $의 경우 $M = U ^ \a턴 D U $와 같은 단일 $U $. 또한 $D $의 대각선 항목은 $M $의 고유 값가 됩니다.

$D $로 된 대각선 행렬의 고유 값 및 고유 벡터를 계산 하는 방법을 이미 알고 있습니다. 이 정리를 사용 하는 경우 $v $가 eigenvalue $c $, 즉 $Dv = cv $를 사용 하는 $D의 eigenvector 경우 $U ^ \aae $는 eigenvalue $M $와 $c $의 eigenvector입니다. 그 이유는 다음과 같습니다.

$ $M (U ^ \ariv) = U ^ \a턴 D U (u ^ \aav) = U ^ \a턴 d (U U ^ \aaa) v = U ^ \Aad v = c U ^ \aa. $ $

## <a name="matrix-exponentials"></a>행렬 지 수
[*행렬 지*](https://en.wikipedia.org/wiki/Matrix_exponential) 수는 지 수 함수를 정확 하 게 유추 하 여 정의할 수도 있습니다.  행렬 $A $의 행렬 지 수는로 표현 될 수 있습니다.

$ $ e ^ A = \boldone + A + \frac{A ^ 2} {2!} + \frac{A ^ 3} {3!} + \ci$ $

이는 iB Hermitian 행렬 $B $에 대 한 ^ {} $ $e 형식의 단일 매트릭스에서 퀀텀 기계 시간 발전을 설명 하기 때문에 중요 합니다.  이러한 이유로 matrix 지 수를 수행 하는 것은 퀀텀 컴퓨팅의 기본 부분이 며, 이러한 Q #은 이러한 작업을 설명 하는 기본 루틴을 제공 합니다.
기존 컴퓨터에서 행렬 지 수를 계산 하는 방법에는 여러 가지가 있습니다. 일반적으로 이러한 지 수는 점이로 위험이 크기 합니다.  [*Cleve Moler 및 Charles Van 대출을 참조 하세요. "천구 수상한는 행렬의 지 수를 계산 하는 방법" SIAM 리뷰 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) 은 관련 된 문제에 대 한 자세한 정보를 확인 합니다.

행렬의 지 수를 계산 하는 방법을 이해 하는 가장 쉬운 방법은 해당 행렬의 고유 값 및 고유 벡터를 통하는 것입니다.  특히, 위에 설명 된 spectral 정리는 모든 Hermitian 또는 $A 단일 행렬에 대해 $, $A = U ^ \dagger D U $와 같은 단일 행렬 $U $ 및 대각선 행렬 $D $가 있습니다.  단위 인자의 속성 때문에 모든 power $p $ $A ^ p = U ^ \ard ^ p U $에 대해 ^ 2 = U ^ \aad ^ 2 U $와 유사 하 게 $A 합니다.  이를 연산자 지 수의 연산자 정의로 대체 하는 경우 다음을 가져옵니다.

$ $ e ^ A = U ^ \ara\left (\boldone + D + \frac{D ^ 2} {2!} + \cstst\right) U = U ^ \\begin{bmatrix}\exp (D_{11}) & 0 & \ca& 0\\\\ 0 &{22}exp (D_ &) & \cdots\\0 \\ & \vom& \cdots & \cdots\\\cdots \\ 0 & 0 & \cst& \exp (D_ {NN}) \end{bmatrix} U. $ $

즉, $A 매트릭스의 eigenbasis으로 변환 하는 경우 행렬의 지 수를 계산 하는 것은 행렬의 eigenbasis의 일반 지 수를 계산 하는 것과 같습니다.  퀀텀 컴퓨팅의 많은 작업에서 행렬 지 수 수행 하는 것과 관련 하 여 연산자 지 수를 단순화 하기 위해 행렬의 eigenbasis으로 변환 하는이 트릭은 자주 나타나고 다음과 같은 다양 한 퀀텀 알고리즘의 기반이 됩니다. Trotter – Suzuki-이 가이드의 뒷부분에서 설명 하는 퀀텀 시뮬레이션 방법입니다.

또 다른 유용한 속성은 $ $B $B = B ^{-1}= B ^ \aaa, $B ^ 2 = \boldone $입니다. 위의 행렬 지 수 확장에이 규칙을 적용 하 고 $ \boldone $ 및 $B $ 항을 함께 그룹화 하 여 $ $ 및 $ 항을 함께 그룹화 하면 $ identity $x 모든 실수 값을 확인할 수 있습니다.

$ $e ^ {iBx} = \boldone \cos (x) + iB\sin (x) $ $


갖고. 이 트릭은 $B $ 차원이 단일 Hermitian와 경우에만 특수 한 $B 경우에 발생 하는 작업 행렬 지 수에 대 한 이유를 허용 하기 때문에 특히 유용 합니다.
