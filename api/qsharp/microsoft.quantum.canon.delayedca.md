---
uid: Microsoft.Quantum.Canon.DelayedCA
title: DelayedCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: c44e3448c471f2a20f995d4546ee54f3affb726e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840541"
---
# <a name="delayedca-function"></a><span data-ttu-id="a78c4-102">DelayedCA 함수</span><span class="sxs-lookup"><span data-stu-id="a78c4-102">DelayedCA function</span></span>

<span data-ttu-id="a78c4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a78c4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a78c4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a78c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a78c4-105">지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78c4-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="a78c4-106">입력</span><span class="sxs-lookup"><span data-stu-id="a78c4-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a78c4-107">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a78c4-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a78c4-108">반환 값을 적용 한 결과로 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a78c4-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="a78c4-109">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="a78c4-109">arg : 'T</span></span>

<span data-ttu-id="a78c4-110">작업이 `op` 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="a78c4-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="a78c4-111">출력: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a78c4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a78c4-112">입력에 적용 되는 새 작업입니다. `op``arg`</span><span class="sxs-lookup"><span data-stu-id="a78c4-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a78c4-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a78c4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a78c4-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="a78c4-114">'T</span></span>

<span data-ttu-id="a78c4-115">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a78c4-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="a78c4-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a78c4-116">See Also</span></span>

- [<span data-ttu-id="a78c4-117">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="a78c4-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="a78c4-118">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="a78c4-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)