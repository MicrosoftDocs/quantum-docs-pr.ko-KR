---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: ApplyToElementCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 599a8afe1ab97b0ab0d6621cabd7707faaeddda3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717445"
---
# <a name="applytoelementca-operation"></a><span data-ttu-id="75fe6-102">ApplyToElementCA 작업</span><span class="sxs-lookup"><span data-stu-id="75fe6-102">ApplyToElementCA operation</span></span>

<span data-ttu-id="75fe6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="75fe6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="75fe6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="75fe6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="75fe6-105">배열의 지정 된 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fe6-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="75fe6-106">Description</span><span class="sxs-lookup"><span data-stu-id="75fe6-106">Description</span></span>

<span data-ttu-id="75fe6-107">작업 `op` , 인덱스 `index` 및 대상의 배열이 지정 된 `targets` 경우 적용 됩니다 `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="75fe6-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="75fe6-108">입력</span><span class="sxs-lookup"><span data-stu-id="75fe6-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="75fe6-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="75fe6-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="75fe6-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="75fe6-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="75fe6-111">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="75fe6-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="75fe6-112">대상 배열의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="75fe6-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="75fe6-113">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="75fe6-113">targets : 'T[]</span></span>

<span data-ttu-id="75fe6-114">에 대해 가능한 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="75fe6-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="75fe6-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="75fe6-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="75fe6-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="75fe6-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="75fe6-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="75fe6-117">'T</span></span>

<span data-ttu-id="75fe6-118">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="75fe6-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="75fe6-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="75fe6-119">See Also</span></span>

- [<span data-ttu-id="75fe6-120">Microsoft. 양자. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="75fe6-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="75fe6-121">Microsoft. 양자. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="75fe6-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="75fe6-122">Microsoft. 양자. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="75fe6-122">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)