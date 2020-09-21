---
<span data-ttu-id="0304c-101">제목: 퀀텀 oracles 설명: 다른 알고리즘에 대 한 입력으로 사용 되는 퀀텀 oracles 및 블랙 박스 작업을 사용 하 고 정의 하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-101">title: Quantum oracles description: Learn how to work with and define quantum oracles, black box operations that are used as input to another algorithm.</span></span>
<span data-ttu-id="0304c-102">작성자: cgranade uid: oracles. author: chgranad: 07/11/2018 밀리초. 토픽: 문서 번호:</span><span class="sxs-lookup"><span data-stu-id="0304c-102">author: cgranade uid: microsoft.quantum.concepts.oracles ms.author: chgranad ms.date: 07/11/2018 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="0304c-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="0304c-103">"Q#"</span></span>
- <span data-ttu-id="0304c-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="0304c-104">"$$v"</span></span>
- <span data-ttu-id="0304c-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="0304c-105">"$$"</span></span>
- <span data-ttu-id="0304c-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="0304c-106">"$$"</span></span>
- <span data-ttu-id="0304c-107">"$"</span><span class="sxs-lookup"><span data-stu-id="0304c-107">"$"</span></span>
- <span data-ttu-id="0304c-108">"$"</span><span class="sxs-lookup"><span data-stu-id="0304c-108">"$"</span></span>
- <span data-ttu-id="0304c-109">"$"</span><span class="sxs-lookup"><span data-stu-id="0304c-109">"$"</span></span>
- <span data-ttu-id="0304c-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="0304c-110">"$$"</span></span>
- <span data-ttu-id="0304c-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="0304c-111">"\cdots"</span></span>
- <span data-ttu-id="0304c-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="0304c-112">"bmatrix"</span></span>
- <span data-ttu-id="0304c-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="0304c-113">"\ddots"</span></span>
- <span data-ttu-id="0304c-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="0304c-114">"\equiv"</span></span>
- <span data-ttu-id="0304c-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="0304c-115">"\sum"</span></span>
- <span data-ttu-id="0304c-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="0304c-116">"\begin"</span></span>
- <span data-ttu-id="0304c-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="0304c-117">"\end"</span></span>
- <span data-ttu-id="0304c-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="0304c-118">"\sqrt"</span></span>
- <span data-ttu-id="0304c-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="0304c-119">"\otimes"</span></span>
- <span data-ttu-id="0304c-120">"{"</span><span class="sxs-lookup"><span data-stu-id="0304c-120">"{"</span></span>
- <span data-ttu-id="0304c-121">"}"</span><span class="sxs-lookup"><span data-stu-id="0304c-121">"}"</span></span>
- <span data-ttu-id="0304c-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="0304c-122">"\text"</span></span>
- <span data-ttu-id="0304c-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="0304c-123">"\phi"</span></span>
- <span data-ttu-id="0304c-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="0304c-124">"\kappa"</span></span>
- <span data-ttu-id="0304c-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="0304c-125">"\psi"</span></span>
- <span data-ttu-id="0304c-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="0304c-126">"\alpha"</span></span>
- <span data-ttu-id="0304c-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="0304c-127">"\beta"</span></span>
- <span data-ttu-id="0304c-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="0304c-128">"\gamma"</span></span>
- <span data-ttu-id="0304c-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="0304c-129">"\delta"</span></span>
- <span data-ttu-id="0304c-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="0304c-130">"\omega"</span></span>
- <span data-ttu-id="0304c-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="0304c-131">"\bra"</span></span>
- <span data-ttu-id="0304c-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="0304c-132">"\ket"</span></span>
- <span data-ttu-id="0304c-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="0304c-133">"\boldone"</span></span>
- <span data-ttu-id="0304c-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="0304c-134">"\\\\"</span></span>
- <span data-ttu-id="0304c-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="0304c-135">"\\"</span></span>
- <span data-ttu-id="0304c-136">"="</span><span class="sxs-lookup"><span data-stu-id="0304c-136">"="</span></span>
- <span data-ttu-id="0304c-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="0304c-137">"\frac"</span></span>
- <span data-ttu-id="0304c-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="0304c-138">"\text"</span></span>
- <span data-ttu-id="0304c-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="0304c-139">"\mapsto"</span></span>
- <span data-ttu-id="0304c-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="0304c-140">"\dagger"</span></span>
- <span data-ttu-id="0304c-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="0304c-141">"\to"</span></span>
- <span data-ttu-id="0304c-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="0304c-142">"\begin{cases}"</span></span>
- <span data-ttu-id="0304c-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="0304c-143">"\end{cases}"</span></span>
- <span data-ttu-id="0304c-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="0304c-144">"\operatorname"</span></span>
- <span data-ttu-id="0304c-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="0304c-145">"\braket"</span></span>
- <span data-ttu-id="0304c-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="0304c-146">"\id"</span></span>
- <span data-ttu-id="0304c-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="0304c-147">"\expect"</span></span>
- <span data-ttu-id="0304c-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="0304c-148">"\defeq"</span></span>
- <span data-ttu-id="0304c-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="0304c-149">"\variance"</span></span>
- <span data-ttu-id="0304c-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="0304c-150">"\dd"</span></span>
- <span data-ttu-id="0304c-151">"&"</span><span class="sxs-lookup"><span data-stu-id="0304c-151">"&"</span></span>
- <span data-ttu-id="0304c-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="0304c-152">"\begin{align}"</span></span>
- <span data-ttu-id="0304c-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="0304c-153">"\end{align}"</span></span>
- <span data-ttu-id="0304c-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="0304c-154">"\Lambda"</span></span>
- <span data-ttu-id="0304c-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="0304c-155">"\lambda"</span></span>
- <span data-ttu-id="0304c-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="0304c-156">"\Omega"</span></span>
- <span data-ttu-id="0304c-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="0304c-157">"\mathrm"</span></span>
- <span data-ttu-id="0304c-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="0304c-158">"\left"</span></span>
- <span data-ttu-id="0304c-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="0304c-159">"\right"</span></span>
- <span data-ttu-id="0304c-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="0304c-160">"\qquad"</span></span>
- <span data-ttu-id="0304c-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="0304c-161">"\times"</span></span>
- <span data-ttu-id="0304c-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="0304c-162">"\big"</span></span>
- <span data-ttu-id="0304c-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="0304c-163">"\langle"</span></span>
- <span data-ttu-id="0304c-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="0304c-164">"\rangle"</span></span>
- <span data-ttu-id="0304c-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="0304c-165">"\bigg"</span></span>
- <span data-ttu-id="0304c-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="0304c-166">"\Big"</span></span>
- <span data-ttu-id="0304c-167">"|"</span><span class="sxs-lookup"><span data-stu-id="0304c-167">"|"</span></span>
- <span data-ttu-id="0304c-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="0304c-168">"\mathbb"</span></span>
- <span data-ttu-id="0304c-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="0304c-169">"\vec"</span></span>
- <span data-ttu-id="0304c-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="0304c-170">"\in"</span></span>
- <span data-ttu-id="0304c-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="0304c-171">"\texttt"</span></span>
- <span data-ttu-id="0304c-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="0304c-172">"\ne"</span></span>
- <span data-ttu-id="0304c-173">"<"</span><span class="sxs-lookup"><span data-stu-id="0304c-173">"<"</span></span>
- <span data-ttu-id="0304c-174">">"</span><span class="sxs-lookup"><span data-stu-id="0304c-174">">"</span></span>
- <span data-ttu-id="0304c-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="0304c-175">"\leq"</span></span>
- <span data-ttu-id="0304c-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="0304c-176">"\geq"</span></span>
- <span data-ttu-id="0304c-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="0304c-177">"~~"</span></span>
- <span data-ttu-id="0304c-178">"~"</span><span class="sxs-lookup"><span data-stu-id="0304c-178">"~"</span></span>
- <span data-ttu-id="0304c-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="0304c-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="0304c-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="0304c-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="0304c-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="0304c-181">"\_"</span></span>

