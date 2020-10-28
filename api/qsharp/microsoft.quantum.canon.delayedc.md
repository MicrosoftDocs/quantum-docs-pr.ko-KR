---
uid: Microsoft.Quantum.Canon.DelayedC
title: DelayedC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716213"
---
# <a name="delayedc-function"></a><span data-ttu-id="47e1b-102">DelayedC 함수</span><span class="sxs-lookup"><span data-stu-id="47e1b-102">DelayedC function</span></span>

<span data-ttu-id="47e1b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="47e1b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="47e1b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="47e1b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="47e1b-105">지정 된 인수를 사용 하 여 지정 된 작업을 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e1b-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="47e1b-106">입력</span><span class="sxs-lookup"><span data-stu-id="47e1b-106">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="47e1b-107">op: ' t => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="47e1b-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="47e1b-108">반환 값을 적용 한 결과로 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="47e1b-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="47e1b-109">인수: ' '</span><span class="sxs-lookup"><span data-stu-id="47e1b-109">arg : 'T</span></span>

<span data-ttu-id="47e1b-110">작업이 `op` 적용 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="47e1b-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl"></a><span data-ttu-id="47e1b-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="47e1b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="47e1b-112">입력에 적용 되는 새 작업입니다. `op``arg`</span><span class="sxs-lookup"><span data-stu-id="47e1b-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="47e1b-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="47e1b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47e1b-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="47e1b-114">'T</span></span>

<span data-ttu-id="47e1b-115">연기할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="47e1b-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="47e1b-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="47e1b-116">See Also</span></span>

- [<span data-ttu-id="47e1b-117">Microsoft. 양자. 지연</span><span class="sxs-lookup"><span data-stu-id="47e1b-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="47e1b-118">Microsoft. 양자 지연</span><span class="sxs-lookup"><span data-stu-id="47e1b-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)