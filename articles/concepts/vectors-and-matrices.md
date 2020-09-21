---
<span data-ttu-id="22144-101">제목: 퀀텀 계산의 벡터 및 행렬 설명: 벡터 및 매트릭스를 사용 하는 방법에 대 한 기본 사항을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="22144-101">title: Vectors and matrices in quantum computing description: Learn the basics of how to work with vectors and matrices.</span></span>
<span data-ttu-id="22144-102">작성자: QuantumWriter uid: benbra: 12/11/2017. 날짜: 밀리초. 토픽: 문서 번호-loc:</span><span class="sxs-lookup"><span data-stu-id="22144-102">author: QuantumWriter uid: microsoft.quantum.concepts.vectors ms.author: v-benbra ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="22144-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="22144-103">"Q#"</span></span>
- <span data-ttu-id="22144-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="22144-104">"$$v"</span></span>
- <span data-ttu-id="22144-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="22144-105">"$$"</span></span>
- <span data-ttu-id="22144-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="22144-106">"$$"</span></span>
- <span data-ttu-id="22144-107">"$"</span><span class="sxs-lookup"><span data-stu-id="22144-107">"$"</span></span>
- <span data-ttu-id="22144-108">"$"</span><span class="sxs-lookup"><span data-stu-id="22144-108">"$"</span></span>
- <span data-ttu-id="22144-109">"$"</span><span class="sxs-lookup"><span data-stu-id="22144-109">"$"</span></span>
- <span data-ttu-id="22144-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="22144-110">"$$"</span></span>
- <span data-ttu-id="22144-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="22144-111">"\cdots"</span></span>
- <span data-ttu-id="22144-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="22144-112">"bmatrix"</span></span>
- <span data-ttu-id="22144-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="22144-113">"\ddots"</span></span>
- <span data-ttu-id="22144-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="22144-114">"\equiv"</span></span>
- <span data-ttu-id="22144-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="22144-115">"\sum"</span></span>
- <span data-ttu-id="22144-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="22144-116">"\begin"</span></span>
- <span data-ttu-id="22144-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="22144-117">"\end"</span></span>
- <span data-ttu-id="22144-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="22144-118">"\sqrt"</span></span>
- <span data-ttu-id="22144-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="22144-119">"\otimes"</span></span>
- <span data-ttu-id="22144-120">"{"</span><span class="sxs-lookup"><span data-stu-id="22144-120">"{"</span></span>
- <span data-ttu-id="22144-121">"}"</span><span class="sxs-lookup"><span data-stu-id="22144-121">"}"</span></span>
- <span data-ttu-id="22144-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="22144-122">"\text"</span></span>
- <span data-ttu-id="22144-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="22144-123">"\phi"</span></span>
- <span data-ttu-id="22144-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="22144-124">"\kappa"</span></span>
- <span data-ttu-id="22144-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="22144-125">"\psi"</span></span>
- <span data-ttu-id="22144-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="22144-126">"\alpha"</span></span>
- <span data-ttu-id="22144-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="22144-127">"\beta"</span></span>
- <span data-ttu-id="22144-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="22144-128">"\gamma"</span></span>
- <span data-ttu-id="22144-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="22144-129">"\delta"</span></span>
- <span data-ttu-id="22144-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="22144-130">"\omega"</span></span>
- <span data-ttu-id="22144-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="22144-131">"\bra"</span></span>
- <span data-ttu-id="22144-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="22144-132">"\ket"</span></span>
- <span data-ttu-id="22144-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="22144-133">"\boldone"</span></span>
- <span data-ttu-id="22144-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="22144-134">"\\\\"</span></span>
- <span data-ttu-id="22144-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="22144-135">"\\"</span></span>
- <span data-ttu-id="22144-136">"="</span><span class="sxs-lookup"><span data-stu-id="22144-136">"="</span></span>
- <span data-ttu-id="22144-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="22144-137">"\frac"</span></span>
- <span data-ttu-id="22144-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="22144-138">"\text"</span></span>
- <span data-ttu-id="22144-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="22144-139">"\mapsto"</span></span>
- <span data-ttu-id="22144-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="22144-140">"\dagger"</span></span>
- <span data-ttu-id="22144-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="22144-141">"\to"</span></span>
- <span data-ttu-id="22144-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="22144-142">"\begin{cases}"</span></span>
- <span data-ttu-id="22144-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="22144-143">"\end{cases}"</span></span>
- <span data-ttu-id="22144-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="22144-144">"\operatorname"</span></span>
- <span data-ttu-id="22144-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="22144-145">"\braket"</span></span>
- <span data-ttu-id="22144-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="22144-146">"\id"</span></span>
- <span data-ttu-id="22144-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="22144-147">"\expect"</span></span>
- <span data-ttu-id="22144-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="22144-148">"\defeq"</span></span>
- <span data-ttu-id="22144-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="22144-149">"\variance"</span></span>
- <span data-ttu-id="22144-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="22144-150">"\dd"</span></span>
- <span data-ttu-id="22144-151">"&"</span><span class="sxs-lookup"><span data-stu-id="22144-151">"&"</span></span>
- <span data-ttu-id="22144-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="22144-152">"\begin{align}"</span></span>
- <span data-ttu-id="22144-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="22144-153">"\end{align}"</span></span>
- <span data-ttu-id="22144-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="22144-154">"\Lambda"</span></span>
- <span data-ttu-id="22144-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="22144-155">"\lambda"</span></span>
- <span data-ttu-id="22144-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="22144-156">"\Omega"</span></span>
- <span data-ttu-id="22144-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="22144-157">"\mathrm"</span></span>
- <span data-ttu-id="22144-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="22144-158">"\left"</span></span>
- <span data-ttu-id="22144-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="22144-159">"\right"</span></span>
- <span data-ttu-id="22144-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="22144-160">"\qquad"</span></span>
- <span data-ttu-id="22144-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="22144-161">"\times"</span></span>
- <span data-ttu-id="22144-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="22144-162">"\big"</span></span>
- <span data-ttu-id="22144-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="22144-163">"\langle"</span></span>
- <span data-ttu-id="22144-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="22144-164">"\rangle"</span></span>
- <span data-ttu-id="22144-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="22144-165">"\bigg"</span></span>
- <span data-ttu-id="22144-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="22144-166">"\Big"</span></span>
- <span data-ttu-id="22144-167">"|"</span><span class="sxs-lookup"><span data-stu-id="22144-167">"|"</span></span>
- <span data-ttu-id="22144-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="22144-168">"\mathbb"</span></span>
- <span data-ttu-id="22144-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="22144-169">"\vec"</span></span>
- <span data-ttu-id="22144-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="22144-170">"\in"</span></span>
- <span data-ttu-id="22144-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="22144-171">"\texttt"</span></span>
- <span data-ttu-id="22144-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="22144-172">"\ne"</span></span>
- <span data-ttu-id="22144-173">"<"</span><span class="sxs-lookup"><span data-stu-id="22144-173">"<"</span></span>
- <span data-ttu-id="22144-174">">"</span><span class="sxs-lookup"><span data-stu-id="22144-174">">"</span></span>
- <span data-ttu-id="22144-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="22144-175">"\leq"</span></span>
- <span data-ttu-id="22144-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="22144-176">"\geq"</span></span>
- <span data-ttu-id="22144-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="22144-177">"~~"</span></span>
- <span data-ttu-id="22144-178">"~"</span><span class="sxs-lookup"><span data-stu-id="22144-178">"~"</span></span>
- <span data-ttu-id="22144-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="22144-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="22144-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="22144-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="22144-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="22144-181">"\_"</span></span>

