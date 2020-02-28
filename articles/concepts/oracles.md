---
title: 양자 오라클
description: 다른 알고리즘의 입력으로 사용 되는 퀀텀 oracles 블랙 박스 작업을 사용 하 고 정의 하는 방법에 대해 알아봅니다.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
ms.openlocfilehash: 1d1d0b0903db8e994166c3e8a5798f70742a1c7e
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904930"
---
# <a name="quantum-oracles"></a><span data-ttu-id="af65f-103">퀀텀 Oracles</span><span class="sxs-lookup"><span data-stu-id="af65f-103">Quantum Oracles</span></span>

<span data-ttu-id="af65f-104">Oracle $O $은 다른 알고리즘에 대 한 입력으로 사용 되는 "블랙 박스" 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="af65f-105">이러한 작업은 $f 기존 함수를 사용 하 여 정의 되는 경우가 많습니다. \\{0, 1\\} ^ n \ \\{0, 1\\} ^ m $은 $n $ 비트 이진 입력을 사용 하 고 $m $ bit 이진 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="af65f-106">이렇게 하려면 특정 이진 입력 $x = (x_{0}, x_{1}, \dots, x_ {n-1}) $를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="af65f-107">\Ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cst\otimes \ket{x_ {n-1}} $로 stbit 상태에 레이블을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="af65f-108">먼저 $O $를 $O \ket{x} = \ket{f (x)} $로 정의 하려고 할 수 있지만, 여기에는 몇 가지 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="af65f-109">첫째, $f $에는 다른 크기의 입력 및 출력 ($n \ne m $)이 있을 수 있습니다 .이 경우 $O $을 적용 하면 레지스터의 원하는 비트 수가 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="af65f-110">둘째, $n = m $ 인 경우에도 함수를 반전할 수 없습니다. 일부 $x \ne y $로 $f (x) = f (y) $를 입력 하는 경우에는 \ket{x} = O\ket {y} $ 이지만 $O ^ \dagger O\ket {x} \ne O ^ \Dagger {y} $를 $O 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="af65f-111">즉, adjoint 작업 $O ^ \dagger $에 생성할 수 없으며,이에 대해 adjoint가 정의 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="af65f-112">계산 기준 상태에 영향을 미치는 oracle 정의</span><span class="sxs-lookup"><span data-stu-id="af65f-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="af65f-113">이러한 두 가지 문제를 해결할 수 있습니다. 이러한 문제는 답변을 보유 하기 위해 $ $ $m의 두 번째 레지스터를 도입 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="af65f-114">그런 다음 모든 계산 기준에 대 한 oracle의 효과를 정의 합니다. 모든 $x \in \\{0, 1\\} ^ n $ 및 \\{0, 1\\} ^ m $의 $y \in</span><span class="sxs-lookup"><span data-stu-id="af65f-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="af65f-115">$ $ \begin{align} O (\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \otimes f (x)}.</span><span class="sxs-lookup"><span data-stu-id="af65f-115">$$ \begin{align} O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="af65f-116">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="af65f-116">\end{align} $$</span></span>

<span data-ttu-id="af65f-117">이제 생성에의 한 $O = O ^ \aate$를 생성 했으므로 이전 문제를 모두 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-117">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="af65f-118">$O = O ^ {\dagger} $에 대 한 자세한 내용은 $a \oplus b\oplus b = a $ for all $a, b \bin \{0, 1\}$ 이므로 ^ 2 = \boldone $ $O.</span><span class="sxs-lookup"><span data-stu-id="af65f-118">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="af65f-119">결과적으로 \ket{x} \ket{y \oplus f (x)} = \ket{x} \ket{y \oplus f (x) \oplus f (x)} = \ket{x} \ket{y} $를 $O 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-119">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="af65f-120">중요 한 것은 각 계산 기준 상태 $ \ket{x}\ket{y} $에 대해 oracle을 정의 하 $O는 것은 다른 모든 상태에 대해 $가 작동 하는 방법을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-120">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="af65f-121">이는 모든 퀀텀 작업과 마찬가지로 $O $가 작동 하는 상태에서 선형 이라는 사실을 즉시 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-121">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="af65f-122">예를 들어 $H \ket{0} = \ket{+} $ 및 $H \ket{1} = \ket{-}$에 의해 정의 된 Hadamard 작업을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-122">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="af65f-123">$ \Ket{+} $에서 $H $가 작동 하는 방법을 알고 싶으면 $ is linear $H를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-123">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="af65f-124">$ $ \begin{align} H\ket {+} & = \frac{1}{\sqrt{2}} H (\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0}-\ket{1}) = \ket{0}.</span><span class="sxs-lookup"><span data-stu-id="af65f-124">$$ \begin{align} H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="af65f-125">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="af65f-125">\end{align} $$</span></span>

