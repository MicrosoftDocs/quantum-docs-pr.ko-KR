---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: ApplyPermutationUsingDecompositionWithVariableOrder 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: f33d2980ff1775b1ae8d2e2e7a4fa1e5cbe7d5ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858873"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="5bf1d-102">ApplyPermutationUsingDecompositionWithVariableOrder 작업</span><span class="sxs-lookup"><span data-stu-id="5bf1d-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="5bf1d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5bf1d-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5bf1d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5bf1d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5bf1d-105">분해 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5bf1d-106">설명</span><span class="sxs-lookup"><span data-stu-id="5bf1d-106">Description</span></span>

<span data-ttu-id="5bf1d-107">이 작업은 @"microsoft.quantum.synthesis.applypermutationusingdecomposition" 변수 순서를 지정할 수 있는 보다 일반적인 버전의입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="5bf1d-108">다른 변수 순서는 제어 되는 게이트에 사용 되는 분해 시퀀스와 진위 테이블을 변경 합니다 @"microsoft.quantum.intrinsic.x" .</span><span class="sxs-lookup"><span data-stu-id="5bf1d-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="5bf1d-109">따라서 변수 순서를 변경 하면 순열 실현에 사용 되는 전체 게이트 수가 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="5bf1d-110">입력</span><span class="sxs-lookup"><span data-stu-id="5bf1d-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="5bf1d-111">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5bf1d-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5bf1d-112">0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="5bf1d-113">variableOrder: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5bf1d-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5bf1d-114">0부터 시작 하는 $n $ 요소의 순열입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="5bf1d-115">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5bf1d-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5bf1d-116">순열이 적용 되는 $ 이상 비트 $n 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5bf1d-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5bf1d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="5bf1d-118">예</span><span class="sxs-lookup"><span data-stu-id="5bf1d-118">Example</span></span>

<span data-ttu-id="5bf1d-119">작업을 합성 하려면 `SWAP` :</span><span class="sxs-lookup"><span data-stu-id="5bf1d-119">To synthesize a `SWAP` operation:</span></span>

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingDecompositionWithVariableOrder([0, 2, 1, 3], [1, 0], LittleEndian(qubits));
}
```

## <a name="see-also"></a><span data-ttu-id="5bf1d-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5bf1d-120">See Also</span></span>

- [<span data-ttu-id="5bf1d-121">ApplyPermutationUsingDecomposition.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-121">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="5bf1d-122">ApplyPermutationUsingTransformation.</span><span class="sxs-lookup"><span data-stu-id="5bf1d-122">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)