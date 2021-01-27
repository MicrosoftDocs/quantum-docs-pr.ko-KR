---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: TransformedOperationCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840117"
---
# <a name="transformedoperationca-function"></a><span data-ttu-id="f2439-102">TransformedOperationCA 함수</span><span class="sxs-lookup"><span data-stu-id="f2439-102">TransformedOperationCA function</span></span>

<span data-ttu-id="f2439-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f2439-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f2439-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f2439-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f2439-105">함수 및 작업이 지정 된 경우 지정 된 함수가 입력을 변환 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="f2439-106">입력</span><span class="sxs-lookup"><span data-stu-id="f2439-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="f2439-107">fn: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="f2439-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="f2439-108">지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="f2439-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="f2439-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f2439-110">변형할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj--ctl"></a><span data-ttu-id="f2439-111">출력: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="f2439-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f2439-112">Tbat는 입력을 사용 하 여를 호출 하 `fn` 고 결과 출력을에 전달 `op` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2439-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2439-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f2439-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f2439-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="f2439-115">' U</span><span class="sxs-lookup"><span data-stu-id="f2439-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="f2439-116">예</span><span class="sxs-lookup"><span data-stu-id="f2439-116">Example</span></span>

<span data-ttu-id="f2439-117">다음 호출에서는를 사용 하 여 입력 @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" 용으로 설계 된 작업을 @"Microsoft.Quantum.Arithmetic.BigEndian" 형식의 입력을 허용 하는 작업으로 변환 합니다 @"Microsoft.Quantum.Arithmetic.LittleEndian" .</span><span class="sxs-lookup"><span data-stu-id="f2439-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="f2439-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f2439-118">See Also</span></span>

- [<span data-ttu-id="f2439-119">TransformedOperation입니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="f2439-120">TransformedOperationA입니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-120">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="f2439-121">TransformedOperationCA입니다.</span><span class="sxs-lookup"><span data-stu-id="f2439-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="f2439-122">Microsoft. 양자. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="f2439-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="f2439-123">Microsoft. 양자 구성</span><span class="sxs-lookup"><span data-stu-id="f2439-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)