---

# <a name="vectors-and-matrices"></a><span data-ttu-id="22144-182">벡터 및 행렬</span><span class="sxs-lookup"><span data-stu-id="22144-182">Vectors and Matrices</span></span>

<span data-ttu-id="22144-183">몇 가지 벡터와 행렬에 대해 잘 알고 있는 것은 퀀텀 컴퓨팅을 이해 하는 데 필수적입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-183">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="22144-184">아래에서 간략하게 소개 하 고 관심 있는 독자는 *Strang, G. (1993)와 같은 선형 대 수 표준 참조를 읽는 것이 좋습니다. 선형 대 수 (Vol. 3)에 대해 소개 합니다. Wellesley, MA: Wellesley-캠브리지* 또는 [Linear 대 수](http://joshua.smcvt.edu/linearalgebra/)같은 온라인 참조를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="22144-184">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="22144-185">차원 (또는 크기)의 열 벡터 (또는 단순한 [*벡터*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ v는 $ $ $ $ $ $ $ 열로 정렬 된 n 복소수 (v_1, v_2, \ldots, v_n)의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-185">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="22144-186">$$v =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-186">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="22144-187">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-187">v_1\\\\</span></span>
<span data-ttu-id="22144-188">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-188">v_2\\\\</span></span>
<span data-ttu-id="22144-189">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-189">\vdots\\\\</span></span>
<span data-ttu-id="22144-190">v_n \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="22144-190">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="22144-191">벡터 $ v는 $ $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $ 로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22144-191">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="22144-192">벡터가 1 인 경우 벡터는 unit (또는 [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)라고 함) 이라고 합니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="22144-192">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="22144-193">[*벡터 v의 adjoint*](https://en.wikipedia.org/wiki/Adjoint_matrix) 는 $ $ $ v ^로 표시 되며 \dagger $ 은 $ \* $ 복소수 복소수를 나타내는 다음 행 벡터로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22144-193">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="22144-194">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ \* & \cdots & v_n ^ \*\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="22144-194">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="22144-195">두 벡터를 하나로 곱하는 가장 일반적인 방법은 점 제품이 라고도 하는 [*내부 제품*](https://en.wikipedia.org/wiki/Inner_product_space)을 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-195">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="22144-196">내부 제품은 한 벡터의 프로젝션을 다른 벡터에 제공 하며, 한 벡터를 다른 간단한 벡터의 합계로 표현 하는 방법을 설명 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22144-196">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="22144-197">U $ , v를 표시 하는 u와 v 사이의 내부 곱 $ $ $ $ \left \langle \right \rangle $ 은로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22144-197">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

$$
<span data-ttu-id="22144-198">\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="22144-198">\langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="22144-199">이 표기법을 사용 하면 벡터 $ v를 $ $ \sqrt { \langle v, v \rangle } $ 로 작성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-199">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="22144-200">벡터와 숫자 c를 곱하여 $ $ 해당 항목에 c를 곱한 새 벡터를 만들 수 있습니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="22144-200">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="22144-201">U 및 v 라는 두 개의 $ 벡터 $ 를 추가 하 여 $ $ 항목이 $ u 및 v 항목의 합계인 새 벡터를 $ $ $ 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-201">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="22144-202">이러한 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-202">These operations are depicted below:</span></span>

<span data-ttu-id="22144-203">$$\mathrm{U 인 경우 } ~=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-203">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="22144-204">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-204">u_1\\\\</span></span>
<span data-ttu-id="22144-205">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-205">u_2\\\\</span></span>
<span data-ttu-id="22144-206">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-206">\vdots\\\\</span></span>
<span data-ttu-id="22144-207">u_n \end{bmatrix} ~ \mathrm { 및}~</span><span class="sxs-lookup"><span data-stu-id="22144-207">u_n \end{bmatrix}~\mathrm{and}~</span></span>
<span data-ttu-id="22144-208">hyper-v =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-208">v =\begin{bmatrix}</span></span>
    <span data-ttu-id="22144-209">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-209">v_1\\\\</span></span>
    <span data-ttu-id="22144-210">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-210">v_2\\\\</span></span>
    <span data-ttu-id="22144-211">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-211">\vdots\\\\</span></span>
    <span data-ttu-id="22144-212">v_n \end{bmatrix} ~ \mathrm { 다음}~</span><span class="sxs-lookup"><span data-stu-id="22144-212">v_n \end{bmatrix},~\mathrm{then}~</span></span>
<span data-ttu-id="22144-213">오스트레일리아 + bv =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-213">au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="22144-214">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-214">au_1+bv_1\\\\</span></span>
<span data-ttu-id="22144-215">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-215">au_2+bv_2\\\\</span></span>
<span data-ttu-id="22144-216">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-216">\vdots\\\\</span></span>
<span data-ttu-id="22144-217">au_n + bv_n \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="22144-217">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="22144-218">크기 [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) $ m n의 행렬 \times $ 은 아래와 $ $ $ $ 같이 m 행과 $ n 개의 $ 열로 정렬 된 mn 복소수의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-218">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="22144-219">$$매 =</span><span class="sxs-lookup"><span data-stu-id="22144-219">$$M =</span></span> 
\begin{bmatrix}
<span data-ttu-id="22144-220">M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1n}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-220">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
<span data-ttu-id="22144-221">M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-221">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="22144-222">M_ { m1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { mn}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-222">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\</span></span>
<span data-ttu-id="22144-223">\end{bmatrix}.$$</span><span class="sxs-lookup"><span data-stu-id="22144-223">\end{bmatrix}.$$</span></span>

