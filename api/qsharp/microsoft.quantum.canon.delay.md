---
uid: Microsoft.Quantum.Canon.Delay
title: 지연 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c8ba128e44a9b217ec196e39ff1df639ef276784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840651"
---
# <a name="delay-operation"></a><span data-ttu-id="b8fe7-102">지연 작업</span><span class="sxs-lookup"><span data-stu-id="b8fe7-102">Delay operation</span></span>

<span data-ttu-id="b8fe7-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b8fe7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b8fe7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b8fe7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b8fe7-105">지정 된 작업을 지연 시간에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="b8fe7-106">설명</span><span class="sxs-lookup"><span data-stu-id="b8fe7-106">Description</span></span>

<span data-ttu-id="b8fe7-107">작업 및 해당 작업에 대 한 입력이 주어진 경우 추가 입력이 제공 되 면에서 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="b8fe7-108">특히 식은 `Delay(op, arg, _)` `op` 호출 될 때에 적용 되는 연산입니다 `arg` .</span><span class="sxs-lookup"><span data-stu-id="b8fe7-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="b8fe7-109">식을 `Delay(op,arg,_)` 사용 하면의 응용 프로그램을 연기할 수 있습니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="b8fe7-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="b8fe7-110">입력</span><span class="sxs-lookup"><span data-stu-id="b8fe7-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="b8fe7-111">op: ' t => ' U</span><span class="sxs-lookup"><span data-stu-id="b8fe7-111">op : 'T => 'U</span></span> 

<span data-ttu-id="b8fe7-112">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="b8fe7-113">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="b8fe7-113">arg : 'T</span></span>

<span data-ttu-id="b8fe7-114">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="b8fe7-115">aux: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b8fe7-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="b8fe7-116">부분 응용 프로그램을 사용 하 여 작업의 응용 프로그램을 지연 하는 데 사용 되는 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="b8fe7-117">출력: ' U</span><span class="sxs-lookup"><span data-stu-id="b8fe7-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b8fe7-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8fe7-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b8fe7-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="b8fe7-119">'T</span></span>

<span data-ttu-id="b8fe7-120">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="b8fe7-121">' U</span><span class="sxs-lookup"><span data-stu-id="b8fe7-121">'U</span></span>

<span data-ttu-id="b8fe7-122">연기할 작업의 반환 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8fe7-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b8fe7-123">See Also</span></span>

- [<span data-ttu-id="b8fe7-124">Microsoft 양자. DelayC</span><span class="sxs-lookup"><span data-stu-id="b8fe7-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="b8fe7-125">DelayA입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="b8fe7-126">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="b8fe7-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="b8fe7-127">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="b8fe7-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)