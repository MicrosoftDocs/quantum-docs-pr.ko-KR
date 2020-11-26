---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Applyto헤드 Ca 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: f28cff599e06090145fac860dbaf8274c966f80a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208553"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="59478-102">Applyto헤드 Ca 작업</span><span class="sxs-lookup"><span data-stu-id="59478-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="59478-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="59478-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="59478-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59478-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59478-105">배열의 첫 번째 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59478-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="59478-106">Description</span><span class="sxs-lookup"><span data-stu-id="59478-106">Description</span></span>

<span data-ttu-id="59478-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="59478-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="59478-108">입력</span><span class="sxs-lookup"><span data-stu-id="59478-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="59478-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="59478-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="59478-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="59478-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="59478-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="59478-111">targets : 'T[]</span></span>

<span data-ttu-id="59478-112">첫 번째가 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="59478-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="59478-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59478-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="59478-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="59478-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="59478-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="59478-115">'T</span></span>

<span data-ttu-id="59478-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="59478-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="59478-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="59478-117">See Also</span></span>

- [<span data-ttu-id="59478-118">Microsoft. 양자. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="59478-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="59478-119">Microsoft. 양자..</span><span class="sxs-lookup"><span data-stu-id="59478-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="59478-120">Microsoft. 양자. Applyto헤드 c</span><span class="sxs-lookup"><span data-stu-id="59478-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)