<span data-ttu-id="22144-224">차원 n의 벡터는 $ $ 단순히 n 1 크기의 행렬입니다 $ \times $ .</span><span class="sxs-lookup"><span data-stu-id="22144-224">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="22144-225">벡터와 마찬가지로 행렬을 숫자 c와 곱하여 $ $ 모든 항목에 c를 곱한 새 행렬을 얻을 수 $ 있으며, $ 동일한 크기의 두 행렬을 추가 하 여 해당 항목이 두 행렬의 각 항목의 합계인 새 행렬을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-225">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="22144-226">행렬 곱하기 및 텐서 제품</span><span class="sxs-lookup"><span data-stu-id="22144-226">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="22144-227">또한 다음과 같이 dimension m n 및 n 차원의 두 행렬 m을 곱하여 $ $ $ \times $ $ $ $ n \times p 차원의 $ 새 매트릭스 p를 $ 가져올 $ $ \times $ 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-227">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

\begin{align}
&\begin{bmatrix}
    <span data-ttu-id="22144-228">M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1n}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-228">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
    <span data-ttu-id="22144-229">M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-229">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
    \ddots\\\\
    <span data-ttu-id="22144-230">M_ { m1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { mn}</span><span class="sxs-lookup"><span data-stu-id="22144-230">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
\end{bmatrix}
\begin{bmatrix}
<span data-ttu-id="22144-231">N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1 p}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-231">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\</span></span>
<span data-ttu-id="22144-232">N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2p}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-232">N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="22144-233">N_ { n1 } ~~ N_ { n2 } ~~ \cdots ~~ N_ { np}</span><span class="sxs-lookup"><span data-stu-id="22144-233">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
\end{bmatrix}=\begin{bmatrix}
<span data-ttu-id="22144-234">P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1 p}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-234">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\</span></span>
<span data-ttu-id="22144-235">P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2p}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-235">P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="22144-236">P_ { m1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { mp}</span><span class="sxs-lookup"><span data-stu-id="22144-236">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
\end{bmatrix}
\end{align}

