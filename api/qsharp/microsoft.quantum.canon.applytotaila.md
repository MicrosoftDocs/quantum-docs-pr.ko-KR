---
uid: Microsoft.Quantum.Canon.ApplyToTailA
title: ApplyToTailA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: a84fa6c53f3e11bef82b8b83fffa1451a8299511
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716976"
---
# <a name="applytotaila-operation"></a><span data-ttu-id="d7ec2-102">ApplyToTailA 작업</span><span class="sxs-lookup"><span data-stu-id="d7ec2-102">ApplyToTailA operation</span></span>

<span data-ttu-id="d7ec2-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d7ec2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d7ec2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d7ec2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d7ec2-105">배열의 마지막 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailA<'T> (op : ('T => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="d7ec2-106">Description</span><span class="sxs-lookup"><span data-stu-id="d7ec2-106">Description</span></span>

<span data-ttu-id="d7ec2-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d7ec2-108">입력</span><span class="sxs-lookup"><span data-stu-id="d7ec2-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="d7ec2-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="d7ec2-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="d7ec2-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d7ec2-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="d7ec2-111">targets : 'T[]</span></span>

<span data-ttu-id="d7ec2-112">마지막이 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="d7ec2-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d7ec2-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d7ec2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d7ec2-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d7ec2-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d7ec2-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="d7ec2-115">'T</span></span>

<span data-ttu-id="d7ec2-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7ec2-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d7ec2-117">See Also</span></span>

- [<span data-ttu-id="d7ec2-118">Microsoft. 양자. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="d7ec2-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="d7ec2-119">ApplyToTailC입니다.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="d7ec2-120">ApplyToTailCA입니다.</span><span class="sxs-lookup"><span data-stu-id="d7ec2-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)