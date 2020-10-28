---
uid: Microsoft.Quantum.Canon.CurriedOp
title: CurriedOp 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716367"
---
# <a name="curriedop-function"></a><span data-ttu-id="c0978-102">CurriedOp 함수</span><span class="sxs-lookup"><span data-stu-id="c0978-102">CurriedOp function</span></span>

<span data-ttu-id="c0978-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c0978-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c0978-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c0978-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c0978-105">두 입력에 대해 변환 된 작업 버전을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="c0978-106">즉, 두 개의 입력으로 작업을 제공 하는 경우이 함수는 isomorphism $f (x, y) \equiv f (x) (y) $를 적용 하 여 한 입력의 작업을 반환 하는 하나의 입력 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="c0978-107">입력</span><span class="sxs-lookup"><span data-stu-id="c0978-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="c0978-108">op: (' t ', ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c0978-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c0978-109">입력이 쌍 인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="c0978-110">출력: ' U ' > ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c0978-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c0978-111">쌍의 첫 번째 요소를 수락 하 고 원래 작업의 입력에 대 한 두 번째 요소를 입력으로 받아 들이는 작업을 반환 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c0978-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0978-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c0978-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="c0978-113">'T</span></span>

<span data-ttu-id="c0978-114">쌍에 정의 된 함수의 첫 번째 구성 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="c0978-115">' U</span><span class="sxs-lookup"><span data-stu-id="c0978-115">'U</span></span>

<span data-ttu-id="c0978-116">쌍에 정의 된 함수의 두 번째 구성 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0978-117">설명</span><span class="sxs-lookup"><span data-stu-id="c0978-117">Remarks</span></span>

<span data-ttu-id="c0978-118">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0978-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```