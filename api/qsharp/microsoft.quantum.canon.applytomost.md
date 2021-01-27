---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: ApplyToMost의 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a3918233e101f3d8956601dcc7d85edcf6196ac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850602"
---
# <a name="applytomost-operation"></a><span data-ttu-id="21e80-102">ApplyToMost의 작업</span><span class="sxs-lookup"><span data-stu-id="21e80-102">ApplyToMost operation</span></span>

<span data-ttu-id="21e80-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="21e80-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="21e80-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="21e80-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="21e80-105">배열의 마지막 요소를 제외한 모든 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21e80-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="21e80-106">설명</span><span class="sxs-lookup"><span data-stu-id="21e80-106">Description</span></span>

<span data-ttu-id="21e80-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="21e80-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="21e80-108">입력</span><span class="sxs-lookup"><span data-stu-id="21e80-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="21e80-109">op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21e80-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="21e80-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="21e80-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="21e80-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="21e80-111">targets : 'T[]</span></span>

<span data-ttu-id="21e80-112">마지막가 적용 되는 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="21e80-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="21e80-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21e80-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="21e80-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="21e80-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="21e80-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="21e80-115">'T</span></span>

<span data-ttu-id="21e80-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="21e80-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="21e80-117">예</span><span class="sxs-lookup"><span data-stu-id="21e80-117">Example</span></span>

<span data-ttu-id="21e80-118">다음 Q # 코드 조각은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="21e80-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToMost(ApplyCNOTChain, register);
ApplyCNOTChain(Most(register));
```

## <a name="see-also"></a><span data-ttu-id="21e80-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="21e80-119">See Also</span></span>

- [<span data-ttu-id="21e80-120">Microsoft. 양자. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="21e80-120">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="21e80-121">Microsoft. 양자. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="21e80-121">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="21e80-122">Microsoft. 양자. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="21e80-122">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)