---
# <a name="quantum-oracles"></a><span data-ttu-id="0304c-182">퀀텀 Oracles</span><span class="sxs-lookup"><span data-stu-id="0304c-182">Quantum Oracles</span></span>

<span data-ttu-id="0304c-183">Oracle $ O는 $ 다른 알고리즘에 대 한 입력으로 사용 되는 "블랙 박스" 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-183">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="0304c-184">이러한 작업은 일반적으로 $ f: \\ { 0, 1 \\ } ^ n 0, 1 ^ m을 사용 하 여 정의 되며 \to \\ { \\ } $ $ n $ 비트 이진 입력을 사용 하 고 $ m $ 비트 이진 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-184">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="0304c-185">이렇게 하려면 특정 이진 입력 $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1)를 고려 } $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-185">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="0304c-186">$ \ket { \vec { } } = \ket { X_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 } } $ 을 x로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-186">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="0304c-187">처음에 $ $ 는 $ o \ket { x f (x)로 o를 정의 하려고 시도할 수 } = \ket { } $ 있지만 여기에는 몇 가지 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-187">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="0304c-188">첫째, $ f에 $ 는 다른 크기의 입력 및 출력 (n m)이 있을 수 있습니다 $ \ne $ .이 경우 O를 적용 하면 $ $ 레지스터의 원하는 비트 수가 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-188">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="0304c-189">둘째, n m 인 경우에도 $ = $ 함수는 반전할 수 없습니다. $ x (x) = f (y) $ 가 일부 $ x y 이면 \ne $ $ o x o y는 o ^ \ket o { } = \ket { } $ $ \dagger \ket { } \ne \dagger \ket { } $ x o ^ o y입니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-189">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="0304c-190">즉, adjoint 작업 $ O ^를 생성할 수 \dagger $ 없고 oracles에 대해 adjoint가 정의 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-190">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="0304c-191">계산 기준 상태에 영향을 미치는 oracle 정의</span><span class="sxs-lookup"><span data-stu-id="0304c-191">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="0304c-192">$ $ 답변을 유지 하기 위해 두 번째 레지스터를 도입 하 여 이러한 문제를 모두 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-192">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="0304c-193">그런 다음 모든 계산 기반 상태에 oracle의 효과를 정의 합니다. 모든 $ x \in \\ { 0, 1 \\ } ^ n $ 및 $ y \in \\ { 0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="0304c-193">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

