---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: ApplyIfA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: d2880bbb95ebaf621ef9e5885051b94f32a3f1cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218770"
---
# <a name="applyifa-operation"></a><span data-ttu-id="78ecf-102">ApplyIfA 작업</span><span class="sxs-lookup"><span data-stu-id="78ecf-102">ApplyIfA operation</span></span>

<span data-ttu-id="78ecf-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="78ecf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="78ecf-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="78ecf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="78ecf-105">클래식 비트에 adjointable 작업 조건 화 된을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78ecf-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="78ecf-106">Description</span><span class="sxs-lookup"><span data-stu-id="78ecf-106">Description</span></span>

<span data-ttu-id="78ecf-107">작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="78ecf-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="78ecf-108">이면이 `false` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="78ecf-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="78ecf-109">접미사는 `A` 적용 될 작업이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="78ecf-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="78ecf-110">입력</span><span class="sxs-lookup"><span data-stu-id="78ecf-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="78ecf-111">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="78ecf-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="78ecf-112">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="78ecf-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="78ecf-113">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="78ecf-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="78ecf-114">op가 적용 되는지 여부를 제어 하는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="78ecf-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="78ecf-115">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="78ecf-115">target : 'T</span></span>

<span data-ttu-id="78ecf-116">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="78ecf-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="78ecf-117">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="78ecf-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="78ecf-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="78ecf-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="78ecf-119">없습니다</span><span class="sxs-lookup"><span data-stu-id="78ecf-119">'T</span></span>

<span data-ttu-id="78ecf-120">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="78ecf-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="78ecf-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="78ecf-121">See Also</span></span>

- [<span data-ttu-id="78ecf-122">Microsoft. 양자. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="78ecf-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="78ecf-123">Microsoft. 양자. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="78ecf-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="78ecf-124">Microsoft 양자. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="78ecf-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)