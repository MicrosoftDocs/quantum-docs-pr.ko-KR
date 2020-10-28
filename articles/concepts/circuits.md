---
<span data-ttu-id="06ead-101">제목: 퀀텀 회로 설명: 퀀텀 회로 다이어그램으로 단순 하 고 복잡 한 퀀텀 작업을 시각적으로 표시 하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-101">title: Quantum circuits description: Learn how to visually represent simple and complex quantum operations with quantum circuit diagrams.</span></span>
<span data-ttu-id="06ead-102">작성자: QuantumWriter uid: benbra: 12/11/2017. 날짜: 밀리초. 토픽: 문서 번호-loc:</span><span class="sxs-lookup"><span data-stu-id="06ead-102">author: QuantumWriter uid: microsoft.quantum.concepts.circuits ms.author: v-benbra ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="06ead-103">":::no-loc(Q#):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-103">":::no-loc(Q#):::"</span></span>
- <span data-ttu-id="06ead-104">":::no-loc($$v):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-104">":::no-loc($$v):::"</span></span>
- <span data-ttu-id="06ead-105">":::no-loc($$):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-105">":::no-loc($$):::"</span></span>
- <span data-ttu-id="06ead-106">":::no-loc($$):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-106">":::no-loc($$):::"</span></span>
- <span data-ttu-id="06ead-107">":::no-loc($):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-107">":::no-loc($):::"</span></span>
- <span data-ttu-id="06ead-108">":::no-loc($):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-108">":::no-loc($):::"</span></span>
- <span data-ttu-id="06ead-109">":::no-loc($):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-109">":::no-loc($):::"</span></span>
- <span data-ttu-id="06ead-110">":::no-loc($$):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-110">":::no-loc($$):::"</span></span>
- <span data-ttu-id="06ead-111">":::no-loc(\cdots):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-111">":::no-loc(\cdots):::"</span></span>
- <span data-ttu-id="06ead-112">":::no-loc(bmatrix):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-112">":::no-loc(bmatrix):::"</span></span>
- <span data-ttu-id="06ead-113">":::no-loc(\ddots):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-113">":::no-loc(\ddots):::"</span></span>
- <span data-ttu-id="06ead-114">":::no-loc(\equiv):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-114">":::no-loc(\equiv):::"</span></span>
- <span data-ttu-id="06ead-115">":::no-loc(\sum):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-115">":::no-loc(\sum):::"</span></span>
- <span data-ttu-id="06ead-116">":::no-loc(\begin):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-116">":::no-loc(\begin):::"</span></span>
- <span data-ttu-id="06ead-117">":::no-loc(\end):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-117">":::no-loc(\end):::"</span></span>
- <span data-ttu-id="06ead-118">":::no-loc(\sqrt):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-118">":::no-loc(\sqrt):::"</span></span>
- <span data-ttu-id="06ead-119">":::no-loc(\otimes):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-119">":::no-loc(\otimes):::"</span></span>
- <span data-ttu-id="06ead-120">":::no-loc({):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-120">":::no-loc({):::"</span></span>
- <span data-ttu-id="06ead-121">":::no-loc(}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-121">":::no-loc(}):::"</span></span>
- <span data-ttu-id="06ead-122">":::no-loc(\text):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-122">":::no-loc(\text):::"</span></span>
- <span data-ttu-id="06ead-123">":::no-loc(\phi):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-123">":::no-loc(\phi):::"</span></span>
- <span data-ttu-id="06ead-124">":::no-loc(\kappa):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-124">":::no-loc(\kappa):::"</span></span>
- <span data-ttu-id="06ead-125">":::no-loc(\psi):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-125">":::no-loc(\psi):::"</span></span>
- <span data-ttu-id="06ead-126">":::no-loc(\alpha):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-126">":::no-loc(\alpha):::"</span></span>
- <span data-ttu-id="06ead-127">":::no-loc(\beta):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-127">":::no-loc(\beta):::"</span></span>
- <span data-ttu-id="06ead-128">":::no-loc(\gamma):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-128">":::no-loc(\gamma):::"</span></span>
- <span data-ttu-id="06ead-129">":::no-loc(\delta):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-129">":::no-loc(\delta):::"</span></span>
- <span data-ttu-id="06ead-130">":::no-loc(\omega):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-130">":::no-loc(\omega):::"</span></span>
- <span data-ttu-id="06ead-131">":::no-loc(\bra):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-131">":::no-loc(\bra):::"</span></span>
- <span data-ttu-id="06ead-132">":::no-loc(\ket):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-132">":::no-loc(\ket):::"</span></span>
- <span data-ttu-id="06ead-133">":::no-loc(\boldone):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-133">":::no-loc(\boldone):::"</span></span>
- <span data-ttu-id="06ead-134">":::no-loc(\\\\):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-134">":::no-loc(\\\\):::"</span></span>
- <span data-ttu-id="06ead-135">":::no-loc(\\):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-135">":::no-loc(\\):::"</span></span>
- <span data-ttu-id="06ead-136">":::no-loc(=):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-136">":::no-loc(=):::"</span></span>
- <span data-ttu-id="06ead-137">":::no-loc(\frac):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-137">":::no-loc(\frac):::"</span></span>
- <span data-ttu-id="06ead-138">":::no-loc(\text):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-138">":::no-loc(\text):::"</span></span>
- <span data-ttu-id="06ead-139">":::no-loc(\mapsto):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-139">":::no-loc(\mapsto):::"</span></span>
- <span data-ttu-id="06ead-140">":::no-loc(\dagger):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-140">":::no-loc(\dagger):::"</span></span>
- <span data-ttu-id="06ead-141">":::no-loc(\to):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-141">":::no-loc(\to):::"</span></span>
- <span data-ttu-id="06ead-142">":::no-loc(\begin{cases}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-142">":::no-loc(\begin{cases}):::"</span></span>
- <span data-ttu-id="06ead-143">":::no-loc(\end{cases}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-143">":::no-loc(\end{cases}):::"</span></span>
- <span data-ttu-id="06ead-144">":::no-loc(\operatorname):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-144">":::no-loc(\operatorname):::"</span></span>
- <span data-ttu-id="06ead-145">":::no-loc(\braket):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-145">":::no-loc(\braket):::"</span></span>
- <span data-ttu-id="06ead-146">":::no-loc(\id):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-146">":::no-loc(\id):::"</span></span>
- <span data-ttu-id="06ead-147">":::no-loc(\expect):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-147">":::no-loc(\expect):::"</span></span>
- <span data-ttu-id="06ead-148">":::no-loc(\defeq):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-148">":::no-loc(\defeq):::"</span></span>
- <span data-ttu-id="06ead-149">":::no-loc(\variance):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-149">":::no-loc(\variance):::"</span></span>
- <span data-ttu-id="06ead-150">":::no-loc(\dd):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-150">":::no-loc(\dd):::"</span></span>
- <span data-ttu-id="06ead-151">":::no-loc(&):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-151">":::no-loc(&):::"</span></span>
- <span data-ttu-id="06ead-152">":::no-loc(\begin{align}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-152">":::no-loc(\begin{align}):::"</span></span>
- <span data-ttu-id="06ead-153">":::no-loc(\end{align}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-153">":::no-loc(\end{align}):::"</span></span>
- <span data-ttu-id="06ead-154">":::no-loc(\Lambda):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-154">":::no-loc(\Lambda):::"</span></span>
- <span data-ttu-id="06ead-155">":::no-loc(\lambda):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-155">":::no-loc(\lambda):::"</span></span>
- <span data-ttu-id="06ead-156">":::no-loc(\Omega):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-156">":::no-loc(\Omega):::"</span></span>
- <span data-ttu-id="06ead-157">":::no-loc(\mathrm):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-157">":::no-loc(\mathrm):::"</span></span>
- <span data-ttu-id="06ead-158">":::no-loc(\left):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-158">":::no-loc(\left):::"</span></span>
- <span data-ttu-id="06ead-159">":::no-loc(\right):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-159">":::no-loc(\right):::"</span></span>
- <span data-ttu-id="06ead-160">":::no-loc(\qquad):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-160">":::no-loc(\qquad):::"</span></span>
- <span data-ttu-id="06ead-161">":::no-loc(\times):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-161">":::no-loc(\times):::"</span></span>
- <span data-ttu-id="06ead-162">":::no-loc(\big):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-162">":::no-loc(\big):::"</span></span>
- <span data-ttu-id="06ead-163">":::no-loc(\langle):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-163">":::no-loc(\langle):::"</span></span>
- <span data-ttu-id="06ead-164">":::no-loc(\rangle):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-164">":::no-loc(\rangle):::"</span></span>
- <span data-ttu-id="06ead-165">":::no-loc(\bigg):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-165">":::no-loc(\bigg):::"</span></span>
- <span data-ttu-id="06ead-166">":::no-loc(\Big):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-166">":::no-loc(\Big):::"</span></span>
- <span data-ttu-id="06ead-167">":::no-loc(|):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-167">":::no-loc(|):::"</span></span>
- <span data-ttu-id="06ead-168">":::no-loc(\mathbb):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-168">":::no-loc(\mathbb):::"</span></span>
- <span data-ttu-id="06ead-169">":::no-loc(\vec):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-169">":::no-loc(\vec):::"</span></span>
- <span data-ttu-id="06ead-170">":::no-loc(\in):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-170">":::no-loc(\in):::"</span></span>
- <span data-ttu-id="06ead-171">":::no-loc(\texttt):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-171">":::no-loc(\texttt):::"</span></span>
- <span data-ttu-id="06ead-172">":::no-loc(\ne):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-172">":::no-loc(\ne):::"</span></span>
- <span data-ttu-id="06ead-173">":::no-loc(<):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-173">":::no-loc(<):::"</span></span>
- <span data-ttu-id="06ead-174">":::no-loc(>):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-174">":::no-loc(>):::"</span></span>
- <span data-ttu-id="06ead-175">":::no-loc(\leq):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-175">":::no-loc(\leq):::"</span></span>
- <span data-ttu-id="06ead-176">":::no-loc(\geq):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-176">":::no-loc(\geq):::"</span></span>
- <span data-ttu-id="06ead-177">":::no-loc(~~):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-177">":::no-loc(~~):::"</span></span>
- <span data-ttu-id="06ead-178">":::no-loc(~):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-178">":::no-loc(~):::"</span></span>
- <span data-ttu-id="06ead-179">":::no-loc(\begin{bmatrix}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-179">":::no-loc(\begin{bmatrix}):::"</span></span>
- <span data-ttu-id="06ead-180">":::no-loc(\end{bmatrix}):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-180">":::no-loc(\end{bmatrix}):::"</span></span>
- <span data-ttu-id="06ead-181">":::no-loc(\_):::"</span><span class="sxs-lookup"><span data-stu-id="06ead-181">":::no-loc(\_):::"</span></span>

