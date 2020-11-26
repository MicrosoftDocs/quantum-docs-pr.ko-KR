---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: ApplyIfZeroA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: ab5b05791213da7c8bee5915764c342cb0bed851
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218498"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="92b46-102">ApplyIfZeroA 작업</span><span class="sxs-lookup"><span data-stu-id="92b46-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="92b46-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="92b46-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="92b46-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92b46-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92b46-105">클래식 결과 값에 0이 adjointable 작업 조건 화 된을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-105">Applies an adjointable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="92b46-106">Description</span><span class="sxs-lookup"><span data-stu-id="92b46-106">Description</span></span>

<span data-ttu-id="92b46-107">작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="92b46-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="92b46-108">이면이 `One` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="92b46-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="92b46-109">접미사는 `A` 적용 될 작업이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="92b46-110">입력</span><span class="sxs-lookup"><span data-stu-id="92b46-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="92b46-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="92b46-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="92b46-112">Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="92b46-113">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="92b46-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="92b46-114">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="92b46-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="92b46-115">target : 'T</span></span>

<span data-ttu-id="92b46-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="92b46-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="92b46-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="92b46-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="92b46-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="92b46-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="92b46-119">'T</span></span>

<span data-ttu-id="92b46-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="92b46-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="92b46-121">See Also</span></span>

- [<span data-ttu-id="92b46-122">ApplyIfZeroC입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="92b46-123">ApplyIfZeroA입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="92b46-124">ApplyIfZeroCA입니다.</span><span class="sxs-lookup"><span data-stu-id="92b46-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)