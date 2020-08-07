---
<span data-ttu-id="e6159-101">제목: 고급 행렬 개념 설명: 퀀텀 알고리즘을 설명 하 고 시뮬레이트하는 데 사용 되는 기본 도구인 고유 벡터, eigenvalues 및 matrix 지 수에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-101">title: Advanced matrix concepts description: Learn about eigenvectors, eigenvalues, and matrix exponentials, the fundamental tools used to describe and simulate quantum algorithms.</span></span>
<span data-ttu-id="e6159-102">작성자: QuantumWriter uid:-advanced ms. author: nawiebe@microsoft.com ms. 날짜: 12/11/2017. 토픽: 문서 번호-loc:</span><span class="sxs-lookup"><span data-stu-id="e6159-102">author: QuantumWriter uid: microsoft.quantum.concepts.matrix-advanced ms.author: nawiebe@microsoft.com ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="e6159-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="e6159-103">"Q#"</span></span>
- <span data-ttu-id="e6159-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="e6159-104">"$$v"</span></span>
- <span data-ttu-id="e6159-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="e6159-105">"$$"</span></span>
- <span data-ttu-id="e6159-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="e6159-106">"$$"</span></span>
- <span data-ttu-id="e6159-107">"$"</span><span class="sxs-lookup"><span data-stu-id="e6159-107">"$"</span></span>
- <span data-ttu-id="e6159-108">"$"</span><span class="sxs-lookup"><span data-stu-id="e6159-108">"$"</span></span>
- <span data-ttu-id="e6159-109">"$"</span><span class="sxs-lookup"><span data-stu-id="e6159-109">"$"</span></span>
- <span data-ttu-id="e6159-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="e6159-110">"$$"</span></span>
- <span data-ttu-id="e6159-111">"$$$"</span><span class="sxs-lookup"><span data-stu-id="e6159-111">"$$$"</span></span>
- <span data-ttu-id="e6159-112">"$$$"</span><span class="sxs-lookup"><span data-stu-id="e6159-112">"$$$"</span></span>
- <span data-ttu-id="e6159-113">"$$$"</span><span class="sxs-lookup"><span data-stu-id="e6159-113">"$$$"</span></span>
- <span data-ttu-id="e6159-114">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="e6159-114">"\cdots"</span></span>
- <span data-ttu-id="e6159-115">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="e6159-115">"bmatrix"</span></span>
- <span data-ttu-id="e6159-116">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="e6159-116">"\ddots"</span></span>
- <span data-ttu-id="e6159-117">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="e6159-117">"\equiv"</span></span>
- <span data-ttu-id="e6159-118">"\sum"</span><span class="sxs-lookup"><span data-stu-id="e6159-118">"\sum"</span></span>
- <span data-ttu-id="e6159-119">"\begin"</span><span class="sxs-lookup"><span data-stu-id="e6159-119">"\begin"</span></span>
- <span data-ttu-id="e6159-120">"\end"</span><span class="sxs-lookup"><span data-stu-id="e6159-120">"\end"</span></span>
- <span data-ttu-id="e6159-121">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="e6159-121">"\sqrt"</span></span>
- <span data-ttu-id="e6159-122">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="e6159-122">"\otimes"</span></span>
- <span data-ttu-id="e6159-123">"{"</span><span class="sxs-lookup"><span data-stu-id="e6159-123">"{"</span></span>
- <span data-ttu-id="e6159-124">"}"</span><span class="sxs-lookup"><span data-stu-id="e6159-124">"}"</span></span>
- <span data-ttu-id="e6159-125">"\text"</span><span class="sxs-lookup"><span data-stu-id="e6159-125">"\text"</span></span>
- <span data-ttu-id="e6159-126">"\phi"</span><span class="sxs-lookup"><span data-stu-id="e6159-126">"\phi"</span></span>
- <span data-ttu-id="e6159-127">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="e6159-127">"\kappa"</span></span>
- <span data-ttu-id="e6159-128">"\psi"</span><span class="sxs-lookup"><span data-stu-id="e6159-128">"\psi"</span></span>
- <span data-ttu-id="e6159-129">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="e6159-129">"\alpha"</span></span>
- <span data-ttu-id="e6159-130">"\beta"</span><span class="sxs-lookup"><span data-stu-id="e6159-130">"\beta"</span></span>
- <span data-ttu-id="e6159-131">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="e6159-131">"\gamma"</span></span>
- <span data-ttu-id="e6159-132">"\delta"</span><span class="sxs-lookup"><span data-stu-id="e6159-132">"\delta"</span></span>
- <span data-ttu-id="e6159-133">"\omega"</span><span class="sxs-lookup"><span data-stu-id="e6159-133">"\omega"</span></span>
- <span data-ttu-id="e6159-134">"\bra"</span><span class="sxs-lookup"><span data-stu-id="e6159-134">"\bra"</span></span>
- <span data-ttu-id="e6159-135">"\ket"</span><span class="sxs-lookup"><span data-stu-id="e6159-135">"\ket"</span></span>
- <span data-ttu-id="e6159-136">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="e6159-136">"\boldone"</span></span>
- <span data-ttu-id="e6159-137">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="e6159-137">"\\\\"</span></span>
- <span data-ttu-id="e6159-138">"\\"</span><span class="sxs-lookup"><span data-stu-id="e6159-138">"\\"</span></span>
- <span data-ttu-id="e6159-139">"="</span><span class="sxs-lookup"><span data-stu-id="e6159-139">"="</span></span>
- <span data-ttu-id="e6159-140">"\frac"</span><span class="sxs-lookup"><span data-stu-id="e6159-140">"\frac"</span></span>
- <span data-ttu-id="e6159-141">"\text"</span><span class="sxs-lookup"><span data-stu-id="e6159-141">"\text"</span></span>
- <span data-ttu-id="e6159-142">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="e6159-142">"\mapsto"</span></span>
- <span data-ttu-id="e6159-143">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="e6159-143">"\dagger"</span></span>
- <span data-ttu-id="e6159-144">"\to"</span><span class="sxs-lookup"><span data-stu-id="e6159-144">"\to"</span></span>
- <span data-ttu-id="e6159-145">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="e6159-145">"\begin{cases}"</span></span>
- <span data-ttu-id="e6159-146">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="e6159-146">"\end{cases}"</span></span>
- <span data-ttu-id="e6159-147">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="e6159-147">"\operatorname"</span></span>
- <span data-ttu-id="e6159-148">"\braket"</span><span class="sxs-lookup"><span data-stu-id="e6159-148">"\braket"</span></span>
- <span data-ttu-id="e6159-149">"\id"</span><span class="sxs-lookup"><span data-stu-id="e6159-149">"\id"</span></span>
- <span data-ttu-id="e6159-150">"\expect"</span><span class="sxs-lookup"><span data-stu-id="e6159-150">"\expect"</span></span>
- <span data-ttu-id="e6159-151">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="e6159-151">"\defeq"</span></span>
- <span data-ttu-id="e6159-152">"\variance"</span><span class="sxs-lookup"><span data-stu-id="e6159-152">"\variance"</span></span>
- <span data-ttu-id="e6159-153">"\dd"</span><span class="sxs-lookup"><span data-stu-id="e6159-153">"\dd"</span></span>
- <span data-ttu-id="e6159-154">"&"</span><span class="sxs-lookup"><span data-stu-id="e6159-154">"&"</span></span>
- <span data-ttu-id="e6159-155">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="e6159-155">"\begin{align}"</span></span>
- <span data-ttu-id="e6159-156">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="e6159-156">"\end{align}"</span></span>
- <span data-ttu-id="e6159-157">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="e6159-157">"\Lambda"</span></span>
- <span data-ttu-id="e6159-158">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="e6159-158">"\lambda"</span></span>
- <span data-ttu-id="e6159-159">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="e6159-159">"\Omega"</span></span>
- <span data-ttu-id="e6159-160">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="e6159-160">"\mathrm"</span></span>
- <span data-ttu-id="e6159-161">"\left"</span><span class="sxs-lookup"><span data-stu-id="e6159-161">"\left"</span></span>
- <span data-ttu-id="e6159-162">"\right"</span><span class="sxs-lookup"><span data-stu-id="e6159-162">"\right"</span></span>
- <span data-ttu-id="e6159-163">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="e6159-163">"\qquad"</span></span>
- <span data-ttu-id="e6159-164">"\times"</span><span class="sxs-lookup"><span data-stu-id="e6159-164">"\times"</span></span>
- <span data-ttu-id="e6159-165">"\big"</span><span class="sxs-lookup"><span data-stu-id="e6159-165">"\big"</span></span>
- <span data-ttu-id="e6159-166">"\langle"</span><span class="sxs-lookup"><span data-stu-id="e6159-166">"\langle"</span></span>
- <span data-ttu-id="e6159-167">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="e6159-167">"\rangle"</span></span>
- <span data-ttu-id="e6159-168">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="e6159-168">"\bigg"</span></span>
- <span data-ttu-id="e6159-169">"\Big"</span><span class="sxs-lookup"><span data-stu-id="e6159-169">"\Big"</span></span>
- <span data-ttu-id="e6159-170">"|"</span><span class="sxs-lookup"><span data-stu-id="e6159-170">"|"</span></span>
- <span data-ttu-id="e6159-171">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="e6159-171">"\mathbb"</span></span>
- <span data-ttu-id="e6159-172">"\vec"</span><span class="sxs-lookup"><span data-stu-id="e6159-172">"\vec"</span></span>
- <span data-ttu-id="e6159-173">"\in"</span><span class="sxs-lookup"><span data-stu-id="e6159-173">"\in"</span></span>
- <span data-ttu-id="e6159-174">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="e6159-174">"\texttt"</span></span>
- <span data-ttu-id="e6159-175">"\ne"</span><span class="sxs-lookup"><span data-stu-id="e6159-175">"\ne"</span></span>
- <span data-ttu-id="e6159-176">"<"</span><span class="sxs-lookup"><span data-stu-id="e6159-176">"<"</span></span>
- <span data-ttu-id="e6159-177">">"</span><span class="sxs-lookup"><span data-stu-id="e6159-177">">"</span></span>
- <span data-ttu-id="e6159-178">"\leq"</span><span class="sxs-lookup"><span data-stu-id="e6159-178">"\leq"</span></span>
- <span data-ttu-id="e6159-179">"\geq"</span><span class="sxs-lookup"><span data-stu-id="e6159-179">"\geq"</span></span>
- <span data-ttu-id="e6159-180">"~~"</span><span class="sxs-lookup"><span data-stu-id="e6159-180">"~~"</span></span>
- <span data-ttu-id="e6159-181">"~"</span><span class="sxs-lookup"><span data-stu-id="e6159-181">"~"</span></span>
- <span data-ttu-id="e6159-182">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="e6159-182">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="e6159-183">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="e6159-183">"\end{bmatrix}"</span></span>
- <span data-ttu-id="e6159-184">"\_"</span><span class="sxs-lookup"><span data-stu-id="e6159-184">"\_"</span></span>

