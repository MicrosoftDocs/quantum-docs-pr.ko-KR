---
title: 양자 컴퓨팅을 위한 선형 대수
description: 양자 컴퓨팅을 이해하는 데 필요한 기본 선형 대수 개념에 대해 알아봅니다.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.algebra
ms.openlocfilehash: 4cf6cce870c7661a7fffc21dcb60dd53cf281ddd
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415443"
---
# <a name="linear-algebra-for-quantum-computing"></a><span data-ttu-id="721a8-103">양자 컴퓨팅을 위한 선형 대수</span><span class="sxs-lookup"><span data-stu-id="721a8-103">Linear algebra for quantum computing</span></span>

<span data-ttu-id="721a8-104">선형 대수는 양자 컴퓨팅의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-104">Linear algebra is the language of quantum computing.</span></span> <span data-ttu-id="721a8-105">양자 프로그램을 구현하거나 작성하기 위해 알 필요는 없지만, 큐비트 상태와 양자 연산을 설명하고 양자 컴퓨터가 일련의 명령에 응답하여 수행하는 작업을 예측하는 데 널리 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-105">Although you don’t need to know it to implement or write quantum programs, it is widely used to describe qubit states, quantum operations, and to predict what a quantum computer will do in response to a sequence of instructions.</span></span>

<span data-ttu-id="721a8-106">[양자 물리학의 기본 개념](xref:microsoft.quantum.overview.understanding)을 익히는 것이 양자 컴퓨팅을 이해하는데 도움이 되는 것처럼 몇 가지 기본적인 선형 대수를 알면 양자 알고리즘의 작동 방식을 이해하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-106">Just like being familiar with the [basic concepts of quantum physics](xref:microsoft.quantum.overview.understanding) can help you understand quantum computing, knowing some basic linear algebra can help you understand how quantum algorithms work.</span></span> <span data-ttu-id="721a8-107">적어도 **벡터** 및 **행렬 곱**에 익숙해져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-107">At the least, you’ll want to be familiar with **vectors** and **matrix multiplication**.</span></span> <span data-ttu-id="721a8-108">이러한 대수 개념에 대한 지식을 새로 고쳐야 하는 경우 기본 사항을 다루고 있는 몇 가지 자습서는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-108">If you need to refresh your knowledge of these algebra concepts, here are some tutorials that cover the basics:</span></span>