$$
\begin{align}
    <span data-ttu-id="0304c-194">O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="0304c-194">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

<span data-ttu-id="0304c-195">이제 $ = 생성을 통해 o o ^ ^ ^ \dagger $ 이 (가) 이전 문제를 모두 해결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-195">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
<span data-ttu-id="0304c-196">>$O = o ^ ^ ^ 2를 확인 하려면 { \dagger } $ $ = \boldone $ $ 모든 a에 대해 \oplus b \oplus a와 b a를 모두 포함 하 여 o ^ 2를 확인 = $ $ 합니다. b \in \: :: 비 loc ({)::: 0, 1 \: :: no loc (})::: $</span><span class="sxs-lookup"><span data-stu-id="0304c-196">> To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
<span data-ttu-id="0304c-197">>결과적으로 $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ 입니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-197">> As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="0304c-198">중요 한 점은 각 계산 기준 상태에 대해 oracle을 정의 $ \ket { } \ket { } $ 하는 것은 $ $ 다른 모든 상태에 대해 O가 작동 하는 방식도 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-198">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="0304c-199">이는 $ $ 모든 퀀텀 작업과 같이 O가 작동 하는 상태에서 선형 이라는 점에서 즉시 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-199">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="0304c-200">예를 들어 $ h \ket { 0 } = \ket { + } $ 및 $ h \ket { 1 } = \ket { - } $ 로 정의 되는 Hadamard 작업을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-200">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="0304c-201">H가 어떻게 작동 하는지 알고 $ 싶으면 $ h를 $ \ket { + } $ $ $ 선형으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-201">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

