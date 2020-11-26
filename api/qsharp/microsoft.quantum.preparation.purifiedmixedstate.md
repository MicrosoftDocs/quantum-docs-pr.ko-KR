---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: PurifiedMixedState 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 73b031f1082d0a12975abad074b07184dcbabdbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230024"
---
# <a name="purifiedmixedstate-function"></a><span data-ttu-id="04f55-102">PurifiedMixedState 함수</span><span class="sxs-lookup"><span data-stu-id="04f55-102">PurifiedMixedState function</span></span>

<span data-ttu-id="04f55-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="04f55-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="04f55-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="04f55-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="04f55-105">지정 된 혼합 상태의 purification을 준비 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-105">Returns an operation that prepares a a purification of a given mixed state.</span></span>
<span data-ttu-id="04f55-106">"Purified mixed state"는 계수 {pi}의 벡터로 지정 된 | ψ ⟩ = Σi √ pi | i ⟩ | garbagei ⟩ 형식의 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-106">A "purified mixed state" refers to states of the form |ψ⟩ = Σᵢ √𝑝ᵢ |𝑖⟩ |garbageᵢ⟩ specified by a vector of coefficients {𝑝ᵢ}.</span></span> <span data-ttu-id="04f55-107">이 양식의 상태를 혼합 된 상태 ρ ≔ pi | i ⟩ ⟨ i로 줄일 수 있습니다. "가비지" 레지스터를 추적 하는 방법 (즉, 계산 기반의 대각선 인 혼합 된 상태).</span><span class="sxs-lookup"><span data-stu-id="04f55-107">States of this form can be reduced to mixed states ρ ≔ 𝑝ᵢ |𝑖⟩⟨𝑖| by tracing over the "garbage" register (that is, a mixed state that is diagonal in the computational basis).</span></span>

<span data-ttu-id="04f55-108">자세한 내용은 https://arxiv.org/pdf/1805.03662.pdf?page=15 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="04f55-108">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="04f55-109">설명</span><span class="sxs-lookup"><span data-stu-id="04f55-109">Description</span></span>

<span data-ttu-id="04f55-110">는 퀀텀 ROM 기술을 사용 하 여 지정 된 밀도 행렬을 나타내고 해당 표현을 상태 준비 작업으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-110">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="04f55-111">특히 $ 계수의 $ \ alpha_j $ $N 목록이 제공 됩니다 .이 함수는 퀀텀 ROM 기술을 사용 하 여 근사값 $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \end{align} $ $을 (를) 혼합 된 상태 $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ frac {| alpha_j |}에 대해 준비 하는 작업을 반환 합니다. {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{align} $ $ $p 각 _j $는 지정 된 계수 $ \ alpha_j $와 같이 $ $ \begin{align} \left | p_j \frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ $j $.</span><span class="sxs-lookup"><span data-stu-id="04f55-111">In particular, given a list of $N$ coefficients $\alpha_j$, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="04f55-112">에서 인덱스 레지스터가 전달 되 고 가비지를 등록 하는 경우 처음에는 $ \ket {0} \ket{00\cdots 0} 상태에서 반환 된 작업을 통해 $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _j}, \end{align} $ $의 purification에 두 레지스터를 모두 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-112">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="04f55-113">입력</span><span class="sxs-lookup"><span data-stu-id="04f55-113">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="04f55-114">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="04f55-114">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="04f55-115">$ \Epsilon $ 대상 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-115">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="04f55-116">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="04f55-116">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="04f55-117">기본 상태의 확률을 지정 하는 $N $ 계수의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-117">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="04f55-118">음수 $-\ alpha_j $는 긍정 $ | \ alpha_j | $로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-118">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="04f55-119">출력: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="04f55-119">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="04f55-120">$ \Tilde \rho $를 조인트 인덱스 및 가비지 레지스터에 purification로 준비 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-120">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f55-121">설명</span><span class="sxs-lookup"><span data-stu-id="04f55-121">Remarks</span></span>

<span data-ttu-id="04f55-122">이 작업에 제공 되는 계수는 1을 기준으로 정규화 됩니다 .이에 따라 계수는 항상 유효한 범주 확률 분포를 설명 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04f55-122">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="04f55-123">참조</span><span class="sxs-lookup"><span data-stu-id="04f55-123">References</span></span>

- <span data-ttu-id="04f55-124">선형 T 복잡성 Ryan Babbush, Craig Gidney, Dominic Berry, 네, Spectra Wiebe, Jarrod McClean, Alexandru 고, 연한, 오스틴 Fowler, Hartmut Neven를 사용 하 여 퀀텀 회로에서 전자 인코딩 https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="04f55-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="04f55-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="04f55-125">See Also</span></span>

- [<span data-ttu-id="04f55-126">PurifiedMixedStateWithData.</span><span class="sxs-lookup"><span data-stu-id="04f55-126">Microsoft.Quantum.Preparation.PurifiedMixedStateWithData</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)