---

# <a name="quantum-circuits"></a><span data-ttu-id="06ead-182">퀀텀 회로</span><span class="sxs-lookup"><span data-stu-id="06ead-182">Quantum Circuits</span></span>
<span data-ttu-id="06ead-183">단일 변환 :::no-loc($)::: :::no-loc(\text)::: :::no-loc({)::: cnot :::no-loc(})::: _ :::no-loc({)::: 01 :::no-loc(})::: (H :::no-loc(\otimes)::: 1) :::no-loc($)::: 의 순간을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-183">Consider for a moment the unitary transformation :::no-loc($)::::::no-loc(\text)::::::no-loc({)::: CNOT:::no-loc(}):::_:::no-loc({):::01:::no-loc(}):::(H:::no-loc(\otimes)::: 1):::no-loc($):::.</span></span>
<span data-ttu-id="06ead-184">이 게이트 시퀀스는 최대 entangled의 2 상 비트 상태를 만들기 때문에 퀀텀 컴퓨팅에 대 한 근본적인 중요 한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-184">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="06ead-185">:::no-loc($$)::::::no-loc(\mathrm)::::::no-loc({):::Cnot :::no-loc(})::: _ :::no-loc({)::: 01 :::no-loc(})::: (H :::no-loc(\otimes)::: 1) :::no-loc(\ket)::: :::no-loc({)::: 00 :::no-loc(})::: :::no-loc(=)::: :::no-loc(\frac)::: :::no-loc({)::: 1 :::no-loc(})::: :::no-loc({)::: :::no-loc(\sqrt)::: :::no-loc({)::: 2 :::no-loc(})::: :::no-loc(})::: :::no-loc(\left)::: ( :::no-loc(\ket)::: :::no-loc({)::: 00 :::no-loc(}):::  +  :::no-loc(\ket)::: :::no-loc({)::: 11 :::no-loc(})::: :::no-loc(\right)::: ),:::no-loc($$):::</span><span class="sxs-lookup"><span data-stu-id="06ead-185">:::no-loc($$)::::::no-loc(\mathrm)::::::no-loc({):::CNOT:::no-loc(}):::_:::no-loc({):::01:::no-loc(}):::(H:::no-loc(\otimes)::: 1):::no-loc(\ket)::::::no-loc({):::00:::no-loc(})::: :::no-loc(=)::: :::no-loc(\frac)::::::no-loc({):::1:::no-loc(})::::::no-loc({)::::::no-loc(\sqrt)::::::no-loc({):::2:::no-loc(})::::::no-loc(})::: :::no-loc(\left):::(:::no-loc(\ket)::::::no-loc({):::00:::no-loc(})::: + :::no-loc(\ket)::::::no-loc({):::11:::no-loc(})::: :::no-loc(\right):::),:::no-loc($$):::</span></span>

