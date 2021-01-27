---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: ApplySeriesOfOps 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841507"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="cc6aa-102">ApplySeriesOfOps 작업</span><span class="sxs-lookup"><span data-stu-id="cc6aa-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="cc6aa-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cc6aa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cc6aa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc6aa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc6aa-105">Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6aa-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="cc6aa-106">입력</span><span class="sxs-lookup"><span data-stu-id="cc6aa-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="cc6aa-107">listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="cc6aa-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="cc6aa-108">각각의 배열을 적용 하는 작업의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cc6aa-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="cc6aa-109">가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc6aa-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="cc6aa-110">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="cc6aa-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="cc6aa-111">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="cc6aa-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="cc6aa-112">각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6aa-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="cc6aa-113">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="cc6aa-113">register : 'T[]</span></span>

<span data-ttu-id="cc6aa-114">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="cc6aa-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cc6aa-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cc6aa-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cc6aa-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cc6aa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cc6aa-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="cc6aa-117">'T</span></span>



## <a name="example"></a><span data-ttu-id="cc6aa-118">예</span><span class="sxs-lookup"><span data-stu-id="cc6aa-118">Example</span></span>

<span data-ttu-id="cc6aa-119">다음은 Exp ([PauliX, PauliY], 0.5)를 PauliY에 적용 하 고, 1//then X to ybit 2 let ops = [Exp ([PauliX,], 0.5, _), Applytofirst Bit (X, _)];를 적용 합니다. let 인덱스 = [[0, 1], [2]]; ApplySeriesOfOps (ops, 인덱스, 및 Bitbitarray);</span><span class="sxs-lookup"><span data-stu-id="cc6aa-119">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubit(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOps(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="cc6aa-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cc6aa-120">See Also</span></span>

- [<span data-ttu-id="cc6aa-121">Microsoft. 양자. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="cc6aa-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)