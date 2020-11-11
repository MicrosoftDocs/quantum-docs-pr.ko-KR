---
uid: Microsoft.Quantum.Canon.ApplyIfZeroCA
title: ApplyIfZeroCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being zero.
ms.openlocfilehash: 85612bd3dd7af45b7901fef775a7d556eb229608
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718005"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="ed003-102">ApplyIfZeroCA 작업</span><span class="sxs-lookup"><span data-stu-id="ed003-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="ed003-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ed003-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ed003-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ed003-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ed003-105">기존 결과 값에 0이 조건 화 된 단일 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-105">Applies a unitary operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="ed003-106">Description</span><span class="sxs-lookup"><span data-stu-id="ed003-106">Description</span></span>

<span data-ttu-id="ed003-107">작업 `op` 및 결과 값이 지정 된 `result` `op` `target` 경우이 인 경우에 적용 됩니다 `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="ed003-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="ed003-108">이면이 `One` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="ed003-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="ed003-109">접미사는 `CA` 적용 될 작업이 단일 (제어 가능 및 adjointable) 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="ed003-110">입력</span><span class="sxs-lookup"><span data-stu-id="ed003-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="ed003-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="ed003-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="ed003-112">Op가 적용 되는지 여부를 제어 하는 측정 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="ed003-113">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="ed003-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ed003-114">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="ed003-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="ed003-115">target : 'T</span></span>

<span data-ttu-id="ed003-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed003-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed003-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ed003-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed003-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed003-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="ed003-119">'T</span></span>

<span data-ttu-id="ed003-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed003-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ed003-121">See Also</span></span>

- [<span data-ttu-id="ed003-122">ApplyIfZeroC입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="ed003-123">ApplyIfZeroA입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="ed003-124">ApplyIfZeroCA입니다.</span><span class="sxs-lookup"><span data-stu-id="ed003-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)