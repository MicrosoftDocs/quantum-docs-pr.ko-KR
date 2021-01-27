---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: ApplyToTailCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 4c702a9d310adae7a4ec404f3cf12893547623b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841190"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="1997d-102">ApplyToTailCA 작업</span><span class="sxs-lookup"><span data-stu-id="1997d-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="1997d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1997d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1997d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1997d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1997d-105">배열의 마지막 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1997d-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="1997d-106">설명</span><span class="sxs-lookup"><span data-stu-id="1997d-106">Description</span></span>

<span data-ttu-id="1997d-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="1997d-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="1997d-108">입력</span><span class="sxs-lookup"><span data-stu-id="1997d-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="1997d-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="1997d-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1997d-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1997d-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="1997d-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="1997d-111">targets : 'T[]</span></span>

<span data-ttu-id="1997d-112">마지막이 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="1997d-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1997d-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1997d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1997d-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1997d-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1997d-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="1997d-115">'T</span></span>

<span data-ttu-id="1997d-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1997d-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="1997d-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1997d-117">See Also</span></span>

- [<span data-ttu-id="1997d-118">Microsoft. 양자. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="1997d-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="1997d-119">ApplyToTailA입니다.</span><span class="sxs-lookup"><span data-stu-id="1997d-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="1997d-120">ApplyToTailC입니다.</span><span class="sxs-lookup"><span data-stu-id="1997d-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)