- [<span data-ttu-id="721a8-109">선형 대수에 대한 Jupyter Notebook 자습서</span><span class="sxs-lookup"><span data-stu-id="721a8-109">Jupyter notebook tutorial on linear algebra</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)
- [<span data-ttu-id="721a8-110">복소수 연산에 대한 Jupyter Notebook 자습서</span><span class="sxs-lookup"><span data-stu-id="721a8-110">Jupyter notebook tutorial on complex arithmetic</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)
- [<span data-ttu-id="721a8-111">양자 계산을 위한 선형 대수</span><span class="sxs-lookup"><span data-stu-id="721a8-111">Linear Algebra for Quantum Computation</span></span>](https://cds.cern.ch/record/1522001/files/978-1-4614-6336-8_BookBackMatter.pdf)
- [<span data-ttu-id="721a8-112">선형 대수의 기본 사항</span><span class="sxs-lookup"><span data-stu-id="721a8-112">Fundamentals of Linear Algebra</span></span>](https://www.math.ubc.ca/~carrell/NB.pdf)
- [<span data-ttu-id="721a8-113">양자 계산 입문</span><span class="sxs-lookup"><span data-stu-id="721a8-113">Quantum Computation Primer</span></span>](https://www.codeproject.com/Articles/5155638/Quantum-Computation-Primer-Part-1#exploring-quantum-superposition)

## <a name="vectors-and-matrices-in-quantum-computing"></a><span data-ttu-id="721a8-114">양자 컴퓨팅의 벡터 및 행렬</span><span class="sxs-lookup"><span data-stu-id="721a8-114">Vectors and matrices in quantum computing</span></span>

<span data-ttu-id="721a8-115">[양자 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding) 항목에서 큐비트가 1 또는 0 상태이거나 중첩이거나 둘 다일 수 있음을 확인했습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-115">In the topic [Understanding quantum computing](xref:microsoft.quantum.overview.understanding), you saw that a qubit can be in a state of 1 or 0 or a superposition or both.</span></span> <span data-ttu-id="721a8-116">선형 대수를 사용하면 큐비트 상태가 벡터로 설명되며 $\begin{bmatrix} a \\\\  b \end{bmatrix}$ 단일 열 **행렬**로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-116">Using linear algebra, the state of a qubit is described as a vector and is represented by a single column **matrix** $\begin{bmatrix} a \\\\  b \end{bmatrix}$.</span></span> <span data-ttu-id="721a8-117">또한 **양자 상태 벡터**라고도 하며 $|a|^2 + |b|^2 = 1$라는 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-117">It is also known as a **quantum state vector** and must meet the requirement that $|a|^2 + |b|^2 = 1$.</span></span>  

<span data-ttu-id="721a8-118">행렬의 요소는 큐비트가 한 방향 또는 다른 방향으로 붕괴될 확률을 나타내며, $|a|^2$는 0으로 붕괴될 확률이고 $|b|^2$는 1로 붕괴될 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-118">The elements of the matrix represent the probability of the qubit collapsing one way or the other, with $|a|^2$ being the probability of collapsing to zero, and $|b|^2$ being the probability of collapsing to one.</span></span> <span data-ttu-id="721a8-119">다음 행렬은 모두 유효한 양자 상태 벡터를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-119">The following matrices all represent valid quantum state vectors:</span></span>

<span data-ttu-id="721a8-120">$$\begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \begin{bmatrix} 0 \\\\  1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{ and }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{i}{\sqrt{2}} \end{bmatrix}.$$</span><span class="sxs-lookup"><span data-stu-id="721a8-120">$$\begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \begin{bmatrix} 0 \\\\  1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{ and }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{i}{\sqrt{2}} \end{bmatrix}.$$</span></span>

<span data-ttu-id="721a8-121">[양자 컴퓨터 및 양자 시뮬레이터](xref:microsoft.quantum.overview.simulators)에서도 양자 연산이 큐비트 상태를 수정하는 데 사용됨을 확인했습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-121">In [Quantum computers and quantum simulators](xref:microsoft.quantum.overview.simulators) you also saw that quantum operations are used to modify the state of a qubit.</span></span>  <span data-ttu-id="721a8-122">또한 양자 연산은 행렬로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-122">Quantum operations can also be represented by a matrix.</span></span> <span data-ttu-id="721a8-123">양자 연산이 큐비트에 적용되면 이를 나타내는 두 개의 행렬을 곱하고 결과 답에서 연산 후의 새 큐비트 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-123">When a quantum operation is applied to a qubit, the two matrices that represent them are multiplied and the resulting answer represents the new state of the qubit after the operation.</span></span>  

<span data-ttu-id="721a8-124">다음은 행렬 곱으로 나타내는 두 가지 일반적인 양자 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-124">Here are two common quantum operations represented with matrix multiplication.</span></span>


<span data-ttu-id="721a8-125">[`X` 연산](xref:microsoft.quantum.intrinsic.x)은 $X$ Pauli 행렬로 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-125">The [`X` operation](xref:microsoft.quantum.intrinsic.x) is represented by the Pauli matrix $X$,</span></span>

<span data-ttu-id="721a8-126">$$X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix},$$</span><span class="sxs-lookup"><span data-stu-id="721a8-126">$$X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix},$$</span></span>
    
<span data-ttu-id="721a8-127">그리고 큐비트 상태를 0에서 1로(또는 반대로) 대칭 이동하는 데 사용됩니다. 예를 들어 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-127">and is used to flip the state of a qubit from 0 to 1 (or vice-versa), for example</span></span>

<span data-ttu-id="721a8-128">$$\begin{bmatrix}0 &1\\\\ 1 &0\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \begin{bmatrix} 0 \\\\  1 \end{bmatrix}.$$</span><span class="sxs-lookup"><span data-stu-id="721a8-128">$$\begin{bmatrix}0 &1\\\\ 1 &0\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \begin{bmatrix} 0 \\\\  1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="721a8-129">['H' 연산](xref:microsoft.quantum.intrinsic.h)은 $H$ Hadamard 변환으로 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-129">The ['H' operation](xref:microsoft.quantum.intrinsic.h) is represented by the Hadamard transformation $H$,</span></span>

<span data-ttu-id="721a8-130">$$H = \dfrac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix},$$</span><span class="sxs-lookup"><span data-stu-id="721a8-130">$$H = \dfrac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix},$$</span></span>

 <span data-ttu-id="721a8-131">그리고 아래와 같이 큐비트를 어느 한 쪽으로 붕괴될 확률이 동일한 중첩 상태로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-131">and puts a qubit into a superposition state where it has an even probability of collapsing either way, as shown here</span></span>

<span data-ttu-id="721a8-132">$$\frac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix}=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=\left(\frac{1}{\sqrt{2}}\right)^2=\frac{1}{2}.$$</span><span class="sxs-lookup"><span data-stu-id="721a8-132">$$\frac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix}=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=\left(\frac{1}{\sqrt{2}}\right)^2=\frac{1}{2}.$$</span></span>

<span data-ttu-id="721a8-133">양자 연산을 나타내는 행렬에는 **단위** 행렬이어야 한다는 한 가지 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-133">A matrix that represents a quantum operation has one requirement – it must be a **unitary** matrix.</span></span> <span data-ttu-id="721a8-134">**역** 행렬이 행렬의 **켤레 전치(conjugate transpose)** 와 같으면 해당 행렬은 단위 행렬입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-134">A matrix is unitary if the **inverse** of the matrix is equal to the **conjugate transpose** of the matrix.</span></span>

## <a name="representing-two-qubit-states"></a><span data-ttu-id="721a8-135">2개 큐비트 상태 표현</span><span class="sxs-lookup"><span data-stu-id="721a8-135">Representing two-qubit states</span></span>

