---
uid: Microsoft.Quantum.Canon.DelayA
title: DelayA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 7c3325fd98a85c7e9123f383cbdc0a68627222c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207142"
---
# <a name="delaya-operation"></a><span data-ttu-id="8ba99-102">DelayA 작업</span><span class="sxs-lookup"><span data-stu-id="8ba99-102">DelayA operation</span></span>

<span data-ttu-id="8ba99-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8ba99-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8ba99-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8ba99-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8ba99-105">지정 된 작업을 지연 시간에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba99-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="8ba99-106">Description</span><span class="sxs-lookup"><span data-stu-id="8ba99-106">Description</span></span>

<span data-ttu-id="8ba99-107">작업 및 해당 작업에 대 한 입력이 주어진 경우 추가 입력이 제공 되 면에서 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba99-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="8ba99-108">특히 식은 `Delay(op, arg, _)` `op` 호출 될 때에 적용 되는 연산입니다 `arg` .</span><span class="sxs-lookup"><span data-stu-id="8ba99-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="8ba99-109">식을 `Delay(op,arg,_)` 사용 하면의 응용 프로그램을 연기할 수 있습니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="8ba99-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="8ba99-110">입력</span><span class="sxs-lookup"><span data-stu-id="8ba99-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="8ba99-111">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="8ba99-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="8ba99-112">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba99-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="8ba99-113">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="8ba99-113">arg : 'T</span></span>

<span data-ttu-id="8ba99-114">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba99-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="8ba99-115">aux: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8ba99-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="8ba99-116">부분 응용 프로그램을 사용 하 여 작업의 응용 프로그램을 지연 하는 데 사용 되는 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba99-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8ba99-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8ba99-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8ba99-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ba99-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8ba99-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="8ba99-119">'T</span></span>

<span data-ttu-id="8ba99-120">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba99-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ba99-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8ba99-121">See Also</span></span>

- [<span data-ttu-id="8ba99-122">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="8ba99-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="8ba99-123">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="8ba99-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)