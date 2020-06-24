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
# <a name="vectors-and-matrices"></a><span data-ttu-id="ef562-103">벡터 및 행렬</span><span class="sxs-lookup"><span data-stu-id="ef562-103">Vectors and Matrices</span></span>

<span data-ttu-id="ef562-104">몇 가지 벡터와 행렬에 대해 잘 알고 있는 것은 퀀텀 컴퓨팅을 이해 하는 데 필수적입니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-104">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="ef562-105">아래에서 간략하게 소개 하 고 관심 있는 독자는 *Strang, G. (1993)와 같은 선형 대 수 표준 참조를 읽는 것이 좋습니다. 선형 대 수 (Vol. 3)에 대해 소개 합니다. Wellesley, MA: Wellesley-캠브리지* 또는 [Linear 대 수](http://joshua.smcvt.edu/linearalgebra/)같은 온라인 참조를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-105">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="ef562-106">차원 (또는 크기 $n)의 열 벡터 (또는 단순한 [*벡터*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v는 $ $ $ 열로 정렬 된 $n 복소수 $ (v_1, v_2, \ldots, v_n) $의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-106">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="ef562-107">$ $v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-107">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="ef562-108">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-108">v_1\\\\</span></span>
<span data-ttu-id="ef562-109">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-109">v_2\\\\</span></span>
<span data-ttu-id="ef562-110">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-110">\vdots\\\\</span></span>
<span data-ttu-id="ef562-111">v_n \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="ef562-111">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="ef562-112">벡터 $v의 일반은 $ $ \sqrt { \sqrt \_ i | v \_ i | ^ 2 } $로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-112">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="ef562-113">벡터가 $1 인 경우 벡터는 unit (또는 [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)라고 함) 이라고 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-113">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="ef562-114">[*벡터 $v의 adjoint*](https://en.wikipedia.org/wiki/Adjoint_matrix) 는 $ $v ^ \a와 같이 표시 되며 $ $ \* $가 복소수 복소수를 나타내는 다음 행 벡터로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-114">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="ef562-115">$ $ \begin{ bmatrix } v_1 \\ \\ \vsts \\ \\ v_n \begin{ bmatrix } ^ \aate= \begin{ bmatrix } v_1 ^ \* & \cs& v_n ^ \* \begin{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="ef562-115">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="ef562-116">두 벡터를 하나로 곱하는 가장 일반적인 방법은 점 제품이 라고도 하는 [*내부 제품*](https://en.wikipedia.org/wiki/Inner_product_space)을 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-116">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="ef562-117">내부 제품은 한 벡터의 프로젝션을 다른 벡터에 제공 하며, 한 벡터를 다른 간단한 벡터의 합계로 표현 하는 방법을 설명 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-117">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="ef562-118">$U와 $v 사이의 내부 곱 ( $ $ $ \left \langle u, v \right \rangle $ 는로 정의 됨)</span><span class="sxs-lookup"><span data-stu-id="ef562-118">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

<span data-ttu-id="ef562-119">$ $ \langle u, v \rangle = u ^ \langle = u \_ 1 ^ { \* } v_1 + \langle + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="ef562-119">$$ \langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="ef562-120">이 표기법을 사용 하면 벡터 $v를 $ $ \sqrt { \larv, v $로 작성할 수도 있습니다 \rangle } .</span><span class="sxs-lookup"><span data-stu-id="ef562-120">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="ef562-121">벡터를 숫자 $c와 곱하여 $ 해당 항목에 $c를 곱한 새 벡터를 만들 수 있습니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-121">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="ef562-122">$U 두 개의 벡터를 추가 $ 하 고 $v $ $u 및 $v 항목의 합 인 새 벡터를 형성할 수 있습니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-122">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="ef562-123">이러한 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-123">These operations are depicted below:</span></span>

<span data-ttu-id="ef562-124">$ $ \mathrm{If } ~ u = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-124">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="ef562-125">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-125">u_1\\\\</span></span>
<span data-ttu-id="ef562-126">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-126">u_2\\\\</span></span>
<span data-ttu-id="ef562-127">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-127">\vdots\\\\</span></span>
<span data-ttu-id="ef562-128">u_n \end{ bmatrix } ~ \mathrm{and } ~ v = \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-128">u_n \end{bmatrix}~\mathrm{and}~ v =\begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-129">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-129">v_1\\\\</span></span>
    <span data-ttu-id="ef562-130">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-130">v_2\\\\</span></span>
    <span data-ttu-id="ef562-131">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-131">\vdots\\\\</span></span>
    <span data-ttu-id="ef562-132">v_n \end{ bmatrix } , ~ \mathrm{then } ~ au + bv = \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-132">v_n \end{bmatrix},~\mathrm{then}~ au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="ef562-133">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-133">au_1+bv_1\\\\</span></span>
<span data-ttu-id="ef562-134">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-134">au_2+bv_2\\\\</span></span>
<span data-ttu-id="ef562-135">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-135">\vdots\\\\</span></span>
<span data-ttu-id="ef562-136">au_n + bv_n \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="ef562-136">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="ef562-137">$M \times n 크기의 [*행렬*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) $ 은 아래와 $ $ 같이 $m 행과 $n 열에 정렬 된 $mn 복소수 모음입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-137">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="ef562-138">$ $M = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-138">$$M = \begin{bmatrix}</span></span>
<span data-ttu-id="ef562-139">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1n } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \cdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-139">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="ef562-140">M_ {m1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {mn } \\ \\ \cdots bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="ef562-140">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\ \end{bmatrix}.$$</span></span>

<span data-ttu-id="ef562-141">차원 $n 벡터는 $ 단순히 \times 1 $n 크기의 행렬입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-141">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="ef562-142">벡터를 사용 하는 것 처럼 행렬을 숫자 $c와 곱하여 $ 모든 항목에 $c를 곱하는 새 행렬을 얻을 수 $ 있으며, 동일한 크기의 두 행렬을 추가 하 여 항목이 두 행렬의 각 항목의 합계인 새 행렬을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-142">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="ef562-143">행렬 곱하기 및 텐서 제품</span><span class="sxs-lookup"><span data-stu-id="ef562-143">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="ef562-144">또한 다음과 $ 같이 차원 $m \times n 및 차원 $n \times p $N의 두 행렬 $M 곱하여 n $ $ $ $ 차원에 대 한 새 행렬 $P을 얻을 $ 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-144">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

<span data-ttu-id="ef562-145">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="ef562-145">\begin{align}</span></span>
<span data-ttu-id="ef562-146">& \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-146">&\begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-147">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1n } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \cdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-147">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
    <span data-ttu-id="ef562-148">M_ {m1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {mn}</span><span class="sxs-lookup"><span data-stu-id="ef562-148">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
<span data-ttu-id="ef562-149">종단bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-149">\end{bmatrix}</span></span>
<span data-ttu-id="ef562-150">시작bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-150">\begin{bmatrix}</span></span>
<span data-ttu-id="ef562-151">N_ {11 } ~ ~ N_ {12 } ~ ~ \cdots ~ ~ N_ {1 p } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \cdots ~ ~ N_ {2p } \\ \\ \cdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-151">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\ N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="ef562-152">N_ {n1 } ~ ~ N_ {n2 } ~ ~ \comi~ ~ N_ {np}</span><span class="sxs-lookup"><span data-stu-id="ef562-152">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
<span data-ttu-id="ef562-153">\end{ bmatrix } = \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-153">\end{bmatrix}=\begin{bmatrix}</span></span>
<span data-ttu-id="ef562-154">P_ {11 } ~ ~ P_ {12 } ~ ~ \cdots ~ ~ P_ {1 p } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \cdots ~ ~ P_ {2p } \\ \\ \cdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-154">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\ P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="ef562-155">P_ {m1 } ~ ~ P_ {m2 } ~ ~ \cdots ~ ~ P_ {mp}</span><span class="sxs-lookup"><span data-stu-id="ef562-155">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
<span data-ttu-id="ef562-156">종단bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-156">\end{bmatrix}</span></span>
<span data-ttu-id="ef562-157">\end{align}</span><span class="sxs-lookup"><span data-stu-id="ef562-157">\end{align}</span></span>

<span data-ttu-id="ef562-158">$P의 항목은 $ $P _ {ik } = \ sum_j M_ {ij} N_ {jk } $입니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-158">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="ef562-159">예를 들어 $P _ {11 $ 항목은 } $ $N의 첫 번째 열에 $M 첫 번째 행의 내부 곱입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-159">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$.</span></span> <span data-ttu-id="ef562-160">벡터는 단순히 행렬의 특별 한 사례 이므로이 정의는 행렬-벡터 곱셈으로 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-160">Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="ef562-161">이를 고려 하는 모든 행렬은 행과 열 수가 같거나 $1 열에 해당 하는 벡터입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-161">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="ef562-162">하나의 특수 사각형 행렬은 [*id 매트릭스*](https://en.wikipedia.org/wiki/Identity_matrix)이며, $ \boldone는 $ 모든 대각선 요소가 $1이 $ 고 나머지 요소는 $0와 동일 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-162">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

<span data-ttu-id="ef562-163">$ $ \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-163">$$\boldone=\begin{bmatrix}</span></span>
<span data-ttu-id="ef562-164">1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-164">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="ef562-165">0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-165">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="ef562-166">~ ~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-166">~~ \ddots\\\\</span></span>
<span data-ttu-id="ef562-167">0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \cdots bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="ef562-167">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="ef562-168">사각형 행렬 $A의 $ $ 경우 $AB = BA = \boldone 인 경우 행렬 $B [*역행렬*](https://en.wikipedia.org/wiki/Invertible_matrix) 이라고 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-168">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="ef562-169">행렬의 역함수는 존재 하지 않아도 되지만,이 경우에는 고유 하 고 ^ {-1 $ $A를 나타냅니다 } .</span><span class="sxs-lookup"><span data-stu-id="ef562-169">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="ef562-170">행렬 $M의 경우 $ $M의 adjoint 또는 복소수는 $ $ _ {ij } = M_ {ji $ $N 하는 행렬 $N입니다 } ^ \* .</span><span class="sxs-lookup"><span data-stu-id="ef562-170">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="ef562-171">$M의 adjoint는 $ 일반적으로 $M ^ \aatea로 표시 됩니다 $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-171">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="ef562-172">$$UU ^ \a턴 = [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) u ^ \dagger; $ $U ^ {-1 } = u ^ \dagger 인 경우 행렬 $U는 단일 인 것으로 가정 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-172">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="ef562-173">단일 매트릭스의 가장 중요 한 속성은 벡터의 표준을 유지 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-173">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="ef562-174">이는 다음과 같은 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-174">This happens because</span></span> 

<span data-ttu-id="ef562-175">$ $ \langle v, v \rangle = v ^ \aav = v ^ \langle U ^ {-1 } U v = v ^ \aau ^ \aau v = \laru v, U v \rangle . $ $</span><span class="sxs-lookup"><span data-stu-id="ef562-175">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="ef562-176">$$M = M ^ [*\dagger*](https://en.wikipedia.org/wiki/Hermitian_matrix) 인 경우 행렬 $M는 라고 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-176">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="ef562-177">마지막으로 크기가 $m n 인 두 $M 행렬의 [*텐서 product*](https://en.wikipedia.org/wiki/Tensor_product) (또는 Kronecker product) $ \times $ $N와 크기 $ $p \times q는 크기가 $ 더 큰 행렬 $P = M n n a M e \otimes $ nq, $mp $ 에서 얻은 것 이며 다음과 같이 $M에서 가져옵니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="ef562-177">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

<span data-ttu-id="ef562-178">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="ef562-178">\begin{align}</span></span>
    <span data-ttu-id="ef562-179">M \otimes N &= \otimesbmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-179">M \otimes N &= \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-180">M_ {11 } ~ ~ \cdots ~ ~ M_ {1n } \\ \\ \cdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-180">M_{11} ~~ \cdots ~~ M_{1n} \\\\ \ddots\\\\</span></span>
        <span data-ttu-id="ef562-181">M_ {m1 } ~ ~ \cdots ~ ~ M_ {mn}</span><span class="sxs-lookup"><span data-stu-id="ef562-181">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    <span data-ttu-id="ef562-182">종단bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-182">\end{bmatrix}</span></span>
    <span data-ttu-id="ef562-183">\otimes \otimesbmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-183">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-184">N_ {11 } ~ ~ \cdots ~ ~ N_ {1q } \\ \\ \cdots\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-184">N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="ef562-185">N_ {p1 } ~ ~ \csti~ ~ N_ {pq}</span><span class="sxs-lookup"><span data-stu-id="ef562-185">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    <span data-ttu-id="ef562-186">\end{ bmatrix } \\ \\ &= \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-186">\end{bmatrix}\\\\ &= \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-187">M_ { } 11\begin{ bmatrix } N_ {11 } ~ ~ \cststii~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{ bmatrix } ~ ~ \cf~ ~ M_ {1q } \begin{ bmatrix } N_ {11 } ~ ~ \begin{~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{ bmatrix } \\ \\ \begin{\\\\</span><span class="sxs-lookup"><span data-stu-id="ef562-187">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="ef562-188">M_ {m1 } \begin{ bmatrix } N_ {11 } ~ ~ \begin{~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{ bmatrix } ~ \begin{점 ~ ~ M_ {mn } \begin{ bmatrix } N_ {11 } ~ ~ \begin{~ ~ N_ {1q } \\ \\ \begin{ \\\\ N_ {p1 } ~ ~ \begin{~ ~ N_ {pq } \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-188">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="ef562-189">\end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="ef562-189">\end{bmatrix}.</span></span>
<span data-ttu-id="ef562-190">\end{align}</span><span class="sxs-lookup"><span data-stu-id="ef562-190">\end{align}</span></span>

<span data-ttu-id="ef562-191">몇 가지 예제를 통해이를 보다 잘 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-191">This is better demonstrated with some examples:</span></span>

<span data-ttu-id="ef562-192">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-192">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-193">a \\ \\ b \end{ bmatrix } \end{\end{ bmatrix } c \\ \\ d \\ \\ e \end{ bmatrix } = \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-193">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-194">a \begin{ bmatrix } c \\ \\ d \\ \\ e \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-194">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="ef562-195">\\\\[1.5 em] b \begin{ bmatrix } c \\ \\ d \\ \\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-195">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    <span data-ttu-id="ef562-196">종단bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-196">\end{bmatrix}</span></span>
    <span data-ttu-id="ef562-197">= \begin{ bmatrix } a c a \\ \\ d \\ \\ a e \\ \\ b c \\ \\ b d \\ \\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-197">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="ef562-198">및</span><span class="sxs-lookup"><span data-stu-id="ef562-198">and</span></span>

<span data-ttu-id="ef562-199">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-199">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-200">a \ b \\ \\ c \ d \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-200">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    <span data-ttu-id="ef562-201">\otimes \otimesbmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-201">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="ef562-202">e \ f \\ \\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-202">e\ f\\\\g\ h \end{bmatrix}</span></span>
     <span data-ttu-id="ef562-203">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-203">= \begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-204">은\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-204">a\begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-205">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-205">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="ef562-206">b\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-206">b\begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-207">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-207">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="ef562-208">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-208">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-209">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-209">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="ef562-210">2\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-210">d\begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-211">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-211">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="ef562-212">종단bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-212">\end{bmatrix}</span></span>
    <span data-ttu-id="ef562-213">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ef562-213">= \begin{bmatrix}</span></span>
    <span data-ttu-id="ef562-214">ae \ n a m e \ n a m e \ i n \ \\ \\ bg \ bh \\ \\ w\ f\ de \ df \\ \\ cg \ ch \ bmatrix }</span><span class="sxs-lookup"><span data-stu-id="ef562-214">ae\ af\ be\ bf \\\\ ag\ ah\ bg\ bh \\\\ ce\ cf\ de\ df \\\\ cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="ef562-215">텐서 제품에 대 한 최종 유용한 표기법 밑수 규칙은 모든 벡터 $v $ 또는 행렬 $v $M에 대해 $ ^ {\otimes n } $ 또는 $M ^ {\otimes n } $은 $n $ 접기 반복 텐서 제품에 대 한 짧은 손입니다.</span><span class="sxs-lookup"><span data-stu-id="ef562-215">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="ef562-216">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ef562-216">For example:</span></span>

<span data-ttu-id="ef562-217">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="ef562-217">\begin{align}</span></span>
<span data-ttu-id="ef562-218">& \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } ^ {\begin{1 } = \begin{1 0 \begin{, bmatrix } \\ \\ bmatrix } \qquad \begin{bmatrix} 1 \\ \\ 0\end{ bmatrix } ^ {\begin{2 } = \begin{ bmatrix } 1 \\ \\ 0 0 \\ \\ \\ \\ 0 \begin{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ -1 \begin{ bmatrix } ^ {\begin{2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \begin{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 1 & 0 \begin{ bmatrix } ^ {\begin{1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \begin{ bmatrix } , \qquad \begin{bmatrix} 0 & 1 \\ \\ 1 0&& end{ bmatrix } ^ {\begin{2 } = \begin{ bmatrix } 0 &0&0 &1 0 \\ \\ \\ \\ \\\\ \end{bmatrix}&0&1 &0 0&1&0 &0&0&0 0</span><span class="sxs-lookup"><span data-stu-id="ef562-218">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ &\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}    0& 1 \\\\ 1& 0  \end{bmatrix},  \qquad\begin{bmatrix} 0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
<span data-ttu-id="ef562-219">\end{align}</span><span class="sxs-lookup"><span data-stu-id="ef562-219">\end{align}</span></span>
