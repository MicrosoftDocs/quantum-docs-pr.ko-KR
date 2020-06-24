---
title: 양자 회로
description: 퀀텀 회로 다이어그램을 사용 하 여 단순 하 고 복잡 한 퀀텀 작업을 시각적으로 표시 하는 방법을 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
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
ms.openlocfilehash: 59c32928ddc9252009ad101a3cf3ac33f4968e28
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269612"
---
# <a name="quantum-circuits"></a><span data-ttu-id="42bb0-103">퀀텀 회로</span><span class="sxs-lookup"><span data-stu-id="42bb0-103">Quantum Circuits</span></span>
<span data-ttu-id="42bb0-104">그 순간에는 단일 변환 $ \text { cnot} _ {01 } (H \otimes 1) $을 고려 하십시오.</span><span class="sxs-lookup"><span data-stu-id="42bb0-104">Consider for a moment the unitary transformation $\text{ CNOT}_{01}(H\otimes 1)$.</span></span>
<span data-ttu-id="42bb0-105">이 게이트 시퀀스는 최대 entangled의 2 상 비트 상태를 만들기 때문에 퀀텀 컴퓨팅에 대 한 근본적인 중요 한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-105">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="42bb0-106">$ $ \mathrm{CNOT}_{01 } (H \otimes 1) \ket{00 } = \frac{1 } {\sqrt{2 } } \left (\ket{00 } + \ket{11 } \right), $ $</span><span class="sxs-lookup"><span data-stu-id="42bb0-106">$$\mathrm{CNOT}_{01}(H\otimes 1)\ket{00} = \frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right),$$</span></span>

