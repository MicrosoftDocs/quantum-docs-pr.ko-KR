---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState
title: ApproximatelyPrepareArbitraryState 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryState
qsharp.summary: >-
  > [!WARNING]

  > ApproximatelyPrepareArbitraryState has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> instead.


  Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: 9e1b172258acd0cb09b824a773e7e79d44fec20c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193712"
---
# <a name="approximatelypreparearbitrarystate-operation"></a><span data-ttu-id="88f2a-102">ApproximatelyPrepareArbitraryState 작업</span><span class="sxs-lookup"><span data-stu-id="88f2a-102">ApproximatelyPrepareArbitraryState operation</span></span>

<span data-ttu-id="88f2a-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="88f2a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="88f2a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="88f2a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="88f2a-105">ApproximatelyPrepareArbitraryState는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-105">ApproximatelyPrepareArbitraryState has been deprecated.</span></span> <span data-ttu-id="88f2a-106">대신 <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="88f2a-106">Please use <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="88f2a-107">계수 집합 및 작은 endian로 인코딩된 퀀텀 레지스터가 지정 된 경우 지정 된 계수에 의해 설명 된 레지스터의 상태를 지정 된 근사값까지 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-107">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryState (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="88f2a-108">Description</span><span class="sxs-lookup"><span data-stu-id="88f2a-108">Description</span></span>

<span data-ttu-id="88f2a-109">이 작업을 수행 하면 $n $-stbit compute 기준 상태 $ \ket{0 \cdots} $에서 _j e ^ {i t_j} $ $r 복합 계수를 사용 하 여 임의의 퀀텀 상태 $ $가 준비 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-109">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="88f2a-110">특히이 작업의 작업은 모든 0에서 다음과 같이 작동 하는 단일 변환 $U $에서 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-110">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="88f2a-111">$ $ \begin{align} U\ket {0 ... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="88f2a-111">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="88f2a-112">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="88f2a-112">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="88f2a-113">입력</span><span class="sxs-lookup"><span data-stu-id="88f2a-113">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="88f2a-114">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="88f2a-114">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="88f2a-115">지정 된 상태를 준비할 때 사용할 근사 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-115">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--complexpolar"></a><span data-ttu-id="88f2a-116">계수: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="88f2a-116">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="88f2a-117">절대 값으로 표현 되는 $2 ^ n $ 복합 계수와 $ (r_j, t_j) $ 단계로 이루어진 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-117">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="88f2a-118">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-118">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="88f2a-119">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="88f2a-119">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="88f2a-120">이상 비트 레지스터 인코딩 번호는 작은 endian 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-120">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="88f2a-121">이는 계산 기준 상태 $ \ket{0...0} $에서 초기화 될 것으로 예상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-121">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="88f2a-122">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88f2a-122">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="88f2a-123">설명</span><span class="sxs-lookup"><span data-stu-id="88f2a-123">Remarks</span></span>

<span data-ttu-id="88f2a-124">음수 입력 계수 $r _j < $0는 값 $ | r_j | $로 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-124">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="88f2a-125">`coefficients` $2 ^ n $ 보다 작은 경우는 $ (r_j, t_j) = (0.0, 0.0) $ 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="88f2a-125">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="88f2a-126">참조 항목</span><span class="sxs-lookup"><span data-stu-id="88f2a-126">References</span></span>

- <span data-ttu-id="88f2a-127">퀀텀 논리 회로 Vivek Shende, Stephen S. Markov, Igor, Igor L. https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="88f2a-127">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="88f2a-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="88f2a-128">See Also</span></span>

- [<span data-ttu-id="88f2a-129">ApproximatelyPrepareArbitraryState.</span><span class="sxs-lookup"><span data-stu-id="88f2a-129">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)