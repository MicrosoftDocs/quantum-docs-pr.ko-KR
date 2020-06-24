---
title: Dirac 표기법
description: Diac 표기법을 사용 하 여 퀀텀 상태를 나타내고 퀀텀 작업을 시뮬레이트하는 방법에 대해 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.dirac
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
ms.openlocfilehash: f9dddfa25e9fd1e3d8aaf92b2e3b17c96ed8b72a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269509"
---
# <a name="dirac-notation"></a><span data-ttu-id="fbf55-103">기타 ac 표기법</span><span class="sxs-lookup"><span data-stu-id="fbf55-103">Dirac Notation</span></span>

<span data-ttu-id="fbf55-104">열 벡터 표기법이 선형 대 수에서 사용 되는 반면 특히 여러 비트를 처리할 때 특히 양자를 계산 하는 것은 복잡 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-104">While column vector notation is ubiquitous in linear algebra, it is often cumbersome in quantum computing especially when dealing with multiple qubits.</span></span>  <span data-ttu-id="fbf55-105">예를 들어 $ \psi $ 를 벡터로 정의 하면 $ \psi $ 가 행 또는 열 벡터 인지 여부를 명시적으로 명확 하 게 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-105">For example, when we define $\psi$ to be a vector it is not explicitly clear whether $\psi$ is a row or a column vector.</span></span>  <span data-ttu-id="fbf55-106">따라서 $ $ \\a및 $ \phi가 벡터 인 경우 $ \\\\a\psi $ $ 의 셰이프가 $ $ 컨텍스트에서 명확 하지 않을 수 있기 때문에 $ \\a\psi가 정의 된 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-106">Thus if $\phi$ and $\psi$ are vectors then it is equally unclear if $\phi \psi$ is even defined because the shapes of $\phi$ and $\psi$ may be unclear in the context.</span></span>  <span data-ttu-id="fbf55-107">벡터의 모양에 대 한 모호성 외에도 앞에서 소개한 선형 대 수 표기법을 사용 하 여 간단한 벡터를 표현 하는 것은 매우 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-107">Beyond the ambiguity about the shapes of vectors, expressing even simple vectors using the linear algebraic notation introduced earlier can be very cumbersome.</span></span> <span data-ttu-id="fbf55-108">예를 들어, $ 각가 값 $0를 사용 하는 $n-고 비트 상태를 설명 하려는 경우 $ 다음과 같이 공식적으로 상태를 표현 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-108">For example, if we wish to describe an $n$-qubit state where each qubit takes the value $0$ then we would formally express the state as</span></span> 

