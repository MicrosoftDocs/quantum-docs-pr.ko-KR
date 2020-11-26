---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: ApplyPermutationUsingDecompositionWithVariableOrder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: a5ca9b366f7ff477070e21fea047ff04b425439c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203436"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="2108c-102">ApplyPermutationUsingDecompositionWithVariableOrder 작업</span><span class="sxs-lookup"><span data-stu-id="2108c-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="2108c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="2108c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="2108c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2108c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2108c-105">분해 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2108c-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="2108c-106">설명</span><span class="sxs-lookup"><span data-stu-id="2108c-106">Description</span></span>

<span data-ttu-id="2108c-107">이 작업은 @"microsoft.quantum.synthesis.applypermutationusingdecomposition" 변수 순서를 지정할 수 있는 보다 일반적인 버전의입니다.</span><span class="sxs-lookup"><span data-stu-id="2108c-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="2108c-108">다른 변수 순서는 제어 되는 게이트에 사용 되는 분해 시퀀스와 진위 테이블을 변경 합니다 @"microsoft.quantum.intrinsic.x" .</span><span class="sxs-lookup"><span data-stu-id="2108c-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="2108c-109">따라서 변수 순서를 변경 하면 순열 실현에 사용 되는 전체 게이트 수가 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2108c-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="2108c-110">입력</span><span class="sxs-lookup"><span data-stu-id="2108c-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="2108c-111">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2108c-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2108c-112">0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.</span><span class="sxs-lookup"><span data-stu-id="2108c-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="2108c-113">variableOrder: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2108c-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2108c-114">0부터 시작 하는 $n $ 요소의 순열입니다.</span><span class="sxs-lookup"><span data-stu-id="2108c-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="2108c-115">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2108c-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2108c-116">순열이 적용 되는 $ 이상 비트 $n 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2108c-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2108c-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2108c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="2108c-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2108c-118">See Also</span></span>

- [<span data-ttu-id="2108c-119">ApplyPermutationUsingDecomposition.</span><span class="sxs-lookup"><span data-stu-id="2108c-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="2108c-120">ApplyPermutationUsingTransformation.</span><span class="sxs-lookup"><span data-stu-id="2108c-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)