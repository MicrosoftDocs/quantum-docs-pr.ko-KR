---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: UncurriedOpC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715212"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="9e931-102">UncurriedOpC 함수</span><span class="sxs-lookup"><span data-stu-id="9e931-102">UncurriedOpC function</span></span>

<span data-ttu-id="9e931-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e931-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e931-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9e931-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9e931-105">작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e931-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="9e931-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e931-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="9e931-107">입력</span><span class="sxs-lookup"><span data-stu-id="9e931-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="9e931-108">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="9e931-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9e931-109">작업을 반환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="9e931-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl"></a><span data-ttu-id="9e931-110">출력: (' t, ' U) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="9e931-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9e931-111">에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="9e931-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9e931-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e931-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e931-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="9e931-113">'T</span></span>

<span data-ttu-id="9e931-114">커리 된 함수의 첫 번째 인수 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9e931-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="9e931-115">' U</span><span class="sxs-lookup"><span data-stu-id="9e931-115">'U</span></span>

<span data-ttu-id="9e931-116">커리 된 함수의 두 번째 인수 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9e931-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e931-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9e931-117">See Also</span></span>

- [<span data-ttu-id="9e931-118">Microsoft. 양자. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="9e931-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)