---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: PurifiedMixedStateWithData 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: c89ee8f5df58e5d6b154b67d2b39db208bc8a215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229956"
---
# <a name="purifiedmixedstatewithdata-function"></a><span data-ttu-id="9af01-102">PurifiedMixedStateWithData 함수</span><span class="sxs-lookup"><span data-stu-id="9af01-102">PurifiedMixedStateWithData function</span></span>

<span data-ttu-id="9af01-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="9af01-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="9af01-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9af01-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9af01-105">지정 된 데이터 컬렉션을 나타내는 레지스터와 함께 지정 된 혼합 된 상태의 purification을 준비 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-105">Returns an operation that prepares a a purification of a given mixed state, entangled with a register representing a given collection of data.</span></span>
<span data-ttu-id="9af01-106">"Purified mixed state with data"는 Σi √ pi | i ⟩ | 크 ⟩ | garbagei ⟩ 형식의 상태를 나타냅니다. 여기서 각 크 크는 register | i ⟩에 연결 된 추가 데이터를 인코딩하는 bitstring입니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-106">A "purified mixed state with data" refers to a state of the form Σᵢ √𝑝ᵢ |𝑖⟩ |𝑥ᵢ⟩ |garbageᵢ⟩, where each 𝑥ᵢ is a bitstring encoding additional data associated with the register |𝑖⟩.</span></span>

<span data-ttu-id="9af01-107">자세한 내용은 https://arxiv.org/pdf/1805.03662.pdf?page=15 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9af01-107">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="9af01-108">설명</span><span class="sxs-lookup"><span data-stu-id="9af01-108">Description</span></span>

<span data-ttu-id="9af01-109">는 퀀텀 ROM 기술을 사용 하 여 지정 된 밀도 행렬을 나타내고 해당 표현을 상태 준비 작업으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-109">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="9af01-110">특히 $ 계수의 $ \ alpha_j $ $N 목록과 각 계수와 연결 된 bitstring $ \vec{x} j $ 목록이 제공 됩니다._이 함수는 퀀텀 ROM 기술을 사용 하 여 근사값 $ $ \begin{align} \tilde\rho = \sum_{j = 0} ^ {n-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x}_j} \end{align} $ $의 혼합 된 상태 $ $ \begin{align} \rho = \sum_{j = 0} ^ {n-1} \ frac {| alpha_j |}을 준비 하는 작업을 반환 합니다. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x} _j}, \end{align} $ $ (각 $p _j alpha_j $는 $ $ \begin{align} \left | p_j \frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ $j $.</span><span class="sxs-lookup"><span data-stu-id="9af01-110">In particular, given a list of $N$ coefficients $\alpha_j$, and a bitstring $\vec{x}_j$ associated with each coefficient, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="9af01-111">에서 처음에는 $ \ket \ket{00\cdots 0} 상태로 인덱스 레지스터가 전달 되 고 가비지의 레지스터가 발생 합니다. {0} 반환 된 작업은 두 레지스터를 모두 $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _j} \ket{\text{garbage} _j}, \end{align} $ $로 반환 합니다 .이는 가비지 레지스터를 다시 설정 하거나 할당 취소 하 여 대상 오류 $ \tilde $ 내에서 원하는 준비를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-111">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j} \ket{\vec{x}_j} \ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="9af01-112">입력</span><span class="sxs-lookup"><span data-stu-id="9af01-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="9af01-113">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9af01-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9af01-114">$ \Epsilon $ 대상 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--doublebool"></a><span data-ttu-id="9af01-115">계수: ([Double](xref:microsoft.quantum.lang-ref.double),[Bool](xref:microsoft.quantum.lang-ref.bool)[]) []</span><span class="sxs-lookup"><span data-stu-id="9af01-115">coefficients : ([Double](xref:microsoft.quantum.lang-ref.double),[Bool](xref:microsoft.quantum.lang-ref.bool)[])[]</span></span>

<span data-ttu-id="9af01-116">각 계수와 연결 된 bitstring $ \vec{x} _j $와 함께 기본 상태의 확률을 지정 하는 $N $ 계수의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-116">Array of $N$ coefficients specifying the probability of basis states, along with the bitstring $\vec{x}_j$ associated with each coefficient.</span></span>
<span data-ttu-id="9af01-117">음수 $-\ alpha_j $는 긍정 $ | \ alpha_j | $로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="9af01-118">출력: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="9af01-118">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="9af01-119">$ \Tilde \rho $를 조인트 인덱스 및 가비지 레지스터에 purification로 준비 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-119">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af01-120">설명</span><span class="sxs-lookup"><span data-stu-id="9af01-120">Remarks</span></span>

<span data-ttu-id="9af01-121">이 작업에 제공 되는 계수는 1을 기준으로 정규화 됩니다 .이에 따라 계수는 항상 유효한 범주 확률 분포를 설명 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9af01-121">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="9af01-122">참조 항목</span><span class="sxs-lookup"><span data-stu-id="9af01-122">References</span></span>

- <span data-ttu-id="9af01-123">선형 T 복잡성 Ryan Babbush, Craig Gidney, Dominic Berry, 네, Spectra Wiebe, Jarrod McClean, Alexandru 고, 연한, 오스틴 Fowler, Hartmut Neven를 사용 하 여 퀀텀 회로에서 전자 인코딩 https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="9af01-123">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="9af01-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9af01-124">See Also</span></span>

- [<span data-ttu-id="9af01-125">PurifiedMixedState.</span><span class="sxs-lookup"><span data-stu-id="9af01-125">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)