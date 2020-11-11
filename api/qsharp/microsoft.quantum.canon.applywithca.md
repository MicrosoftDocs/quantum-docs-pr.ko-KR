---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: ApplyWithCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: abc62791416e78c1b2937a226327b71da8b8e288
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716885"
---
# <a name="applywithca-operation"></a><span data-ttu-id="2a36c-102">ApplyWithCA 작업</span><span class="sxs-lookup"><span data-stu-id="2a36c-102">ApplyWithCA operation</span></span>

<span data-ttu-id="2a36c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a36c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a36c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a36c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a36c-105">두 작업을 수행 하는 경우 conjugated로 다른 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="2a36c-106">Description</span><span class="sxs-lookup"><span data-stu-id="2a36c-106">Description</span></span>

<span data-ttu-id="2a36c-107">$U $ 및 $V $와 같은 단일 연산자에 의해 각각 설명 된 두 개의 작업은 ^ {\dagger} V U $ $U 시퀀스에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="2a36c-108">즉,이 작업은 $U $와 $V $ conjugated에서 제공 하는 단일 연산자를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="2a36c-109">입력</span><span class="sxs-lookup"><span data-stu-id="2a36c-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="2a36c-110">outerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="2a36c-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="2a36c-111">$U $는 켤레 $V $로 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="2a36c-112">외부 작업 $U $은 (는) adjointable 해야 하지만 제어할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-adj--ctl"></a><span data-ttu-id="2a36c-113">innerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="2a36c-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="2a36c-114">작업 $V $가 conjugated입니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="2a36c-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="2a36c-115">target : 'T</span></span>

<span data-ttu-id="2a36c-116">외부 및 내부 작업에 제공 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2a36c-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a36c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2a36c-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2a36c-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a36c-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="2a36c-119">'T</span></span>

<span data-ttu-id="2a36c-120">각 내부 및 외부 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a36c-121">설명</span><span class="sxs-lookup"><span data-stu-id="2a36c-121">Remarks</span></span>

<span data-ttu-id="2a36c-122">외부 작업은 항상 adjointable으로 간주 되지만 결합 된 작업을 제어 하기 위해 제어 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a36c-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a36c-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2a36c-123">See Also</span></span>

- [<span data-ttu-id="2a36c-124">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="2a36c-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="2a36c-125">Microsoft. 양자. ApplyWithA</span><span class="sxs-lookup"><span data-stu-id="2a36c-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="2a36c-126">Microsoft. 양자. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="2a36c-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)