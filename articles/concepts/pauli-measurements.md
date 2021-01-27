---
<span data-ttu-id="b1e36-101">제목: Pauli 측정 설명: 단일 및 다중 값 비트를 사용 하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-101">title: Pauli Measurements description: Learn how to work with single- and multi-qubit Pauli measurement operations.</span></span>
<span data-ttu-id="b1e36-102">만든이: bradben uid: benbra: 12/11/2017: 밀리초. 항목: 개념 비-. s u m:</span><span class="sxs-lookup"><span data-stu-id="b1e36-102">author: bradben uid: microsoft.quantum.concepts.pauli ms.author: v-benbra ms.date: 12/11/2017 ms.topic: conceptual no-loc:</span></span>
- <span data-ttu-id="b1e36-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="b1e36-103">"Q#"</span></span>
- <span data-ttu-id="b1e36-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="b1e36-104">"$$v"</span></span>
- <span data-ttu-id="b1e36-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="b1e36-105">"$$"</span></span>
- <span data-ttu-id="b1e36-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="b1e36-106">"$$"</span></span>
- <span data-ttu-id="b1e36-107">"$"</span><span class="sxs-lookup"><span data-stu-id="b1e36-107">"$"</span></span>
- <span data-ttu-id="b1e36-108">"$"</span><span class="sxs-lookup"><span data-stu-id="b1e36-108">"$"</span></span>
- <span data-ttu-id="b1e36-109">"$"</span><span class="sxs-lookup"><span data-stu-id="b1e36-109">"$"</span></span>
- <span data-ttu-id="b1e36-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="b1e36-110">"$$"</span></span>
- <span data-ttu-id="b1e36-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="b1e36-111">"\cdots"</span></span>
- <span data-ttu-id="b1e36-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="b1e36-112">"bmatrix"</span></span>
- <span data-ttu-id="b1e36-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="b1e36-113">"\ddots"</span></span>
- <span data-ttu-id="b1e36-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="b1e36-114">"\equiv"</span></span>
- <span data-ttu-id="b1e36-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="b1e36-115">"\sum"</span></span>
- <span data-ttu-id="b1e36-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="b1e36-116">"\begin"</span></span>
- <span data-ttu-id="b1e36-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="b1e36-117">"\end"</span></span>
- <span data-ttu-id="b1e36-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="b1e36-118">"\sqrt"</span></span>
- <span data-ttu-id="b1e36-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="b1e36-119">"\otimes"</span></span>
- <span data-ttu-id="b1e36-120">"{"</span><span class="sxs-lookup"><span data-stu-id="b1e36-120">"{"</span></span>
- <span data-ttu-id="b1e36-121">"}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-121">"}"</span></span>
- <span data-ttu-id="b1e36-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="b1e36-122">"\text"</span></span>
- <span data-ttu-id="b1e36-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="b1e36-123">"\phi"</span></span>
- <span data-ttu-id="b1e36-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="b1e36-124">"\kappa"</span></span>
- <span data-ttu-id="b1e36-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="b1e36-125">"\psi"</span></span>
- <span data-ttu-id="b1e36-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="b1e36-126">"\alpha"</span></span>
- <span data-ttu-id="b1e36-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="b1e36-127">"\beta"</span></span>
- <span data-ttu-id="b1e36-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="b1e36-128">"\gamma"</span></span>
- <span data-ttu-id="b1e36-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="b1e36-129">"\delta"</span></span>
- <span data-ttu-id="b1e36-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="b1e36-130">"\omega"</span></span>
- <span data-ttu-id="b1e36-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="b1e36-131">"\bra"</span></span>
- <span data-ttu-id="b1e36-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="b1e36-132">"\ket"</span></span>
- <span data-ttu-id="b1e36-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="b1e36-133">"\boldone"</span></span>
- <span data-ttu-id="b1e36-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="b1e36-134">"\\\\"</span></span>
- <span data-ttu-id="b1e36-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="b1e36-135">"\\"</span></span>
- <span data-ttu-id="b1e36-136">"="</span><span class="sxs-lookup"><span data-stu-id="b1e36-136">"="</span></span>
- <span data-ttu-id="b1e36-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="b1e36-137">"\frac"</span></span>
- <span data-ttu-id="b1e36-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="b1e36-138">"\text"</span></span>
- <span data-ttu-id="b1e36-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="b1e36-139">"\mapsto"</span></span>
- <span data-ttu-id="b1e36-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="b1e36-140">"\dagger"</span></span>
- <span data-ttu-id="b1e36-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="b1e36-141">"\to"</span></span>
- <span data-ttu-id="b1e36-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-142">"\begin{cases}"</span></span>
- <span data-ttu-id="b1e36-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-143">"\end{cases}"</span></span>
- <span data-ttu-id="b1e36-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="b1e36-144">"\operatorname"</span></span>
- <span data-ttu-id="b1e36-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="b1e36-145">"\braket"</span></span>
- <span data-ttu-id="b1e36-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="b1e36-146">"\id"</span></span>
- <span data-ttu-id="b1e36-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="b1e36-147">"\expect"</span></span>
- <span data-ttu-id="b1e36-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="b1e36-148">"\defeq"</span></span>
- <span data-ttu-id="b1e36-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="b1e36-149">"\variance"</span></span>
- <span data-ttu-id="b1e36-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="b1e36-150">"\dd"</span></span>
- <span data-ttu-id="b1e36-151">"&"</span><span class="sxs-lookup"><span data-stu-id="b1e36-151">"&"</span></span>
- <span data-ttu-id="b1e36-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-152">"\begin{align}"</span></span>
- <span data-ttu-id="b1e36-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-153">"\end{align}"</span></span>
- <span data-ttu-id="b1e36-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="b1e36-154">"\Lambda"</span></span>
- <span data-ttu-id="b1e36-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="b1e36-155">"\lambda"</span></span>
- <span data-ttu-id="b1e36-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="b1e36-156">"\Omega"</span></span>
- <span data-ttu-id="b1e36-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="b1e36-157">"\mathrm"</span></span>
- <span data-ttu-id="b1e36-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="b1e36-158">"\left"</span></span>
- <span data-ttu-id="b1e36-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="b1e36-159">"\right"</span></span>
- <span data-ttu-id="b1e36-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="b1e36-160">"\qquad"</span></span>
- <span data-ttu-id="b1e36-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="b1e36-161">"\times"</span></span>
- <span data-ttu-id="b1e36-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="b1e36-162">"\big"</span></span>
- <span data-ttu-id="b1e36-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="b1e36-163">"\langle"</span></span>
- <span data-ttu-id="b1e36-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="b1e36-164">"\rangle"</span></span>
- <span data-ttu-id="b1e36-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="b1e36-165">"\bigg"</span></span>
- <span data-ttu-id="b1e36-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="b1e36-166">"\Big"</span></span>
- <span data-ttu-id="b1e36-167">"|"</span><span class="sxs-lookup"><span data-stu-id="b1e36-167">"|"</span></span>
- <span data-ttu-id="b1e36-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="b1e36-168">"\mathbb"</span></span>
- <span data-ttu-id="b1e36-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="b1e36-169">"\vec"</span></span>
- <span data-ttu-id="b1e36-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="b1e36-170">"\in"</span></span>
- <span data-ttu-id="b1e36-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="b1e36-171">"\texttt"</span></span>
- <span data-ttu-id="b1e36-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="b1e36-172">"\ne"</span></span>
- <span data-ttu-id="b1e36-173">"<"</span><span class="sxs-lookup"><span data-stu-id="b1e36-173">"<"</span></span>
- <span data-ttu-id="b1e36-174">">"</span><span class="sxs-lookup"><span data-stu-id="b1e36-174">">"</span></span>
- <span data-ttu-id="b1e36-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="b1e36-175">"\leq"</span></span>
- <span data-ttu-id="b1e36-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="b1e36-176">"\geq"</span></span>
- <span data-ttu-id="b1e36-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="b1e36-177">"~~"</span></span>
- <span data-ttu-id="b1e36-178">"~"</span><span class="sxs-lookup"><span data-stu-id="b1e36-178">"~"</span></span>
- <span data-ttu-id="b1e36-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="b1e36-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="b1e36-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="b1e36-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="b1e36-181">"\_"</span></span>

