---
title: 고급 행렬 개념
description: 퀀텀 알고리즘을 설명 하 고 시뮬레이트하는 데 사용 되는 기본 도구인 고유 벡터, eigenvalues 및 matrix 지 수에 대해 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
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
ms.openlocfilehash: 8d3c646715f13c454e51b9295cbfdabf6a236ffc
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630143"
---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="187fc-103">고급 행렬 개념</span><span class="sxs-lookup"><span data-stu-id="187fc-103">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="187fc-104">이제 [*고유 벡터*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 및 [*지 수*](https://en.wikipedia.org/wiki/Matrix_exponential) 에 대 한 행렬 조작을 확장 하 여 퀀텀 알고리즘을 설명 하 고 구현 하는 데 필요한 기본적인 도구 집합을 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-104">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="187fc-105">Eigenvalues 및 고유 벡터</span><span class="sxs-lookup"><span data-stu-id="187fc-105">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="187fc-106">$M $ 사각형 행렬로 $v 하 고 $ 모든 0 벡터가 아닌 벡터 (즉, 모든 항목이 $0 인 벡터)가 될 수 있도록 합니다. $</span><span class="sxs-lookup"><span data-stu-id="187fc-106">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="187fc-107">$V $ 은 [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $ $ 일부 숫자 $c에 대 한 $Mv = cv 인 경우 $M eigenvector입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-107">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="187fc-108">$Eigenvector $v에 해당 하는 [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $c 이라고 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-108">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="187fc-109">일반적으로 행렬 $M는 $ 벡터를 다른 벡터로 변환할 수 있지만 eigenvector는 숫자로 곱할 때를 제외 하 고는 변경 되지 않은 상태로 유지 되기 때문에 특수 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-109">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="187fc-110">$V $ 가 eigenvalue $c를 사용 하는 eigenvector 경우 $ $ 동일한 eigenvalue를 사용 하는 eigenvector (0이 아닌 $a의 경우)도 $av 됩니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-110">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="187fc-111">예를 들어 id 매트릭스의 경우 모든 vector $v $ 는 eigenvalue $1을 사용 하는 eigenvector입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-111">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="187fc-112">또 다른 예로 대각선에 0이 아닌 항목을 포함 하는 $D [*대각선 행렬*](https://en.wikipedia.org/wiki/Diagonal_matrix) 을 생각해 보십시오 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-112">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

<span data-ttu-id="187fc-113">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="187fc-113">$$ \begin{bmatrix}</span></span>
<span data-ttu-id="187fc-114">d_1 & 0 & 0 \\ \\ 0 & d_2 & 0 \\ \\ 0 & 0 & d_3 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="187fc-114">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="187fc-115">벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-115">The vectors</span></span>

<span data-ttu-id="187fc-116">$ $ \begin{ bmatrix } 1 \\ \\ 0 \\ \\ 0 \begin{ bmatrix } , \begin{ bmatrix } 0 \\ \\ 1 \\ \\ 0 \end { bmatrix } 및 \begin{ bmatrix } 0 \\ \\ 0 \\ \\ 1 \end {bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="187fc-116">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="187fc-117">는이 행렬을 고유 값 $d _1 $ , $d _2 $ 및 $d _3로 각각 고유 벡터 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-117">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="187fc-118">$D _1 $ $d _2 $ 및 $d _3이 $ 고유한 숫자인 경우 이러한 벡터 (및 해당)는 행렬 $D의 유일한 고유 벡터입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-118">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$.</span></span> <span data-ttu-id="187fc-119">일반적으로 대각선 행렬의 경우 고유 값 및 고유 벡터를 쉽게 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-119">In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="187fc-120">고유 값는 대각선에 표시 되는 모든 숫자이 고 각 고유 벡터는 $1와 동일한 항목을 포함 하는 단위 벡터이 $ 고 나머지 항목은 $0와 동일 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-120">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="187fc-121">위의 예제에서 고유 벡터 $D의는 $ $3 차원 벡터의 기반을 형성 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-121">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="187fc-122">기반은 벡터를 선형 조합으로 작성할 수 있도록 벡터 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-122">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="187fc-123">$ $ $ 모든 벡터 $v를 $v $v $ a_1 v_1 + a_2 v_2 + a_3 v_3으로 작성할 수 있는 경우 보다 명시적, $v _1, $v _2 및 _3으로 구성 됩니다 $ $ $ $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-123">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="187fc-124">Hermitian 행렬 (자체 adjoint 라고도 함)은 해당 하는 복잡 한 켤레와 동일한 복잡 한 정사각형 행렬 이지만, 단일 행렬은 역행렬이 복소수와 동일한 복잡 한 사각형입니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-124">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate, while a unitary matrix is a complex square matrix whose inverse is equal to its complex conjugate.</span></span>
<span data-ttu-id="187fc-125">기본적으로 퀀텀 컴퓨팅에서 발생 하는 유일한 매트릭스가 Hermitian 및 단일 행렬의 경우 [*spectral 정리*](https://en.wikipedia.org/wiki/Spectral_theorem)라고 하는 일반적인 결과가 있습니다. 예를 들면 다음을 어설션 합니다. Hermitian 또는 단일 행렬 $M의 경우 $ $ $ 일부 대각선 행렬 $D의 경우 $M = u ^ \aad u에 해당 하는 단일 $U $ 있습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-125">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$.</span></span> <span data-ttu-id="187fc-126">또한 $D의 대각선 항목은 $ $M의 고유 값가 됩니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-126">Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="187fc-127">$D는 대각선 행렬의 고유 값 및 고유 벡터를 계산 하는 방법을 이미 알고 $ 있습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-127">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$.</span></span> <span data-ttu-id="187fc-128">이 정리를 사용 하는 경우 $v $ 가 eigenvalue $c (예: $Dv = cv)를 사용 하는 $D의 eigenvector 경우 $ $ $ $U ^ \aav는 $ $ eigenvalue $M와 $c의 eigenvector 됩니다 $ .</span><span class="sxs-lookup"><span data-stu-id="187fc-128">Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="187fc-129">그 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-129">This is because</span></span>

<span data-ttu-id="187fc-130">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span><span class="sxs-lookup"><span data-stu-id="187fc-130">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="187fc-131">행렬 지 수</span><span class="sxs-lookup"><span data-stu-id="187fc-131">Matrix Exponentials</span></span>
<span data-ttu-id="187fc-132">[*행렬 지*](https://en.wikipedia.org/wiki/Matrix_exponential) 수는 지 수 함수를 정확 하 게 유추 하 여 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-132">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="187fc-133">행렬 $A의 행렬 지 수는 $ 로 표현 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-133">The matrix exponential of a matrix $A$ can be expressed as</span></span>

<span data-ttu-id="187fc-134">$ $ e ^ A = \boldone + a + \frac{A ^ 2 } {2!} + \frac{A ^ 3 } {3!} + \ci$ $</span><span class="sxs-lookup"><span data-stu-id="187fc-134">$$ e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots $$</span></span>

<span data-ttu-id="187fc-135">이는 퀀텀 기계 시간 진화는 $e ^ {iB } $ For Hermitian matrix $B 형식의 단일 행렬에서 설명 하기 때문에 중요 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-135">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.</span></span>  <span data-ttu-id="187fc-136">이러한 이유로 matrix 지 수를 수행 하는 것은 퀀텀 컴퓨팅의 기본 부분이 며, 이러한 Q #은 이러한 작업을 설명 하는 기본 루틴을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-136">For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="187fc-137">기존 컴퓨터에서 행렬 지 수를 계산 하는 방법에는 여러 가지가 있습니다. 일반적으로 이러한 지 수는 점이로 위험이 크기 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-137">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="187fc-138">[*Cleve Moler 및 Charles Van 대출을 참조 하세요. "천구 수상한는 행렬의 지 수를 계산 하는 방법" SIAM 리뷰 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) 은 관련 된 문제에 대 한 자세한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-138">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="187fc-139">행렬의 지 수를 계산 하는 방법을 이해 하는 가장 쉬운 방법은 해당 행렬의 고유 값 및 고유 벡터를 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-139">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="187fc-140">특히 위에 설명 된 spectral 정리는 모든 Hermitian 또는 단일 $A 행렬에 대해 $ $ $ $A = u ^ \A라 D u를 $D 하는 단일 행렬 $U와 대각선 행렬 있음을 의미 합니다 $ .  단위 인자의 속성 때문에 모든 power $A $p에 대해 ^ 2 = U ^ \a턴 D ^ 2 U $ 및 이와 유사한 $A 있습니다 $ . ^ p = u ^ \ard ^ p U $  이를 연산자 지 수의 연산자 정의로 대체 하는 경우 다음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-140">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

<span data-ttu-id="187fc-141">$ $ e ^ A = U ^ \ara\left (\boldone + D + \frac{D ^ 2 } {2!} + \cstst\right) U = u ^ \ara\ac\begin{ bmatrix } \exp (D_ {11 } ) & 0 & \cdots 0 \\\\ 0 & \exp (D_ {22 } ) & \c90 & \\\\ \cdots & \cdots & \cdots & \cdots \\\\ 0&0 D_ & c도트 & \exp ({NN } ) \cdots bmatrix } U $ $</span><span class="sxs-lookup"><span data-stu-id="187fc-141">$$ e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="187fc-142">즉, $A 행렬의 eigenbasis으로 변환 하는 경우 행렬 $ 의 지 수를 계산 하는 것은 행렬의 eigenbasis의 일반 지 수를 계산 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-142">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="187fc-143">퀀텀 컴퓨팅의 많은 작업에는 matrix 지 수 수행이 포함 되어 있으므로, 연산자 지 수를 단순화 하기 위해 행렬의 eigenbasis으로 변환 하는이 트릭은 자주 나타나고이 가이드의 뒷부분에서 설명 하는 Trotter – Suzuki 퀀텀 시뮬레이션 방법과 같은 여러 퀀텀 알고리즘의 기반이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-143">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="187fc-144">또 다른 유용한 속성은 $B $ $B = b ^ {-1 } = b ^ \aa$B $ ^ 2 = \boldone $ 입니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-144">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="187fc-145">위의 행렬 지 수 확장에이 규칙을 적용 하 고 $ \boldone $ 및 $B 항을 함께 그룹화 하 여 $ id $x 모든 실수 값을 확인할 수 있습니다. $</span><span class="sxs-lookup"><span data-stu-id="187fc-145">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="187fc-146">$ $e ^ {iBx } = \boldone \cos (x) + iB\sin (x) $ $</span><span class="sxs-lookup"><span data-stu-id="187fc-146">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="187fc-147">갖고.</span><span class="sxs-lookup"><span data-stu-id="187fc-147">holds.</span></span> <span data-ttu-id="187fc-148">이 트릭은 $B 차원이 $ 여러 개의 $ 단일 및 Hermitian $B 경우에만 특수 한 경우에 사용 되는 경우에도 작업 행렬 지 수에 대 한 이유를 발생 시킬 수 있기 때문에 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="187fc-148">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
