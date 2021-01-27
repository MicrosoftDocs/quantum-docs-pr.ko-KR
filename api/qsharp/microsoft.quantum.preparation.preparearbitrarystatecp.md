---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateCP
title: PrepareArbitraryStateCP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateCP
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 1e293057f8b549dc57817cdce350e50e2b91682a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856918"
---
# <a name="preparearbitrarystatecp-operation"></a><span data-ttu-id="16d1e-102">PrepareArbitraryStateCP 작업</span><span class="sxs-lookup"><span data-stu-id="16d1e-102">PrepareArbitraryStateCP operation</span></span>

<span data-ttu-id="16d1e-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="16d1e-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="16d1e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="16d1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="16d1e-105">계수 집합과 작은 endian 인코딩된 퀀텀 레지스터가 지정 된 경우는 지정 된 계수에 설명 된 레지스터에 상태를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryStateCP (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="16d1e-106">설명</span><span class="sxs-lookup"><span data-stu-id="16d1e-106">Description</span></span>

<span data-ttu-id="16d1e-107">이 작업을 수행 하면 $n $-stbit compute 기준 상태 $ \ket{0 \cdots} $에서 _j e ^ {i t_j} $ $r 복합 계수를 사용 하 여 임의의 퀀텀 상태 $ $가 준비 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="16d1e-108">특히이 작업의 작업은 모든 0에서 다음과 같이 작동 하는 단일 변환 $U $에서 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="16d1e-109">$ $ \begin{align} U\ket {0 ... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="16d1e-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="16d1e-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="16d1e-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="16d1e-111">입력</span><span class="sxs-lookup"><span data-stu-id="16d1e-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="16d1e-112">계수: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="16d1e-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="16d1e-113">절대 값으로 표현 되는 $2 ^ n $ 복합 계수와 $ (r_j, t_j) $ 단계로 이루어진 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="16d1e-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="16d1e-115">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="16d1e-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="16d1e-116">이상 비트 레지스터 인코딩 번호는 작은 endian 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="16d1e-117">이는 계산 기준 상태 $ \ket{0...0} $에서 초기화 될 것으로 예상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16d1e-118">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16d1e-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="16d1e-119">설명</span><span class="sxs-lookup"><span data-stu-id="16d1e-119">Remarks</span></span>

<span data-ttu-id="16d1e-120">음수 입력 계수 $r _j < $0는 값 $ | r_j | $로 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="16d1e-121">`coefficients` $2 ^ n $ 보다 작은 경우는 $ (r_j, t_j) = (0.0, 0.0) $ 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="16d1e-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="16d1e-122">참조</span><span class="sxs-lookup"><span data-stu-id="16d1e-122">References</span></span>

- <span data-ttu-id="16d1e-123">퀀텀 논리 회로 Vivek Shende, Stephen S. Markov, Igor, Igor L. https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="16d1e-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="16d1e-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="16d1e-124">See Also</span></span>

- [<span data-ttu-id="16d1e-125">ApproximatelyPrepareArbitraryState.</span><span class="sxs-lookup"><span data-stu-id="16d1e-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)