---

# <a name="pauli-measurements"></a><span data-ttu-id="b1e36-182">Pauli 측정</span><span class="sxs-lookup"><span data-stu-id="b1e36-182">Pauli Measurements</span></span>

<span data-ttu-id="b1e36-183">위의 논의에서 계산 기준 측정에 중점을 두었습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-183">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="b1e36-184">사실, 표기법 밑수 관점에서 계산 기준 측정 측면에서 편리 하 게 사용할 수 있는 퀀텀 컴퓨팅에서 발생 하는 다른 일반적인 측정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-184">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="b1e36-185">로 작업할 때 Q# 가장 일반적인 측정 종류는 다른 기본에 대 한 측정치를 포함 하는 계산 기준 측정을 일반화 하 고 다양 한 비트 간의 패리티를 포함 하는 *Pauli 측정이* 될 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-185">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements*, which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="b1e36-186">이 경우 일반적으로 $ x, Y, z $ 또는 $ z \otimes z, x \otimes x, x \otimes Y $ 등의 연산자를 통해 pauli 연산자를 측정 하는 방법을 설명 하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-186">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span> 

> [!TIP]
<span data-ttu-id="b1e36-187">> 에서 Q# 다기능 비트 Pauli 연산자는 일반적으로 형식의 배열로 표시 됩니다 `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="b1e36-187">> In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
<span data-ttu-id="b1e36-188">> 예를 들어 $ X \otimes Z Y를 \otimes 나타내려면 $ 배열을 사용할 수 있습니다 `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="b1e36-188">> For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="b1e36-189">Pauli 연산자를 기준으로 측정값을 논의 하는 것은 퀀텀 오류 수정의 하위 필드에서 특히 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-189">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="b1e36-190">에서는 Q# 비슷한 규칙을 따르고 있습니다. 이제 이러한 대체 측정값에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-190">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="b1e36-191">Pauli를 측정 하는 방법에 대 한 세부 정보를 살펴보기 하기 전에 퀀텀 컴퓨터 내의 단일 요소를 퀀텀 상태로 측정 하는 것을 고려 하는 것이 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-191">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="b1e36-192">N bit 퀀텀 상태를 보유 하 고 있다고 가정 $ $ 합니다. 그런 다음, $ $ 해당 상태가 될 수 있는 2 ^ n의 절반에 해당 하는 규칙을 즉시 측정 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-192">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="b1e36-193">즉, 측정은 퀀텀 상태를 두 개의 반 공간 중 하나로 프로젝션 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-193">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="b1e36-194">이 intuition을 반영 하기 위해 측정 하는 방식을 일반화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-194">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="b1e36-195">이러한 하위 공간을 간결 하 게 식별 하기 위해 설명을 위한 언어가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-195">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="b1e36-196">두 개의 하위 공간을 설명 하는 한 가지 방법은 규칙에 따라 \pm 1을 사용 하 여 두 개의 고유한 eigenvalues만 있는 행렬을 통해 지정 하는 것입니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="b1e36-196">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="b1e36-197">이러한 방식으로 하위 공간을 설명 하는 간단한 예제를 보려면 Z를 고려 하십시오 $ $ .</span><span class="sxs-lookup"><span data-stu-id="b1e36-197">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

$$
\begin{align}
  <span data-ttu-id="b1e36-198">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="b1e36-198">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="b1e36-199">Pauli-z 행렬의 대각선 요소를 읽으면 $ $ $ z $ 에 $ \ket { } $ $ \ket { } $ 해당 고유 값이 $ \pm 1 인 $ 두 개의 고유 벡터 0과 1이 있음을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-199">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="b1e36-200">따라서, (상태 0에 해당 하는 경우)를 측정 하 고 가져오는 경우 `Zero` $ \ket { } $ 이의 상태는 $ $ Z 연산자의 + 1 eigenstate 임을 알 수 $ $ 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-200">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="b1e36-201">마찬가지로,를 얻을 경우 `One` 이의 상태는 $ z의-1 eigenstate 임을 알 수 $ $ $ 있습니다. 이 프로세스는 "측정값을 측정 합니다." 라고 하는 Pauli 측정 언어에서 $ $ 계산 기준 측정을 수행 하는 것과 완전히 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-201">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$. This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="b1e36-202">$ \times $ Z의 단일 변환 인 2 2 행렬 $ $ 도이 조건을 충족 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-202">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="b1e36-203">즉, u $ = ^ \dagger Z u를 사용할 수도 있습니다 $ $ . 여기서 u $ 는 다른 단일 행렬을 사용 하 여 \pm 1 고유 벡터에서 측정의 두 가지 결과를 정의 하는 행렬을 제공 $ $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-203">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="b1e36-204">Pauli 측정의 표기법은 $ X, Y, Z $ 측정을 동일한 측정으로 식별 하 여이 단일 동등성을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-204">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="b1e36-205">이러한 측정은 편의를 위해 아래에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-205">These measurements are given below for convenience.</span></span>


<span data-ttu-id="b1e36-206">|Pauli 측정  | 단일 변환  |</span><span class="sxs-lookup"><span data-stu-id="b1e36-206">|Pauli Measurement  |Unitary transformation  |</span></span>
|-------------------|------------------------|
<span data-ttu-id="b1e36-207">|$ $ Z |               $\boldone$             |</span><span class="sxs-lookup"><span data-stu-id="b1e36-207">| $Z$               | $\boldone$             |</span></span>
<span data-ttu-id="b1e36-208">|$ $ X | $H               $                    |</span><span class="sxs-lookup"><span data-stu-id="b1e36-208">| $X$               | $H$                    |</span></span>
<span data-ttu-id="b1e36-209">|$ $ Y | $HS ^               {\dagger}$         |</span><span class="sxs-lookup"><span data-stu-id="b1e36-209">| $Y$               | $HS^{\dagger}$         |</span></span>

<span data-ttu-id="b1e36-210">즉,이 언어를 사용 하는 경우 "measure $ Y $ "는 HS ^를 적용 한 다음 계산 단위로 측정 하는 것과 같습니다. $ \dagger $ 여기서 [`S`](xref:Microsoft.Quantum.Intrinsic.S) 는 "단계 게이트" 라고도 하는 내장 퀀텀 연산이 며 단일 행렬에 의해 시뮬레이션 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-210">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:Microsoft.Quantum.Intrinsic.S) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

$$
\begin{align}
    <span data-ttu-id="b1e36-211">S =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="b1e36-211">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="b1e36-212">1 & 0 \\\\ 0 & i \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="b1e36-212">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="b1e36-213">다음 작업을 수행 하는 경우 $ 에도 HS ^ \dagger $ 를 퀀텀 상태 벡터에 적용 한 다음 $ Z를 측정 $ `Measure([PauliY], [q])` 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-213">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

```qsharp
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        Adjoint S(q);
        H(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

<span data-ttu-id="b1e36-214">그런 다음 계산 기준으로 다시 변환 하 여 올바른 상태를 확인할 수 있습니다 $ .이는 SH를 $ 퀀텀 상태 벡터에 적용 하는 것입니다. 위의 코드 조각에서 계산 기준으로 다시 변환 하는 것은 블록을 사용 하 여 자동으로 처리 됩니다 `within … apply` .</span><span class="sxs-lookup"><span data-stu-id="b1e36-214">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="b1e36-215">에서는 결과 Q# ---, 상태---와 상호 작용 하 여 추출 된 클래식 정보를 값 j 0으로 지정 합니다 .이 정보는 결과가 지정 된 `Result` $ \in \\ { \texttt { } \texttt { } \\ } $ $ (-1) ^ j # 연산자의 (-1) ^ j $ eigenspace에 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-215">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="b1e36-216">여러 비트 측정</span><span class="sxs-lookup"><span data-stu-id="b1e36-216">Multiple-qubit measurements</span></span>

<span data-ttu-id="b1e36-217">다음에서 볼 수 있듯이 다중 기능 비트 Pauli 연산자의 측정은 유사 하 게 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-217">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

$$
<span data-ttu-id="b1e36-218">Z \otimes z 1 0 0 0 0 = \begin{bmatrix} & & -1 0 0 0 0 & \\\\ & & & \\\\ & & -1 & 0 \\\\ & & & \end{bmatrix} 0 0 0 0 1.</span><span class="sxs-lookup"><span data-stu-id="b1e36-218">Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="b1e36-219">따라서 두 개의 Pauli-Z 연산자의 텐서 제품은 $ $ $ + 1 $ 및 $ -1 $ eigenvalues로 구성 된 두 개의 공백으로 구성 된 행렬을 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-219">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="b1e36-220">단일 고 비트 사례와 마찬가지로 두 가지 모두 반 공간을 구성 합니다 .이는 액세스 가능한 벡터 공간의 절반이 $ + 1 $ eigenspace에 속하고 나머지는 $ -1 $ eigenspace를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-220">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="b1e36-221">일반적으로 텐서 제품의 정의에서 쉽게 확인할 수 있습니다 .이는 Pauli-Z 연산자의 텐서 제품이 $ $ 고이를 따르는 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-221">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="b1e36-222">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-222">For example,</span></span>

$$
\begin{align}
    <span data-ttu-id="b1e36-223">\otimes \boldone Z =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="b1e36-223">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="b1e36-224">1 & 0 & 0 0 &\\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-224">1 &  0 &  0 &  0 \\\\</span></span>
        <span data-ttu-id="b1e36-225">0 &  1 &  0 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-225">0 &  1 &  0 &  0 \\\\</span></span>
        <span data-ttu-id="b1e36-226">0 &  0 & -1 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-226">0 &  0 & -1 &  0 \\\\</span></span>
        <span data-ttu-id="b1e36-227">0 &  0 & & -1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="b1e36-227">0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="b1e36-228">이전과 마찬가지로 이러한 매트릭스의 모든 단일 변환은 $ \pm 1 eigenvalues로 레이블이 지정 된 두 개의 반 공간에 대해서도 설명 $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-228">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="b1e36-229">예를 들어 $ \otimes = z HXH id의 x x h \otimes h (z \otimes z) h \otimes h입니다 $ $ = $ .</span><span class="sxs-lookup"><span data-stu-id="b1e36-229">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="b1e36-230">1 ~ 2 비트의 경우와 마찬가지로, $ \dagger 4 개의 \otimes \id $ $ \times $ 단일 행렬 $ u $ 에 대해 모든 2-수준 pauli 측정값을 u ^ (Z) u로 작성할 수 있습니다. 다음 표에서는 변환을 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-230">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$. We enumerate the transformations in the following table.</span></span>

> [!NOTE]
<span data-ttu-id="b1e36-231">>아래 표에서는 전환을 사용 하 여 $ \operatorname { } $ 행렬 > 을 표시 합니다.$$</span><span class="sxs-lookup"><span data-stu-id="b1e36-231">> In the table below, we use $\operatorname{SWAP}$ to indicate the matrix > $$</span></span>
<span data-ttu-id="b1e36-232">> \begin{align}</span><span class="sxs-lookup"><span data-stu-id="b1e36-232">> \begin{align}</span></span>
<span data-ttu-id="b1e36-233">>     \operatorname{교환 } &=</span><span class="sxs-lookup"><span data-stu-id="b1e36-233">>     \operatorname{SWAP} & =</span></span>
<span data-ttu-id="b1e36-234">>     \left( \begin { 행렬}</span><span class="sxs-lookup"><span data-stu-id="b1e36-234">>     \left(\begin{matrix}</span></span>
<span data-ttu-id="b1e36-235">>1 & 0 & 0 0 &\\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-235">>         1 & 0 & 0 & 0 \\\\</span></span>
<span data-ttu-id="b1e36-236">>         0 & 0 & 1 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-236">>         0 & 0 & 1 & 0 \\\\</span></span>
<span data-ttu-id="b1e36-237">>         0 & 1 & 0 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-237">>         0 & 1 & 0 & 0 \\\\</span></span>
<span data-ttu-id="b1e36-238">>0 0 0 & & & 1 > \end { 행렬 } \right ) >     \end{align}</span><span class="sxs-lookup"><span data-stu-id="b1e36-238">>         0 & 0 & 0 & 1 >     \end{matrix}\right) > \end{align}</span></span>
<span data-ttu-id="b1e36-239">> $$</span><span class="sxs-lookup"><span data-stu-id="b1e36-239">> $$</span></span>
<span data-ttu-id="b1e36-240">> 내장 작업을 시뮬레이션 하는 데 사용 [`SWAP`](xref:Microsoft.Quantum.Intrinsic) 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-240">> used to simulate the intrinsic operation [`SWAP`](xref:Microsoft.Quantum.Intrinsic).</span></span>

<span data-ttu-id="b1e36-241">|Pauli 측정     | 단일 변환  |</span><span class="sxs-lookup"><span data-stu-id="b1e36-241">|Pauli Measurement     |Unitary transformation  |</span></span>
|----------------------|------------------------|
<span data-ttu-id="b1e36-242">|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|</span><span class="sxs-lookup"><span data-stu-id="b1e36-242">| $Z\otimes \boldone$ | $\boldone\otimes \boldone$ |</span></span>
<span data-ttu-id="b1e36-243">|$ \otimes \boldone X $ | $ \otimes \boldone H $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-243">| $X\otimes \boldone$ | $H\otimes \boldone$ |</span></span>
<span data-ttu-id="b1e36-244">|$ \otimes \boldone Y $ | $ HS \dagger \otimes \boldone ^ $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-244">| $Y\otimes \boldone$ | $HS^\dagger\otimes \boldone$ |</span></span>
<span data-ttu-id="b1e36-245">|$\boldone \otimes Z $ | $ \operatorname { 교환 } $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-245">| $\boldone \otimes Z$ | $\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="b1e36-246">|$\boldone \otimes X $ | $ (H \otimes \boldone ) \operatorname { 교환 } $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-246">| $\boldone \otimes X$ | $(H\otimes \boldone)\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="b1e36-247">|$\boldone \otimes Y $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { 교환 } $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-247">| $\boldone \otimes Y$ | $(HS^\dagger\otimes \boldone)\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="b1e36-248">|$Z \otimes Z $ | $ \operatorname { cnot } \_ { 10 } $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-248">| $Z\otimes Z$ | $\operatorname{CNOT}\_{10}$ |</span></span>
<span data-ttu-id="b1e36-249">|$X \otimes Z 시간 $ | $ \operatorname { } \_ { 10 } (H \otimes \boldone ) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-249">| $X\otimes Z$ | $\operatorname{CNOT}\_{10}(H\otimes \boldone)$ |</span></span>
<span data-ttu-id="b1e36-250">|$Y \otimes Z $ | $ \operatorname { cnot } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-250">| $Y\otimes Z$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$ |</span></span>
<span data-ttu-id="b1e36-251">|$Z \otimes X $ | $ \operatorname { cnot } \_ { 10 } ( \boldone \otimes H) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-251">| $Z\otimes X$ | $\operatorname{CNOT}\_{10}(\boldone\otimes H)$ |</span></span>
<span data-ttu-id="b1e36-252">|$X \otimes X $ | $ \operatorname { cnot } \_ { 10 } (h \otimes h) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-252">| $X\otimes X$ | $\operatorname{CNOT}\_{10}(H\otimes H)$ |</span></span>
<span data-ttu-id="b1e36-253">|$Y \otimes X $ | $ \operatorname { cnot } \_ { 10 } (HS ^ \dagger \otimes H) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-253">| $Y\otimes X$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$ |</span></span>
<span data-ttu-id="b1e36-254">|$Z \otimes Y $ | $ \operatorname { cnot } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-254">| $Z\otimes Y$ | $\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$ |</span></span>
<span data-ttu-id="b1e36-255">|$X \otimes Y $ | $ \operatorname { cnot } \_ { 10 } (H \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-255">| $X\otimes Y$ | $\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$ |</span></span>
<span data-ttu-id="b1e36-256">|$Y \otimes Y $ | $ \operatorname { cnot } \_ { 10 } (hs ^ \dagger \otimes hs ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="b1e36-256">| $Y\otimes Y$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$ |</span></span>

<span data-ttu-id="b1e36-257">여기에서 [`CNOT`](xref:Microsoft.Quantum.Intrinsic.CNOT) 다음과 같은 이유로 작업이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-257">Here, the [`CNOT`](xref:Microsoft.Quantum.Intrinsic.CNOT) operation appears for the following reason.</span></span>
<span data-ttu-id="b1e36-258">행렬을 포함 하지 않는 각 pauli 측정값 $ \boldone $ 은 $ 위의 추론에 의해 단일에서 z z까지 동일 \otimes $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-258">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="b1e36-259">Z z의 고유 값는 $ \otimes $ 각 계산 기준 벡터를 구성 하는 eibit의 패리티에만 의존 하며 제어 되지 않는 연산은이 패리티를 계산 하 여 첫 번째 비트에 저장 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-259">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="b1e36-260">그런 다음 첫 번째 비트를 측정 한 후에는 Pauli 연산자를 측정 하는 것과 동일한 결과의 절반 공간 id를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-260">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="b1e36-261">한 가지 추가 참고 사항: z z 측정 $ \otimes $ 은 z 1을 순차적으로 측정 하는 것과 동일한 것으로 간주 될 수 있지만 $ \otimes \mathbb { } $ $ \mathbb { } \otimes $ 이 가정은 false가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-261">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="b1e36-262">그 이유는 $ z z 측정 \otimes $ 에서 $ $ $ 이러한 연산자의 + 1 또는-1 $ eigenstate로 퀀텀 상태를 프로젝션 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-262">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="b1e36-263">$Z \otimes \mathbb { 1을 측정 한 } $ 다음 $ \mathbb { 1 } \otimes z는 $ 퀀텀 상태 벡터를 z 1의 절반 공간에 먼저 투영 $ \otimes \mathbb { } $ 하 고 그 다음에 $ \mathbb { 1 } \otimes z $ 의 반쪽 공간으로 투영 합니다. 네 가지 계산 기준 벡터가 있으므로 두 측정값을 모두 수행 하면 상태가 1/4로 줄어들고 단일 계산 기준 벡터로 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-263">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="b1e36-264">큐비트 간의 상관 관계</span><span class="sxs-lookup"><span data-stu-id="b1e36-264">Correlations between qubits</span></span>
<span data-ttu-id="b1e36-265">X x 또는 Z z와 같은 Pauli 매트릭스의 텐서 곱을 측정 하는 또 다른 방법은 $ \otimes $ $ \otimes $ 이러한 측정을 사용 하 여 두 개의 두 비트 간 상관 관계에 저장 된 정보를 확인할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-265">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="b1e36-266">X를 측정 $ \otimes \id $ 하면 첫 번째 비트에 로컬로 저장 된 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-266">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="b1e36-267">두 유형의 측정은 모두 퀀텀 컴퓨팅에서 동일 하 게 중요 하지만, 이전에는 퀀텀 컴퓨팅의 기능을 비춥니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-267">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="b1e36-268">이는 퀀텀 컴퓨팅에서 배워야 하는 정보가 단일의 모든 비트에 저장 되지 않고 한 번에 모든 모든 기능에 로컬로 저장 되는 것이 아니라 공동 측정 (예: z z)을 통해 확인 하는 경우에만 $ \otimes $ 이 정보가 매니페스트가 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-268">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="b1e36-269">예를 들어 오류 수정에서는 보호 하려는 상태에 대 한 정보를 확인 하는 동안 발생 한 오류를 배우는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-269">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="b1e36-270">[비트 대칭 코드 샘플](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code) 에서는 $ z \otimes z \otimes \id $ 및 $ \id \otimes z \otimes z $ < 와 같은 측정을 사용 하 여이 작업을 수행할 수 있는 방법의 예를 보여 줍니다. --TODO: 비트 대칭 코드 샘플이 온-등록 인 경우 바로 샘플 브라우저에 대 한 링크를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-270">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$. <!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded.</span></span> -->

<span data-ttu-id="b1e36-271">X Y Z와 같은 임의 pauli 연산자를 $ \otimes \otimes \otimes \boldone $ 측정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-271">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="b1e36-272">이러한 모든 텐서 제품의 pauli 연산자에는 두 개의 고유 값 $ \pm 1만 있고 $ 고유 값는 전체 벡터 공간의 반 공간을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-272">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="b1e36-273">따라서 위에 명시 된 요구 사항과 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-273">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="b1e36-274">에서 Q# $ $ 측정이 기호 $ (-1) ^ j의 결과를 생성 하는 경우 이러한 측정값은 j를 반환 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="b1e36-274">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="b1e36-275">의 기본 제공 기능으로 Pauli를 측정 하 Q# 는 것은 이러한 연산자를 측정 하는 데 시간이 오래 걸릴 수 $ $ $ $ $ \id $ 있습니다 .이는 Z 및의 텐서 곱으로 작업을 표현 하는 데 필요한 diagonalizing U 게이트를 설명 하기 위해 이러한 연산자를 측정 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-275">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$.</span></span>
<span data-ttu-id="b1e36-276">이러한 미리 정의 된 측정값 중 하나를 수행 하도록 지정할 수 있으므로 계산 기준 측정이 필요한 정보를 제공 하도록를 변환 하는 방법을 걱정 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-276">By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="b1e36-277">Q# 자동으로 필요한 모든 기본 변환을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-277">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="b1e36-278">자세한 내용은 및 작업을 참조 [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) 하세요 [`MeasurePaulis`](xref:Microsoft.Quantum.Measurement.MeasurePaulis) .</span><span class="sxs-lookup"><span data-stu-id="b1e36-278">For more information, see the [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) and [`MeasurePaulis`](xref:Microsoft.Quantum.Measurement.MeasurePaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="b1e36-279">No-Cloning 정리</span><span class="sxs-lookup"><span data-stu-id="b1e36-279">The No-Cloning Theorem</span></span>

<span data-ttu-id="b1e36-280">퀀텀 정보는 강력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-280">Quantum information is powerful.</span></span>
<span data-ttu-id="b1e36-281">이를 통해 가장 잘 알려진 기존 알고리즘 보다 많은 수치를 지 원하는 것과 같은 놀라운 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-281">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="b1e36-282">그러나 퀀텀 컴퓨팅의 기능에는 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-282">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="b1e36-283">이러한 제한 사항 중 하나는 *복제 안 함 정리* 에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-283">One such limitation is given by the *No-Cloning Theorem*.</span></span>

<span data-ttu-id="b1e36-284">No-Cloning 정리는 무엇입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-284">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="b1e36-285">퀀텀 컴퓨터에의 한 일반 퀀텀 상태 복제를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-285">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="b1e36-286">정리 증명은 매우 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-286">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="b1e36-287">복제 안 함 정리에 대 한 전체 증명은 여기서 논의를 위한 약간의 기술 이지만 추가 보조 기능을 포함 하지 않는 경우에는 범위 내에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-287">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope.</span></span>

<span data-ttu-id="b1e36-288">이러한 퀀텀 컴퓨터의 경우 단일 행렬에서 복제 작업을 설명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-288">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="b1e36-289">복제 하려고 하는 퀀텀 상태를 손상 시킬 수 있으므로 측정이 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-289">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="b1e36-290">복제 작업을 시뮬레이션 하기 위해 속성을 사용 하는 데 사용 되는 단일 행렬을 원합니다. $$</span><span class="sxs-lookup"><span data-stu-id="b1e36-290">To simulate the cloning operation, we want the unitary matrix used to have the property that $$</span></span>
  <span data-ttu-id="b1e36-291">U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}</span><span class="sxs-lookup"><span data-stu-id="b1e36-291">U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
$$
<span data-ttu-id="b1e36-292">모든 상태에 대해 $ \ket { \psi } $ 입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-292">for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="b1e36-293">행렬 곱셈의 선형 속성은 두 번째 $ 퀀텀 상태의 선형 속성을 의미 \ket 합니다. { \phi } $</span><span class="sxs-lookup"><span data-stu-id="b1e36-293">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

$$
\begin{align}
    <span data-ttu-id="b1e36-294">U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}</span><span class="sxs-lookup"><span data-stu-id="b1e36-294">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="b1e36-295">&= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}</span><span class="sxs-lookup"><span data-stu-id="b1e36-295">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="b1e36-296">+ \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-296">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\</span></span>
    <span data-ttu-id="b1e36-297">&= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}</span><span class="sxs-lookup"><span data-stu-id="b1e36-297">& = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="b1e36-298">\right) \\\\</span><span class="sxs-lookup"><span data-stu-id="b1e36-298">\right) \\\\</span></span>
    <span data-ttu-id="b1e36-299">&\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ).</span><span class="sxs-lookup"><span data-stu-id="b1e36-299">& \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
