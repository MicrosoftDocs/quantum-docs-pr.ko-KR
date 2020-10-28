---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: ApplyToRest 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 29bf080d693c668421181f10faef50f5681683be
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717109"
---
# <a name="applytorest-operation"></a><span data-ttu-id="0451c-102">ApplyToRest 작업</span><span class="sxs-lookup"><span data-stu-id="0451c-102">ApplyToRest operation</span></span>

<span data-ttu-id="0451c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0451c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0451c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0451c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0451c-105">배열의 첫 번째 요소를 제외한 모든 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0451c-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="0451c-106">Description</span><span class="sxs-lookup"><span data-stu-id="0451c-106">Description</span></span>

<span data-ttu-id="0451c-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="0451c-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="0451c-108">입력</span><span class="sxs-lookup"><span data-stu-id="0451c-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="0451c-109">op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0451c-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0451c-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0451c-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="0451c-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="0451c-111">targets : 'T[]</span></span>

<span data-ttu-id="0451c-112">첫 번째가 적용 되는 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="0451c-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0451c-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0451c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0451c-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0451c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0451c-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="0451c-115">'T</span></span>

<span data-ttu-id="0451c-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0451c-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0451c-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0451c-117">See Also</span></span>

- [<span data-ttu-id="0451c-118">Microsoft. 양자. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="0451c-118">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="0451c-119">Microsoft. 양자. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="0451c-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="0451c-120">Microsoft 양자. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="0451c-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)