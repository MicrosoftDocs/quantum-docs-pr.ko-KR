---
uid: Microsoft.Quantum.Canon.ApplyIf
title: ApplyIf 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: c5a1012328fa012ee02707aa59c94ac9c44b8e87
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218838"
---
# <a name="applyif-operation"></a><span data-ttu-id="d0693-102">ApplyIf 작업</span><span class="sxs-lookup"><span data-stu-id="d0693-102">ApplyIf operation</span></span>

<span data-ttu-id="d0693-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d0693-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d0693-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d0693-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d0693-105">클래식 비트에 조건 화 된 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0693-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="d0693-106">Description</span><span class="sxs-lookup"><span data-stu-id="d0693-106">Description</span></span>

<span data-ttu-id="d0693-107">작업 `op` 및 비트 값이 지정 된 `bit` `op` `target` 경우가 인 경우에 적용 됩니다 `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="d0693-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="d0693-108">이면이 `false` 발생 하지 않습니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="d0693-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="d0693-109">입력</span><span class="sxs-lookup"><span data-stu-id="d0693-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="d0693-110">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0693-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d0693-111">조건부로 적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d0693-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="d0693-112">bit: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d0693-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d0693-113">op가 적용 되는지 여부를 제어 하는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="d0693-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="d0693-114">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="d0693-114">target : 'T</span></span>

<span data-ttu-id="d0693-115">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="d0693-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0693-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0693-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d0693-117">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0693-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d0693-118">없습니다</span><span class="sxs-lookup"><span data-stu-id="d0693-118">'T</span></span>

<span data-ttu-id="d0693-119">조건부로 적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d0693-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0693-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d0693-120">See Also</span></span>

- [<span data-ttu-id="d0693-121">Microsoft. 양자. ApplyIfC</span><span class="sxs-lookup"><span data-stu-id="d0693-121">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="d0693-122">Microsoft. 양자. ApplyIfA</span><span class="sxs-lookup"><span data-stu-id="d0693-122">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="d0693-123">Microsoft 양자. ApplyIfCA</span><span class="sxs-lookup"><span data-stu-id="d0693-123">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)