\end{align}
$$

<span data-ttu-id="b1e36-300">이는 No-Cloning 정리의 기본적인 intuition을 제공 합니다. 알 수 없는 퀀텀 상태를 복사 하는 모든 장치는 복사 하는 일부 상태에서 오류를 유도 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-300">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="b1e36-301">Cloner는 입력 상태에서 선형으로 작동 하는 주요 가정을 추가 하 고 보조 비트를 측정 하 여 위반할 수 있지만 이러한 상호 작용은 측정 통계를 통해 시스템에 대 한 정보를 누출 하 고 이러한 경우에도 정확한 복제를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-301">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="b1e36-302">No-Cloning에 대 한 자세한 [내용은](xref:microsoft.quantum.more-information)정리을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1e36-302">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="b1e36-303">No-Cloning 정리는 퀀텀 상태 저렴를 복제할 수 있는 경우 퀀텀 상태에서 배울 수 있는 근거리 마법의 기능을 제공 하기 때문에 퀀텀 컴퓨팅에 대 한 정 성적 이해에 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-303">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="b1e36-304">정말 Heisenberg의 vaunted 불확실성 원칙을 위반할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-304">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="b1e36-305">또는 최적의 cloner를 사용 하 여 복잡 한 퀀텀 배포에서 단일 샘플을 가져오고 한 샘플에서 해당 배포에 대해 알아볼 수 있는 모든 것을 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-305">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="b1e36-306">이는 동전 및 관찰 헤드를 대칭 이동 하는 것과 마찬가지로 "Ah가 해당 동전의 분포는 $ p = 0.512643 \ ldots!"를 통해 베르누이 되어야 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="b1e36-306">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="b1e36-307">한 가지 정보 (헤드 결과)가 상당한 이전 정보 없이 배포를 인코딩하는 데 필요한 많은 양의 정보를 제공할 수 없기 때문에 이러한 문은 sensical 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-307">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="b1e36-308">마찬가지로, 이전 정보가 없으면 p를 몰라도 이러한 동전의 앙상블를 준비할 수 없기 때문에 퀀텀 상태를 완벽 하 게 복제할 수 없습니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="b1e36-308">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="b1e36-309">정보는 퀀텀 컴퓨팅에서 무료로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-309">Information is not free in quantum computing.</span></span>
<span data-ttu-id="b1e36-310">측정 된 각는 단일 비트 정보를 제공 하 고, No-Cloning 정리는 시스템 및 해당 시스템에 대해 발생 하는 파업에 대 한 정보 간의 기본적인 균형을 유지 하기 위해 악용할 수 있는 백도어가 없다는 것을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1e36-310">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