<span data-ttu-id="06ead-186">이러한 복잡성을 포함 하는 작업은 퀀텀 알고리즘과 퀀텀 오류 수정에서 사용할 수 있으므로 *퀀텀 회로 다이어그램* 이라고 하는 시각화에 대 한 간단한 메서드가 있는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-186">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram* .</span></span>
<span data-ttu-id="06ead-187">이 최대 entangled 퀀텀 상태를 준비 하기 위한 회로 다이어그램은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-187">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<span data-ttu-id="06ead-188">:::no-loc(<):::!--- ![](.\media\1.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-188">:::no-loc(<):::!--- ![](.\media\1.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-189">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-189">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-190">![최대 entangled 2 상 비트 상태에 대 한 회로 다이어그램](:::no-loc(~):::/media/1.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-190">![Circuit diagram for a maximally entangled two-qubit state](:::no-loc(~):::/media/1.svg)</span></span>

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="06ead-191">퀀텀 회로 다이어그램 규칙</span><span class="sxs-lookup"><span data-stu-id="06ead-191">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="06ead-192">퀀텀 작업의 시각적 언어는 퀀텀 회로를 표현 하는 규칙을 이해 하 고 나면 동등한 행렬을 작성 하는 것 보다 훨씬 더 쉽게 좋게 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-192">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="06ead-193">아래에서 이러한 규칙을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-193">We review these conventions below.</span></span>

<span data-ttu-id="06ead-194">회로 다이어그램에서 각 실선은 보다 일반적으로는 이상 비트 레지스터를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-194">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="06ead-195">규칙에 따라 맨 위 줄은 이란 비트 레지스터 :::no-loc($)::: 0이 :::no-loc($)::: 고 나머지는 순차적으로 레이블이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-195">By convention, the top line is qubit register :::no-loc($):::0:::no-loc($)::: and the remainder are labeled sequentially.</span></span> <span data-ttu-id="06ead-196">위의 예제 회로는 두 개의 비트에서 작동 하는 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-196">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="06ead-197">하나 이상의 이상 비트 레지스터에서 동작 하는 게이트가 상자로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-197">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="06ead-198">예: 기호</span><span class="sxs-lookup"><span data-stu-id="06ead-198">For example, the symbol</span></span>

<span data-ttu-id="06ead-199">:::no-loc(<):::!--- ![](.\media\2.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-199">:::no-loc(<):::!--- ![](.\media\2.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-200">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-200">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-201">![단일 기능 비트 레지스터에서 작동 하는 Hadamard 작업에 대 한 기호](:::no-loc(~):::/media/2.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-201">![Symbol for a Hadamard operation acting on a single-qubit register](:::no-loc(~):::/media/2.svg)</span></span>

<span data-ttu-id="06ead-202">는 단일의 비트 레지스터에서 작동 하는 [Hadamard](xref:Microsoft.Quantum.Intrinsic.H) 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-202">is a [Hadamard](xref:Microsoft.Quantum.Intrinsic.H) operation acting on a single-qubit register.</span></span>

<span data-ttu-id="06ead-203">퀀텀 게이트는 처음에는 관문을 중심으로 가장 왼쪽의 게이트가 있는 시간순으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-203">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="06ead-204">즉, 퀀텀을 퀀텀 상태를 유지 하는 경우 와이어는 다이어그램의 각 게이트를 통해 퀀텀 상태를 왼쪽에서 오른쪽으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-204">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="06ead-205">예를 들면</span><span class="sxs-lookup"><span data-stu-id="06ead-205">That is to say</span></span> 

<span data-ttu-id="06ead-206">:::no-loc(<):::!--- ![](.\media\3.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-206">:::no-loc(<):::!--- ![](.\media\3.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-207">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-207">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-208">![왼쪽에서 오른쪽으로 적용 되는 퀀텀 게이트 다이어그램](:::no-loc(~):::/media/3.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-208">![Diagram of quantum gates being applied left-to-right](:::no-loc(~):::/media/3.svg)</span></span>

<span data-ttu-id="06ead-209">는 단일 행렬 :::no-loc($)::: cba :::no-loc($)::: 입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-209">is the unitary matrix :::no-loc($):::CBA:::no-loc($):::.</span></span>
<span data-ttu-id="06ead-210">행렬 곱셈은 반대 규칙을 따르는 합니다. 가장 오른쪽의 행렬이 먼저 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-210">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="06ead-211">그러나 퀀텀 회로 다이어그램에서 가장 왼쪽의 게이트가 먼저 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-211">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="06ead-212">이러한 차이는 때때로 혼란 스 러 울 수 있으므로 선형 대 수 표기법과 퀀텀 회로 다이어그램 간의 상당한 차이를 확인 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-212">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="06ead-213">퀀텀 회로의 입/출력</span><span class="sxs-lookup"><span data-stu-id="06ead-213">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="06ead-214">지정 된 앞의 모든 예제에는 퀀텀 게이트의 와이어 수와 동일한 수의 와이어 (는)를 퀀텀 게이트에 정확 하 게 입력 했습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-214">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="06ead-215">처음에는 퀀텀 회로가 일반적으로 입력 하는 것 보다 더 많거나 적을 수 있다는 것이 합리적입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-215">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="06ead-216">그러나 모든 퀀텀 작업을 저장 하는 것은 단일 작업 이므로 해독 가능 하기 때문에 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-216">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="06ead-217">입력과 동일한 수의 출력을 포함 하지 않은 경우에는 해독 하지 않고 일치 하지 않는 단일 사용자가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-217">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="06ead-218">이러한 이유로 회로 다이어그램에 그려진 상자는 종료 하는 것과 정확히 동일한 수의 와이어로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-218">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="06ead-219">다중 기능 비트 회로 다이어그램은 유사한 규칙에 따라 단일 비트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-219">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="06ead-220">명확 하 게 이해 하는 예로, 2 배 비트 단일 작업 B를 :::no-loc($)::: :::no-loc($)::: :::no-loc($)::: (H S X)로 정의 하 :::no-loc(\otimes)::: :::no-loc($)::: 고 회로를 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-220">As a clarifying example, we can define a two-qubit unitary operation :::no-loc($):::B:::no-loc($)::: to be :::no-loc($):::(H S:::no-loc(\otimes)::: X):::no-loc($)::: and express the circuit equivalently as</span></span>

<span data-ttu-id="06ead-221">:::no-loc(<):::!--- ![](.\media\4.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-221">:::no-loc(<):::!--- ![](.\media\4.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-222">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-222">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-223">![두 개의 단일 비트 작업의 회로 다이어그램](:::no-loc(~):::/media/4.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-223">![Circuit diagram of a two-qubit unitary operation](:::no-loc(~):::/media/4.svg)</span></span>

<span data-ttu-id="06ead-224">또한 회로를 사용 하는 :::no-loc($)::: :::no-loc($)::: 컨텍스트에 따라 2 1-가 비트 레지스터 보다는 단일 2의 비트 레지스터에 대 한 작업으로 B를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-224">We can also view :::no-loc($):::B:::no-loc($)::: as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="06ead-225">이러한 추상 회로 다이어그램의 가장 유용한 속성은 기본 게이트로 컴파일하지 않고도 복잡 한 퀀텀 알고리즘을 높은 수준으로 설명할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-225">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="06ead-226">즉, 알고리즘 내의 각 서브루틴이 작동 하는 방식에 대 한 모든 세부 정보를 이해 하지 않고도 대량 퀀텀 알고리즘에 대 한 데이터 흐름에 대 한 intuition를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-226">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="06ead-227">제어 된 게이트</span><span class="sxs-lookup"><span data-stu-id="06ead-227">Controlled gates</span></span>
<span data-ttu-id="06ead-228">Multi-factor bit 퀀텀 회로 다이어그램에 기본 제공 되는 다른 구문은 제어입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-228">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="06ead-229">(G)로 표시 되는 퀀텀 단일 제어 되는 게이트의 작업 (g :::no-loc($)::: :::no-loc(\Lambda)::: )은 (g) :::no-loc($)::: :::no-loc($)::: :::no-loc($)::: 제품 상태 입력 :::no-loc($)::: :::no-loc(\Lambda)::: (g) ( :::no-loc(\alpha)::: :::no-loc(\ket)::: :::no-loc({)::: 0 :::no-loc(}):::  +  :::no-loc(\beta)::: :::no-loc(\ket)::: :::no-loc({)::: 1 :::no-loc(})::: ) :::no-loc(\ket)::: :::no-loc({)::: :::no-loc(\psi)::: :::no-loc(})::: :::no-loc(=)::: :::no-loc(\alpha)::: :::no-loc(\ket)::: :::no-loc({)::: 0 :::no-loc(})::: :::no-loc(\ket)::: :::no-loc({)::: :::no-loc(\psi)::: :::no-loc(}):::  +  :::no-loc(\beta)::: :::no-loc(\ket)::: :::no-loc({)::: 1 :::no-loc(})::: G :::no-loc(\ket)::: :::no-loc({)::: :::no-loc(\psi)::: :::no-loc(})::: :::no-loc($)::: 의 다음 예를 살펴보면 이해할 수 있습니다. 즉, 제어 되는 게이트는 컨트롤의 값이 1 인 경우에 :::no-loc($)::: :::no-loc($)::: 만가 포함 된 레지스터에 G를 적용 합니다 :::no-loc($)::: :::no-loc(\psi)::: :::no-loc($)::: :::no-loc($)::: :::no-loc($)::: .</span><span class="sxs-lookup"><span data-stu-id="06ead-229">The action of a quantum singly controlled gate, denoted :::no-loc($)::::::no-loc(\Lambda):::(G):::no-loc($):::, where a single qubit's value controls the application of :::no-loc($):::G:::no-loc($):::, can be understood by looking at the following example of a product state input :::no-loc($)::::::no-loc(\Lambda):::(G) (:::no-loc(\alpha)::: :::no-loc(\ket)::::::no-loc({):::0:::no-loc(})::: + :::no-loc(\beta)::: :::no-loc(\ket)::::::no-loc({):::1:::no-loc(}):::) :::no-loc(\ket)::::::no-loc({)::::::no-loc(\psi)::::::no-loc(})::: :::no-loc(=)::: :::no-loc(\alpha)::: :::no-loc(\ket)::::::no-loc({):::0:::no-loc(})::: :::no-loc(\ket)::::::no-loc({)::::::no-loc(\psi)::::::no-loc(})::: + :::no-loc(\beta)::: :::no-loc(\ket)::::::no-loc({):::1:::no-loc(})::: G:::no-loc(\ket)::::::no-loc({)::::::no-loc(\psi)::::::no-loc(})::::::no-loc($):::. That is to say, the controlled gate applies :::no-loc($):::G:::no-loc($)::: to the register containing :::no-loc($)::::::no-loc(\psi)::::::no-loc($)::: if and only if the control qubit takes the value :::no-loc($):::1:::no-loc($):::.</span></span>
<span data-ttu-id="06ead-230">일반적으로 회로 다이어그램에서 이와 같이 제어 되는 작업을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-230">In general, we describe such controlled operations in circuit diagrams as</span></span>

<span data-ttu-id="06ead-231">:::no-loc(<):::!--- ![](.\media\5.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-231">:::no-loc(<):::!--- ![](.\media\5.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-232">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-232">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-233">![단일 제어 게이트 회로 다이어그램](:::no-loc(~):::/media/5.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-233">![Circuit diagram of a singly controlled gate](:::no-loc(~):::/media/5.svg)</span></span>

<span data-ttu-id="06ead-234">여기서 검은색 원은 게이트가 제어 되는 퀀텀 비트를 나타내며, 세로는 컨트롤의 값이 1 인 경우 적용 되는 단일를 나타냅니다 :::no-loc($)::: :::no-loc($)::: .</span><span class="sxs-lookup"><span data-stu-id="06ead-234">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value :::no-loc($):::1:::no-loc($):::.</span></span>
<span data-ttu-id="06ead-235">:::no-loc($):::G :::no-loc(=)::: X :::no-loc($)::: 및 g Z의 경우 제어 되는 :::no-loc($)::: :::no-loc(=)::: :::no-loc($)::: 게이트 버전을 설명 하는 다음과 같은 표기법이 도입 됩니다 (제어 된 X 게이트는 [ :::no-loc($)::: cnot :::no-loc($)::: 게이트](xref:Microsoft.Quantum.Intrinsic.CNOT)).</span><span class="sxs-lookup"><span data-stu-id="06ead-235">For the special cases where :::no-loc($):::G:::no-loc(=):::X:::no-loc($)::: and :::no-loc($):::G:::no-loc(=):::Z:::no-loc($)::: we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [:::no-loc($):::CNOT:::no-loc($)::: gate](xref:Microsoft.Quantum.Intrinsic.CNOT)):</span></span>

<span data-ttu-id="06ead-236">:::no-loc(<):::!--- ![](.\media\6.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-236">:::no-loc(<):::!--- ![](.\media\6.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-237">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-237">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-238">![제어 되는 게이트의 특수 사례에 대 한 회로 다이어그램](:::no-loc(~):::/media/6.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-238">![Circuit diagram for special cases of controlled gates](:::no-loc(~):::/media/6.svg)</span></span>

<span data-ttu-id="06ead-239">:::no-loc(Q#)::: 작업의 제어 된 버전을 자동으로 생성 하는 메서드를 제공 합니다. 그러면 프로그래머가 이러한 작업을 직접 코딩할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-239">:::no-loc(Q#)::: provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="06ead-240">이에 대 한 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-240">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl :::no-loc({)::: // Auto-generate the controlled specialization of the operation
    H(qubit);
:::no-loc(}):::
```

## <a name="measurement-operator"></a><span data-ttu-id="06ead-241">측정 연산자</span><span class="sxs-lookup"><span data-stu-id="06ead-241">Measurement operator</span></span>
<span data-ttu-id="06ead-242">회로 다이어그램에서 시각화 하는 나머지 작업은 측정입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-242">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="06ead-243">측정은 더 많은 비트 레지스터를 사용 하 여 측정 하 고 결과를 기존 정보로 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-243">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="06ead-244">측정 연산은 미터 기호로 표시 되 고 항상 (실선으로 표시 됨)에 대 한 입력으로 사용 되며, 이중 줄로 표시 되는 고전적인 정보를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-244">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="06ead-245">특히 이러한 subcircuit는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-245">Specifically, such a subcircuit looks like:</span></span>

<span data-ttu-id="06ead-246">:::no-loc(<):::!--- ![](.\media\7.svg) ----:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-246">:::no-loc(<):::!--- ![](.\media\7.svg) ----:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-247">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-247">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-248">![측정 작업을 나타내는 기호](:::no-loc(~):::/media/7.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-248">![Symbol representing a measurement operation](:::no-loc(~):::/media/7.svg)</span></span>

<span data-ttu-id="06ead-249">:::no-loc(Q#)::: 이 목적에 대 한 [측정값 연산자](xref:Microsoft.Quantum.Intrinsic.Measure) 를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-249">:::no-loc(Q#)::: implements a [Measure operator](xref:Microsoft.Quantum.Intrinsic.Measure) for this purpose.</span></span>
<span data-ttu-id="06ead-250">자세한 내용은 [측정에](xref:microsoft.quantum.libraries.standard.prelude#measurements) 대 한 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06ead-250">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="06ead-251">마찬가지로 subcircuit</span><span class="sxs-lookup"><span data-stu-id="06ead-251">Similarly, the subcircuit</span></span>

<span data-ttu-id="06ead-252">:::no-loc(<):::!--- ![](.\media\8.svg) ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-252">:::no-loc(<):::!--- ![](.\media\8.svg) ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-253">:::no-loc(<):::!--를 쉽게 가운데에 맞출 수 없습니다. 필요한 확장이 있을 수 있습니다.:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-253">:::no-loc(<):::!-- Can't find a way to easily center this... probably an extension needed:  --:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-254">![제어 된 작업을 나타내는 회로 다이어그램](:::no-loc(~):::/media/8.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-254">![Circuit diagram representing a controlled operation](:::no-loc(~):::/media/8.svg)</span></span>

<span data-ttu-id="06ead-255">일반적으로 제어 되는 게이트를 제공 :::no-loc($)::: 합니다 :::no-loc($)::: . 여기서 G는 클래식 컨트롤 비트에 값 1로 조건 화 된 적용 됩니다 :::no-loc($)::: :::no-loc($)::: .</span><span class="sxs-lookup"><span data-stu-id="06ead-255">gives a classically controlled gate, where :::no-loc($):::G:::no-loc($)::: is applied conditioned on the classical control bit being value :::no-loc($):::1:::no-loc($):::.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="06ead-256">Teleportation 회로 다이어그램</span><span class="sxs-lookup"><span data-stu-id="06ead-256">Teleportation circuit diagram</span></span>
<span data-ttu-id="06ead-257">퀀텀 teleportation는 이러한 구성 요소를 보여 주는 최상의 퀀텀 알고리즘이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-257">Quantum teleportation is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="06ead-258">해당 하는 [퀀텀 Kata](xref:microsoft.quantum.overview.katas) 퀀텀 teleportation은 되거나 얽 히 및 측정을 사용 하 여 퀀텀 컴퓨터 내에서 (또는 퀀텀 네트워크의 먼 퀀텀 컴퓨터 간) 데이터를 이동 하는 방법에 대해 배울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-258">You can learn hands-on with the corresponding [Quantum Kata](xref:microsoft.quantum.overview.katas) Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="06ead-259">흥미롭게도, 실제 값을 알고 있는 것이 아니라, 지정 된의 값을 한 가지 이상에서 다른 값으로 이동 하는 것은 사실입니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-259">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="06ead-260">이는 프로토콜이 퀀텀 메커니즘의 법에 따라 작동 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-260">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="06ead-261">퀀텀 teleportation 회로는 아래에 제공 됩니다. 또한 퀀텀 회로를 읽는 방법을 보여 주기 위해 주석이 추가 된 회로 버전을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ead-261">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<span data-ttu-id="06ead-262">:::no-loc(<):::!--- ![](.\media\tp2.svg) :::no-loc({)::: 너비 :::no-loc(=)::: 50%:::no-loc(})::: ---:::no-loc(>):::</span><span class="sxs-lookup"><span data-stu-id="06ead-262">:::no-loc(<):::!--- ![](.\media\tp2.svg):::no-loc({)::: width:::no-loc(=):::50% :::no-loc(})::: ---:::no-loc(>):::</span></span>
<span data-ttu-id="06ead-263">![퀀텀 teleportation 회로](:::no-loc(~):::/media/tp2.svg)</span><span class="sxs-lookup"><span data-stu-id="06ead-263">![Quantum teleportation circuit](:::no-loc(~):::/media/tp2.svg)</span></span>
