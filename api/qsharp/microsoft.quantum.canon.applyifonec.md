---
uid: Microsoft.Quantum.Canon.ApplyIfOneC
title: ApplyIfOneC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being one.
ms.openlocfilehash: 9a2e020c596b02d9cb38309d02ca02056c1dec75
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718089"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="592fd-102">ApplyIfOneC 작업</span><span class="sxs-lookup"><span data-stu-id="592fd-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="592fd-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="592fd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="592fd-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="592fd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="592fd-105">기존 결과 값에 조건 화 된 제어 가능한 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-105">Applies a controllable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="592fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="592fd-106">Description</span></span>

<span data-ttu-id="592fd-107">작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="592fd-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="592fd-108">이면이 `Zero` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="592fd-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="592fd-109">접미사는 적용 되는 작업을 제어할 수 있음을 `C` 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="592fd-110">입력</span><span class="sxs-lookup"><span data-stu-id="592fd-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="592fd-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="592fd-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="592fd-112">Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="592fd-113">op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="592fd-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="592fd-114">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="592fd-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="592fd-115">target : 'T</span></span>

<span data-ttu-id="592fd-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="592fd-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="592fd-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="592fd-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="592fd-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="592fd-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="592fd-119">'T</span></span>

<span data-ttu-id="592fd-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="592fd-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="592fd-121">See Also</span></span>

- [<span data-ttu-id="592fd-122">Microsoft. 양자. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="592fd-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="592fd-123">Microsoft. 양자. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="592fd-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="592fd-124">ApplyIfOneCA입니다.</span><span class="sxs-lookup"><span data-stu-id="592fd-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)