<span data-ttu-id="22144-237">여기서 P의 항목 $ 은 $ $ { ik } = \sum _j M_ { ij } N_ jk P_ { } $ .</span><span class="sxs-lookup"><span data-stu-id="22144-237">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="22144-238">예를 들어 $ P_ 11 항목 { 은 } $ $ $ N의 첫 번째 열을 가진 M의 첫 번째 행의 내부 곱 $ 입니다 $ . 벡터는 단순히 행렬의 특별 한 사례 이므로이 정의는 행렬-벡터 곱셈으로 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22144-238">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$. Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="22144-239">이를 고려 하는 모든 행렬은 행과 열 수가 같거나 벡터 (1 개 열에만 해당) 인 정사각형 행렬입니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="22144-239">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="22144-240">하나의 특수 사각형 행렬은 [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix) $ \boldone $ 모든 대각선 요소를 1로, $ $ 나머지 요소를 0으로 $ $ 유지 하는 id 매트릭스입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-240">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

$$\boldone=\begin{bmatrix}
<span data-ttu-id="22144-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="22144-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="22144-243">~~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-243">~~ \ddots\\\\</span></span>
<span data-ttu-id="22144-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$</span><span class="sxs-lookup"><span data-stu-id="22144-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="22144-245">사각형 행렬 a의 $ $ $ 경우 B 행렬은 $ AB BA 인 경우 [*역*](https://en.wikipedia.org/wiki/Invertible_matrix) 이라고 $ = = \boldone $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="22144-245">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="22144-246">행렬의 역은 존재 하지 않아도 되지만, 존재 하는 경우에는 고유 하 고 $ ^ { -1을 나타냅니다 } $ .</span><span class="sxs-lookup"><span data-stu-id="22144-246">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="22144-247">모든 matrix $ m $ 에서 m의 adjoint 또는 복소수는 $ $ $ $ $ N_ { ij } = M_ { ji } ^ \* $ 하는 행렬 N입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-247">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="22144-248">M의 adjoint $ 는 $ 보통 m ^로 표시 됩니다 $ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="22144-248">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="22144-249">$ $ [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) $ UU ^ u \dagger = ^ \dagger u = \boldone $ 또는 동등 ( $ u ^ { -1 } = u ^ \dagger $ ) 인 경우에는 행렬 u가 단일 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22144-249">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="22144-250">단일 매트릭스의 가장 중요 한 속성은 벡터의 표준을 유지 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-250">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="22144-251">이는 다음과 같은 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="22144-251">This happens because</span></span> 

<span data-ttu-id="22144-252">$$\langlev, v v \rangle = ^ \dagger v = v ^ \dagger u ^ { -1 } u v = v ^ u ^ u v \dagger \dagger = \langle , u v \rangle .$$</span><span class="sxs-lookup"><span data-stu-id="22144-252">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="22144-253">$ $ M m ^ 인 경우 행렬 m은 [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) 라고 $ = \dagger $ 합니다.</span><span class="sxs-lookup"><span data-stu-id="22144-253">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="22144-254">마지막으로, 크기가 m n 및 n 인 두 행렬 m의 [*텐서 product*](https://en.wikipedia.org/wiki/Tensor_product) (또는 Kronecker product)는 $ $ $ \times $ $ $ $ \times $ $ 크기 mp nq의 더 큰 행렬 p = m n 이며 다음과 \otimes $ $ \times $ $ $ 같이 m과 n에서 가져옵니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="22144-254">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

\begin{align}
    <span data-ttu-id="22144-255">M \otimes N &=</span><span class="sxs-lookup"><span data-stu-id="22144-255">M \otimes N &=</span></span>
    \begin{bmatrix}
        <span data-ttu-id="22144-256">M_ { 11 } ~~ \cdots ~~ M_ { 1n }\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-256">M_{11} ~~ \cdots ~~ M_{1n} \\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="22144-257">M_ { m1 } ~~ \cdots ~~ M_ { mn  }</span><span class="sxs-lookup"><span data-stu-id="22144-257">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        <span data-ttu-id="22144-258">N_ { 11 } ~~ \cdots ~~ N_ { 1q  }\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-258">N_{11}  ~~ \cdots ~~ N_{1q}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="22144-259">N_ { p1 } ~~ \cdots ~~ N_ { pq}</span><span class="sxs-lookup"><span data-stu-id="22144-259">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        <span data-ttu-id="22144-260">M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1q } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="22144-260">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="22144-261">M_ { 1n } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1n } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-261">M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="22144-262">M_ { m1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1q } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="22144-262">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="22144-263">M_ { mn } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1q } \\\\ \ddots \\\\ N_ { p1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-263">M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="22144-264">\end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="22144-264">\end{bmatrix}.</span></span>
