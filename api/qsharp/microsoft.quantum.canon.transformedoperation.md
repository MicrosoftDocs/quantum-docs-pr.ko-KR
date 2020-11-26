---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: TransformedOperation 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: a26cc178f67fd99324355ac230d9e91081b6e238
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204932"
---
# <a name="transformedoperation-function"></a><span data-ttu-id="467c0-102">TransformedOperation 함수</span><span class="sxs-lookup"><span data-stu-id="467c0-102">TransformedOperation function</span></span>

<span data-ttu-id="467c0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="467c0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="467c0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="467c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="467c0-105">함수 및 작업이 지정 된 경우 지정 된 함수가 입력을 변환 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a><span data-ttu-id="467c0-106">입력</span><span class="sxs-lookup"><span data-stu-id="467c0-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="467c0-107">fn: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="467c0-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="467c0-108">지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="467c0-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="467c0-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="467c0-110">변형할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-110">The operation to be transformed.</span></span>



## <a name="output--u--unit"></a><span data-ttu-id="467c0-111">출력: ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="467c0-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="467c0-112">Tbat는 입력을 사용 하 여를 호출 하 `fn` 고 결과 출력을에 전달 `op` 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="467c0-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="467c0-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="467c0-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="467c0-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="467c0-115">' U</span><span class="sxs-lookup"><span data-stu-id="467c0-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="467c0-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="467c0-116">See Also</span></span>

- [<span data-ttu-id="467c0-117">TransformedOperationA입니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-117">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="467c0-118">TransformedOperationC입니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="467c0-119">TransformedOperationCA입니다.</span><span class="sxs-lookup"><span data-stu-id="467c0-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="467c0-120">Microsoft. 양자. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="467c0-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="467c0-121">Microsoft. 양자 구성</span><span class="sxs-lookup"><span data-stu-id="467c0-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)