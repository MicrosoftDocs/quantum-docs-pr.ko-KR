---
uid: Microsoft.Quantum.Canon.Delay
title: 지연 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: f9f0e5c3120eb69bd7431d52d6cde5e846ffbe4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716318"
---
# <a name="delay-operation"></a><span data-ttu-id="4ded5-102">지연 작업</span><span class="sxs-lookup"><span data-stu-id="4ded5-102">Delay operation</span></span>

<span data-ttu-id="4ded5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4ded5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4ded5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4ded5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4ded5-105">지정 된 작업을 지연 시간에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="4ded5-106">Description</span><span class="sxs-lookup"><span data-stu-id="4ded5-106">Description</span></span>

<span data-ttu-id="4ded5-107">작업 및 해당 작업에 대 한 입력이 주어진 경우 추가 입력이 제공 되 면에서 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="4ded5-108">특히 식은 `Delay(op, arg, _)` `op` 호출 될 때에 적용 되는 연산입니다 `arg` .</span><span class="sxs-lookup"><span data-stu-id="4ded5-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="4ded5-109">식을 `Delay(op,arg,_)` 사용 하면의 응용 프로그램을 연기할 수 있습니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="4ded5-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="4ded5-110">입력</span><span class="sxs-lookup"><span data-stu-id="4ded5-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="4ded5-111">op: ' t => ' U</span><span class="sxs-lookup"><span data-stu-id="4ded5-111">op : 'T => 'U</span></span> 

<span data-ttu-id="4ded5-112">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="4ded5-113">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="4ded5-113">arg : 'T</span></span>

<span data-ttu-id="4ded5-114">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="4ded5-115">aux: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4ded5-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="4ded5-116">부분 응용 프로그램을 사용 하 여 작업의 응용 프로그램을 지연 하는 데 사용 되는 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="4ded5-117">출력: ' U</span><span class="sxs-lookup"><span data-stu-id="4ded5-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4ded5-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ded5-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4ded5-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="4ded5-119">'T</span></span>

<span data-ttu-id="4ded5-120">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="4ded5-121">' U</span><span class="sxs-lookup"><span data-stu-id="4ded5-121">'U</span></span>

<span data-ttu-id="4ded5-122">연기할 작업의 반환 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ded5-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4ded5-123">See Also</span></span>

- [<span data-ttu-id="4ded5-124">Microsoft 양자. DelayC</span><span class="sxs-lookup"><span data-stu-id="4ded5-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="4ded5-125">DelayA입니다.</span><span class="sxs-lookup"><span data-stu-id="4ded5-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="4ded5-126">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="4ded5-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="4ded5-127">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="4ded5-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)