---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="e6159-185">고급 행렬 개념</span><span class="sxs-lookup"><span data-stu-id="e6159-185">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="e6159-186">이제 [*고유 벡터*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 및 [*지 수*](https://en.wikipedia.org/wiki/Matrix_exponential) 에 대 한 행렬 조작을 확장 하 여 퀀텀 알고리즘을 설명 하 고 구현 하는 데 필요한 기본적인 도구 집합을 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-186">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="e6159-187">Eigenvalues 및 고유 벡터</span><span class="sxs-lookup"><span data-stu-id="e6159-187">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="e6159-188">$M을 $ 사각형 행렬로 $ , v를 $ 모두 0 벡터가 아닌 벡터 (즉, 모든 항목이 0 인 벡터 $ $ )로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-188">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="e6159-189">$ $ [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $ M은 $ $ = $ 일부 숫자 c에 대해 Mv cv 인 $ 경우 M은 eigenvector입니다 $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-189">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="e6159-190">$ $ Eigenvector v에 해당 하는 [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) 를 c 라고 $ 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-190">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="e6159-191">일반적으로 행렬과 $ M은 $ 벡터를 다른 벡터로 변환할 수 있지만 eigenvector는 숫자를 곱하는 경우를 제외 하 고는 변경 되지 않은 상태로 유지 되기 때문에 특수 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-191">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="e6159-192">$V $ 가 eigenvalue c를 사용 하는 eigenvector $ 경우 $ $ av $ 는 $ $ 동일한 eigenvalue를 사용 하는 eigenvector (0이 아닌 경우) 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-192">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="e6159-193">예를 들어 id 매트릭스의 경우 모든 벡터 $ v $ 는 eigenvalue 1을 사용 하는 eigenvector입니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-193">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="e6159-194">또 다른 예로 [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ $ 대각선에 0이 아닌 항목을 포함 하는 대각선 행렬 D를 생각해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-194">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

$$
\begin{bmatrix}
<span data-ttu-id="e6159-195">d_1 & 0 0 0 & d_2 0 0 0 \\\\ & & \\\\ & & d_3 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="e6159-195">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="e6159-196">벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-196">The vectors</span></span>

<span data-ttu-id="e6159-197">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} 및 \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="e6159-197">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="e6159-198">는이 행렬에서 고유 값 $ d_1 $ , $ d_2 $ 및 $ d_3 $ 를 각각 고유 벡터 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-198">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="e6159-199">$D_1 $ , $ d_2 $ 및 $ d_3 $ 고유한 숫자인 경우 이러한 벡터 (및 해당)는 행렬 d의 유일한 고유 벡터입니다 $ $ . 일반적으로 대각선 행렬의 경우 고유 값 및 고유 벡터를 쉽게 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-199">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$. In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="e6159-200">고유 값는 대각선에 표시 되는 모든 숫자이 고 각 고유 벡터는 1과 동일한 항목이 $ 1이 $ 고 나머지 항목이 0 인 단위 벡터입니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-200">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="e6159-201">위의 예제에서 고유 벡터 $ D는 $ $ 3 차원 벡터의 기반을 형성 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-201">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="e6159-202">기반은 벡터를 선형 조합으로 작성할 수 있도록 벡터 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-202">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="e6159-203">더 명시적, $ v_1 $ , $ v_2 $ 및 $ v_3 $ v_1 a_2 $ $ $ = $ $ $ , $ v_2 $ 및 $ a_3 $ 일부 숫자에 대 한 v a_1 v_3 + a_1 a_2 + a_3에 대 한 모든 벡터 v를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-203">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="e6159-204">Hermitian 매트릭스 (자체 adjoint 라고도 함)는 자체의 복소수 복소수와 동일한 복잡 한 정사각형 행렬 이지만, 단일 행렬은 해당 하는가 adjoint 또는 복소수 복소수와 동일한 복잡 한 사각형 행렬입니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-204">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate transpose, while a unitary matrix is a complex square matrix whose inverse is equal to its adjoint or complex conjugate transpose.</span></span>
<span data-ttu-id="e6159-205">기본적으로 퀀텀 컴퓨팅에서 발생 하는 유일한 행렬 인 Hermitian 및 단일 매트릭스의 경우 [*spectral 정리*](https://en.wikipedia.org/wiki/Spectral_theorem)라고 하는 일반적인 결과가 있습니다. 즉, 모든 Hermitian 또는 단일 매트릭스 m의 경우 $ $ $ $ $ = \dagger $ 일부 대각선 행렬 d에 대 한 M u ^ d u $ 와 같은 단일 U $ 가 있습니다. 또한 D의 대각선 항목은 $ $ M의 고유 값가 됩니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-205">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$. Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="e6159-206">대각선 행렬 D의 고유 값 및 고유 벡터를 계산 하는 방법을 이미 알고 $ $ 있습니다. 이 정리를 사용 하 여 $ v $ 가 $ eigenvalue c를 포함 하는 D의 eigenvector (예 $ : Dv cv) 인 경우 $ $ $ = $ $ U ^ \dagger v는 $ $ $ eigenvalue c가 있는 eigenvector의입니다 $ $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-206">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$. Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="e6159-207">그 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-207">This is because</span></span>

<span data-ttu-id="e6159-208">$$M (U ^ \dagger v) = u ^ \dagger d u (u ^ \dagger v) = U ^ \dagger d (u u ^ \dagger ) v = u ^ \dagger d v = c u ^ \dagger v.$$</span><span class="sxs-lookup"><span data-stu-id="e6159-208">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="e6159-209">행렬 지 수</span><span class="sxs-lookup"><span data-stu-id="e6159-209">Matrix Exponentials</span></span>
<span data-ttu-id="e6159-210">[*행렬 지*](https://en.wikipedia.org/wiki/Matrix_exponential) 수는 지 수 함수를 정확 하 게 유추 하 여 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-210">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="e6159-211">행렬 a의 행렬 지 $ 수는 $ 로 표현 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-211">The matrix exponential of a matrix $A$ can be expressed as</span></span>

$$
<span data-ttu-id="e6159-212">e ^ A = \boldone + a + \frac { a ^ 2 } { 2! } + \frac { ^ 3 } { 3!}+\cdots</span><span class="sxs-lookup"><span data-stu-id="e6159-212">e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots</span></span>
$$

<span data-ttu-id="e6159-213">이는 퀀텀 기계 시간 진화는 $ e ^ { IB } $ for Hermitian matrix $ B $ 형식의 단일 행렬에서 설명 하기 때문에 중요 합니다.  이러한 이유로 matrix 지 수를 수행 하는 것은 퀀텀 컴퓨팅의 기본 부분이 며 Q# 이러한 작업을 설명 하기 위한 내장 루틴을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-213">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.  For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="e6159-214">기존 컴퓨터에서 행렬 지 수를 계산 하는 방법에는 여러 가지가 있습니다. 일반적으로 이러한 지 수는 점이로 위험이 크기 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-214">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="e6159-215">[*Cleve Moler 및 Charles Van 대출을 참조 하세요. "천구 수상한는 행렬의 지 수를 계산 하는 방법" SIAM 리뷰 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) 은 관련 된 문제에 대 한 자세한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-215">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="e6159-216">행렬의 지 수를 계산 하는 방법을 이해 하는 가장 쉬운 방법은 해당 행렬의 고유 값 및 고유 벡터를 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-216">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="e6159-217">특히 위에 설명 된 spectral 정리는 모든 Hermitian 또는 단일 행렬에 대 한 $ 단일 $ 매트릭스 $ u $ 와 대각선 행렬 $ d ( $ $ = u ^ \dagger d u $ )가 존재 한다는 것을 의미 합니다.  단위 인자의 속성 때문에 $ ^ 2 = u ^ \dagger d ^ 2 u $ 및 이와 유사한 모든 전원 $ p $ $ a ^ p = u ^ \dagger d ^ p u $ 를 사용할 수 있습니다.  이를 연산자 지 수의 연산자 정의로 대체 하는 경우 다음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-217">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

$$
<span data-ttu-id="e6159-218">e ^ A = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \exp (D_ { 11 } ) & 0 0 0 & \cdots & \\\\ 0 & \exp (D_ { 22 } ) & \cdots & 0 \\\\ \vst\vst\v도트 & & \ddots & \\\\ 0 & 0 & \cdots & \exp (D_ { NN } ) \end{bmatrix} U.$$</span><span class="sxs-lookup"><span data-stu-id="e6159-218">e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="e6159-219">즉, 행렬 A의 eigenbasis으로 변환 하는 경우 행렬 $ $ 의 지 수를 계산 하는 것은 행렬의 eigenbasis의 일반 지 수를 계산 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-219">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="e6159-220">퀀텀 컴퓨팅의 많은 작업에는 matrix 지 수 수행이 포함 되어 있으므로, 연산자 지 수를 단순화 하기 위해 행렬의 eigenbasis으로 변환 하는이 트릭은 자주 나타나고이 가이드의 뒷부분에서 설명 하는 Trotter – Suzuki 퀀텀 시뮬레이션 방법과 같은 여러 퀀텀 알고리즘의 기반이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6159-220">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="e6159-221">또 다른 유용한 속성은 $ b $ 가 단일 and Hermitian 경우입니다 (예: $ b = b ^ { -1 } = b ^ \dagger $ then $ b ^ 2 = \boldone $ ).</span><span class="sxs-lookup"><span data-stu-id="e6159-221">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="e6159-222">이러한 행렬 지 수의 위 확장에이 규칙을 적용 하 고 $ \boldone $ 및 $ B 용어를 함께 그룹화 하면 $ 모든 실수 값 $ x에서 id를 볼 수 있습니다 $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-222">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="e6159-223">$$e ^ { ibx } = \boldone \cos (x) + iB\sin (x)$$</span><span class="sxs-lookup"><span data-stu-id="e6159-223">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="e6159-224">갖고.</span><span class="sxs-lookup"><span data-stu-id="e6159-224">holds.</span></span> <span data-ttu-id="e6159-225">이 트릭은 b의 차원이 $ $ $ 단일 및 Hermitian 경우의 특수 한 경우에도 b의 차원이 수많은 지 수 작업 행렬에 대 한 이유를 허용 하기 때문에 특히 유용 합니다 $ .</span><span class="sxs-lookup"><span data-stu-id="e6159-225">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
