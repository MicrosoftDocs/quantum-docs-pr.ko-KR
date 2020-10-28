---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: ApplyIfElseBC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 032d92484dc96481cb981d9d8acfeed248a9116d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718213"
---
# <a name="applyifelsebc-operation"></a><span data-ttu-id="24b4d-102">ApplyIfElseBC 작업</span><span class="sxs-lookup"><span data-stu-id="24b4d-102">ApplyIfElseBC operation</span></span>

<span data-ttu-id="24b4d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="24b4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="24b4d-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24b4d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24b4d-105">클래식 비트의 값에 따라 제어 가능한 두 작업 중 하나를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b4d-105">Applies one of two controllable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="24b4d-106">Description</span><span class="sxs-lookup"><span data-stu-id="24b4d-106">Description</span></span>

<span data-ttu-id="24b4d-107">비트가 지정 된 경우 `bit` 가 인 경우 `trueOp` 해당 입력으로 작업을 적용 `trueInput` `bit` `true` 하 고가 인 경우 적용 됩니다 `falseOp(falseInput)` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="24b4d-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="24b4d-108">입력</span><span class="sxs-lookup"><span data-stu-id="24b4d-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="24b4d-109">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="24b4d-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="24b4d-110">또는를 적용할지 여부를 결정 하는 데 사용 되는 부울 값 `trueOp` `falseOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="24b4d-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit-ctl"></a><span data-ttu-id="24b4d-111">trueOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="24b4d-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="24b4d-112">가 일 때 적용 되는 제어 가능한 작업입니다 `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="24b4d-112">The controllable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="24b4d-113">trueInput: ' '</span><span class="sxs-lookup"><span data-stu-id="24b4d-113">trueInput : 'T</span></span>

<span data-ttu-id="24b4d-114">가 인 경우에 제공 되는 입력입니다 `trueOp` `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="24b4d-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit-ctl"></a><span data-ttu-id="24b4d-115">falseOp: ' U => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="24b4d-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="24b4d-116">가 일 때 적용 되는 제어 가능한 작업입니다 `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="24b4d-116">The controllable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="24b4d-117">falseInput: ' U</span><span class="sxs-lookup"><span data-stu-id="24b4d-117">falseInput : 'U</span></span>

<span data-ttu-id="24b4d-118">가 인 경우에 제공 되는 입력입니다 `falseOp` `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="24b4d-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="24b4d-119">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="24b4d-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="24b4d-120">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="24b4d-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="24b4d-121">없습니다</span><span class="sxs-lookup"><span data-stu-id="24b4d-121">'T</span></span>

<span data-ttu-id="24b4d-122">조건부로 적용할 작업의 입력 형식 `trueOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="24b4d-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="24b4d-123">' U</span><span class="sxs-lookup"><span data-stu-id="24b4d-123">'U</span></span>

<span data-ttu-id="24b4d-124">조건부로 적용할 작업의 입력 형식 `falseOp` 입니다.</span><span class="sxs-lookup"><span data-stu-id="24b4d-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="24b4d-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="24b4d-125">See Also</span></span>

- [<span data-ttu-id="24b4d-126">Microsoft. 양자. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="24b4d-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="24b4d-127">Microsoft. 양자. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="24b4d-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="24b4d-128">Microsoft. 양자. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="24b4d-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="24b4d-129">Microsoft. 양자. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="24b4d-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="24b4d-130">Microsoft. 양자. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="24b4d-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)