---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: ApplyIfA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: 279a069176ee24ed83406f72170462bf58c790d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718249"
---
# <a name="applyifa-operation"></a><span data-ttu-id="b720f-102">ApplyIfA 작업</span><span class="sxs-lookup"><span data-stu-id="b720f-102">ApplyIfA operation</span></span>

<span data-ttu-id="b720f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b720f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b720f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b720f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b720f-105">클래식 비트에 adjointable 작업 조건 화 된을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b720f-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="b720f-106">Description</span><span class="sxs-lookup"><span data-stu-id="b720f-106">Description</span></span>

<span data-ttu-id="b720f-107">작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="b720f-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="b720f-108">이면이 `false` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="b720f-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="b720f-109">접미사는 `A` 적용 될 작업이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b720f-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="b720f-110">입력</span><span class="sxs-lookup"><span data-stu-id="b720f-110">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="b720f-111">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="b720f-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="b720f-112">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b720f-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="b720f-113">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b720f-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b720f-114">op가 적용 되는지 여부를 제어 하는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="b720f-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="b720f-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="b720f-115">target : 'T</span></span>

<span data-ttu-id="b720f-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="b720f-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b720f-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b720f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b720f-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b720f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b720f-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="b720f-119">'T</span></span>

<span data-ttu-id="b720f-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b720f-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b720f-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b720f-121">See Also</span></span>

- [<span data-ttu-id="b720f-122">Microsoft. 양자. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="b720f-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="b720f-123">Microsoft. 양자. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="b720f-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="b720f-124">Microsoft 양자. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="b720f-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)