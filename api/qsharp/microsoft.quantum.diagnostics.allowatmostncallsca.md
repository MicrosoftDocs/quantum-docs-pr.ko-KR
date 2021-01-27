---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: AllowAtMostNCallsCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853532"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="39e70-102">AllowAtMostNCallsCA 작업</span><span class="sxs-lookup"><span data-stu-id="39e70-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="39e70-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="39e70-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="39e70-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39e70-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39e70-105">이 작업 및 해당 adjoint 호출 사이에는 지정 된 작업이 지정 된 횟수 만큼만 호출 됨을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e70-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="39e70-106">입력</span><span class="sxs-lookup"><span data-stu-id="39e70-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="39e70-107">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39e70-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39e70-108">호출 될 수 있는 최대 횟수입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="39e70-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="39e70-109">op: ' TInput => ' TOutput is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="39e70-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="39e70-110">호출을 제한 해야 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="39e70-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="39e70-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="39e70-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="39e70-112">실패 시 표시 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="39e70-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39e70-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39e70-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="39e70-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="39e70-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="39e70-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="39e70-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="39e70-116">' TOutput</span><span class="sxs-lookup"><span data-stu-id="39e70-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="39e70-117">예</span><span class="sxs-lookup"><span data-stu-id="39e70-117">Example</span></span>

<span data-ttu-id="39e70-118">다음 코드 조각은이 진단을 지 원하는 컴퓨터에서 실행 되는 경우 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e70-118">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a><span data-ttu-id="39e70-119">설명</span><span class="sxs-lookup"><span data-stu-id="39e70-119">Remarks</span></span>

<span data-ttu-id="39e70-120">이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="39e70-120">This operation may be replaced by a no-op on targets which do not support it.</span></span>