<span data-ttu-id="721a8-136">위의 예에서 한 큐비트의 상태는 $\begin{bmatrix} a \\\\  b \end{bmatrix}$ 단일 열 행렬을 사용하여 설명했으며, 연산을 적용하는 것은 두 행렬을 곱하여 설명했습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-136">In the examples above, the state of one qubit was described using a single column matrix $\begin{bmatrix} a \\\\  b \end{bmatrix}$, and applying an operation to it was described by multiplying the two matrices.</span></span> <span data-ttu-id="721a8-137">그러나 양자 컴퓨터는 둘 이상의 큐비트를 사용하므로 두 큐비트의 결합된 상태는 어떻게 설명할까요?</span><span class="sxs-lookup"><span data-stu-id="721a8-137">However, quantum computers use more than one qubit, so how do you describe the combined state of two qubits?</span></span> 

<span data-ttu-id="721a8-138">각 큐비트는 벡터 공간이므로 곱할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-138">Remember that each qubit is a vector space, so they can't just be multiplied.</span></span> <span data-ttu-id="721a8-139">대신 개별 벡터 공간에서 새 벡터 공간을 만들고 $\otimes$ 기호로 표현되는 관련 연산인 **텐서 곱**을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-139">Instead, you use a **tensor product**, which is a related operation that creates a new vector space from individual vector spaces, and is represented by the $\otimes$ symbol.</span></span> <span data-ttu-id="721a8-140">예를 들어 두 개의 큐비트 상태($\begin{bmatrix} a \\\\  b \end{bmatrix}$ 및 $\begin{bmatrix} c \\\\  d \end{bmatrix}$)의 텐서 곱이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-140">For example, the tensor product of two qubit states $\begin{bmatrix} a \\\\  b \end{bmatrix}$ and $\begin{bmatrix} c \\\\  d \end{bmatrix}$ is calculated</span></span>

<span data-ttu-id="721a8-141">$$ \begin{bmatrix} a \\\\  b \end{bmatrix} \otimes \begin{bmatrix} c \\\\  d \end{bmatrix} =\begin{bmatrix} a \begin{bmatrix} c \\\\  d \end{bmatrix} \\\\ b \begin{bmatrix}c \\\\  d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="721a8-141">$$ \begin{bmatrix} a \\\\  b \end{bmatrix} \otimes \begin{bmatrix} c \\\\  d \end{bmatrix} =\begin{bmatrix} a \begin{bmatrix} c \\\\  d \end{bmatrix} \\\\ b \begin{bmatrix}c \\\\  d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}.</span></span> $$

<span data-ttu-id="721a8-142">결과는 각 요소에서 확률을 나타내는 4차원 행렬입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-142">The result is a four-dimensional matrix, with each element representing a probability.</span></span> <span data-ttu-id="721a8-143">예를 들어 $ac$는 두 큐비트가 0과 0으로 붕괴될 확률이고, $ad$는 0과 1의 확률 등입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-143">For example, $ac$ is the probability of the two qubits collapsing to 0 and 0, $ad$ is the probability of 0 and 1, and so on.</span></span> 

<span data-ttu-id="721a8-144">양자 상태를 나타내기 위해 $\begin{bmatrix} a \\\\  b \end{bmatrix}$ 단일 큐비트 상태에서 $|a|^2 + |b|^2 = 1$라는 요구 사항을 충족해야 하는 것처럼 $\begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}$ 2개 큐비트 상태는 $|ac|^2 + |ad|^2 + |bc|^2+ |bd|^2 = 1$라는 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-144">Just as a single qubit state $\begin{bmatrix} a \\\\  b \end{bmatrix}$ must meet the requirement that $|a|^2 + |b|^2 = 1$ in order to represent a quantum state, a two-qubit state $\begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}$ must meet the requirement that $|ac|^2 + |ad|^2 + |bc|^2+ |bd|^2 = 1$.</span></span>

## <a name="summary"></a><span data-ttu-id="721a8-145">요약</span><span class="sxs-lookup"><span data-stu-id="721a8-145">Summary</span></span>

<span data-ttu-id="721a8-146">선형 대수는 양자 컴퓨팅과 양자 물리학을 설명하기 위한 표준 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-146">Linear algebra is the standard language for describing quantum computing and quantum physics.</span></span> <span data-ttu-id="721a8-147">Microsoft Quantum Development Kit에 포함된 [라이브러리](xref:microsoft.quantum.libraries)는 기본 수학을 자세히 숙지하지 않고도 고급 양자 알고리즘을 실행하는 데 도움이 되지만, 기본 사항을 이해하면 빠르게 시작하고 견고한 기반을 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="721a8-147">Even though the [libraries](xref:microsoft.quantum.libraries) included with the Microsoft Quantum Development Kit will help you run advanced quantum algorithms without diving into the underlying math, understanding the basics will help you get started quickly and provide a solid foundation to build on.</span></span>

## <a name="next-steps"></a><span data-ttu-id="721a8-148">다음 단계</span><span class="sxs-lookup"><span data-stu-id="721a8-148">Next steps</span></span>

[<span data-ttu-id="721a8-149">QDK 설치</span><span class="sxs-lookup"><span data-stu-id="721a8-149">Install the QDK</span></span>](xref:microsoft.quantum.install)