<span data-ttu-id="fbf55-109">$ $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } \begin{\cst\otimes \begin { bmatrix } 1 \\ \\ 0\end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-109">$$\begin{bmatrix}1 \\\\  0 \end{bmatrix}\otimes \cdots \otimes\begin{bmatrix}1 \\\\  0 \end{bmatrix}.</span></span> $$  

<span data-ttu-id="fbf55-110">이 텐서 제품을 평가 하는 과정은 벡터가 매우 많은 공간에 있기 때문에 실용적이 지 않으므로이 표기법이 이전 표기법을 사용 하 여 제공할 수 있는 상태에 대 한 최상의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-110">Of course evaluating this tensor product is impractical because the vector lies in an exponentially large space and so this notation is in fact the best description of the state that can be given using the previous notation.</span></span>  

<span data-ttu-id="fbf55-111">[*Diac 표기법*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) 은 퀀텀 메커니즘의 정확한 요구에 맞게 새로운 언어를 제공 하 여 이러한 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-111">[*Dirac notation*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) solves these issues by presenting a new language to fit the precise needs of quantum mechanics.</span></span>  <span data-ttu-id="fbf55-112">이러한 이유로 독자는이 섹션의 예제를 퀀텀 상태를 설명 하는 방법의 고정 prescription 하는 것이 좋지만 퀀텀 아이디어를 간결 하 게 표현 하는 데 사용할 수 있는 제안 사항으로이를 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-112">For this reason, we recommend the reader not view the examples in this section as a rigid prescription of how to describe quantum states, but rather encourage the reader to view these as suggestions that can be used to concisely express quantum ideas.</span></span>

<span data-ttu-id="fbf55-113">단일 Ac 표기법에는 두 가지 유형의 벡터가 있습니다. *bra* vector와 *k* vector는 함께 배치 될 때 *braket* 또는 inner 곱을 형성 하기 때문에 이름이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-113">There are two types of vectors in Dirac notation: the *bra* vector and the *ket* vector, so named because when put together they form a *braket* or inner product.</span></span>  <span data-ttu-id="fbf55-114">$ \Psi $ 가 열 벡터 인 경우 $ \ket \psi $로 서는 Nac 표기법으로 작성할 수 있습니다. { } 여기서 $ \ket { \cdot } $는 단위 열 벡터 (즉, *k* vector) 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-114">If $\psi$ is a column vector then we can write it in Dirac notation as $\ket{\psi}$, where the $\ket{\cdot}$ denotes that it is a unit column vector, i.e., a *ket* vector.</span></span>  <span data-ttu-id="fbf55-115">마찬가지로, $ \psi ^ \psi 행은 $ $ { \psi $로 표시 됩니다 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-115">Similarly, the row vector $\psi^\dagger$ is expressed as $\bra{\psi}$.</span></span> <span data-ttu-id="fbf55-116">즉, $ \psi ^ \atea는 $ $ \psi의 요소에 대 한 초급 복합 활용 적용 하 여 가져옵니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-116">In other words, $\psi^\dagger$ is obtained by applying entry-wise complex conjugation to the elements of the transpose of $\psi$.</span></span> <span data-ttu-id="fbf55-117">Bra-k notation은 $ \braket { \psi | \psi } $가 $ 정의 $1에 따라 자체와 vector $ \psi의 내부 곱 $ 임을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-117">The bra-ket notation directly implies that $\braket{\psi|\psi}$ is the inner product of vector $\psi$ with itself, which is by definition $1$.</span></span>  

<span data-ttu-id="fbf55-118">더 일반적으로 $ \psi $ 및 $ $ \sis가 퀀텀 상태 벡터 인 경우 해당 내부 제품은 $ \braket { \\a\psi $로, $ | } \ket { \psi } $를 $ \ket \\a$로 측정할 확률은 $ { } | \braket { \\a\psi | } | ^ 2 $ 입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-118">More generally, if $\psi$ and $\phi$ are quantum state vectors their inner product is $\braket{\phi|\psi}$ which implies that the probability of measuring the state $\ket{\psi}$ to be $\ket{\phi}$ is $|\braket{\phi|\psi}|^2$.</span></span>  

<span data-ttu-id="fbf55-119">다음 규칙은 0과 1의 값을 인코딩하는 퀀텀 상태를 설명 하는 데 사용 됩니다 (단일 값 비트 계산 기준 상태).</span><span class="sxs-lookup"><span data-stu-id="fbf55-119">The following convention is used to describe the quantum states that encode the values of zero and one (the single-qubit computational basis states):</span></span>

<span data-ttu-id="fbf55-120">$ $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } = \ket{0 } , \qquad \begin{ bmatrix } 0 \\ \\ 1 \begin{ bmatrix } = \ket{1 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-120">$$ \begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \ket{0},\qquad \begin{bmatrix} 0 \\\\  1 \end{bmatrix} = \ket{1}.</span></span>
$$

### <a name="example-representing-the-hadamard-operation-with-dirac-notation"></a><span data-ttu-id="fbf55-121">예:가 중 Ac 표기법으로 Hadamard 작업 표현</span><span class="sxs-lookup"><span data-stu-id="fbf55-121">Example: representing the Hadamard operation with Dirac notation</span></span>

<span data-ttu-id="fbf55-122">다음 표기법은 Hadamard gate를 $ \ket{0 $ 및 $ \ket{1 $에 적용 하 여 발생 하는 상태를 설명 하는 데 주로 사용 됩니다 .이는 $ } } + x 및 $-x의 단위 벡터에 해당 하는 $ $ Bloch 구의 방향입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-122">The following notation is often used to describe the states that result from applying the Hadamard gate to $\ket{0}$ and $\ket{1}$ (which correspond to the unit vectors in the $+x$ and $-x$ directions on the Bloch sphere):</span></span>

<span data-ttu-id="fbf55-123">$ $ \frac{1 } {\sqrt{2 } } \begin{ bmatrix } 1 \\ \\ 1 \end{ bmatrix } = h \ket {0 } = \ket { +}, \qquad \frac{1 } {\sqrt{2 } } \begin{ bmatrix } 1 \\ \\ -1 \end{ bmatrix } = h \ket {1 } = \ket { -}.</span><span class="sxs-lookup"><span data-stu-id="fbf55-123">$$ \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=H\ket{0} = \ket{+},\qquad \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  -1 \end{bmatrix} =H\ket{1} = \ket{-} .</span></span>
$$

<span data-ttu-id="fbf55-124">이러한 상태를 $ \ket{0 } $ 및 $ \ket{1 $의 합으로 사용 하 여 확장할 수도 있습니다 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-124">These states can also be expanded using Dirac notation as sums of $\ket{0}$ and $\ket{1}$:</span></span>

<span data-ttu-id="fbf55-125">$ $ \ket { +} = \frac{1 } {\sqrt{2 } } (\ket{0 } + \ket{1 } ), \qquad \ket { -} = \frac{1 } {\sqrt{2 } } (\ket{0 } -\ket{1 } ).</span><span class="sxs-lookup"><span data-stu-id="fbf55-125">$$ \ket{+} = \frac{1}{\sqrt{2}}(\ket{0} + \ket{1}),\qquad \ket{-} = \frac{1}{\sqrt{2}}(\ket{0} - \ket{1}).</span></span>
$$

### <a name="computational-basis-vectors"></a><span data-ttu-id="fbf55-126">계산 기준 벡터</span><span class="sxs-lookup"><span data-stu-id="fbf55-126">Computational basis vectors</span></span>
<span data-ttu-id="fbf55-127">이러한 상태를 종종 *계산 기준*이라고 하는 이유를 보여 줍니다. 모든 퀀텀 상태는 항상 계산 기준 벡터의 합계로 표현 될 수 있으며 이러한 합계는 기타 ac 표기법을 사용 하 여 쉽게 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-127">This demonstrates why these states are often called a *computational basis*: every quantum state can always be expressed as sums of computational basis vectors and such sums are easily expressed using Dirac notation.</span></span>  <span data-ttu-id="fbf55-128">또한 상태 $ \ket { +} $ 및 $ \ket { -} $는 퀀텀 상태에 대 한 기반을 형성 한다는 것에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-128">The converse is also true in that the states $\ket{+}$ and $\ket{-}$ also form a basis for quantum states.</span></span>  <span data-ttu-id="fbf55-129">이 사실을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-129">You can see this from the fact that</span></span>

<span data-ttu-id="fbf55-130">$ $ \ket{0 } = \frac{1 } {\sqrt{2 } } (\ket { +} + \ket { -}), \qquad \ket{1 } = \frac{1 } {\sqrt{2 } } (\ket { +}-\ket { -}).</span><span class="sxs-lookup"><span data-stu-id="fbf55-130">$$ \ket{0} = \frac{1}{\sqrt{2}}(\ket{+} + \ket{-}),\qquad \ket{1} = \frac{1}{\sqrt{2}}(\ket{+} - \ket{-}).</span></span>
$$

<span data-ttu-id="fbf55-131">나머지 Ac 표기법의 예로, } $0과 $1 사이의 내부 제품인 braket $ \braket{0 | 1 $을 고려 $ $ 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbf55-131">As an example of Dirac notation, consider the braket $\braket{0 | 1}$, which is the inner product between $0$ and $1$.</span></span>  <span data-ttu-id="fbf55-132">다음으로 작성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-132">It can be written as</span></span> 

<span data-ttu-id="fbf55-133">$ $ \braket{0 | 1 } = \begin{ bmatrix } 1 & 0 \begin{ bmatrix } \begin{ bmatrix } 0 \\\\ 1 \end{bmatrix} = 0. $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-133">$$\braket{0 | 1}=\begin{bmatrix} 1 & 0 \end{bmatrix}\begin{bmatrix}0\\\\ 1\end{bmatrix}=0.$$</span></span>

<span data-ttu-id="fbf55-134">$ \Ket{0 } $ 및 $ \ket{1 } $는 직교 벡터입니다. 즉, $ \braket{0 | 1 } = \braket{1 | 0 } = 0입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-134">This says that $\ket{0}$ and $\ket{1}$ are orthogonal vectors, meaning that $\braket{0 | 1} = \braket{1 | 0} =0$.</span></span>  <span data-ttu-id="fbf55-135">또한 정의 $ \braket{0 | 0 } = \braket{1 | 1 } = 1입니다 $ .이는 두 계산 기준 벡터를 *orthonormal*호출할 수도 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-135">Also by definition $\braket{0 | 0} = \braket{1 | 1}=1$, which means that the two computational basis vectors can also be called *orthonormal*.</span></span>
<span data-ttu-id="fbf55-136">이러한 orthonormal 속성은 다음 예제에서 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-136">These orthonormal properties will be useful in the following example.</span></span> <span data-ttu-id="fbf55-137">$ \Ket { \psi } = {\frac{3 } {5 } } \ket{1 } + {\frac{4 } {5 } } \ket{0 $가 있는 경우 } $ \braket{1 | 0 } = 0 이므로 $ 측정 $1의 확률은 $ 입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-137">If we have a state $\ket{\psi} = {\frac{3}{5}} \ket{1} + {\frac{4}{5}} \ket{0}$ then because $\braket{1 | 0} =0$ the probability of measuring $1$  is</span></span>  

<span data-ttu-id="fbf55-138">$ $ \big | \braket{1 | \big } \big | ^ 2 = \big | \frac{3 } {5 } \braket{1 | 1 } + \frac{4 } {5 } \braket{1 | 0 } \big | ^ 2 = \frac{9 } {25 } . $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-138">$$\big|\braket{1 | \psi}\big|^2= \left|\frac{3}{5}\braket{1 | 1} +\frac{4}{5}\braket{1 | 0}\right|^2=\frac{9}{25}.$$</span></span> 

### <a name="tensor-product-notation"></a><span data-ttu-id="fbf55-139">텐서 product 표기법</span><span class="sxs-lookup"><span data-stu-id="fbf55-139">Tensor product notation</span></span>
<span data-ttu-id="fbf55-140">또한 내부에는 암시적인 텐서 product 구조가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-140">Dirac notation also includes an implicit tensor product structure within it.</span></span>  <span data-ttu-id="fbf55-141">이는 퀀텀 컴퓨팅에서 두 개의 상관 관계가 없는 퀀텀 레지스터에 설명 된 상태 벡터가 두 상태 벡터의 텐서 제품 이기 때문에 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-141">This is important because in quantum computing, the state vector described by two uncorrelated quantum registers is the tensor products of the two state vectors.</span></span>  <span data-ttu-id="fbf55-142">퀀텀 계산을 설명 하려면 텐서 제품 구조를 간결 하 게 설명 하거나 그에 대 한 이해가 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-142">Concisely describing the tensor product structure, or lack thereof, is vital if you want to explain a quantum computation.</span></span>  <span data-ttu-id="fbf55-143">텐서 product 구조는 $ 두 개의 퀀텀 상태 벡터 $ \psi $ 및 $ \bnn\\an\\an\\\ann $로 $ \ket \psi $ { } { } \otimes \ket \an$로 명시적으로 작성 된 경우와 { } { } 벡터 사이에서 $ \otime을 작성 하는 규칙이 $ 필요 하지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-143">The tensor product structure implies that we can write $\psi \otimes \phi$ for any two quantum state vectors $\phi$ and $\psi$ as $\ket{\psi} \ket{\phi}$, sometimes explicitly written as $\ket{\psi} \otimes \ket{\phi}$, however by convention writing $\otimes$ in between the vectors is unnecessary.</span></span>  <span data-ttu-id="fbf55-144">예를 들어 0 상태로 초기화 된 두 개의 상태를 제공 하는 상태는</span><span class="sxs-lookup"><span data-stu-id="fbf55-144">For example, the state with two qubits initialized to the zero state is given by</span></span>

<span data-ttu-id="fbf55-145">$ $ \begin{ bmatrix } 1 0 0 0 \\ \\ \\ \\ \\ \\ \begin{ bmatrix } = \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } \begin{\begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } = \ket{0 } \begin{\ket{0 } = \ket{0 } \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-145">$$ \begin{bmatrix} 1 \\\\  0 \\\\  0 \\\\  0 \end{bmatrix}= \begin{bmatrix} 1 \\\\  0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \ket{0} \otimes \ket{0}= \ket{0} \ket{0}.</span></span>
$$

<span data-ttu-id="fbf55-146">마찬가지로 } 정수 $p에 대 한 상태 $ \ket{p $는 $ 정수 $p를 이진 표현으로 인코딩하는 퀀텀 상태를 나타냅니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-146">Similarly,  the state $\ket{p}$ for integer $p$ represents a quantum state that encodes in binary representation the integer $p$.</span></span>  <span data-ttu-id="fbf55-147">예를 들어, $ 부호 없는 이진 인코딩을 사용 하 여 숫자 $5을 표현 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="fbf55-147">For example, if we wish to express the number $5$ using an unsigned binary encoding we could equally express it as</span></span>

<span data-ttu-id="fbf55-148">$ $ \ket{1 } \ket{0 } \ket{1 } = \ket{101 } = \ket{5 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-148">$$ \ket{1}\ket{0}\ket{1} = \ket{101} = \ket{5}.</span></span>
$$

<span data-ttu-id="fbf55-149">이 표기법 내에서 $ \ket{0 } $는 단일의 비트 상태를 참조할 필요는 없으며 이진 인코딩을 $0로 저장 하는 이상 *비트 레지스터* 입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-149">Within this notation $\ket{0}$ need not refer to a single-qubit state but rather a *qubit register* storing a binary encoding of $0$.</span></span>  <span data-ttu-id="fbf55-150">이러한 두 표기법 간의 차이점은 일반적으로 컨텍스트에서 명확 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-150">The differences between these two notations is usually clear from the context.</span></span>  <span data-ttu-id="fbf55-151">이 규칙은 다음 중 한 가지 방법으로 작성할 수 있는 첫 번째 예제를 간소화 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-151">This convention is useful for simplifying the first example which can be written in any of the following ways:</span></span>

<span data-ttu-id="fbf55-152">$ $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } \begin{\cst\otimes \begin { bmatrix } 1 \\ \\ 0 \end{ bmatrix } = \ket{0 } \begin{\cst\otimes \ket{0 } = | 0 \cdots 0 \rangle = \ket{0 } ^ {\begin{n } = \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-152">$$ \begin{bmatrix}1 \\\\  0 \end{bmatrix}\otimes \cdots \otimes\begin{bmatrix}1 \\\\  0 \end{bmatrix} = \ket{0} \otimes \cdots \otimes \ket{0}= |0\cdots 0\rangle = \ket{0}^{\otimes n} = \ket{0}.</span></span>
$$

### <a name="example-describing-superposition-with-dirac-notation"></a><span data-ttu-id="fbf55-153">예:가 중 Ac 표기법을 사용 하 여 superposition 설명</span><span class="sxs-lookup"><span data-stu-id="fbf55-153">Example: Describing superposition with Dirac notation</span></span>
<span data-ttu-id="fbf55-154">Diac 표기법을 사용 하 여 퀀텀 상태를 설명 하는 방법에 대 한 또 다른 예로, 가능한 모든 비트 문자열 길이에 비해 동일한 superposition 퀀텀 상태를 작성 하는 다음과 같은 방법을 고려 하십시오 $n$</span><span class="sxs-lookup"><span data-stu-id="fbf55-154">As another example of how you can use Dirac notation to describe a quantum state, consider the following equivalent ways of writing a quantum state that is an equal superposition over every possible bit string of length $n$</span></span>

<span data-ttu-id="fbf55-155">$ $ H ^ {\otimes n } \ket{0 } = \frac{1 } {2 ^ {n/2 } } \ sum_ {j = 0 } ^ {2 ^ n-1 } \ket{j } = \ket { +} ^ {\otimes n } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-155">$$ H^{\otimes n} \ket{0} = \frac{1}{2^{n/2}} \sum_{j=0}^{2^n-1} \ket{j} = \ket{+}^{\otimes n}.</span></span>
$$

<span data-ttu-id="fbf55-156">여기에서 $n 비트의 합계가 $0에서 $ $2 ^ {n-1로 이동 하는 이유를 궁금할 수 있습니다 } $ $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-156">Here you may wonder why the sum goes from $0$ to $2^{n}-1$ for $n$ bits.</span></span>  <span data-ttu-id="fbf55-157">먼저 } $n bits에서 수행할 수 있는 $2 ^ {n $ 구성이 다릅니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-157">First note that there are $2^{n}$ different configurations that $n$ bits can take.</span></span>  <span data-ttu-id="fbf55-158">한 비트에서 $2 값을 사용할 수 $ 있지만 두 비트에서 $4 값을 사용할 수 있다는 것을 확인 하 여이를 확인할 수 있습니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-158">You can see this by noting that one bit can take $2$ values but two bits can take $4$ values and so forth.</span></span> <span data-ttu-id="fbf55-159">일반적으로 $2 ^ n $ 다른 가능한 비트 문자열이 있지만 $1 1 = 2 ^ n-1에서 가장 큰 값을 인코딩한 것 이므로 \cdots $ 합계의 상한입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-159">In general, this means that there are $2^n$ different possible bit strings but the largest value encoded in any of them $1\cdots 1=2^n-1$ and hence it is the upper limit for the sum.</span></span>
<span data-ttu-id="fbf55-160">이 예에서 { $ \ket +} ^ {\otimes n = } \ket { +} $를 사용 하지 않았습니다 } .이 } } 표기법 밑수 규칙은 일반적으로 0으로 초기화 된 모든 비트와 함께 계산 기준 상태를 위해 예약 되기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-160">As a side note, in this example we did not use $\ket{+}^{\otimes n}=\ket{+}$ in analogy to $\ket{0}^{\otimes n} = \ket{0}$ because this notational convention is usually reserved for the computational basis state with every qubit initialized to zero.</span></span>  <span data-ttu-id="fbf55-161">이러한 규칙은이 경우에 유용 하지만 퀀텀 컴퓨팅 자료에서 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-161">While such a convention would be sensible in this case, it is not employed in the quantum computing literature.</span></span>

### <a name="expressing-linearity-with-dirac-notation"></a><span data-ttu-id="fbf55-162">Diac 표기법으로 선형 표현</span><span class="sxs-lookup"><span data-stu-id="fbf55-162">Expressing linearity with Dirac notation</span></span>
<span data-ttu-id="fbf55-163">뛰어난 Ac 표기법의 또 다른 유용한 기능은 선형 이라는 점입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-163">Another nice feature of Dirac notation is the fact that it is linear.</span></span>  <span data-ttu-id="fbf55-164">네 가지 퀀텀 상태 벡터에 대해 작성 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="fbf55-164">If we wish to write for any four quantum state vectors,</span></span> 

<span data-ttu-id="fbf55-165">$ $ (\alpha \ket { \alpha } + \ket { \\an\) } \otime (\alpha \ket { } \alpha + \alpha \ket { \000d } ) = \alpha \gamma \ket { \alpha } \ket { a\\ket } + \aa\\ket \alpha \alpha \delta { } { } \gamma \ket { } { } \delta \ket { } { } \00a\ a\ a\ \alpha \alpha \alpha $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-165">$$(\alpha \ket{\psi} +\beta\ket{\phi})\otimes (\gamma \ket{\chi} + \delta \ket{\omega})= \alpha\gamma \ket{\psi}\ket{\chi} + \alpha\delta \ket{\psi}\ket{\omega}+\beta\gamma\ket{\phi}\ket{\chi}+\beta\delta\ket{\phi}\ket{\omega}.$$</span></span>

<span data-ttu-id="fbf55-166">즉, 상태 벡터 사이에 텐서 제품을 가져오는 것이 일반적인 곱셈 처럼 종료 되도록 텐서 제품 표기법을 Diac 표기법으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-166">That is to say, you can distribute the tensor product notation in Dirac notation so that taking tensor products between state vectors ends up looking just like ordinary multiplication.</span></span>

<span data-ttu-id="fbf55-167">Bra 벡터는 비슷한 규칙에 따라 벡터를 k 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-167">Bra vectors follow a similar convention to ket vectors.</span></span>  <span data-ttu-id="fbf55-168">예를 들어 vector $ \bra { \psi } \bra { \\s$는 } 상태 vector $ \psi ^ \aa\otimes \psi ^ \aate( = \psi \aa\l \otimes ) ^ \psi와 동일 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="fbf55-168">For example, the vector $\bra{\psi}\bra{\phi}$ is equivalent to the state vector $\psi^\dagger \otimes \phi^\dagger=(\psi\otimes \phi)^\dagger$.</span></span> <span data-ttu-id="fbf55-169">K vector $ \ket { \psi } $가 $ \psi \ket{0 } + \psi \ket{1 $ 인 경우 } 벡터의 bra vector 버전은 $ \bra { \psi } = \ket { \psi } ^ \psi = (\bra{1 } \psi ^ \* + } \psi ^ \*) $입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-169">If the ket vector $\ket{\psi}$ is $\alpha \ket{0} + \beta \ket{1}$ then the bra vector version of the vector is $\bra{\psi}=\ket{\psi}^\dagger = (\bra{0}\alpha^\* +\bra{1}\beta^\*)$.</span></span>

<span data-ttu-id="fbf55-170">예를 들어 상태를 { } } } } } } } 측정 하기 위한 퀀텀 프로그램을 $ \ket{0 { +} $ 또는 $ \ket { -} $로 사용 하 여 $ \ket \psi = \frac{3 {5 \ket{1 + \frac{4 {5 \ket $ 상태를 측정 하는 확률을 계산 하고자 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-170">As an example, imagine that we wish to calculate the probability of measuring the state $\ket{\psi} = \frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}$ using a quantum program for measuring states to be either $\ket{+}$ or $\ket{-}$.</span></span> <span data-ttu-id="fbf55-171">그런 다음 장치가 상태를 $ \ket { -} $로 출력할 확률은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-171">Then the probability that the device would output that the state is $\ket{-}$ is</span></span> 

<span data-ttu-id="fbf55-172">$ $ | \braket { -| \psi } | ^ 2 = \psi | \frac{1 } {\sqrt{2 } } (\bra{0 } -\bra{1 } ) (\frac{3 } {5 } \ket{1 } + \frac{4 } {5 } \ket{0 } ) \psi | ^ 2 = \psi | -\frac{3 } {5 \sqrt {2 } } + \frac{4 } {5 \sqrt {2 } } \psi | ^ 2 = \frac{1 } {50 } . $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-172">$$|\braket{- | \psi}|^2= \left|\frac{1}{\sqrt{2}}(\bra{0} - \bra{1})(\frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}) \right|^2=\left|-\frac{3}{5\sqrt{2}} + \frac{4}{5\sqrt{2}}\right|^2=\frac{1}{50}.$$</span></span>

<span data-ttu-id="fbf55-173">확률을 계산 하는 데 음수 기호가 표시 되는 사실은 퀀텀 간섭의 노력입니다 .이는 퀀텀 컴퓨팅이 기존 컴퓨팅 보다 이점을 얻는 메커니즘 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-173">The fact that the negative sign appears in the calculation of the probability is a manifestation of quantum interference, which is one of the mechanisms by which quantum computing gains advantages over classical computing.</span></span>

## <a name="ketbra-or-outer-product"></a><span data-ttu-id="fbf55-174">ketbra 또는 외부 제품</span><span class="sxs-lookup"><span data-stu-id="fbf55-174">ketbra or outer product</span></span>
<span data-ttu-id="fbf55-175">마지막 항목은 *ketbra* 또는 외부 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-175">The final item worth discussing in Dirac notation is the *ketbra* or outer product.</span></span>  <span data-ttu-id="fbf55-176">외부 제품은 Uac 표기법 내에서 $ \ket { \psi } \bra { \\an$로 표시 되 } 고 bras 및 kets가 brakets와 반대 순서로 발생 하기 때문에 ketbras 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-176">The outer product is represented within Dirac notations as $\ket{\psi} \bra{\phi}$, and sometimes called ketbras because the bras and kets occur in the opposite order as brakets.</span></span>  <span data-ttu-id="fbf55-177">외부 제품은 행렬 곱셈을 $ \ket { \psi } \bra { } \a= \psi \aa^ \aa> $ 퀀텀 상태 벡터 $ \psi $ 및 $ \bl에 대해 정의 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-177">The outer product is defined via matrix multiplication as $\ket{\psi} \bra{\phi} = \psi \phi^\dagger$ for quantum state vectors $\psi$ and $\phi$.</span></span>  <span data-ttu-id="fbf55-178">이 표기법의 가장 일반적인 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-178">The simplest, and arguably most common example of this notation, is</span></span>

<span data-ttu-id="fbf55-179">$ $ \ket{0 } \bra{0 } = \begin{ bmatrix } 1 \\\\ 0 \begin{ bmatrix } \begin{ bmatrix } 1&0 \begin{ bmatrix } = \begin{} bmatrix 1 &0 \\\\ 0 &0 \end{bmatrix} \qquad \ket{1 } \bra{1 } = \begin{} bmatrix 0 \\\\ 1 \begin{ bmatrix } \begin{} bmatrix 0&1 \begin{ bmatrix } = \begin{} 0 bmatrix &0 \\\\ 0 &1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="fbf55-179">$$ \ket{0} \bra{0} = \begin{bmatrix}1\\\\ 0 \end{bmatrix}\begin{bmatrix}1&0 \end{bmatrix}= \begin{bmatrix}1 &0\\\\ 0 &0\end{bmatrix} \qquad \ket{1} \bra{1} = \begin{bmatrix}0\\\\ 1 \end{bmatrix}\begin{bmatrix}0&1 \end{bmatrix}= \begin{bmatrix}0 &0\\\\ 0 &1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="fbf55-180">Ketbras는 고정 값에 퀀텀 상태를 프로젝션 하기 때문에 종종 프로젝터 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-180">Ketbras are often called projectors because they project a quantum state onto a fixed value.</span></span>  <span data-ttu-id="fbf55-181">이러한 작업은 단일가 아니지만 벡터의 표준을 유지 하지 않으므로 퀀텀 컴퓨터에서 프로젝터를 명확 하 게 적용할 수 없다는 것이 놀라운 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-181">Since these operations are not unitary (and do not even preserve the norm of a vector), it should come as no surprise that a quantum computer cannot deterministically apply a projector.</span></span>  <span data-ttu-id="fbf55-182">그러나 프로젝터가 퀀텀 상태에 대해 측정 하는 작업을 설명 하는 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-182">However projectors do a beautiful job of describing the action that measurement has on a quantum state.</span></span>  <span data-ttu-id="fbf55-183">예를 들어 $ \ket { \psi $ 상태를 } $0로 측정 하는 경우 $ 결과 변환은 측정 결과로 발생 하는 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-183">For example, if we measure a state $\ket{\psi}$ to be $0$ then the resulting transformation that the state experiences as a result of the measurement is</span></span>

  <span data-ttu-id="fbf55-184">$ $ \ket { \psi } \rightarrow \frac { (\ket{0 } \bra{0 } ) \ket { \psi } } {| \braket{0 | \psi } |} = \ket{0 } , $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-184">$$\ket{\psi} \rightarrow \frac{(\ket{0} \bra{0})\ket{\psi}}{|\braket{0 | \psi}|}= \ket{0},$$</span></span>

<span data-ttu-id="fbf55-185">상태를 측정 하 고 $ \ket{0 $로 확인 하는 경우를 가정 } 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-185">as one expects if you were to measure the state and find it to be $\ket{0}$.</span></span>  <span data-ttu-id="fbf55-186">즉, 이러한 프로젝터는 퀀텀 컴퓨터의 상태에 따라 명확 하 게 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-186">To reiterate, such projectors cannot be applied on a state in a quantum computer deterministically.</span></span>  <span data-ttu-id="fbf55-187">대신, } 몇 가지 고정 확률로 표시 되는 $ \ket{0 $ 결과와 함께 임의로 임의로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-187">Instead, they can at best be applied randomly with the result $\ket{0}$ appearing with some fixed probability.</span></span>  <span data-ttu-id="fbf55-188">이러한 측정의 확률은 상태에서 퀀텀 프로젝터의 예상 값으로 작성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-188">The probability of such a measurement succeeding can be written as the expectation value of the quantum projector in the state</span></span>

<span data-ttu-id="fbf55-189">$ $ \bra { \psi } (\ket{0 } \bra{0 } ) \ket { \psi } = | \braket { \psi | 0 } | ^ 2, $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-189">$$ \bra{\psi} (\ket{0} \bra{0})\ket{\psi} = |\braket{\psi | 0}|^2, $$</span></span>

<span data-ttu-id="fbf55-190">이는 프로젝터가 측정 프로세스를 표현 하는 새로운 방법을 제공 한다는 것을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-190">which illustrates that projectors simply give a new way of expressing the measurement process.</span></span>

<span data-ttu-id="fbf55-191">대신, multi-factor bit 상태의 첫 번째 비트를 $1로 측정 하는 것을 고려 하는 경우에는 $ 이 프로세스를 프로젝터 및 기타 ac 표기법을 사용 하 여 편리 하 게 설명할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-191">If instead we consider measuring the first qubit of a multi-qubit state to be $1$ then we can also describe this process conveniently using projectors and Dirac notation:</span></span>

<span data-ttu-id="fbf55-192">$ $ P (\text{first stbit = 1 } ) = \bra { \cc\\ket{1 } } } \boldone ^ {\otimes n-1 } \right) \ket { \psi } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-192">$$ P(\text{first qubit = 1})= \bra{\psi}\left(\ket{1}\bra{1}\otimes \boldone^{\otimes n-1}\right) \ket{\psi}.</span></span>
$$

<span data-ttu-id="fbf55-193">여기에서 id 매트릭스는 다음과 같이 다른 것 처럼 편리 하 게 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-193">Here the identity matrix can be conveniently written in Dirac notation as</span></span>

<span data-ttu-id="fbf55-194">$ $ \boldone = \ket{0 } \bra{0 } + \ket{1 } \bra{1 } = \begin{ bmatrix } 1&0 \\\\ 0&1 \begin{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-194">$$ \boldone = \ket{0} \bra{0}+\ket{1} \bra{1}= \begin{bmatrix}1&0\\\\ 0&1 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="fbf55-195">다음과 같이 두 가지 비트가 있는 경우에는 프로젝터를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-195">For the case where there are two-qubits the projector can be expanded as</span></span> 

<span data-ttu-id="fbf55-196">$ $ \ket{1 } \bra{1 } \otimes \id = \ket{1 } \bra{1 } \otimes (\ket{0 } \bra{0 } + \ket{1 } \bra{1 } ) = \ket{10 } \bra{10 } + \ket{11 } \bra{11 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-196">$$ \ket{1} \bra{1} \otimes \id = \ket{1}\bra{1} \otimes (\ket{0} \bra{0}+\ket{1} \bra{1})= \ket{10}\bra{10} + \ket{11}\bra{11}.</span></span>
$$

<span data-ttu-id="fbf55-197">그러면 열 벡터 표기법을 사용 하 여 다중 기능에 대 한 측정 유사도에 대 한 논의와 일치 하는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-197">We can then see that this is consistent with the discussion about measurement likelihoods for multiqubit states using column-vector notation:</span></span>

<span data-ttu-id="fbf55-198">$ $ P (\text{first stbit = 1 } ) = \text{first \text{first (e \_ {10} e { \_ 10 } ^ \text{first e \_ {11} \_ {11 } ^ \text{first) \psi = | e \_ {10 } ^ \ara\psi | ^ 2 + | e \_ {11 } ^ \ara\psi ^ | 2, $ $</span><span class="sxs-lookup"><span data-stu-id="fbf55-198">$$ P(\text{first qubit = 1})= \psi^\dagger (e\_{10}e\_{10}^\dagger + e\_{11}e\_{11}^\dagger)\psi = |e\_{10}^\dagger \psi|^2 + |e\_{11}^\dagger \psi|^2, $$</span></span>

<span data-ttu-id="fbf55-199">이는 여러 기능을 비교 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-199">which matches the multi-qubit measurement discussion.</span></span>  <span data-ttu-id="fbf55-200">그러나이 결과의 일반화는 다중 기능 비트 사례에 대 한 일반화는 열 벡터 표기법 보다는 Diac 표기법을 사용 하는 것이 약간 더 간단 하며 이전 처리와 완전히 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-200">The generalization of this result to the multi-qubit case, however, is slightly more straightforward to express using Dirac notation than column-vector notation, and is entirely equivalent to the previous treatment.</span></span>

## <a name="density-operators"></a><span data-ttu-id="fbf55-201">밀도 연산자</span><span class="sxs-lookup"><span data-stu-id="fbf55-201">Density operators</span></span>

<span data-ttu-id="fbf55-202">다른 유용한 연산자는 *상태 연산자*라고도 하는 *밀도 연산자*를 사용 하 여 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-202">Another useful operator to express using Dirac notation is a *density operator*, sometimes also known as a *state operator*.</span></span>
<span data-ttu-id="fbf55-203">퀀텀 상태 벡터의 밀도 연산자는 $ \rho = \ket { \psi } \bra { \psi $ 형식으로 사용 합니다 } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-203">A density operator for a quantum state vector takes the form $\rho = \ket{\psi} \bra{\psi}$.</span></span>
<span data-ttu-id="fbf55-204">벡터 대신 행렬로 상태를 표시 하는 이러한 개념은 확률 계산을 표현 하는 편리한 방법을 제공 하 고 동일한 정해진 내에서 통계 불확실성과 퀀텀 불확실성을 모두 설명할 수 있으므로 편리 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-204">This concept of representing the state as a matrix, rather than a vector, is often convenient because it gives a convenient way of representing probability calculations, and also allows one to describe both statistical uncertainty as well as quantum uncertainty within the same formalism.</span></span>
<span data-ttu-id="fbf55-205">벡터 대신 일반 퀀텀 상태 연산자는 일부 퀀텀 컴퓨팅 영역에서 사용할 수 있지만 필드의 기본 사항을 이해 하는 데에는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-205">General quantum state operators, rather than vectors, are ubiquitous in some areas of quantum computing but are not necessary to understand the basics of the field.</span></span>
<span data-ttu-id="fbf55-206">관심이 있는 독자의 경우에서 제공 하는 참조 서적 중 하나를 참조 하 여 [자세한 내용을](xref:microsoft.quantum.more-information)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbf55-206">For the interested reader, we recommend reading one of the reference books provided in [For more information](xref:microsoft.quantum.more-information).</span></span>

## <a name="q-gate-sequences-equivalent-to-quantum-states"></a><span data-ttu-id="fbf55-207">Q # 퀀텀 상태와 동일한 게이트 시퀀스</span><span class="sxs-lookup"><span data-stu-id="fbf55-207">Q# gate sequences equivalent to quantum states</span></span>
<span data-ttu-id="fbf55-208">최종 지점에서 퀀텀 표기법 및 Q # 프로그래밍 언어를 발생 시킬 수 있습니다 .이 문서의 하기 시작 하면에서 퀀텀 상태는 퀀텀 컴퓨팅에서 정보의 기본적인 개체 라고 언급 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-208">A final point worth raising about quantum notation and the Q# programming language: at the onset of this document we mentioned that the quantum state is the fundamental object of information in quantum computing.</span></span>  <span data-ttu-id="fbf55-209">그러면 Q #에서 퀀텀 상태에 대 한 개념이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-209">It may then come as a surprise that in Q# there is no notion of a quantum state.</span></span>  <span data-ttu-id="fbf55-210">대신 모든 상태는이를 준비 하는 데 사용 되는 작업에 의해서만 설명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-210">Instead, all states are described only by the operations used to prepare them.</span></span>  <span data-ttu-id="fbf55-211">위의 예제는이에 대 한 훌륭한 그림입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-211">The previous example is an excellent illustration of this.</span></span>  <span data-ttu-id="fbf55-212">레지스터의 모든 퀀텀 비트 문자열에 대해 균일 한 superposition을 표현 하는 대신 ^ {\otimes n \ket{0 $ $H으로 결과를 나타낼 수 있습니다 } } .</span><span class="sxs-lookup"><span data-stu-id="fbf55-212">Rather than expressing a uniform superposition over every quantum bit string in a register, we can represent the result as $H^{\otimes n} \ket{0}$.</span></span>  <span data-ttu-id="fbf55-213">이에 대 한 이유를 일반적으로 수 있는 이점 뿐만 아니라이에 대 한 정보를 제공 하는 것은 매우 간단 하지만, 알고리즘을 구현 하기 위해 소프트웨어 스택을 통해 전파 해야 하는 작업도 간결 하 게 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-213">This exponentially shorter description of the state not only has the advantage that we can classically reason about it, but it also concisely defines the operations needed to be propagated through the software stack to implement the algorithm.</span></span>  <span data-ttu-id="fbf55-214">이러한 이유로 Q #은 퀀텀 상태 대신 게이트 시퀀스를 내보내도록 설계 되었습니다. 그러나 이론적 수준에서 두 큐브 뷰는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf55-214">For this reason, Q# is designed to emit gate sequences rather than quantum states; however, at a theoretical level the two perspectives are equivalent.</span></span>
