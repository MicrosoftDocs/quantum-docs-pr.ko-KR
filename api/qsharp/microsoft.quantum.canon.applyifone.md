---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: ApplyIfOne 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: b86aecf3dc3d02d1a6bf0c112bdc45a55a2cf087
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841776"
---
# <a name="applyifone-operation"></a><span data-ttu-id="1540e-102">ApplyIfOne 작업</span><span class="sxs-lookup"><span data-stu-id="1540e-102">ApplyIfOne operation</span></span>

<span data-ttu-id="1540e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1540e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1540e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1540e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1540e-105">기존 결과 값에 조건 화 된 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1540e-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="1540e-106">설명</span><span class="sxs-lookup"><span data-stu-id="1540e-106">Description</span></span>

<span data-ttu-id="1540e-107">작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="1540e-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="1540e-108">이면이 `Zero` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="1540e-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="1540e-109">입력</span><span class="sxs-lookup"><span data-stu-id="1540e-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="1540e-110">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="1540e-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="1540e-111">Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="1540e-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="1540e-112">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1540e-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1540e-113">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1540e-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="1540e-114">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="1540e-114">target : 'T</span></span>

<span data-ttu-id="1540e-115">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="1540e-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1540e-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1540e-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1540e-117">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1540e-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1540e-118">없습니다</span><span class="sxs-lookup"><span data-stu-id="1540e-118">'T</span></span>

<span data-ttu-id="1540e-119">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1540e-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="1540e-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1540e-120">See Also</span></span>

- [<span data-ttu-id="1540e-121">Microsoft. 양자. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="1540e-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="1540e-122">Microsoft. 양자. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="1540e-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="1540e-123">ApplyIfOneCA입니다.</span><span class="sxs-lookup"><span data-stu-id="1540e-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)