---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: ApplySeriesOfOpsCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9dd1343b3ebcc75592441f150eee822cfe83f9a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217886"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="97336-102">ApplySeriesOfOpsCA 작업</span><span class="sxs-lookup"><span data-stu-id="97336-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="97336-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97336-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97336-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="97336-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="97336-105">Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97336-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="97336-106">(Adjoint + 제어 됨)</span><span class="sxs-lookup"><span data-stu-id="97336-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="97336-107">입력</span><span class="sxs-lookup"><span data-stu-id="97336-107">Input</span></span>

### <a name="listofops--t--unit--is-adj--ctl"></a><span data-ttu-id="97336-108">listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl []</span><span class="sxs-lookup"><span data-stu-id="97336-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="97336-109">각각의 배열을 적용 하는 작업의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="97336-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="97336-110">가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97336-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="97336-111">각에는 Adjoint 및 제어 된 함수를 모두 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97336-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="97336-112">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="97336-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="97336-113">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="97336-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="97336-114">각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97336-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="97336-115">등록: ' t []</span><span class="sxs-lookup"><span data-stu-id="97336-115">register : 'T[]</span></span>

<span data-ttu-id="97336-116">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="97336-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97336-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97336-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="97336-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="97336-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="97336-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="97336-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="97336-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="97336-120">See Also</span></span>

- [<span data-ttu-id="97336-121">Microsoft. 양자. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="97336-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)