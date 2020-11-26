---
uid: Microsoft.Quantum.Canon.CurriedOp
title: CurriedOp 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 6c1917d6f1ee69cb29fed1ab173106af1e206533
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216628"
---
# <a name="curriedop-function"></a><span data-ttu-id="84533-102">CurriedOp 함수</span><span class="sxs-lookup"><span data-stu-id="84533-102">CurriedOp function</span></span>

<span data-ttu-id="84533-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84533-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84533-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84533-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84533-105">두 입력에 대해 변환 된 작업 버전을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="84533-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="84533-106">즉, 두 개의 입력으로 작업을 제공 하는 경우이 함수는 isomorphism $f (x, y) \equiv f (x) (y) $를 적용 하 여 한 입력의 작업을 반환 하는 하나의 입력 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="84533-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="84533-107">입력</span><span class="sxs-lookup"><span data-stu-id="84533-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="84533-108">op: (' t ', ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84533-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84533-109">입력이 쌍 인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="84533-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="84533-110">출력: ' U ' > ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84533-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84533-111">쌍의 첫 번째 요소를 수락 하 고 원래 작업의 입력에 대 한 두 번째 요소를 입력으로 받아 들이는 작업을 반환 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="84533-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84533-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="84533-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84533-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="84533-113">'T</span></span>

<span data-ttu-id="84533-114">쌍에 정의 된 함수의 첫 번째 구성 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="84533-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="84533-115">' U</span><span class="sxs-lookup"><span data-stu-id="84533-115">'U</span></span>

<span data-ttu-id="84533-116">쌍에 정의 된 함수의 두 번째 구성 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="84533-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="84533-117">설명</span><span class="sxs-lookup"><span data-stu-id="84533-117">Remarks</span></span>

<span data-ttu-id="84533-118">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="84533-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```