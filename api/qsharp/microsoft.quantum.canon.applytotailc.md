---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: ApplyToTailC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 8408dff24c5c57efbedb649ac182fac49e836a3e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850426"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="03e96-102">ApplyToTailC 작업</span><span class="sxs-lookup"><span data-stu-id="03e96-102">ApplyToTailC operation</span></span>

<span data-ttu-id="03e96-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="03e96-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="03e96-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="03e96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="03e96-105">배열의 마지막 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e96-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="03e96-106">설명</span><span class="sxs-lookup"><span data-stu-id="03e96-106">Description</span></span>

<span data-ttu-id="03e96-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="03e96-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="03e96-108">입력</span><span class="sxs-lookup"><span data-stu-id="03e96-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="03e96-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="03e96-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="03e96-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="03e96-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="03e96-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="03e96-111">targets : 'T[]</span></span>

<span data-ttu-id="03e96-112">마지막이 적용 될 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="03e96-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03e96-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03e96-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="03e96-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="03e96-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="03e96-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="03e96-115">'T</span></span>

<span data-ttu-id="03e96-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="03e96-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="03e96-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="03e96-117">See Also</span></span>

- [<span data-ttu-id="03e96-118">Microsoft. 양자. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="03e96-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="03e96-119">ApplyToTailA입니다.</span><span class="sxs-lookup"><span data-stu-id="03e96-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="03e96-120">ApplyToTailCA입니다.</span><span class="sxs-lookup"><span data-stu-id="03e96-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)