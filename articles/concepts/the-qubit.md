---
title: 퀀텀 컴퓨팅의 고 비트
description: 퀀텀 컴퓨팅의 기본 정보 단위인,이에 대해 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.qubit
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
ms.openlocfilehash: 833c9649b7fbcf8b9fde62c37246b9345fe59a92
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630348"
---
# <a name="the-qubit"></a><span data-ttu-id="aca60-103">고 비트</span><span class="sxs-lookup"><span data-stu-id="aca60-103">The Qubit</span></span>

<span data-ttu-id="aca60-104">Bits가 기존 컴퓨팅 정보에 대 한 기본 개체인 것 [*처럼, (*](https://en.wikipedia.org/wiki/Qubit) 양자 비트)는 퀀텀 컴퓨팅에서 정보의 기본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-104">Just as bits are the fundamental object of information in classical computing, [*qubits*](https://en.wikipedia.org/wiki/Qubit) (quantum bits) are the fundamental object of information in quantum computing.</span></span>  <span data-ttu-id="aca60-105">이러한 대응을 이해 하려면 가장 간단한 예 인 단일 기능을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-105">To understand this correspondence, let's look at the simplest example: a single qubit.</span></span>

## <a name="representing-a-qubit"></a><span data-ttu-id="aca60-106">고 비트를 나타내는</span><span class="sxs-lookup"><span data-stu-id="aca60-106">Representing a Qubit</span></span>

<span data-ttu-id="aca60-107">비트 또는 이진수의 값은 $0 또는 $1 일 수 있지만, $ 이 중 $ 하나는 값을 가질 수 있으며,이 값은 $0 및 $1의 퀀텀 superposition 수 있습니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-107">While a bit, or binary digit, can have value either $0$ or $1$, a qubit can have a value that is either of these or a quantum superposition of $0$ and $1$.</span></span>

<span data-ttu-id="aca60-108">단일 비트의 상태는 unit의 2 차원 열 벡터로 설명할 수 있습니다. 즉, 항목의 제곱 크기는 $1로 합산 되어야 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-108">The state of a single qubit can be described by a two-dimensional column vector of unit norm, that is, the magnitude squared of its entries must sum to $1$.</span></span> <span data-ttu-id="aca60-109">퀀텀 상태 벡터 라고 하는이 벡터는 단일 비트가 이진 변수의 상태를 설명 하는 데 필요한 모든 정보를 보유 하는 것 처럼 단일 수준으로 된 퀀텀 시스템을 설명 하는 데 필요한 모든 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-109">This vector, called the quantum state vector, holds all the information needed to describe the one-qubit quantum system just as a single bit holds all of the information needed to describe the state of a binary variable.</span></span>

<span data-ttu-id="aca60-110">일반 $1를 사용 하는 실수 또는 복소수의 모든 2 차원 열 벡터는 해당 하는 값이 있는 $ 퀀텀 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-110">Any two-dimensional column vector of real or complex numbers with norm $1$ represents a possible quantum state held by a qubit.</span></span> <span data-ttu-id="aca60-111">따라서 $ \begin{ bmatrix } \alpha \\ \\ \beta \begin{ bmatrix } $는 $ $ $ | \alpha | ^ 2 + | \beta | ^ 2 = 1을 만족 하는 복소수입니다. $ \alpha 및 $ \beta가 복소수 이면 stbit 상태를 나타냅니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-111">Thus $\begin{bmatrix} \alpha \\\\  \beta \end{bmatrix}$ represents a qubit state if $\alpha$ and $\beta$ are complex numbers satisfying $|\alpha|^2 + |\beta|^2 = 1$.</span></span> <span data-ttu-id="aca60-112">이를 나타내는 유효한 퀀텀 상태 벡터의 몇 가지 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-112">Some examples of valid quantum state vectors representing qubits include</span></span>

<span data-ttu-id="aca60-113">$ $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } , \begin{ bmatrix } 0 \\ \\ 1 \begin{ bmatrix } , \begin{ bmatrix } \frac{1 } {\sqrt{2 } } \\ \\ \frac{1 } {\sqrt{2 } } \begin{ bmatrix } , \begin{ bmatrix } \frac{1 } {\sqrt{2 } } \\ \\ \begin{ { -1 } {\sqrt{2 } } \begin{ bmatrix } , \ext { and} \begin{ bmatrix } \frac{1 } {\sqrt{2 } } \\ \\ \frac{i } {\sqrt{2 } } \begin{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="aca60-113">$$\begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \begin{bmatrix} 0 \\\\  1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{ and }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{i}{\sqrt{2}} \end{bmatrix}.$$</span></span>

<span data-ttu-id="aca60-114">퀀텀 상태 벡터 $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } $ 및 $ \begin{ bmatrix } 0 \\ \\ 1 \begin{ bmatrix } $는 특별 한 역할을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-114">The quantum state vectors $\begin{bmatrix} 1 \\\\  0 \end{bmatrix}$ and $\begin{bmatrix} 0 \\\\  1 \end{bmatrix}$ take a special role.</span></span> <span data-ttu-id="aca60-115">이러한 두 벡터는 원하는 비트의 상태를 설명 하는 벡터 공간에 대 한 기본을 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-115">These two vectors form a basis for the vector space that describes the qubit's state.</span></span> <span data-ttu-id="aca60-116">즉, 모든 퀀텀 상태 벡터는 이러한 기준 벡터의 합계로 작성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-116">This means that any quantum state vector can be written as a sum of these basis vectors.</span></span> <span data-ttu-id="aca60-117">특히 vector $ \begin{ bmatrix } x \\ \\ y \begin{$는 bmatrix } $x \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } + y \begin{ bmatrix } 0 \\ \\ 1\end{ bmatrix } $로 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-117">Specifically, the vector $\begin{bmatrix} x \\\\  y \end{bmatrix}$ can be written as $x \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} + y \begin{bmatrix} 0 \\\\  1 \end{bmatrix}$.</span></span> <span data-ttu-id="aca60-118">이러한 벡터의 회전은 원하는 비트에 대해 완벽 하 게 유효한 기본으로 사용 되는 반면,이를 *계산 기준*으로 호출 하 여이에 대 한 권한을 부여 하도록 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-118">While any rotation of these vectors would serve as a perfectly valid basis for the qubit, we choose to privilege this one, by calling it the *computational basis*.</span></span>

<span data-ttu-id="aca60-119">이러한 두 퀀텀 상태는 고전 비트의 두 가지 상태 즉, $0 $ 및 $1에 해당 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-119">We take these two quantum states to correspond to the two states of a classical bit, namely $0$ and $1$.</span></span> <span data-ttu-id="aca60-120">표준 규칙은 다음을 선택 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-120">The standard convention is to choose</span></span>

<span data-ttu-id="aca60-121">$ $0 \equiv \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } , \qquad 1 \equiv \begin{ bmatrix } 0 \\ \\ 1 \begin{ bmatrix } , $ $</span><span class="sxs-lookup"><span data-stu-id="aca60-121">$$0\equiv \begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \qquad 1 \equiv \begin{bmatrix} 0 \\\\  1 \end{bmatrix},$$</span></span>

<span data-ttu-id="aca60-122">이와 반대로 선택 하는 것도 동일 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-122">although the opposite choice could equally well be taken.</span></span> <span data-ttu-id="aca60-123">따라서 가능한 단일 값 비트 퀀텀 상태 벡터의 수를 초과 하는 경우 두 가지만 클래식 비트의 상태에 해당 합니다. 다른 모든 퀀텀 상태는 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-123">Thus, out of the infinite number of possible single-qubit quantum state vectors, only two correspond to states of classical bits; all other quantum states do not.</span></span>

## <a name="measuring-a-qubit"></a><span data-ttu-id="aca60-124">고 비트 측정</span><span class="sxs-lookup"><span data-stu-id="aca60-124">Measuring a Qubit</span></span>

<span data-ttu-id="aca60-125">이제는 원하는 비트를 나타내는 방법을 배웠으므로 [*측정*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)개념에 대해 설명 하 여 이러한 상태에 대 한 몇 가지 intuition을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-125">Now that we know how to represent a qubit, we can gain some intuition for what these states represent by discussing the concept of [*measurement*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics).</span></span> <span data-ttu-id="aca60-126">측정값은 vbit에서 "찾는 중" 이라는 비공식적 아이디어에 해당 하며,이는 퀀텀 상태를 $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } $ 또는 $ \begin{ bmatrix } 0 \\ \\ 1 \begin{ bmatrix } $ 중 하나로 즉시 축소 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-126">A measurement corresponds to the informal idea of “looking” at a qubit, which immediately collapses the quantum state to one of the two classical states  $\begin{bmatrix} 1 \\\\  0 \end{bmatrix}$ or  $\begin{bmatrix} 0 \\\\  1 \end{bmatrix}$.</span></span> <span data-ttu-id="aca60-127">퀀텀 상태 vector $ \begin{ bmatrix } \alpha \\ \\ \\b\end{$에서 지정 하는 bmatrix } 것이 측정 되 면 $ 확률 $ | \alpha ^ 2를 사용 하 여 결과 $0을 얻고 | $ $ 확률 $ | \beta ^ 2를 사용 하 여 결과 $1을 얻습니다 | $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-127">When a qubit given by the quantum state vector  $\begin{bmatrix} \alpha \\\\  \beta \end{bmatrix}$ is measured, we obtain the outcome $0$ with probability $|\alpha|^2$ and the outcome $1$  with probability $|\beta|^2$.</span></span> <span data-ttu-id="aca60-128">결과 $0에서 $ ,의 새 상태는 $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } $;입니다. 결과 $1의 경우 $ 상태는 $ \begin{ bmatrix } 0 \\ \\ 1 \begin{ bmatrix } $입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-128">On outcome $0$, the qubit's new state is $\begin{bmatrix} 1 \\\\  0 \end{bmatrix}$; on outcome $1$ its state is $\begin{bmatrix} 0 \\\\  1 \end{bmatrix}$.</span></span> <span data-ttu-id="aca60-129">이러한 확률 $ 은 정규화 조건 $ | \alpha | ^ 2 + | \alpha ^ 2 = 1 때문에 $1까지 합산 | $ 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-129">Note that these probabilities sum up to $1$ because of the normalization condition $|\alpha|^2 + |\beta|^2 = 1$.</span></span>

<span data-ttu-id="aca60-130">또한 측정의 속성은 퀀텀 상태 벡터의 전체 부호가 관련이 없다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-130">The properties of measurement also mean that the overall sign of the quantum state vector is irrelevant.</span></span> <span data-ttu-id="aca60-131">벡터 부정은 $ \alpha \rightarrow-\alpha $ 및 $ \alpha \rightarrow-\alpha와 동일 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-131">Negating a vector is equivalent to $\alpha \rightarrow -\alpha$ and $\beta \rightarrow -\beta$.</span></span> <span data-ttu-id="aca60-132">$0 및 $1의 확률은 $ $ 조건의 제곱 크기에 따라 달라 지므로 이러한 기호를 삽입 해도 확률은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-132">Because the probability of measuring $0$ and $1$ depends on the magnitude squared of the terms, inserting such signs does not change the probabilities whatsoever.</span></span> <span data-ttu-id="aca60-133">이러한 단계를 일반적으로 [ \`\` *전역 단계*' '](https://en.wikipedia.org/wiki/Phase_factor) 이라고 하며, 보다 일반적으로는 } $ \phi 1이 아닌 ^ {\\s$ 형식으로 $e 수 있습니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-133">Such phases are commonly called [\`\`*global phases*''](https://en.wikipedia.org/wiki/Phase_factor) and more generally can be of the form $e^{i \phi}$ rather than just $\pm 1$.</span></span>

<span data-ttu-id="aca60-134">최종 중요 한 측정 속성은 모든 퀀텀 상태 벡터를 손상 시킬 필요는 없다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-134">A final important property of measurement is that it does not necessarily damage all quantum state vectors.</span></span> <span data-ttu-id="aca60-135">bmatrix } \\ \\ 클래식 상태 $0에 해당 하는 $ \begin{1 0 \begin{$ 상태에서이 상태를 측정 하는 경우 bmatrix } $ 이 상태를 측정 하면 항상 결과 $0이 생성 $ 되며 퀀텀 상태는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-135">If we start with a qubit in the state $\begin{bmatrix} 1 \\\\  0 \end{bmatrix}$, which corresponds to the classical state $0$, measuring this state will always yield the outcome $0$ and leave the quantum state unchanged.</span></span> <span data-ttu-id="aca60-136">이러한 점에서 기존 비트만 있는 경우 (즉, $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } $ 또는 $ \begin{ bmatrix } 0 \\ \\ 1 \begin{$ bmatrix } ), 측정은 시스템을 손상 시 키 지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-136">In this sense, if we only have classical bits (i.e., qubits that are either $\begin{bmatrix}1 \\\\  0 \end{bmatrix}$ or $\begin{bmatrix}0 \\\\  1 \end{bmatrix}$) then measurement does not damage the system.</span></span> <span data-ttu-id="aca60-137">즉, 기존 데이터를 복제 하 고 기존 컴퓨터에서 수행할 수 있는 것 처럼 퀀텀 컴퓨터에서 조작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-137">This means that we can replicate classical data and manipulate it on a quantum computer just as one could do on a classical computer.</span></span> <span data-ttu-id="aca60-138">그러나 두 상태에 정보를 한 번에 저장 하는 기능은 퀀텀 데이터 무제한 증가할을 복사 [하는 기능](https://en.wikipedia.org/wiki/No-cloning_theorem)에 대 한 가능한 일반적으로 및 추가 robs 컴퓨터를 초과 하는 퀀텀 컴퓨팅을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-138">The ability, however, to store information in both states at once is what elevates quantum computing beyond what is possible classically and further robs quantum computers of the ability to copy quantum data indiscriminately, see also [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem).</span></span>

## <a name="visualizing-qubits-and-transformations-using-the-bloch-sphere"></a><span data-ttu-id="aca60-139">Bloch 구를 사용 하 여 고 비트 및 변형 시각화</span><span class="sxs-lookup"><span data-stu-id="aca60-139">Visualizing Qubits and Transformations using the Bloch Sphere</span></span>

<span data-ttu-id="aca60-140">[*Bloch 구에*](https://en.wikipedia.org/wiki/Bloch_sphere) 표시를 사용 하 여 $3 $ D에도 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-140">Qubits may also be pictured in $3$D using the [*Bloch sphere*](https://en.wikipedia.org/wiki/Bloch_sphere) representation.</span></span>  <span data-ttu-id="aca60-141">Bloch 구는 단일 값 비트 퀀텀 상태 (2 차원 복합 벡터)를 3 차원 실제 값 벡터로 설명 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-141">The Bloch sphere gives a way of describing a single-qubit quantum state (which is a two-dimensional complex vector) as a three-dimensional real-valued vector.</span></span>  <span data-ttu-id="aca60-142">이는 단일 수준 비트 상태를 시각화 하 여 여러 번째 비트 상태를 이해 하는 데 중요 한 이유를 개발할 수 있도록 하는 것이 중요 합니다 (sadly Bloch 구 표현이 중단 됨).</span><span class="sxs-lookup"><span data-stu-id="aca60-142">This is important because it allows us to visualize single-qubit states and thereby develop reasoning that can be invaluable in understanding multi-qubit states (where sadly the Bloch sphere representation breaks down).</span></span>  <span data-ttu-id="aca60-143">Bloch 구는 다음과 같이 시각화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-143">The Bloch sphere can be visualized as follows:</span></span>

<!--- ![](.\media\bloch.svg){ width=50% } --->
<span data-ttu-id="aca60-144">![Bloch 구](~/media/concepts_bloch.png)</span><span class="sxs-lookup"><span data-stu-id="aca60-144">![Bloch sphere](~/media/concepts_bloch.png)</span></span>

<span data-ttu-id="aca60-145">이 다이어그램의 화살표는 퀀텀 상태 벡터가 가리키는 방향을 보여 주고 화살표의 각 변환은 카디 날 축 중 하나에 대 한 회전으로 간주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-145">The arrows in this diagram show the direction in which the quantum state vector is pointing and each transformation of the arrow can be thought of as a rotation about one of the cardinal axes.</span></span>
<span data-ttu-id="aca60-146">계산 시퀀스로 퀀텀 계산을 고려 하는 것은 강력한 intuition이 intuition를 사용 하 여 알고리즘을 설계 하 고 설명 하는 것이 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-146">While thinking about a quantum computation as a sequence of rotations is a powerful intuition, it is challenging to use this intuition to design and describe algorithms.</span></span> <span data-ttu-id="aca60-147">Q #에서는 이러한 회전을 설명 하는 언어를 제공 하 여이 문제를 완화 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-147">Q# alleviates this issue by providing a language for describing such rotations.</span></span>

## <a name="single-qubit-operations"></a><span data-ttu-id="aca60-148">단일 비트 작업</span><span class="sxs-lookup"><span data-stu-id="aca60-148">Single-Qubit Operations</span></span>

<span data-ttu-id="aca60-149">퀀텀 컴퓨터는 퀀텀 상태 벡터의 회전을 에뮬레이트할 수 있는 유니버설 퀀텀 게이트 집합을 적용 하 여 데이터를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-149">Quantum computers process data by applying a universal set of quantum gates that can emulate any rotation of the quantum state vector.</span></span>
<span data-ttu-id="aca60-150">이 보편성 개념은 입력 비트의 모든 변환이 유한 길이 회로를 사용 하 여 수행 될 수 있는 경우 게이트 집합이 유니버설로 간주 되는 기존 (즉, 일반) 컴퓨팅의 보편성 개념과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-150">This notion of universality is akin to the notion of universality for traditional (i.e., classical) computing where a gate set is considered to be universal if every transformation of the input bits can be performed using a finite length circuit.</span></span>
<span data-ttu-id="aca60-151">퀀텀 컴퓨팅에서 원하는 비트에 대해 수행할 수 있는 유효한 변환은 단일 변환 및 측정입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-151">In quantum computing, the valid transformations that we are allowed to perform on a qubit are unitary transformations and measurement.</span></span>
<span data-ttu-id="aca60-152">*Adjoint 작업* 또는 복소수 복소수는 퀀텀 변환을 반전 해야 하므로 퀀텀 컴퓨팅에 중요 한 중요 한 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-152">The *adjoint operation* or the complex conjugate transpose is of crucial importance to quantum computing because it is needed to invert quantum transformations.</span></span>
<span data-ttu-id="aca60-153">Q #은 게이트 시퀀스를 해당 adjoint로 자동으로 컴파일하는 메서드를 제공 하 여이를 반영 합니다. 그러면 프로그래머가 많은 경우에 코드를 직접 만들지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-153">Q# reflects this by providing methods to automatically compile gate sequences to their adjoint, which saves the programmer from having to hand code adjoints in many cases.</span></span> <span data-ttu-id="aca60-154">이에 대 한 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-154">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Adj { // Auto-generate the adjoint of the operation
    H(qubit);
}
```

<span data-ttu-id="aca60-155">이는 간단한 예제 이지만 ( <xref:microsoft.quantum.intrinsic.h> ) 작업은 자체 adjoint 이지만 보다 복잡 한 추가 비트 작업에 유용 하 게 사용할 수 있는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-155">Although this is a trivial example (as the <xref:microsoft.quantum.intrinsic.h[!OP.NO-LOC(> operation is self-adjoint), you can see how this becomes invaluable for more complicated qubit operations.</span></span>
<span data-ttu-id="aca60-156">자세한 내용은 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aca60-156">For more information, see [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

<span data-ttu-id="aca60-157">기존 컴퓨터에서 1 비트를 1 비트에 매핑하는 함수는 네 개만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-157">There are only four functions that map one bit to one bit on a classical computer.</span></span> <span data-ttu-id="aca60-158">이와 대조적으로 퀀텀 컴퓨터의 단일 비트에는 무한 한 수의 단일 변환만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-158">In contrast, there are an infinite number of unitary transformations on a single qubit on a quantum computer.</span></span> <span data-ttu-id="aca60-159">따라서 [*게이트*](https://en.wikipedia.org/wiki/Quantum_logic_gate)라는 한정 된 기본 퀀텀 작업 집합은 퀀텀 컴퓨팅에서 허용 되는 무한 한 단일 변환 집합을 정확 하 게 복제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-159">Therefore, no finite set of primitive quantum operations, called [*gates*](https://en.wikipedia.org/wiki/Quantum_logic_gate), can exactly replicate the infinite set of unitary transformations allowed in quantum computing.</span></span> <span data-ttu-id="aca60-160">즉, 기존 컴퓨터와는 달리 퀀텀 컴퓨터에서 한정 된 수의 게이트를 사용 하 여 가능한 모든 퀀텀 프로그램을 정확 하 게 구현할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-160">This means, unlike classical computing, it is impossible for a quantum computer to implement every possible quantum program exactly using a finite number of gates.</span></span> <span data-ttu-id="aca60-161">따라서 기존 컴퓨터와 동일한 의미로 퀀텀 컴퓨터를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-161">Thus quantum computers cannot be universal in the same sense of classical computers.</span></span> <span data-ttu-id="aca60-162">결과적으로, 게이트 집합이 퀀텀 컴퓨팅에 대 한 *유니버설* 이라는 것을 알게 되 면 실제로는 기존 컴퓨팅을 사용 하는 것 보다 약간 약한 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-162">As a result, when we say that a set of gates is *universal* for quantum computing we actually mean something slightly weaker than we mean with classical computing.</span></span>
<span data-ttu-id="aca60-163">보편성의 경우 퀀텀 컴퓨터는 유한 길이 게이트 시퀀스를 사용 하 여 유한 오류 내에서 모든 단일 행렬에만 *근사치* 를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-163">For universality, we require that a quantum computer only *approximate* every unitary matrix within a finite error using a finite length gate sequence.</span></span>
<span data-ttu-id="aca60-164">즉, 단일 변환을이 집합에서 게이트의 곱으로 대략적으로 작성할 수 있는 경우 게이트 집합이 범용 게이트 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-164">In other words, a set of gates is a universal gate set if any unitary transformation can be approximately written as a product of gates from this set.</span></span> <span data-ttu-id="aca60-165">지정 된 모든 오류에 대 한 자세한 내용을 보려면 게이트 집합에서 _ {1 } , G_ {2 } , \ldots, G_N $G 게이트가 존재 해야 합니다. $</span><span class="sxs-lookup"><span data-stu-id="aca60-165">We require that for any prescribed error bound, there exist gates $G_{1}, G_{2},\ldots, G_N$ from the gate set such that</span></span>

<span data-ttu-id="aca60-166">$ $ G_N G_ {N-1 } \cdots G_2 G_1 \Aau. $ $</span><span class="sxs-lookup"><span data-stu-id="aca60-166">$$ G_N G_{N-1} \cdots G_2 G_1 \approx U. $$</span></span>

<span data-ttu-id="aca60-167">행렬 곱셈에 대 한 규칙은이 시퀀스에서 첫 번째 게이트 연산을 오른쪽에서 왼쪽으로 곱하는 것 이기 때문에 _N $G $ 실제로는 퀀텀 상태 벡터에 마지막으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-167">Note that because the convention for matrix multiplication is to multiply from right to left the first gate operation in this sequence, $G_N$, is actually the last one applied to the quantum state vector.</span></span> <span data-ttu-id="aca60-168">보다 공식적으로, 이러한 게이트 집합은 모든 오류 허용 오차 $ \ec>0에 대해 $ $G _1, \l도트 G_N 있습니다 .이는 $ $G _N \llt G_1 $ 와 $U 사이의 거리가 $ 최대 $ \epsilon입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-168">More formally, we say that such a gate set is universal if for every error tolerance $\epsilon>0$ there exists $G_1,\ldots, G_N$ such that  the distance between $G_N\ldots G_1$ and $U$ is at most $\epsilon$.</span></span> <span data-ttu-id="aca60-169">이상적으로 $ $ \epsilon의이 거리에 도달 하는 데 필요한 $N 값은 $ 로그를 $1/\ 엡실론으로 조정 해야 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-169">Ideally the value of $N$ needed to reach this distance of $\epsilon$ should scale poly-logarithmically with $1/\epsilon$.</span></span>

<span data-ttu-id="aca60-170">이러한 범용 게이트 집합은 실제로 어떤 모습 인가요?</span><span class="sxs-lookup"><span data-stu-id="aca60-170">What does such a universal gate set look like in practice?</span></span>  <span data-ttu-id="aca60-171">단일 고 비트 게이트에 대 한 가장 간단한 이러한 범용 게이트 집합은 Hadamard gate $H $ 와 $T $ 게이트 ($ \ pi/8 gate 라고도 함 $ ) 라는 두 개의 게이트로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-171">The simplest such universal gate set for single-qubit gates consists of only two gates: the Hadamard gate $H$ and the so-called $T$-gate (also known as the $\pi/8$ gate):</span></span>

<span data-ttu-id="aca60-172">$ $ H = \frac{1 } {\sqrt{2 } } \begin{ bmatrix } 1 & 1 \\ \\ 1 &-1\end{ bmatrix } , \qquad T = \begin{ bmatrix } 1 & 0 \\ \\ 0 & e ^ {i \ pi/ } 4\end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="aca60-172">$$ H=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 & 1 \\\\  1 &-1  \end{bmatrix},\qquad T=\begin{bmatrix} 1 & 0 \\\\  0 & e^{i\pi/4} \end{bmatrix}.</span></span>
$$

<span data-ttu-id="aca60-173">그러나 퀀텀 오류 수정과 관련 된 실제적인 이유로, $H 및 $T를 사용 하 여 생성할 수 있는 보다 큰 게이트 집합을 고려 하는 것이 더 편리할 수 있습니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-173">However, for practical reasons related to quantum error correction it can be more convenient to consider a larger gate set, namely one that can be generated using $H$ and $T$.</span></span>
<span data-ttu-id="aca60-174">퀀텀 게이트를 두 가지 범주 (Clifford 게이트 및 $T 게이트)로 분류할 수 있습니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-174">We can classify the quantum gates into two categories: Clifford gates and the $T$-gate.</span></span>
<span data-ttu-id="aca60-175">이 하위 작업은 여러 퀀텀 오류 수정 체계에서 Clifford 게이트를 구현 하기 쉬우므로, 오류 tolerantly을 구현 하기 위한 작업 및 뛰어난 비트의 리소스를 거의 필요로 하지 않는 반면, Clifford 없는 게이트는 내결함성이 필요한 경우 비용이 많이 듭니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-175">This subdivision is useful because in many quantum error correction schemes the so-called Clifford gates are easy to implement, that is they require very few resources in terms of operations and qubits to implement fault tolerantly, whereas non-Clifford gates are quite costly when requiring fault tolerance.</span></span> <span data-ttu-id="aca60-176">[Q #에서 기본적으로 포함](xref:microsoft.quantum.libraries.standard.prelude)되는 단일가 비트 Clifford 게이트의 표준 집합은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-176">The standard set of single-qubit Clifford gates, [included by default in Q#](xref:microsoft.quantum.libraries.standard.prelude), include</span></span>

<span data-ttu-id="aca60-177">$ $ H = \frac{1 } {\sqrt{2 } } \begin{ bmatrix } 1 & 1 \\ \\ 1 &-1\end{ bmatrix } , \qquad S = \begin{ bmatrix } 1 & 0 \\ \\ 0 & i \end{ bmatrix } = T ^ 2, \qquad X = \begin{ bmatrix } 0 &1 \\ \\ 1 & 0 \end{ bmatrix } = HT ^ 4H, $ $</span><span class="sxs-lookup"><span data-stu-id="aca60-177">$$ H=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 & 1 \\\\  1 &-1  \end{bmatrix} ,\qquad S =\begin{bmatrix} 1 & 0 \\\\  0 & i \end{bmatrix}= T^2,\qquad X=\begin{bmatrix} 0 &1 \\\\  1& 0 \end{bmatrix}= HT^4H, $$</span></span>

<span data-ttu-id="aca60-178">$ $ Y = \begin{ bmatrix } 0 &-i \\ \\ & 0 \Begin{ bmatrix } = T ^ 2ht ^ 4 ht ^ 6, \qquad Z = \begin{ bmatrix } 1&0 \\\\ 0 & -1 \begin{ bmatrix } = t ^ 4입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-178">$$ Y = \begin{bmatrix} 0 & -i \\\\  i & 0 \end{bmatrix}=T^2HT^4  HT^6, \qquad Z=\begin{bmatrix}1&0\\\\ 0&-1 \end{bmatrix}=T^4.</span></span>
$$

<span data-ttu-id="aca60-179">여기에서 작업 $X $ , $Y $ 및 $Z는 $ 특히 자주 사용 되며 작성자 Wolfgang pauli 후에 [*pauli 연산자*](https://en.wikipedia.org/wiki/Pauli_matrices) 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-179">Here the operations $X$, $Y$ and $Z$ are used especially frequently and are named [*Pauli operators*](https://en.wikipedia.org/wiki/Pauli_matrices) after their creator Wolfgang Pauli.</span></span>
<span data-ttu-id="aca60-180">비 Clifford 게이트 ($T $ 게이트)와 함께 이러한 작업을 단일 비트의 모든 단일 변환에 대 한 근사치로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-180">Together with the non-Clifford gate (the $T$-gate), these operations can be composed to approximate any unitary transformation on a single qubit.</span></span>

<span data-ttu-id="aca60-181">이러한 작업, 해당 Bloch 구 표현 및 Q # 구현에 대 한 자세한 내용은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aca60-181">For more information on these operations, their Bloch sphere representations and Q# implementations, see [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions).</span></span>

<span data-ttu-id="aca60-182">이러한 기본 형식에서 단일 변환을 작성 하는 방법의 예로, 위의 Bloch 구에 나오는 세 가지 변환은 게이트 시퀀스 $ \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } \mapsHZH \begin{ bmatrix } 1 \\ \\ 0 \begin{ bmatrix } = \begin{ bmatrix } 0 \\ \\ 1 \begin{$에 해당 bmatrix } 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-182">As an example of how unitary transformations can be built from these primitives, the three transformations pictured in the Bloch spheres above correspond to the gate sequence $\begin{bmatrix} 1 \\\\  0 \end{bmatrix} \mapsto HZH \begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \begin{bmatrix} 0 \\\\  1 \end{bmatrix}$.</span></span>

<span data-ttu-id="aca60-183">이전에는 스택의 논리 수준에 대 한 작업을 설명 하는 데 가장 많이 사용 되는 기본 게이트가 구성 되어 있지만 (논리 수준을 퀀텀 알고리즘의 수준으로 생각), 함수 설명 수준에 가까운 작업과 같이 알고리즘 수준에서 더 작은 기본 작업을 고려 하는 것이 편리한 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-183">While the previous constitute the most popular primitive gates for describing operations on the logical level of the stack (think of the logical level as the level of the quantum algorithm), it is often convenient to consider less basic operations at the algorithmic level, for example operations closer to a function description level.</span></span> <span data-ttu-id="aca60-184">다행히 Q #에는 더 높은 수준의 unitaries을 구현 하는 데 사용할 수 있는 메서드도 있습니다 .이를 통해 Clifford 및 $T에 대 한 모든 것을 명시적으로 분해 하지 않고도 높은 수준의 알고리즘이 구현 될 수 있습니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-184">Fortunately, Q# also has methods available for implementing higher-level unitaries, which in turn allow high-level algorithms to be implemented without explicitly decomposing everything down to Clifford and $T$-gates.</span></span>

<span data-ttu-id="aca60-185">가장 간단한 이러한 기본 형식은 단일의 비트 회전입니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-185">The simplest such primitive is the single qubit-rotation.</span></span> <span data-ttu-id="aca60-186">일반적으로는 $R _x $ , $R _y $ 및 $R _z의 세 가지 단일 비트 회전이 고려 $ 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-186">Three single-qubit rotations are typically considered: $R_x$, $R_y$ and $R_z$.</span></span> <span data-ttu-id="aca60-187">예를 들어, 회전 $R _x (\theta) $의 동작을 시각화 하려면 예를 들어, Bloch 구의 $x 축 방향을 따라 오른쪽 엄지 단추를 가리키고 $ $ \ 테타/2 라디안의 각도를 사용 하 여 손으로 벡터를 회전 한다고 가정 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-187">To visualize the action of the rotation $R_x(\theta)$, for example, imagine pointing your right thumb along the direction of the $x$-axis of the Bloch sphere and rotating the vector with your hand through an angle of $\theta/2$ radians.</span></span> <span data-ttu-id="aca60-188">$2의 이러한 혼동 요인은 $ Bloch 구에 표시 될 때 직교 벡터가 $180 ^ \circ $ 떨어져 있지만 실제로는 실제로 $90 ^ \circ 각도를 분리 한다는 사실입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="aca60-188">This confusing factor of $2$ arises from the fact that orthogonal vectors are $180^\circ$ apart when plotted on the Bloch sphere, yet are actually $90^\circ$ degrees apart geometrically.</span></span> <span data-ttu-id="aca60-189">해당 하는 단일 매트릭스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-189">The corresponding unitary matrices are:</span></span>

<span data-ttu-id="aca60-190">\begin{align *} &R_z (\테타) = e ^ {-i\theta z/2 } = \begin{ bmatrix } e ^ {-i \ 테타/2 } & 0 \\\\ 0 & e ^ {i \ 테타/ } 2\end{ bmatrix } , \\ \\ &R_x (\테타) = e ^ {-i\theta x/2 } = HR_z (\테타) H = \begin{ bmatrix } \cos (\ 테타/2) &-i\theta (\ 테타/2)-i\theta (\ 테타/2) \\ \\ & \cos (\ 테타/2) \end{ bmatrix } , \\ \\ \테타 (&R_y (\테타) = e ^ {-i\theta y/2 } = SHR_z (\테타) HS ^ \begin{align \begin{\cos (\ 테타/2) &-\sin (\ 테타/2) \sin (\ 테타 bmatrix } \\ \\ /2) & \cos (\ 테타/2) \end{ bmatrix } .\end{align*}</span><span class="sxs-lookup"><span data-stu-id="aca60-190">\begin{align *} &R_z(\theta) = e^{-i\theta Z/2} = \begin{bmatrix} e^{-i\theta/2} & 0\\\\  0& e^{i\theta/2} \end{bmatrix}, \\\\ &R_x(\theta) = e^{-i\theta X/2} = HR_z(\theta)H = \begin{bmatrix} \cos(\theta/2) & -i\sin(\theta/2)\\\\  -i\sin(\theta/2) & \cos(\theta/2) \end{bmatrix}, \\\\ &R_y(\theta) = e^{-i\theta Y/2} = SHR_z(\theta)HS^\dagger = \begin{bmatrix} \cos(\theta/2) & -\sin(\theta/2)\\\\  \sin(\theta/2) & \cos(\theta/2) \end{bmatrix}. \end{align*}</span></span>

<span data-ttu-id="aca60-191">세 개의 회전을 함께 결합 하 여 세 개의 차원에서 임의의 회전을 수행할 수 있는 것 처럼 Bloch 구의 표현에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-191">Just as any three rotations can be combined together to perform an arbitrary rotation in three dimensions, it can be seen from the Bloch sphere representation that any unitary matrix can be written as a sequence of three rotations as well.</span></span> <span data-ttu-id="aca60-192">특히 모든 단일 행렬 $U에 대해 $ $ \alpha, \alpha, \alpha, \alpha를 $ $U = e ^ {i \alpha } R_x (\aa\) R_z (\alpha) R_x (\ 델타) $가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-192">Specifically, for every unitary matrix $U$ there exists $\alpha,\beta,\gamma,\delta$ such that $U= e^{i\alpha} R_x(\beta)R_z(\gamma)R_x(\delta)$.</span></span> <span data-ttu-id="aca60-193">따라서 $ \theta는 모든 값을 사용할 수 있기 때문에 $R _z (\theta) $ 및 $H는 $ 불연속 집합이 아닌 경우에도 유니버설 게이트 집합을 형성 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-193">Thus $R_z(\theta)$ and $H$ also form a universal gate set although it is not a discrete set because $\theta$ can take any value.</span></span> <span data-ttu-id="aca60-194">이러한 이유로 퀀텀 시뮬레이션의 응용 프로그램 때문에, 특히 퀀텀 알고리즘 디자인 수준에서 퀀텀 계산에는 이러한 연속 게이트가 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-194">For this reason, and due to applications in quantum simulation, such continuous gates are crucial for quantum computation, especially at the quantum algorithm design level.</span></span> <span data-ttu-id="aca60-195">내결함성이 있는 하드웨어 구현을 위해 궁극적으로 이러한 회전이 거의 근접 한 불연속 게이트 시퀀스로 컴파일됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca60-195">To achieve fault-tolerant hardware implementation, they will ultimately be compiled into discrete gate sequences that closely approximate these rotations.</span></span>
