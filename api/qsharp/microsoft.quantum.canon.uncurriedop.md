---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: UncurriedOp 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: 359c0b2a9dd56445fb39fadc6580809dd9fbf628
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715240"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="4885a-102">UncurriedOp 함수</span><span class="sxs-lookup"><span data-stu-id="4885a-102">UncurriedOp function</span></span>

<span data-ttu-id="4885a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4885a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4885a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4885a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4885a-105">작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4885a-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="4885a-106">입력</span><span class="sxs-lookup"><span data-stu-id="4885a-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="4885a-107">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4885a-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4885a-108">작업을 반환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="4885a-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="4885a-109">출력: (' t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4885a-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4885a-110">에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="4885a-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4885a-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4885a-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4885a-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="4885a-112">'T</span></span>

<span data-ttu-id="4885a-113">변환 작업에 대 한 첫 번째 입력의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4885a-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="4885a-114">' U</span><span class="sxs-lookup"><span data-stu-id="4885a-114">'U</span></span>

<span data-ttu-id="4885a-115">커리 된 작업에 대 한 두 번째 입력의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4885a-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="4885a-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4885a-116">See Also</span></span>

- [<span data-ttu-id="4885a-117">Microsoft. 양자. UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="4885a-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="4885a-118">Microsoft. 양자. UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="4885a-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="4885a-119">Microsoft. 양자. UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="4885a-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)