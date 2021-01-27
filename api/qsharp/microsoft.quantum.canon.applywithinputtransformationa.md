---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationA
title: ApplyWithInputTransformationA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 3ab07f301f310e3ec380981bdb53201fc74bd289
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841134"
---
# <a name="applywithinputtransformationa-operation"></a><span data-ttu-id="3be69-102">ApplyWithInputTransformationA 작업</span><span class="sxs-lookup"><span data-stu-id="3be69-102">ApplyWithInputTransformationA operation</span></span>

<span data-ttu-id="3be69-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3be69-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3be69-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3be69-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3be69-105">일부 입력을 허용 하는 작업, 해당 작업과 호환 되는 출력을 반환 하는 함수 및이 함수에 대 한 입력을 제공 하는 경우 함수를 사용 하 여 작업에 필요한 형식으로 입력을 변환 하는 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj), input : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="3be69-106">입력</span><span class="sxs-lookup"><span data-stu-id="3be69-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="3be69-107">fn: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="3be69-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="3be69-108">지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="3be69-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="3be69-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3be69-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="3be69-111">입력: ' U</span><span class="sxs-lookup"><span data-stu-id="3be69-111">input : 'U</span></span>

<span data-ttu-id="3be69-112">함수에 대 한 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3be69-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3be69-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3be69-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3be69-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3be69-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="3be69-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="3be69-116">' U</span><span class="sxs-lookup"><span data-stu-id="3be69-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="3be69-117">예</span><span class="sxs-lookup"><span data-stu-id="3be69-117">Example</span></span>

<span data-ttu-id="3be69-118">다음 호출에서는를 사용 하 여 @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" 형식의 입력에 대 한 입력 용으로 설계 된 작업을 적용 합니다 @"Microsoft.Quantum.Arithmetic.BigEndian" @"Microsoft.Quantum.Arithmetic.LittleEndian" .</span><span class="sxs-lookup"><span data-stu-id="3be69-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="3be69-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3be69-119">See Also</span></span>

- [<span data-ttu-id="3be69-120">Microsoft. 양자. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="3be69-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="3be69-121">ApplyWithInputTransformationC입니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="3be69-122">ApplyWithInputTransformationCA입니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="3be69-123">TransformedOperation입니다.</span><span class="sxs-lookup"><span data-stu-id="3be69-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)