\end{align}

<span data-ttu-id="22144-265">몇 가지 예제를 통해이를 보다 잘 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-265">This is better demonstrated with some examples:</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="22144-266">a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=</span><span class="sxs-lookup"><span data-stu-id="22144-266">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} =</span></span>
    \begin{bmatrix}
        <span data-ttu-id="22144-267">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-267">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="22144-268">\\\\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-268">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    \end{bmatrix}
    <span data-ttu-id="22144-269">=\begin{bmatrix}a \\\\ ca d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-269">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="22144-270">및</span><span class="sxs-lookup"><span data-stu-id="22144-270">and</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="22144-271">a \ b \\\\ c \ d \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-271">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    \otimes 
    \begin{bmatrix}
        <span data-ttu-id="22144-272">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-272">e\ f\\\\g\ h \end{bmatrix}</span></span>
     =
    \begin{bmatrix}
    <span data-ttu-id="22144-273">은\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-273">a\begin{bmatrix}</span></span>
    <span data-ttu-id="22144-274">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-274">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="22144-275">b\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-275">b\begin{bmatrix}</span></span>
    <span data-ttu-id="22144-276">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-276">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="22144-277">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-277">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="22144-278">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-278">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="22144-279">2\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-279">d\begin{bmatrix}</span></span>
    <span data-ttu-id="22144-280">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="22144-280">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    \end{bmatrix}
    =
    \begin{bmatrix}
    <span data-ttu-id="22144-281">ns\ \\\\</span><span class="sxs-lookup"><span data-stu-id="22144-281">ae\ af\ be\ bf \\\\</span></span>
    <span data-ttu-id="22144-282">ag \ ah \ bg \ bh \\\\</span><span class="sxs-lookup"><span data-stu-id="22144-282">ag\ ah\ bg\ bh \\\\</span></span>
    <span data-ttu-id="22144-283">ce \ cf \ de \ df \\\\</span><span class="sxs-lookup"><span data-stu-id="22144-283">ce\ cf\ de\ df \\\\</span></span>
    <span data-ttu-id="22144-284">cg \ ch \ dg \ dh \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="22144-284">cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="22144-285">텐서 제품에 대 한 최종 유용한 표기법 밑수 규칙은 모든 벡터 $ v $ 또는 매트릭스 M의 $ 경우 $ $ v ^ { \otimes n } $ 또는 $ M ^ { \otimes n } $ 은 $ n $ 접기 반복 텐서 제품에 대 한 짧은 손입니다.</span><span class="sxs-lookup"><span data-stu-id="22144-285">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="22144-286">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22144-286">For example:</span></span>

\begin{align}
<span data-ttu-id="22144-287">&\begin{bmatrix}1 \\\\ 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 0 0 \\\\ \\\\ \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1 \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\</span><span class="sxs-lookup"><span data-stu-id="22144-287">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\</span></span>
  <span data-ttu-id="22144-288">&\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & 0 0 1 0 0 & & \\\\ & & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 1 & 0 & & \end{bmatrix} 0 0.</span><span class="sxs-lookup"><span data-stu-id="22144-288">&\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}  0& 1 \\\\ 1& 0    \end{bmatrix},    \qquad\begin{bmatrix}   0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
\end{align}
