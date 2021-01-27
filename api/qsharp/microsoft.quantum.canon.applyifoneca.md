---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: ApplyIfOneCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 8b27a192c66a127fe5a8acfbba7b78314988bf2e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844921"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="daa25-102">ApplyIfOneCA 작업</span><span class="sxs-lookup"><span data-stu-id="daa25-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="daa25-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="daa25-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="daa25-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="daa25-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="daa25-105">기존 결과 값에 조건 화 된 단일 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="daa25-106">설명</span><span class="sxs-lookup"><span data-stu-id="daa25-106">Description</span></span>

<span data-ttu-id="daa25-107">작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="daa25-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="daa25-108">이면이 `Zero` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="daa25-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="daa25-109">접미사는 `CA` 적용 될 작업이 단일 (제어 가능 및 adjointable) 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="daa25-110">입력</span><span class="sxs-lookup"><span data-stu-id="daa25-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="daa25-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="daa25-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="daa25-112">Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="daa25-113">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="daa25-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="daa25-114">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="daa25-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="daa25-115">target : 'T</span></span>

<span data-ttu-id="daa25-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="daa25-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="daa25-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="daa25-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="daa25-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="daa25-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="daa25-119">'T</span></span>

<span data-ttu-id="daa25-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="daa25-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="daa25-121">See Also</span></span>

- [<span data-ttu-id="daa25-122">Microsoft. 양자. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="daa25-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="daa25-123">Microsoft. 양자. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="daa25-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="daa25-124">ApplyIfOneCA입니다.</span><span class="sxs-lookup"><span data-stu-id="daa25-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)