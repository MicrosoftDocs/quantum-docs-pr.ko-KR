---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: AllowAtMostNCallsCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 7caf33e33318bb74cb160436940eff9f0f2782cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202569"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="1fb98-102">AllowAtMostNCallsCA 작업</span><span class="sxs-lookup"><span data-stu-id="1fb98-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="1fb98-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="1fb98-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="1fb98-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fb98-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fb98-105">이 작업 및 해당 adjoint 호출 사이에는 지정 된 작업이 지정 된 횟수 만큼만 호출 됨을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb98-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="1fb98-106">입력</span><span class="sxs-lookup"><span data-stu-id="1fb98-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="1fb98-107">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1fb98-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1fb98-108">호출 될 수 있는 최대 횟수입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="1fb98-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="1fb98-109">op: ' TInput => ' TOutput is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="1fb98-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="1fb98-110">호출을 제한 해야 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1fb98-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="1fb98-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="1fb98-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="1fb98-112">실패 시 표시 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1fb98-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1fb98-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1fb98-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1fb98-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fb98-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="1fb98-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="1fb98-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="1fb98-116">' TOutput</span><span class="sxs-lookup"><span data-stu-id="1fb98-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="1fb98-117">설명</span><span class="sxs-lookup"><span data-stu-id="1fb98-117">Remarks</span></span>

<span data-ttu-id="1fb98-118">이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb98-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>