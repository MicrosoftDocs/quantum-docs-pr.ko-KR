---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: ApplyToElementC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bc63b6b591781a6283b872ef0c2509094a656b4c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850754"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="97f64-102">ApplyToElementC 작업</span><span class="sxs-lookup"><span data-stu-id="97f64-102">ApplyToElementC operation</span></span>

<span data-ttu-id="97f64-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97f64-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97f64-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="97f64-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="97f64-105">배열의 지정 된 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97f64-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="97f64-106">설명</span><span class="sxs-lookup"><span data-stu-id="97f64-106">Description</span></span>

<span data-ttu-id="97f64-107">작업 `op` , 인덱스 `index` 및 대상의 배열이 지정 된 `targets` 경우 적용 됩니다 `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="97f64-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="97f64-108">입력</span><span class="sxs-lookup"><span data-stu-id="97f64-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="97f64-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="97f64-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="97f64-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="97f64-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="97f64-111">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="97f64-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="97f64-112">대상 배열의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="97f64-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="97f64-113">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="97f64-113">targets : 'T[]</span></span>

<span data-ttu-id="97f64-114">에 대해 가능한 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="97f64-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97f64-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97f64-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="97f64-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="97f64-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="97f64-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="97f64-117">'T</span></span>

<span data-ttu-id="97f64-118">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="97f64-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="97f64-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="97f64-119">See Also</span></span>

- [<span data-ttu-id="97f64-120">Microsoft. 양자. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="97f64-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="97f64-121">Microsoft. 양자. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="97f64-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="97f64-122">Microsoft. 양자. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="97f64-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)