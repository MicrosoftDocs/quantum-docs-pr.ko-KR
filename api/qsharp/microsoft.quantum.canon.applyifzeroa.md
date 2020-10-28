---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: ApplyIfZeroA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: d324cd970e8df49ceb51b6bf5c9f3c9c3ff142f9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718054"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="55724-102">ApplyIfZeroA 작업</span><span class="sxs-lookup"><span data-stu-id="55724-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="55724-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="55724-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="55724-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="55724-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="55724-105">클래식 결과 값에 0이 adjointable 작업 조건 화 된을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="55724-105">Applies an adjointable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="55724-106">Description</span><span class="sxs-lookup"><span data-stu-id="55724-106">Description</span></span>

<span data-ttu-id="55724-107">작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="55724-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="55724-108">이면이 `One` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="55724-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="55724-109">접미사는 `A` 적용 될 작업이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55724-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="55724-110">입력</span><span class="sxs-lookup"><span data-stu-id="55724-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="55724-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="55724-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="55724-112">Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="55724-113">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="55724-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="55724-114">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="55724-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="55724-115">target : 'T</span></span>

<span data-ttu-id="55724-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="55724-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="55724-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="55724-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="55724-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="55724-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="55724-119">'T</span></span>

<span data-ttu-id="55724-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="55724-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="55724-121">See Also</span></span>

- [<span data-ttu-id="55724-122">ApplyIfZeroC입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="55724-123">ApplyIfZeroA입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="55724-124">ApplyIfZeroCA입니다.</span><span class="sxs-lookup"><span data-stu-id="55724-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)