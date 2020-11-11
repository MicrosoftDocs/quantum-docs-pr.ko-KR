---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: ApplyToTailC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 631e08666002d8077c6f8b78525b06b104dd4c7c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716969"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="0854e-102">ApplyToTailC 작업</span><span class="sxs-lookup"><span data-stu-id="0854e-102">ApplyToTailC operation</span></span>

<span data-ttu-id="0854e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0854e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0854e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0854e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0854e-105">배열의 마지막 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0854e-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="0854e-106">Description</span><span class="sxs-lookup"><span data-stu-id="0854e-106">Description</span></span>

<span data-ttu-id="0854e-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="0854e-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="0854e-108">입력</span><span class="sxs-lookup"><span data-stu-id="0854e-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="0854e-109">op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="0854e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="0854e-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0854e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="0854e-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="0854e-111">targets : 'T[]</span></span>

<span data-ttu-id="0854e-112">마지막이 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="0854e-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0854e-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0854e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0854e-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0854e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0854e-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="0854e-115">'T</span></span>

<span data-ttu-id="0854e-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0854e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0854e-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0854e-117">See Also</span></span>

- [<span data-ttu-id="0854e-118">Microsoft. 양자. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="0854e-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="0854e-119">ApplyToTailA입니다.</span><span class="sxs-lookup"><span data-stu-id="0854e-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="0854e-120">ApplyToTailCA입니다.</span><span class="sxs-lookup"><span data-stu-id="0854e-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)