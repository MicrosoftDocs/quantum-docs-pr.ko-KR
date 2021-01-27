---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: ApplyPermutationUsingTransformation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: 79913bec44514d477b7ee0668b43396b297b9ab8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858990"
---
# <a name="applypermutationusingtransformation-operation"></a><span data-ttu-id="205c7-102">ApplyPermutationUsingTransformation 작업</span><span class="sxs-lookup"><span data-stu-id="205c7-102">ApplyPermutationUsingTransformation operation</span></span>

<span data-ttu-id="205c7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="205c7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="205c7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="205c7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="205c7-105">변형 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-105">Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="205c7-106">설명</span><span class="sxs-lookup"><span data-stu-id="205c7-106">Description</span></span>

<span data-ttu-id="205c7-107">이 절차에서는 단방향 변환 기반 합성 방식을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-107">This procedure implements the unidirectional transformation based synthesis approach.</span></span>  <span data-ttu-id="205c7-108">입력은 $2 ^ n $ elements $ \{ 0, \pi, 2 ^ n-1 $을 통한 순열 $ \pi $ \} 로, $n $-변수가 해독 가능한 부울 함수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-108">Input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="205c7-109">알고리즘은 다음 단계를 반복적으로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-109">The algorithm performs iteratively the following steps:</span></span>

1. <span data-ttu-id="205c7-110">$X \ne \ pi (x) = y $와 같은 가장 작은 $x $를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-110">Find smallest $x$ such that $x \ne \pi(x) = y$.</span></span>
2. <span data-ttu-id="205c7-111">출력에 적용 되는 여러 제어 된 Toffoli 작업을 찾습니다. $ \pi (x) = x $를 사용 하 고 모든 $x ' < x $에 대해 $ \pi (x ') $를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-111">Find multiple-controlled Toffoli operations, which applied to the outputs make $\pi(x) = x$ and do not change $\pi(x')$ for all $x' < x$</span></span>

## <a name="input"></a><span data-ttu-id="205c7-112">입력</span><span class="sxs-lookup"><span data-stu-id="205c7-112">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="205c7-113">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="205c7-113">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="205c7-114">0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-114">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="205c7-115">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="205c7-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="205c7-116">순열이 적용 되는 $ 이상 비트 $n 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="205c7-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="205c7-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="205c7-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="205c7-118">예</span><span class="sxs-lookup"><span data-stu-id="205c7-118">Example</span></span>

<span data-ttu-id="205c7-119">작업을 합성 하려면 `SWAP` :</span><span class="sxs-lookup"><span data-stu-id="205c7-119">To synthesize a `SWAP` operation:</span></span>

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingTransformation([0, 2, 1, 3], LittleEndian(qubits));
}
```

## <a name="references"></a><span data-ttu-id="205c7-120">참조</span><span class="sxs-lookup"><span data-stu-id="205c7-120">References</span></span>

- [<span data-ttu-id="205c7-121">*D. Michael*, *Dmitri Maslov*, *Gerhard Dueck* 318-323 2003,,,, 2003</span><span class="sxs-lookup"><span data-stu-id="205c7-121">*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, Proc. DAC 2003, IEEE, pp. 318-323, 2003</span></span>](https://doi.org/10.1145/775832.775915)
- [<span data-ttu-id="205c7-122">*Mathias Soeken*, *Gerhard, Dueck*, *dmichael*, Proc .rc 2016, Springer, pp. 307-321, 2016</span><span class="sxs-lookup"><span data-stu-id="205c7-122">*Mathias Soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, Proc. RC 2016, Springer, pp. 307-321, 2016</span></span>](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a><span data-ttu-id="205c7-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="205c7-123">See Also</span></span>

- [<span data-ttu-id="205c7-124">ApplyPermutationUsingDecomposition.</span><span class="sxs-lookup"><span data-stu-id="205c7-124">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)