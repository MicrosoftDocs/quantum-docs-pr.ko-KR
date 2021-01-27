---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: ApplyToElement 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5159eee07f7398cc6194c9907a37b78a63aaf263
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850787"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="c7bb4-102">ApplyToElement 작업</span><span class="sxs-lookup"><span data-stu-id="c7bb4-102">ApplyToElement operation</span></span>

<span data-ttu-id="c7bb4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7bb4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7bb4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7bb4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7bb4-105">배열의 지정 된 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bb4-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="c7bb4-106">설명</span><span class="sxs-lookup"><span data-stu-id="c7bb4-106">Description</span></span>

<span data-ttu-id="c7bb4-107">작업 `op` , 인덱스 `index` 및 대상의 배열이 지정 된 `targets` 경우 적용 됩니다 `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="c7bb4-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="c7bb4-108">입력</span><span class="sxs-lookup"><span data-stu-id="c7bb4-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="c7bb4-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7bb4-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c7bb4-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bb4-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="c7bb4-111">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7bb4-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7bb4-112">대상 배열의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bb4-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="c7bb4-113">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="c7bb4-113">targets : 'T[]</span></span>

<span data-ttu-id="c7bb4-114">에 대해 가능한 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="c7bb4-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c7bb4-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7bb4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c7bb4-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7bb4-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c7bb4-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="c7bb4-117">'T</span></span>

<span data-ttu-id="c7bb4-118">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bb4-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7bb4-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c7bb4-119">See Also</span></span>

- [<span data-ttu-id="c7bb4-120">Microsoft. 양자. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="c7bb4-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="c7bb4-121">Microsoft. 양자. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="c7bb4-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="c7bb4-122">Microsoft. 양자. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="c7bb4-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)