<span data-ttu-id="42bb0-107">이러한 복잡성을 포함 하는 작업은 퀀텀 알고리즘과 퀀텀 오류 수정에서 사용할 수 있으므로 *퀀텀 회로 다이어그램*이라고 하는 시각화에 대 한 간단한 메서드가 있는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-107">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram*.</span></span>
<span data-ttu-id="42bb0-108">이 최대 entangled 퀀텀 상태를 준비 하기 위한 회로 다이어그램은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-108">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-109">![최대 entangled 2 상 비트 상태에 대 한 회로 다이어그램](~/media/1.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-109">![Circuit diagram for a maximally entangled two-qubit state](~/media/1.svg)</span></span>

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="42bb0-110">퀀텀 회로 다이어그램 규칙</span><span class="sxs-lookup"><span data-stu-id="42bb0-110">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="42bb0-111">퀀텀 작업의 시각적 언어는 퀀텀 회로를 표현 하는 규칙을 이해 하 고 나면 동등한 행렬을 작성 하는 것 보다 훨씬 더 쉽게 좋게 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-111">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="42bb0-112">아래에서 이러한 규칙을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-112">We review these conventions below.</span></span>

<span data-ttu-id="42bb0-113">회로 다이어그램에서 각 실선은 보다 일반적으로는 이상 비트 레지스터를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-113">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="42bb0-114">규칙에 따라 맨 위 줄은 이란 비트 레지스터 $0이 $ 고 나머지는 순차적으로 레이블이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-114">By convention, the top line is qubit register $0$ and the remainder are labeled sequentially.</span></span> <span data-ttu-id="42bb0-115">위의 예제 회로는 두 개의 비트에서 작동 하는 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-115">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="42bb0-116">하나 이상의 이상 비트 레지스터에서 동작 하는 게이트가 상자로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-116">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="42bb0-117">예: 기호</span><span class="sxs-lookup"><span data-stu-id="42bb0-117">For example, the symbol</span></span>

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-118">![단일 기능 비트 레지스터에서 작동 하는 Hadamard 작업에 대 한 기호](~/media/2.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-118">![Symbol for a Hadamard operation acting on a single-qubit register](~/media/2.svg)</span></span>

<span data-ttu-id="42bb0-119">는 단일의 비트 레지스터에서 작동 하는 [Hadamard](xref:microsoft.quantum.intrinsic.h) 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-119">is a [Hadamard](xref:microsoft.quantum.intrinsic.h) operation acting on a single-qubit register.</span></span>

<span data-ttu-id="42bb0-120">퀀텀 게이트는 처음에는 관문을 중심으로 가장 왼쪽의 게이트가 있는 시간순으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-120">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="42bb0-121">즉, 퀀텀을 퀀텀 상태를 유지 하는 경우 와이어는 다이어그램의 각 게이트를 통해 퀀텀 상태를 왼쪽에서 오른쪽으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-121">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="42bb0-122">예를 들면</span><span class="sxs-lookup"><span data-stu-id="42bb0-122">That is to say</span></span> 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-123">![왼쪽에서 오른쪽으로 적용 되는 퀀텀 게이트 다이어그램](~/media/3.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-123">![Diagram of quantum gates being applied left-to-right](~/media/3.svg)</span></span>

<span data-ttu-id="42bb0-124">는 단일 행렬 $CBA입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="42bb0-124">is the unitary matrix $CBA$.</span></span>
<span data-ttu-id="42bb0-125">행렬 곱셈은 반대 규칙을 따르는 합니다. 가장 오른쪽의 행렬이 먼저 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-125">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="42bb0-126">그러나 퀀텀 회로 다이어그램에서 가장 왼쪽의 게이트가 먼저 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-126">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="42bb0-127">이러한 차이는 때때로 혼란 스 러 울 수 있으므로 선형 대 수 표기법과 퀀텀 회로 다이어그램 간의 상당한 차이를 확인 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-127">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="42bb0-128">퀀텀 회로의 입/출력</span><span class="sxs-lookup"><span data-stu-id="42bb0-128">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="42bb0-129">지정 된 앞의 모든 예제에는 퀀텀 게이트의 와이어 수와 동일한 수의 와이어 (는)를 퀀텀 게이트에 정확 하 게 입력 했습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-129">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="42bb0-130">처음에는 퀀텀 회로가 일반적으로 입력 하는 것 보다 더 많거나 적을 수 있다는 것이 합리적입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-130">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="42bb0-131">그러나 모든 퀀텀 작업을 저장 하는 것은 단일 작업 이므로 해독 가능 하기 때문에 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-131">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="42bb0-132">입력과 동일한 수의 출력을 포함 하지 않은 경우에는 해독 하지 않고 일치 하지 않는 단일 사용자가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-132">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="42bb0-133">이러한 이유로 회로 다이어그램에 그려진 상자는 종료 하는 것과 정확히 동일한 수의 와이어로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-133">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="42bb0-134">다중 기능 비트 회로 다이어그램은 유사한 규칙에 따라 단일 비트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-134">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="42bb0-135">명확 하 게 예를 들어 $ $ (H S X) $로 $B 하는 두 개의 단일 비트 작업을 정의 하 \otimes 고 회로를 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-135">As a clarifying example, we can define a two-qubit unitary operation $B$ to be $(H S\otimes X)$ and express the circuit equivalently as</span></span>

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-136">![두 개의 단일 비트 작업의 회로 다이어그램](~/media/4.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-136">![Circuit diagram of a two-qubit unitary operation](~/media/4.svg)</span></span>

<span data-ttu-id="42bb0-137">회로를 사용 하는 $ 컨텍스트에 따라 2 1-가 비트 레지스터가 아닌 단일 2-가 비트 레지스터에 대해 작업을 수행 하는 것으로 $B를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-137">We can also view $B$ as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="42bb0-138">이러한 추상 회로 다이어그램의 가장 유용한 속성은 기본 게이트로 컴파일하지 않고도 복잡 한 퀀텀 알고리즘을 높은 수준으로 설명할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-138">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="42bb0-139">즉, 알고리즘 내의 각 서브루틴이 작동 하는 방식에 대 한 모든 세부 정보를 이해 하지 않고도 대량 퀀텀 알고리즘에 대 한 데이터 흐름에 대 한 intuition를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-139">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="42bb0-140">제어 된 게이트</span><span class="sxs-lookup"><span data-stu-id="42bb0-140">Controlled gates</span></span>
<span data-ttu-id="42bb0-141">Multi-factor bit 퀀텀 회로 다이어그램에 기본 제공 되는 다른 구문은 제어입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-141">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="42bb0-142">퀀텀 단일 제어 출입문의 동작입니다. $ \Lambda (G) $로 표시 된 단일의 \ket{1 값은 $ $ \Lambda (G) $G (\lambda \ket{0 } + \lambda } ) \ket { \lambda } = \lambda \ket{0 } \ket { a\psi } + \lambda \ket{1 } \ket { n\psi } $의 다음 예제를 살펴보면 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-142">The action of a quantum singly controlled gate, denoted $\Lambda(G)$, where a single qubit's value controls the application of $G$, can be understood by looking at the following example of a product state input $\Lambda(G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket{\psi}$.</span></span>
<span data-ttu-id="42bb0-143">즉, 제어 되는 게이트는 컨트롤의 값이 $1를 사용 하는 경우에 $ 만 $ \psi를 포함 하는 레지스터에 $G 적용 됩니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="42bb0-143">That is to say, the controlled gate applies $G$ to the register containing $\psi$ if and only if the control qubit takes the value $1$.</span></span>
<span data-ttu-id="42bb0-144">일반적으로 회로 다이어그램에서 이와 같이 제어 되는 작업을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-144">In general, we describe such controlled operations in circuit diagrams as</span></span>

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-145">![단일 제어 게이트 회로 다이어그램](~/media/5.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-145">![Circuit diagram of a singly controlled gate](~/media/5.svg)</span></span>

<span data-ttu-id="42bb0-146">여기서 검은색 원은 게이트가 제어 되는 퀀텀 비트를 나타내며, 세로는 컨트롤의 값이 $1를 사용 하는 경우 적용 되는 단일를 나타냅니다 $ .</span><span class="sxs-lookup"><span data-stu-id="42bb0-146">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value $1$.</span></span>
<span data-ttu-id="42bb0-147">$G = X $ 및 $G = Z와 같은 특수 한 경우에는 $ 다음 표기법을 도입 하 여 게이트의 제어 된 버전을 설명 합니다 (제어 된 X 게이트는 [$CNOT $ 게이트](xref:microsoft.quantum.intrinsic.cnot)).</span><span class="sxs-lookup"><span data-stu-id="42bb0-147">For the special cases where $G=X$ and $G=Z$ we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [$CNOT$ gate](xref:microsoft.quantum.intrinsic.cnot)):</span></span>

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-148">![제어 되는 게이트의 특수 사례에 대 한 회로 다이어그램](~/media/6.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-148">![Circuit diagram for special cases of controlled gates](~/media/6.svg)</span></span>

