---
uid: Microsoft.Quantum.Canon.ApplyIfElseBCA
title: ApplyIfElseBCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical bit.
ms.openlocfilehash: 0ebd086f4c8166a8d6b593200b0a3354c1420c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718194"
---
# <a name="applyifelsebca-operation"></a><span data-ttu-id="e5a96-102">ApplyIfElseBCA 작업</span><span class="sxs-lookup"><span data-stu-id="e5a96-102">ApplyIfElseBCA operation</span></span>

<span data-ttu-id="e5a96-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e5a96-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e5a96-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5a96-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5a96-105">는 클래식 비트의 값에 따라 두 개의 단일 작업 중 하나를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-105">Applies one of two unitary operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBCA<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Adj + Ctl), trueInput : 'T), (falseOp : ('U => Unit is Adj + Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="e5a96-106">Description</span><span class="sxs-lookup"><span data-stu-id="e5a96-106">Description</span></span>

<span data-ttu-id="e5a96-107">비트가 지정 된 경우 `bit` 가 인 경우 `trueOp` 해당 입력으로 작업을 적용 `trueInput` `bit` `true` 하 고가 인 경우 적용 됩니다 `falseOp(falseInput)` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="e5a96-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="e5a96-108">입력</span><span class="sxs-lookup"><span data-stu-id="e5a96-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="e5a96-109">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e5a96-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e5a96-110">또는를 적용할지 여부를 결정 하는 데 사용 되는 부울 값 `trueOp` `falseOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit-adj--ctl"></a><span data-ttu-id="e5a96-111">trueOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="e5a96-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e5a96-112">가 인 경우 적용 될 단일 작업 `bit` 입니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="e5a96-112">The unitary operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="e5a96-113">trueInput: ' '</span><span class="sxs-lookup"><span data-stu-id="e5a96-113">trueInput : 'T</span></span>

<span data-ttu-id="e5a96-114">가 인 경우에 제공 되는 입력입니다 `trueOp` `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="e5a96-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit-adj--ctl"></a><span data-ttu-id="e5a96-115">falseOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="e5a96-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e5a96-116">가 인 경우 적용 될 단일 작업 `bit` 입니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="e5a96-116">The unitary operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="e5a96-117">falseInput: ' U</span><span class="sxs-lookup"><span data-stu-id="e5a96-117">falseInput : 'U</span></span>

<span data-ttu-id="e5a96-118">가 인 경우에 제공 되는 입력입니다 `falseOp` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="e5a96-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e5a96-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5a96-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e5a96-120">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5a96-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5a96-121">없습니다</span><span class="sxs-lookup"><span data-stu-id="e5a96-121">'T</span></span>

<span data-ttu-id="e5a96-122">조건부로 적용할 작업의 입력 형식 `trueOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="e5a96-123">' U</span><span class="sxs-lookup"><span data-stu-id="e5a96-123">'U</span></span>

<span data-ttu-id="e5a96-124">조건부로 적용할 작업의 입력 형식 `falseOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a96-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5a96-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e5a96-125">See Also</span></span>

- [<span data-ttu-id="e5a96-126">Microsoft. 양자. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="e5a96-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="e5a96-127">Microsoft. 양자. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="e5a96-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="e5a96-128">Microsoft. 양자. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="e5a96-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="e5a96-129">Microsoft. 양자. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="e5a96-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="e5a96-130">Microsoft. 양자. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="e5a96-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)