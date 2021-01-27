---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: ApplyToElementA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 57d870c7fbd099212b13f75bd85e57c046280d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850761"
---
# <a name="applytoelementa-operation"></a><span data-ttu-id="b1ede-102">ApplyToElementA 작업</span><span class="sxs-lookup"><span data-stu-id="b1ede-102">ApplyToElementA operation</span></span>

<span data-ttu-id="b1ede-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b1ede-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b1ede-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b1ede-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b1ede-105">배열의 지정 된 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ede-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="b1ede-106">설명</span><span class="sxs-lookup"><span data-stu-id="b1ede-106">Description</span></span>

<span data-ttu-id="b1ede-107">작업 `op` , 인덱스 `index` 및 대상의 배열이 지정 된 `targets` 경우 적용 됩니다 `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="b1ede-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="b1ede-108">입력</span><span class="sxs-lookup"><span data-stu-id="b1ede-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="b1ede-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="b1ede-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b1ede-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b1ede-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="b1ede-111">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b1ede-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b1ede-112">대상 배열의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="b1ede-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="b1ede-113">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="b1ede-113">targets : 'T[]</span></span>

<span data-ttu-id="b1ede-114">에 대해 가능한 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="b1ede-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b1ede-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1ede-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b1ede-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b1ede-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b1ede-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="b1ede-117">'T</span></span>

<span data-ttu-id="b1ede-118">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b1ede-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1ede-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b1ede-119">See Also</span></span>

- [<span data-ttu-id="b1ede-120">Microsoft. 양자. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="b1ede-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="b1ede-121">Microsoft. 양자. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="b1ede-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="b1ede-122">Microsoft. 양자. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="b1ede-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)