<span data-ttu-id="af65f-126">Oracle $O $를 정의 하는 경우와 비슷한 방법으로 $ \ket{\psi} $ on $n + m $를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-126">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="af65f-127">$ $ \begin{align} \ket{\psi} & = \ sum_ {x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \in (x, y) \ket{x} \ket{y} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="af65f-127">$$ \begin{align} \ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \end{align} $$</span></span>

<span data-ttu-id="af65f-128">여기서 $ \alpha: \\{0, 1\\} ^ n \alpha \\{0, 1\\} ^ m \alpha $ \mathbb{C} $는 state $ $의 계수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-128">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="af65f-129">따라서</span><span class="sxs-lookup"><span data-stu-id="af65f-129">Thus,</span></span>

<span data-ttu-id="af65f-130">$ $ \begin{align} O \ket{\psi} & = O \ sum_ {x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \in (x, y) \ket{x} \ket{y} \\\\ & = \ sum_ {x \ \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \in (x, y) O \ket{x} \ket{y} \\\\ & = \ sum_ {x \in \\{0, 1\\} ^ n , y \in \\{0, 1\\} ^ m} \in (x, y) \ket{x} \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="af65f-130">$$ \begin{align} O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="af65f-131">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="af65f-131">\end{align} $$</span></span>

## <a name="phase-oracles"></a><span data-ttu-id="af65f-132">Oracles 단계</span><span class="sxs-lookup"><span data-stu-id="af65f-132">Phase oracles</span></span>
<span data-ttu-id="af65f-133">또는 $O $에 대 한 입력에 따라 _단계_ 를 적용 하 여 $ $f $를 oracle $O $로 인코딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-133">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="af65f-134">예를 들어 $ $ \begin{align} O \ket{x} = (-1) ^ {f (x)} \ket{x}.와 같은 $를 $O 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-134">For instance, we might define $O$ such that $$ \begin{align} O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="af65f-135">\end{align} $ $ 단계 oracle이 초기에 계산 기준 상태 $ \ket{x} $로 작동 하는 경우이 단계는 글로벌 단계 이므로 관찰 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-135">\end{align} $$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="af65f-136">그러나 이러한 oracle은 superposition에 적용 되거나 제어 된 작업으로 적용 되는 경우 매우 강력한 리소스가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-136">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="af65f-137">예를 들어, 1 단계를 $f $ _f 하는 $O 단계 orcale를 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-137">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="af65f-138">그런 다음 $ $ \begin{align} O_f \ket{+} & = O_f (\ket{0} + \ket{1})/\sqrt{2} \\\\ &{0} = ((-1) ^ {f (0)} \ket{1}+ (-1) ^ {f (1)} \ket{2})/\sqrt \\\\ & = (-1) ^ {f (0)} (\ket{0} + (-1) ^ {f (1)-f (0)} \ket{1})/\sqrt{2} \\\\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket{+}.</span><span class="sxs-lookup"><span data-stu-id="af65f-138">Then, $$ \begin{align} O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="af65f-139">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="af65f-139">\end{align} $$</span></span>

<span data-ttu-id="af65f-140">보다 일반적으로는 oracles의 두 뷰를 넓혔습니다 하 여 단일 비트만이 아닌 실수를 반환 하는 클래식 함수를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-140">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="af65f-141">Oracle을 구현 하는 가장 좋은 방법은 지정 된 알고리즘 내에서이 oracle을 사용 하는 방법에 따라 크게 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-141">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="af65f-142">예를 들어 [Deutsch-Jozsa 알고리즘](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) 은 첫 번째 방법으로 구현 된 oracle을 사용 하는 반면 [Grover의 알고리즘](https://en.wikipedia.org/wiki/Grover's_algorithm) 은 두 번째 방법으로 구현 된 oracle에 의존 합니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-142">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="af65f-143">자세한 내용은 [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465)에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af65f-143">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
