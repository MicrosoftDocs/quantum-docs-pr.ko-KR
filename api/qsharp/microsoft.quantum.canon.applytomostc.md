---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: ApplyToMostC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a5927f6b296dd50afec8979c8e8ac22979b8a082
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717172"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="df251-102">ApplyToMostC 작업</span><span class="sxs-lookup"><span data-stu-id="df251-102">ApplyToMostC operation</span></span>

<span data-ttu-id="df251-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="df251-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="df251-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df251-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df251-105">배열의 마지막 요소를 제외한 모든 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df251-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="df251-106">Description</span><span class="sxs-lookup"><span data-stu-id="df251-106">Description</span></span>

<span data-ttu-id="df251-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="df251-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="df251-108">입력</span><span class="sxs-lookup"><span data-stu-id="df251-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="df251-109">op: ' t [] => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="df251-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="df251-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="df251-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="df251-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="df251-111">targets : 'T[]</span></span>

<span data-ttu-id="df251-112">마지막가 적용 되는 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="df251-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df251-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df251-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="df251-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="df251-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df251-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="df251-115">'T</span></span>

<span data-ttu-id="df251-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="df251-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="df251-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="df251-117">See Also</span></span>

- [<span data-ttu-id="df251-118">Microsoft. 양자. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="df251-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="df251-119">Microsoft. 양자. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="df251-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="df251-120">Microsoft. 양자. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="df251-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)