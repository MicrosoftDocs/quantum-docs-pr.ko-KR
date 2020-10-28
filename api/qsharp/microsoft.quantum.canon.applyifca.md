---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: ApplyIfCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: 9057c79622f15a082963d94fc261664e00322feb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718232"
---
# <a name="applyifca-operation"></a><span data-ttu-id="28bcf-102">ApplyIfCA 작업</span><span class="sxs-lookup"><span data-stu-id="28bcf-102">ApplyIfCA operation</span></span>

<span data-ttu-id="28bcf-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="28bcf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="28bcf-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28bcf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28bcf-105">단일 작업 조건 화 된를 기존 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28bcf-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="28bcf-106">Description</span><span class="sxs-lookup"><span data-stu-id="28bcf-106">Description</span></span>

<span data-ttu-id="28bcf-107">작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="28bcf-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="28bcf-108">이면이 `false` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="28bcf-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="28bcf-109">접미사는 `CA` 적용 될 작업이 단일 (제어 가능 및 adjointable) 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="28bcf-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="28bcf-110">입력</span><span class="sxs-lookup"><span data-stu-id="28bcf-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="28bcf-111">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span><span class="sxs-lookup"><span data-stu-id="28bcf-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="28bcf-112">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="28bcf-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="28bcf-113">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="28bcf-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="28bcf-114">op가 적용 되는지 여부를 제어 하는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="28bcf-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="28bcf-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="28bcf-115">target : 'T</span></span>

<span data-ttu-id="28bcf-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="28bcf-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="28bcf-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="28bcf-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="28bcf-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="28bcf-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="28bcf-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="28bcf-119">'T</span></span>

<span data-ttu-id="28bcf-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="28bcf-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="28bcf-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28bcf-121">See Also</span></span>

- [<span data-ttu-id="28bcf-122">Microsoft. 양자. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="28bcf-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="28bcf-123">Microsoft. 양자. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="28bcf-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="28bcf-124">Microsoft 양자. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="28bcf-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)