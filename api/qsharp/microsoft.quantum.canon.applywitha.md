---
uid: Microsoft.Quantum.Canon.ApplyWithA
title: 작업 (ApplyWithA 작업)
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: f717347a81e4efa5ad1736485ad9e1c518d736a7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841163"
---
# <a name="applywitha-operation"></a><span data-ttu-id="b0293-102">작업 (ApplyWithA 작업)</span><span class="sxs-lookup"><span data-stu-id="b0293-102">ApplyWithA operation</span></span>

<span data-ttu-id="b0293-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b0293-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b0293-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b0293-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b0293-105">두 작업을 수행 하는 경우 conjugated로 다른 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj), target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="b0293-106">설명</span><span class="sxs-lookup"><span data-stu-id="b0293-106">Description</span></span>

<span data-ttu-id="b0293-107">$U $ 및 $V $와 같은 단일 연산자에 의해 각각 설명 된 두 개의 작업은 ^ {\dagger} V U $ $U 시퀀스에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="b0293-108">즉,이 작업은 $U $와 $V $ conjugated에서 제공 하는 단일 연산자를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="b0293-109">입력</span><span class="sxs-lookup"><span data-stu-id="b0293-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="b0293-110">outerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="b0293-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b0293-111">$U $는 켤레 $V $로 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="b0293-112">외부 작업 $U $은 (는) adjointable 해야 하지만 제어할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj"></a><span data-ttu-id="b0293-113">innerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="b0293-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b0293-114">작업 $V $가 conjugated입니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="b0293-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="b0293-115">target : 'T</span></span>

<span data-ttu-id="b0293-116">외부 및 내부 작업에 제공 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b0293-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b0293-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b0293-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0293-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b0293-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="b0293-119">'T</span></span>

<span data-ttu-id="b0293-120">각 내부 및 외부 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0293-121">설명</span><span class="sxs-lookup"><span data-stu-id="b0293-121">Remarks</span></span>

<span data-ttu-id="b0293-122">외부 작업은 항상 adjointable으로 간주 되지만 결합 된 작업을 제어 하기 위해 제어 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0293-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0293-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b0293-123">See Also</span></span>

- [<span data-ttu-id="b0293-124">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="b0293-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="b0293-125">Microsoft. 양자. ApplyWithC</span><span class="sxs-lookup"><span data-stu-id="b0293-125">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [<span data-ttu-id="b0293-126">Microsoft 양자. ApplyWithCA</span><span class="sxs-lookup"><span data-stu-id="b0293-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)