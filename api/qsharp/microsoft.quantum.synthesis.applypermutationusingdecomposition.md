---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: ApplyPermutationUsingDecomposition 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 40b51807da155c57c3fa8d740eff28ceef0a0ffc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725317"
---
# <a name="applypermutationusingdecomposition-operation"></a><span data-ttu-id="80b31-102">ApplyPermutationUsingDecomposition 작업</span><span class="sxs-lookup"><span data-stu-id="80b31-102">ApplyPermutationUsingDecomposition operation</span></span>

<span data-ttu-id="80b31-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="80b31-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="80b31-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80b31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80b31-105">분해 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="80b31-106">Description</span><span class="sxs-lookup"><span data-stu-id="80b31-106">Description</span></span>

<span data-ttu-id="80b31-107">이 절차에서는 분해 기반 합성 방식을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-107">This procedure implements the decomposition based synthesis approach.</span></span>  <span data-ttu-id="80b31-108">입력은 $2 ^ n $ elements $ \{ 0, \pi, 2 ^ n-1 \} $이 고 $n $-변수가 해독 가능한 부울 함수를 나타내는 순열 $ \pi $입니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-108">The input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="80b31-109">알고리즘은 각 변수 인덱스에 대해 다음 단계를 반복적으로 수행 합니다 $i $:</span><span class="sxs-lookup"><span data-stu-id="80b31-109">The algorithm iteratively performs the following steps for each variable index $i$:</span></span>

1. <span data-ttu-id="80b31-110">$ ((\ Pi_l, \ pi_r), \pi ') $를 계산 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소에서 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-110">Compute $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>
2. <span data-ttu-id="80b31-111">$ \Pi \leftarrow \pi ' $를 설정 하 고 고정 지점이 아닌 요소에 따라 $ \ pi_l $ 및 $ \ pi_r $에서 valtables를 파생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-111">Set $\pi \leftarrow \pi'$, and derive truth tables from $\pi_l$ and $\pi_r$ based on elements that are not fixed-points.</span></span>

<span data-ttu-id="80b31-112">모든 변수 인덱스에 대해 이러한 단계를 적용 한 후 나머지 순열 $ \pi $는 id가 되며 수집 된 진위 테이블 및 인덱스에 따라 작업을 사용 하 여 sttable 제어 된 작업을 적용할 수 있습니다 @"microsoft.quantum.intrinsic.x" @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" .</span><span class="sxs-lookup"><span data-stu-id="80b31-112">After applying these steps for all variable indexes, the remaining permutation $\pi$ will be the identity, and based on the collected truth tables and indexes, one can apply truth-table controlled @"microsoft.quantum.intrinsic.x" operations using the @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" operation.</span></span>

<span data-ttu-id="80b31-113">변수 순서는 $0, \ 점, n-$1입니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-113">The variable order is $0, \dots, n - 1$.</span></span>  <span data-ttu-id="80b31-114">작업에서 사용자 지정 변수 순서를 지정할 수 있습니다 @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .</span><span class="sxs-lookup"><span data-stu-id="80b31-114">A custom variable order can be specified in the operation @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder".</span></span>

## <a name="input"></a><span data-ttu-id="80b31-115">입력</span><span class="sxs-lookup"><span data-stu-id="80b31-115">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="80b31-116">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="80b31-116">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="80b31-117">0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-117">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="80b31-118">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="80b31-118">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="80b31-119">순열이 적용 되는 $ 이상 비트 $n 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="80b31-119">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="80b31-120">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="80b31-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="80b31-121">참조</span><span class="sxs-lookup"><span data-stu-id="80b31-121">References</span></span>

- [<span data-ttu-id="80b31-122">*Alexis De Vos* , *Yvan Van rentergem* , 고급 (2), 2008, pp. 183--200</span><span class="sxs-lookup"><span data-stu-id="80b31-122">*Alexis De Vos* , *Yvan Van Rentergem* , Adv. in Math. of Comm. 2(2), 2008, pp. 183--200</span></span>](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [<span data-ttu-id="80b31-123">*Mathias Soeken* , *김 Tague* , *Gerhard* Dueck, *Rolf Drechsler* , 기호화 된 계산 73 (2016), pp. 1--26의 저널</span><span class="sxs-lookup"><span data-stu-id="80b31-123">*Mathias Soeken* , *Laura Tague* , *Gerhard W. Dueck* , *Rolf Drechsler* , Journal of Symbolic Computation 73 (2016), pp. 1--26</span></span>](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a><span data-ttu-id="80b31-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="80b31-124">See Also</span></span>

- [<span data-ttu-id="80b31-125">ApplyPermutationUsingDecompositionWithVariableOrder.</span><span class="sxs-lookup"><span data-stu-id="80b31-125">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [<span data-ttu-id="80b31-126">ApplyPermutationUsingTransformation.</span><span class="sxs-lookup"><span data-stu-id="80b31-126">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)