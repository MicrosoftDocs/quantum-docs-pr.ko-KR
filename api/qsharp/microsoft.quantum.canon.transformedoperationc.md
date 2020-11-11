---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: TransformedOperationC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: b6867a076b654337f6127657189a8453c9973cc2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715324"
---
# <a name="transformedoperationc-function"></a><span data-ttu-id="66ad8-102">TransformedOperationC 함수</span><span class="sxs-lookup"><span data-stu-id="66ad8-102">TransformedOperationC function</span></span>

<span data-ttu-id="66ad8-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="66ad8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="66ad8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="66ad8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="66ad8-105">함수 및 작업이 지정 된 경우 지정 된 함수가 입력을 변환 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="66ad8-106">입력</span><span class="sxs-lookup"><span data-stu-id="66ad8-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="66ad8-107">fn: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="66ad8-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="66ad8-108">지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="66ad8-109">op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="66ad8-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="66ad8-110">변형할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-110">The operation to be transformed.</span></span>



## <a name="output--u--unit-ctl"></a><span data-ttu-id="66ad8-111">출력: ' U => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="66ad8-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="66ad8-112">Tbat는 입력을 사용 하 여를 호출 하 `fn` 고 결과 출력을에 전달 `op` 합니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="66ad8-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="66ad8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="66ad8-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="66ad8-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="66ad8-115">' U</span><span class="sxs-lookup"><span data-stu-id="66ad8-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="66ad8-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="66ad8-116">See Also</span></span>

- [<span data-ttu-id="66ad8-117">TransformedOperation입니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="66ad8-118">TransformedOperationA입니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-118">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="66ad8-119">TransformedOperationCA입니다.</span><span class="sxs-lookup"><span data-stu-id="66ad8-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="66ad8-120">Microsoft. 양자. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="66ad8-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="66ad8-121">Microsoft. 양자 구성</span><span class="sxs-lookup"><span data-stu-id="66ad8-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)