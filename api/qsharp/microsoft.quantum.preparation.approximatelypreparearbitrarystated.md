---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateD
title: ApproximatelyPrepareArbitraryStateD 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: 822efe08e66c43b7a3128d100e3e58a8c2ce3c2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193593"
---
# <a name="approximatelypreparearbitrarystated-operation"></a><span data-ttu-id="4a198-102">ApproximatelyPrepareArbitraryStateD 작업</span><span class="sxs-lookup"><span data-stu-id="4a198-102">ApproximatelyPrepareArbitraryStateD operation</span></span>

<span data-ttu-id="4a198-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="4a198-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="4a198-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a198-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a198-105">계수 집합 및 작은 endian로 인코딩된 퀀텀 레지스터가 지정 된 경우 지정 된 계수에 의해 설명 된 레지스터의 상태를 지정 된 근사값까지 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryStateD (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4a198-106">Description</span><span class="sxs-lookup"><span data-stu-id="4a198-106">Description</span></span>

<span data-ttu-id="4a198-107">이 작업을 수행 하면 $n $-stbit compute 기준 상태 $ \ket{0 \cdots} $에서 _j e ^ {i t_j} $ $r 복합 계수를 사용 하 여 임의의 퀀텀 상태 $ $가 준비 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="4a198-108">특히이 작업의 작업은 모든 0에서 다음과 같이 작동 하는 단일 변환 $U $에서 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="4a198-109">$ $ \begin{align} U\ket {0 ... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="4a198-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="4a198-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="4a198-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="4a198-111">입력</span><span class="sxs-lookup"><span data-stu-id="4a198-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="4a198-112">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4a198-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4a198-113">지정 된 상태를 준비할 때 사용할 근사 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-113">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="4a198-114">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4a198-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4a198-115">최대 $2 ^ n $ real 계수의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-115">Array of up to $2^n$ real coefficients.</span></span> <span data-ttu-id="4a198-116">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="4a198-117">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4a198-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4a198-118">이상 비트 레지스터 인코딩 번호는 작은 endian 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="4a198-119">이는 계산 기준 상태 $ \ket{0...0} $에서 초기화 될 것으로 예상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4a198-120">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a198-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4a198-121">설명</span><span class="sxs-lookup"><span data-stu-id="4a198-121">Remarks</span></span>

<span data-ttu-id="4a198-122">음수 입력 계수 $r _j < $0는 값 $ | r_j | $로 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="4a198-123">`coefficients` $2 ^ n $ 보다 작은 경우는 $ (r_j, t_j) = (0.0, 0.0) $ 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="4a198-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="4a198-124">참조 항목</span><span class="sxs-lookup"><span data-stu-id="4a198-124">References</span></span>

- <span data-ttu-id="4a198-125">퀀텀 논리 회로 Vivek Shende, Stephen S. Markov, Igor, Igor L. https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="4a198-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>