---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: UncurriedOpA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: 21df20354ad2388891f32b1bf1c7781287904983
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715219"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="1b5e4-102">UncurriedOpA 함수</span><span class="sxs-lookup"><span data-stu-id="1b5e4-102">UncurriedOpA function</span></span>

<span data-ttu-id="1b5e4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1b5e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1b5e4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1b5e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1b5e4-105">작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5e4-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="1b5e4-106">한정자는 `A` 작업이 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b5e4-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="1b5e4-107">입력</span><span class="sxs-lookup"><span data-stu-id="1b5e4-107">Input</span></span>

### <a name="curriedop--t---u--unit-adj"></a><span data-ttu-id="1b5e4-108">curriedOp: ' t-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="1b5e4-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="1b5e4-109">작업을 반환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5e4-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-adj"></a><span data-ttu-id="1b5e4-110">출력: (' t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="1b5e4-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="1b5e4-111">에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="1b5e4-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1b5e4-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b5e4-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1b5e4-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="1b5e4-113">'T</span></span>

<span data-ttu-id="1b5e4-114">커리 된 함수의 첫 번째 인수 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5e4-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="1b5e4-115">' U</span><span class="sxs-lookup"><span data-stu-id="1b5e4-115">'U</span></span>

<span data-ttu-id="1b5e4-116">커리 된 함수의 두 번째 인수 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5e4-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b5e4-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1b5e4-117">See Also</span></span>

- [<span data-ttu-id="1b5e4-118">Microsoft. 양자. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="1b5e4-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)