---
uid: Microsoft.Quantum.Canon.DelayedA
title: DelayedA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 11c11cdd75d80d6324666ef56930f7a522121826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716248"
---
# <a name="delayeda-function"></a><span data-ttu-id="5fc0f-102">DelayedA 함수</span><span class="sxs-lookup"><span data-stu-id="5fc0f-102">DelayedA function</span></span>

<span data-ttu-id="5fc0f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5fc0f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5fc0f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fc0f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5fc0f-105">지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="5fc0f-106">입력</span><span class="sxs-lookup"><span data-stu-id="5fc0f-106">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="5fc0f-107">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="5fc0f-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5fc0f-108">반환 값을 적용 한 결과로 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="5fc0f-109">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="5fc0f-109">arg : 'T</span></span>

<span data-ttu-id="5fc0f-110">작업이 `op` 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-adj"></a><span data-ttu-id="5fc0f-111">출력: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="5fc0f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5fc0f-112">입력에 적용 되는 새 작업입니다. `op``arg`</span><span class="sxs-lookup"><span data-stu-id="5fc0f-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5fc0f-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fc0f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5fc0f-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="5fc0f-114">'T</span></span>

<span data-ttu-id="5fc0f-115">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fc0f-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5fc0f-116">See Also</span></span>

- [<span data-ttu-id="5fc0f-117">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="5fc0f-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="5fc0f-118">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="5fc0f-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)