<span data-ttu-id="42bb0-149">Q #은 작업의 제어 된 버전을 자동으로 생성 하는 메서드를 제공 합니다. 그러면 프로그래머가 이러한 작업을 직접 코딩할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-149">Q# provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="42bb0-150">이에 대 한 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-150">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a><span data-ttu-id="42bb0-151">측정 연산자</span><span class="sxs-lookup"><span data-stu-id="42bb0-151">Measurement operator</span></span>
<span data-ttu-id="42bb0-152">회로 다이어그램에서 시각화 하는 나머지 작업은 측정입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-152">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="42bb0-153">측정은 더 많은 비트 레지스터를 사용 하 여 측정 하 고 결과를 기존 정보로 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-153">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="42bb0-154">측정 연산은 미터 기호로 표시 되 고 항상 (실선으로 표시 됨)에 대 한 입력으로 사용 되며, 이중 줄로 표시 되는 고전적인 정보를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-154">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="42bb0-155">특히 이러한 subcircuit는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-155">Specifically, such a subcircuit looks like:</span></span>

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-156">![측정 작업을 나타내는 기호](~/media/7.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-156">![Symbol representing a measurement operation](~/media/7.svg)</span></span>

<span data-ttu-id="42bb0-157">Q #에서는이 목적을 위해 [측정값 연산자](xref:microsoft.quantum.intrinsic.measure) 를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-157">Q# implements a [Measure operator](xref:microsoft.quantum.intrinsic.measure) for this purpose.</span></span>
<span data-ttu-id="42bb0-158">자세한 내용은 [측정에](xref:microsoft.quantum.libraries.standard.prelude#measurements) 대 한 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42bb0-158">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="42bb0-159">마찬가지로 subcircuit</span><span class="sxs-lookup"><span data-stu-id="42bb0-159">Similarly, the subcircuit</span></span>

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="42bb0-160">![제어 된 작업을 나타내는 회로 다이어그램](~/media/8.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-160">![Circuit diagram representing a controlled operation](~/media/8.svg)</span></span>

<span data-ttu-id="42bb0-161">일반적으로 제어 되는 게이트를 제공 합니다 $ . 여기서 $G는 클래식 컨트롤 비트의 조건 화 된 값이 $1에 적용 됩니다 $ .</span><span class="sxs-lookup"><span data-stu-id="42bb0-161">gives a classically controlled gate, where $G$ is applied conditioned on the classical control bit being value $1$.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="42bb0-162">Teleportation 회로 다이어그램</span><span class="sxs-lookup"><span data-stu-id="42bb0-162">Teleportation circuit diagram</span></span>
<span data-ttu-id="42bb0-163">퀀텀 teleportation는 이러한 구성 요소를 보여 주는 최상의 퀀텀 알고리즘이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-163">Quantum teleportation is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="42bb0-164">해당 하는 [퀀텀 Kata](xref:microsoft.quantum.overview.katas) 퀀텀 teleportation은 되거나 얽 히 및 측정을 사용 하 여 퀀텀 컴퓨터 내에서 (또는 퀀텀 네트워크의 먼 퀀텀 컴퓨터 간) 데이터를 이동 하는 방법에 대해 배울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-164">You can learn hands-on with the corresponding [Quantum Kata](xref:microsoft.quantum.overview.katas) Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="42bb0-165">흥미롭게도, 실제 값을 알고 있는 것이 아니라, 지정 된의 값을 한 가지 이상에서 다른 값으로 이동 하는 것은 사실입니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-165">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="42bb0-166">이는 프로토콜이 퀀텀 메커니즘의 법에 따라 작동 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-166">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="42bb0-167">퀀텀 teleportation 회로는 아래에 제공 됩니다. 또한 퀀텀 회로를 읽는 방법을 보여 주기 위해 주석이 추가 된 회로 버전을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="42bb0-167">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<!--- ![](.\media\tp2.svg){ width=50% } --->
<span data-ttu-id="42bb0-168">![퀀텀 teleportation 회로](~/media/tp2.svg)</span><span class="sxs-lookup"><span data-stu-id="42bb0-168">![Quantum teleportation circuit](~/media/tp2.svg)</span></span>
