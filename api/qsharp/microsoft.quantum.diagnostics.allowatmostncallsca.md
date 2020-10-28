---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: AllowAtMostNCallsCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713063"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="385f5-102">AllowAtMostNCallsCA 작업</span><span class="sxs-lookup"><span data-stu-id="385f5-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="385f5-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="385f5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="385f5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="385f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="385f5-105">이 작업 및 해당 adjoint 호출 사이에는 지정 된 작업이 지정 된 횟수 만큼만 호출 됨을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="385f5-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="385f5-106">입력</span><span class="sxs-lookup"><span data-stu-id="385f5-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="385f5-107">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="385f5-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="385f5-108">호출 될 수 있는 최대 횟수입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="385f5-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput-adj--ctl"></a><span data-ttu-id="385f5-109">op: ' TInput => ' TOutput Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="385f5-109">op : 'TInput => 'TOutput Adj + Ctl</span></span>

<span data-ttu-id="385f5-110">호출을 제한 해야 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="385f5-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="385f5-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="385f5-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="385f5-112">실패 시 표시 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="385f5-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="385f5-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="385f5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="385f5-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="385f5-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="385f5-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="385f5-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="385f5-116">' TOutput</span><span class="sxs-lookup"><span data-stu-id="385f5-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="385f5-117">설명</span><span class="sxs-lookup"><span data-stu-id="385f5-117">Remarks</span></span>

<span data-ttu-id="385f5-118">이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="385f5-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>