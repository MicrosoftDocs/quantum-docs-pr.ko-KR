---
uid: Microsoft.Quantum.Canon.ApplyIfElseRC
title: ApplyIfElseRC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical result.
ms.openlocfilehash: b2e4ade84b25b0100fe4b69814c760a672833f06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209488"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="c7be2-102">ApplyIfElseRC 작업</span><span class="sxs-lookup"><span data-stu-id="c7be2-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="c7be2-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7be2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7be2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7be2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7be2-105">클래식 결과의 값에 따라 제어 가능한 두 작업 중 하나를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-105">Applies one of two controllable operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRC<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Ctl), oneInput : 'U)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="c7be2-106">Description</span><span class="sxs-lookup"><span data-stu-id="c7be2-106">Description</span></span>

<span data-ttu-id="c7be2-107">결과를 제공 하면 `result` 가와 같은 경우에는를 사용 하 여 작업을 적용 하 `zeroOp` `zeroInput` `result` `Zero` 고가 적용 됩니다 `oneOp(oneInput)` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="c7be2-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="c7be2-108">입력</span><span class="sxs-lookup"><span data-stu-id="c7be2-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="c7be2-109">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="c7be2-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="c7be2-110">또는이 적용 되었는지 확인 하는 데 사용 되는 측정 결과 `zeroOp` `oneOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-ctl"></a><span data-ttu-id="c7be2-111">zeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="c7be2-112">일 때 적용 되는 제어 가능한 작업 `result == Zero` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-112">The controllable operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="c7be2-113">zeroInput: ' '</span><span class="sxs-lookup"><span data-stu-id="c7be2-113">zeroInput : 'T</span></span>

<span data-ttu-id="c7be2-114">때 제공 되는 입력입니다 `zeroOp` `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="c7be2-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-ctl"></a><span data-ttu-id="c7be2-115">oneOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="c7be2-116">일 때 적용 되는 제어 가능한 작업 `result == One` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-116">The controllable operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="c7be2-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="c7be2-117">oneInput : 'U</span></span>

<span data-ttu-id="c7be2-118">때 제공 되는 입력입니다 `oneOp` `result == One` .</span><span class="sxs-lookup"><span data-stu-id="c7be2-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c7be2-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7be2-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c7be2-120">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7be2-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c7be2-121">없습니다</span><span class="sxs-lookup"><span data-stu-id="c7be2-121">'T</span></span>

<span data-ttu-id="c7be2-122">조건부로 적용할 작업의 입력 형식 `zeroOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="c7be2-123">' U</span><span class="sxs-lookup"><span data-stu-id="c7be2-123">'U</span></span>

<span data-ttu-id="c7be2-124">조건부로 적용할 작업의 입력 형식 `oneOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c7be2-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7be2-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c7be2-125">See Also</span></span>

- [<span data-ttu-id="c7be2-126">Microsoft. 양자. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="c7be2-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="c7be2-127">Microsoft. 양자. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="c7be2-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="c7be2-128">Microsoft. 양자. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="c7be2-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="c7be2-129">Microsoft. 양자. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="c7be2-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="c7be2-130">Microsoft. 양자. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="c7be2-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)