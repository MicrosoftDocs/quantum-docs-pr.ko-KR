---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: ApplySeriesOfOpsC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: 308256833dc607f685e3a5f2278e374cf3b6ce22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844640"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="6d339-102">ApplySeriesOfOpsC 작업</span><span class="sxs-lookup"><span data-stu-id="6d339-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="6d339-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6d339-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6d339-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d339-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d339-105">Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="6d339-106">제어</span><span class="sxs-lookup"><span data-stu-id="6d339-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="6d339-107">입력</span><span class="sxs-lookup"><span data-stu-id="6d339-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="6d339-108">listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl []입니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="6d339-109">각각의 배열을 적용 하는 작업의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="6d339-110">가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="6d339-111">각에는 제어 되는 함수를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="6d339-112">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="6d339-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="6d339-113">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="6d339-114">각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="6d339-115">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="6d339-115">register : 'T[]</span></span>

<span data-ttu-id="6d339-116">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="6d339-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6d339-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6d339-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6d339-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d339-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6d339-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="6d339-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="6d339-120">예</span><span class="sxs-lookup"><span data-stu-id="6d339-120">Example</span></span>

<span data-ttu-id="6d339-121">다음은 Exp ([PauliX, PauliY], 0.5)를 PauliY에 적용 하 고, 1//then X to lybit 2 let ops = [Exp ([PauliX,], 0.5, _), ApplyToFirstQubitC (X, _)];를 적용 합니다. let 인덱스 = [[0, 1], [2]]; ApplySeriesOfOpsC (ops, 인덱스, 및 Bitbitarray);</span><span class="sxs-lookup"><span data-stu-id="6d339-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitC(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsC(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="6d339-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6d339-122">See Also</span></span>

- [<span data-ttu-id="6d339-123">Microsoft. 양자. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="6d339-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)