---
uid: Microsoft.Quantum.Canon.DelayedC
title: DelayedC 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: d8036397559b1587b806f701d89e892eea2da8f9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207017"
---
# <a name="delayedc-function"></a><span data-ttu-id="35eaa-102">DelayedC 함수</span><span class="sxs-lookup"><span data-stu-id="35eaa-102">DelayedC function</span></span>

<span data-ttu-id="35eaa-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="35eaa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="35eaa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="35eaa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="35eaa-105">지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35eaa-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="35eaa-106">입력</span><span class="sxs-lookup"><span data-stu-id="35eaa-106">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="35eaa-107">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="35eaa-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="35eaa-108">반환 값을 적용 한 결과로 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="35eaa-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="35eaa-109">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="35eaa-109">arg : 'T</span></span>

<span data-ttu-id="35eaa-110">작업이 `op` 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="35eaa-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-ctl"></a><span data-ttu-id="35eaa-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit) => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="35eaa-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="35eaa-112">입력에 적용 되는 새 작업입니다. `op``arg`</span><span class="sxs-lookup"><span data-stu-id="35eaa-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="35eaa-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="35eaa-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="35eaa-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="35eaa-114">'T</span></span>

<span data-ttu-id="35eaa-115">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="35eaa-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="35eaa-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="35eaa-116">See Also</span></span>

- [<span data-ttu-id="35eaa-117">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="35eaa-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="35eaa-118">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="35eaa-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)