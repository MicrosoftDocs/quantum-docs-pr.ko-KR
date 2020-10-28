---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationCA
title: ApplyWithInputTransformationCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationCA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: c80ce0887a202a60de81c2d12fa95ce1eab59058
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716836"
---
# <a name="applywithinputtransformationca-operation"></a><span data-ttu-id="65340-102">ApplyWithInputTransformationCA 작업</span><span class="sxs-lookup"><span data-stu-id="65340-102">ApplyWithInputTransformationCA operation</span></span>

<span data-ttu-id="65340-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="65340-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="65340-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="65340-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="65340-105">일부 입력을 허용 하는 작업, 해당 작업과 호환 되는 출력을 반환 하는 함수 및이 함수에 대 한 입력을 제공 하는 경우 함수를 사용 하 여 작업에 필요한 형식으로 입력을 변환 하는 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65340-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="65340-106">입력</span><span class="sxs-lookup"><span data-stu-id="65340-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="65340-107">fn: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="65340-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="65340-108">지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="65340-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="65340-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="65340-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="65340-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="65340-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="65340-111">입력: ' U</span><span class="sxs-lookup"><span data-stu-id="65340-111">input : 'U</span></span>

<span data-ttu-id="65340-112">함수에 대 한 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="65340-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="65340-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="65340-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="65340-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="65340-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="65340-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="65340-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="65340-116">' U</span><span class="sxs-lookup"><span data-stu-id="65340-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="65340-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="65340-117">See Also</span></span>

- [<span data-ttu-id="65340-118">Microsoft. 양자. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="65340-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="65340-119">ApplyWithInputTransformationA입니다.</span><span class="sxs-lookup"><span data-stu-id="65340-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="65340-120">ApplyWithInputTransformationC입니다.</span><span class="sxs-lookup"><span data-stu-id="65340-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="65340-121">TransformedOperation입니다.</span><span class="sxs-lookup"><span data-stu-id="65340-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)