---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: ApplyToHead 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 35f19cbb1090e974e18f338239764c9c8b854116
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217342"
---
# <a name="applytohead-operation"></a><span data-ttu-id="5d48d-102">ApplyToHead 작업</span><span class="sxs-lookup"><span data-stu-id="5d48d-102">ApplyToHead operation</span></span>

<span data-ttu-id="5d48d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5d48d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5d48d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d48d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5d48d-105">배열의 첫 번째 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d48d-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5d48d-106">Description</span><span class="sxs-lookup"><span data-stu-id="5d48d-106">Description</span></span>

<span data-ttu-id="5d48d-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="5d48d-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="5d48d-108">입력</span><span class="sxs-lookup"><span data-stu-id="5d48d-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="5d48d-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d48d-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5d48d-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5d48d-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="5d48d-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="5d48d-111">targets : 'T[]</span></span>

<span data-ttu-id="5d48d-112">첫 번째가 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="5d48d-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5d48d-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d48d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5d48d-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d48d-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5d48d-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="5d48d-115">'T</span></span>

<span data-ttu-id="5d48d-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5d48d-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d48d-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5d48d-117">See Also</span></span>

- [<span data-ttu-id="5d48d-118">Microsoft. 양자..</span><span class="sxs-lookup"><span data-stu-id="5d48d-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="5d48d-119">Microsoft. 양자. Applyto헤드 c</span><span class="sxs-lookup"><span data-stu-id="5d48d-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="5d48d-120">Microsoft 양자. Applyto헤드 Ca</span><span class="sxs-lookup"><span data-stu-id="5d48d-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)