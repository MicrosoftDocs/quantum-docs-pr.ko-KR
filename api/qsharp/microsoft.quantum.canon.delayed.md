---
uid: Microsoft.Quantum.Canon.Delayed
title: 지연 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 863c63d0c1a50339e9d5b9fbe4729932b2706f32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216458"
---
# <a name="delayed-function"></a><span data-ttu-id="94e30-102">지연 함수</span><span class="sxs-lookup"><span data-stu-id="94e30-102">Delayed function</span></span>

<span data-ttu-id="94e30-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="94e30-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="94e30-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94e30-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94e30-105">지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94e30-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="94e30-106">입력</span><span class="sxs-lookup"><span data-stu-id="94e30-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="94e30-107">op: ' t => ' U</span><span class="sxs-lookup"><span data-stu-id="94e30-107">op : 'T => 'U</span></span> 

<span data-ttu-id="94e30-108">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="94e30-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="94e30-109">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="94e30-109">arg : 'T</span></span>

<span data-ttu-id="94e30-110">작업이 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="94e30-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="94e30-111">출력: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="94e30-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="94e30-112">입력에 적용 되는 새 작업입니다. `op``arg`</span><span class="sxs-lookup"><span data-stu-id="94e30-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="94e30-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="94e30-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="94e30-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="94e30-114">'T</span></span>

<span data-ttu-id="94e30-115">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="94e30-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="94e30-116">' U</span><span class="sxs-lookup"><span data-stu-id="94e30-116">'U</span></span>

<span data-ttu-id="94e30-117">연기할 작업의 반환 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="94e30-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="94e30-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="94e30-118">See Also</span></span>

- [<span data-ttu-id="94e30-119">DelayedC입니다.</span><span class="sxs-lookup"><span data-stu-id="94e30-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="94e30-120">Microsoft 양자. DelayedA</span><span class="sxs-lookup"><span data-stu-id="94e30-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="94e30-121">Microsoft 양자. DelayedCA</span><span class="sxs-lookup"><span data-stu-id="94e30-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="94e30-122">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="94e30-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)