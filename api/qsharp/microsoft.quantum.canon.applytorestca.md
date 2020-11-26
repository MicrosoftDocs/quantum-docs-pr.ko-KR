---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: ApplyToRestCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 3123c7f7b5e5c7f5cb17a34eedc81b3912109883
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208162"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="790e4-102">ApplyToRestCA 작업</span><span class="sxs-lookup"><span data-stu-id="790e4-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="790e4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="790e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="790e4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="790e4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="790e4-105">배열의 첫 번째 요소를 제외한 모든 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="790e4-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="790e4-106">설명</span><span class="sxs-lookup"><span data-stu-id="790e4-106">Description</span></span>

<span data-ttu-id="790e4-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="790e4-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="790e4-108">입력</span><span class="sxs-lookup"><span data-stu-id="790e4-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="790e4-109">op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="790e4-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="790e4-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="790e4-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="790e4-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="790e4-111">targets : 'T[]</span></span>

<span data-ttu-id="790e4-112">첫 번째가 적용 되는 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="790e4-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="790e4-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="790e4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="790e4-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="790e4-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="790e4-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="790e4-115">'T</span></span>

<span data-ttu-id="790e4-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="790e4-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="790e4-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="790e4-117">See Also</span></span>

- [<span data-ttu-id="790e4-118">Microsoft. 양자. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="790e4-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="790e4-119">Microsoft. 양자. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="790e4-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="790e4-120">Microsoft. 양자. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="790e4-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)