$$
\begin{align}
<span data-ttu-id="0304c-202">H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\</span><span class="sxs-lookup"><span data-stu-id="0304c-202">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\</span></span>
           <span data-ttu-id="0304c-203">&= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .</span><span class="sxs-lookup"><span data-stu-id="0304c-203">& = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
\end{align}
$$

<span data-ttu-id="0304c-204">Oracle O를 정의 하는 경우에는 $ $ $ \ket { \psi } $ n + m의 모든 상태를 $ $ 로 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-204">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

$$
\begin{align}
<span data-ttu-id="0304c-205">\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}</span><span class="sxs-lookup"><span data-stu-id="0304c-205">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
\end{align}
$$

<span data-ttu-id="0304c-206">where $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C는 } $ 상태의 계수를 나타냅니다 $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="0304c-206">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="0304c-207">그러므로</span><span class="sxs-lookup"><span data-stu-id="0304c-207">Thus,</span></span>

$$
\begin{align}
<span data-ttu-id="0304c-208">O \ket { \psi } & = o \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) o \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\</span><span class="sxs-lookup"><span data-stu-id="0304c-208">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\</span></span>
             <span data-ttu-id="0304c-209">&= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="0304c-209">& = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

## <a name="phase-oracles"></a><span data-ttu-id="0304c-210">Oracles 단계</span><span class="sxs-lookup"><span data-stu-id="0304c-210">Phase oracles</span></span>
<span data-ttu-id="0304c-211">또는 O에 대 한 $ $ $ $ 입력에 따라 _단계_ 를 적용 하 여 f를 oracle O로 $ $ 인코딩할 수 있습니다. 예를 들어, $ $$$</span><span class="sxs-lookup"><span data-stu-id="0304c-211">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$. For instance, we might define $O$ such that $$</span></span>
\begin{align}
    <span data-ttu-id="0304c-212">O \ket { x } = (-1) ^ { f (x) } \ket { x } .</span><span class="sxs-lookup"><span data-stu-id="0304c-212">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
\end{align}
$$
<span data-ttu-id="0304c-213">Oracle 단계가 초기에 계산 기준 상태 x로 작동 하는 경우 $ \ket { } $ 이 단계는 글로벌 단계 이므로 관찰 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-213">If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="0304c-214">그러나 이러한 oracle은 superposition에 적용 되거나 제어 된 작업으로 적용 되는 경우 매우 강력한 리소스가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-214">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="0304c-215">예를 들어 $ $ 단일 기능 비트 함수 f의 oracle O_f 단계를 살펴보겠습니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="0304c-215">For example, consider a phase oracle $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="0304c-216">다음 $$</span><span class="sxs-lookup"><span data-stu-id="0304c-216">Then, $$</span></span>
\begin{align}
    <span data-ttu-id="0304c-217">O_f \ket{+}</span><span class="sxs-lookup"><span data-stu-id="0304c-217">O_f \ket{+}</span></span>
        <span data-ttu-id="0304c-218">&=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="0304c-218">& = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="0304c-219">&=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="0304c-219">& = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="0304c-220">&=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="0304c-220">& = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="0304c-221">&=(-1) ^ { f (0) } z ^ { f (0)-f (1) } \ket { + } .</span><span class="sxs-lookup"><span data-stu-id="0304c-221">& = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
\end{align}
$$

<span data-ttu-id="0304c-222">보다 일반적으로는 oracles의 두 뷰를 넓혔습니다 하 여 단일 비트만이 아닌 실수를 반환 하는 클래식 함수를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-222">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="0304c-223">Oracle을 구현 하는 가장 좋은 방법은 지정 된 알고리즘 내에서이 oracle을 사용 하는 방법에 따라 크게 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-223">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="0304c-224">예를 들어 [Deutsch-Jozsa 알고리즘](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) 은 첫 번째 방법으로 구현 된 oracle을 사용 하는 반면 [Grover의 알고리즘](https://en.wikipedia.org/wiki/Grover's_algorithm) 은 두 번째 방법으로 구현 된 oracle에 의존 합니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-224">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="0304c-225">자세한 내용은 [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465)에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0304c-225">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
