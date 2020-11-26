---
uid: Microsoft.Quantum.Canon.DelayedA
title: DelayedA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 33ff4dab36a6c6e17b9496a623f70b814c9f2fed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207074"
---
# <a name="delayeda-function"></a><span data-ttu-id="18f66-102">DelayedA 함수</span><span class="sxs-lookup"><span data-stu-id="18f66-102">DelayedA function</span></span>

<span data-ttu-id="18f66-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="18f66-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="18f66-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="18f66-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="18f66-105">지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18f66-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="18f66-106">입력</span><span class="sxs-lookup"><span data-stu-id="18f66-106">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="18f66-107">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="18f66-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="18f66-108">반환 값을 적용 한 결과로 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="18f66-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="18f66-109">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="18f66-109">arg : 'T</span></span>

<span data-ttu-id="18f66-110">작업이 `op` 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="18f66-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj"></a><span data-ttu-id="18f66-111">출력: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="18f66-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="18f66-112">입력에 적용 되는 새 작업입니다. `op``arg`</span><span class="sxs-lookup"><span data-stu-id="18f66-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="18f66-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="18f66-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="18f66-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="18f66-114">'T</span></span>

<span data-ttu-id="18f66-115">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="18f66-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="18f66-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="18f66-116">See Also</span></span>

- [<span data-ttu-id="18f66-117">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="18f66-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="18f66-118">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="18f66-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)