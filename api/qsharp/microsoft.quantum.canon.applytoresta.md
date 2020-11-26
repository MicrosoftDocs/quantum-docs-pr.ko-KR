---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: ApplyToRestA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 34cb5071dd939d0831e39bb8f1670670ae1fad31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208308"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="1fab3-102">ApplyToRestA 작업</span><span class="sxs-lookup"><span data-stu-id="1fab3-102">ApplyToRestA operation</span></span>

<span data-ttu-id="1fab3-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1fab3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1fab3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fab3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fab3-105">배열의 첫 번째 요소를 제외한 모든 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fab3-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="1fab3-106">설명</span><span class="sxs-lookup"><span data-stu-id="1fab3-106">Description</span></span>

<span data-ttu-id="1fab3-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="1fab3-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="1fab3-108">입력</span><span class="sxs-lookup"><span data-stu-id="1fab3-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="1fab3-109">op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj</span><span class="sxs-lookup"><span data-stu-id="1fab3-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="1fab3-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1fab3-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="1fab3-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="1fab3-111">targets : 'T[]</span></span>

<span data-ttu-id="1fab3-112">첫 번째가 적용 되는 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="1fab3-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1fab3-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1fab3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1fab3-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fab3-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1fab3-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="1fab3-115">'T</span></span>

<span data-ttu-id="1fab3-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1fab3-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fab3-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1fab3-117">See Also</span></span>

- [<span data-ttu-id="1fab3-118">Microsoft. 양자. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="1fab3-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="1fab3-119">Microsoft. 양자. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="1fab3-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="1fab3-120">Microsoft 양자. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="1fab3-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)