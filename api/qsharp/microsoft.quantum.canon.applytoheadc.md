---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Applyto헤드 c 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3ff6c25837f1219dd456bf1739a2953ff72e2df9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717249"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="5a871-102">Applyto헤드 c 작업</span><span class="sxs-lookup"><span data-stu-id="5a871-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="5a871-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5a871-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5a871-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a871-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5a871-105">배열의 첫 번째 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a871-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5a871-106">Description</span><span class="sxs-lookup"><span data-stu-id="5a871-106">Description</span></span>

<span data-ttu-id="5a871-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="5a871-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="5a871-108">입력</span><span class="sxs-lookup"><span data-stu-id="5a871-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="5a871-109">op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="5a871-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5a871-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5a871-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="5a871-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="5a871-111">targets : 'T[]</span></span>

<span data-ttu-id="5a871-112">첫 번째가 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="5a871-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5a871-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a871-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5a871-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a871-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5a871-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="5a871-115">'T</span></span>

<span data-ttu-id="5a871-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5a871-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a871-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5a871-117">See Also</span></span>

- [<span data-ttu-id="5a871-118">Microsoft. 양자. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="5a871-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="5a871-119">Microsoft. 양자..</span><span class="sxs-lookup"><span data-stu-id="5a871-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="5a871-120">Microsoft 양자. Applyto헤드 Ca</span><span class="sxs-lookup"><span data-stu-id="5a871-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)