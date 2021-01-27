---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: ApplySeriesOfOpsA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: 052cb52d4ee6500e60043ab7f808497058924afe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844661"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="76d73-102">ApplySeriesOfOpsA 작업</span><span class="sxs-lookup"><span data-stu-id="76d73-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="76d73-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="76d73-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="76d73-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="76d73-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="76d73-105">Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="76d73-106">(Adjoint)</span><span class="sxs-lookup"><span data-stu-id="76d73-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="76d73-107">입력</span><span class="sxs-lookup"><span data-stu-id="76d73-107">Input</span></span>

### <a name="listofops--t--unit--is-adj"></a><span data-ttu-id="76d73-108">listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj []</span><span class="sxs-lookup"><span data-stu-id="76d73-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="76d73-109">각각의 배열을 적용 하는 작업의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="76d73-110">가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="76d73-111">각에는 adjoint 함수를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="76d73-112">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="76d73-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="76d73-113">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="76d73-114">각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="76d73-115">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="76d73-115">register : 'T[]</span></span>

<span data-ttu-id="76d73-116">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="76d73-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76d73-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76d73-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="76d73-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="76d73-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="76d73-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="76d73-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="76d73-120">예</span><span class="sxs-lookup"><span data-stu-id="76d73-120">Example</span></span>

<span data-ttu-id="76d73-121">다음은 Exp ([PauliX, PauliY], 0.5)를 PauliY에 적용 하 고, 1//then X to lybit 2 let ops = [Exp ([PauliX,], 0.5, _), ApplyToFirstQubitA (X, _)];를 적용 합니다. let 인덱스 = [[0, 1], [2]]; ApplySeriesOfOpsA (ops, 인덱스, 및 Bitbitarray);</span><span class="sxs-lookup"><span data-stu-id="76d73-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="76d73-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="76d73-122">See Also</span></span>

- [<span data-ttu-id="76d73-123">Microsoft. 양자. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="76d73-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)