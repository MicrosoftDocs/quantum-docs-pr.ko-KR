---
uid: Microsoft.Quantum.Canon.ConjugatedBy
title: ConjugatedBy 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedBy
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 37fbee9a7c11991645933a372f9f12c1fd696b66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716472"
---
# <a name="conjugatedby-function"></a><span data-ttu-id="9d94f-102">ConjugatedBy 함수</span><span class="sxs-lookup"><span data-stu-id="9d94f-102">ConjugatedBy function</span></span>

<span data-ttu-id="9d94f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9d94f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9d94f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d94f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d94f-105">외부 및 내부 연산을 지정 하면는 외부 작업에 의해 내부 작업을 변화 시키고 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedBy<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit)) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="9d94f-106">입력</span><span class="sxs-lookup"><span data-stu-id="9d94f-106">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="9d94f-107">outerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="9d94f-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="9d94f-108">$U $는 켤레 $V $로 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="9d94f-109">외부 작업 $U $은 (는) adjointable 해야 하지만 제어할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit"></a><span data-ttu-id="9d94f-110">innerOperation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d94f-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9d94f-111">작업 $V $가 conjugated입니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="9d94f-112">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d94f-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9d94f-113">해당 작업이 단일 $U ^ {\dagger} V U $로 표시 되는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9d94f-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9d94f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d94f-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="9d94f-115">'T</span></span>

<span data-ttu-id="9d94f-116">각 내부 및 외부 작업이 작동 하는 대상의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d94f-117">설명</span><span class="sxs-lookup"><span data-stu-id="9d94f-117">Remarks</span></span>

<span data-ttu-id="9d94f-118">외부 작업은 항상 adjointable으로 간주 되지만 결합 된 작업을 제어 하기 위해 제어 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d94f-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9d94f-119">See Also</span></span>

- [<span data-ttu-id="9d94f-120">ConjugatedByA입니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="9d94f-121">ConjugatedByC입니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="9d94f-122">ConjugatedByCA입니다.</span><span class="sxs-lookup"><span data-stu-id="9d94f-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="9d94f-123">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="9d94f-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)