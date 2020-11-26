---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: UncurriedOp 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: cad508f166d4af805cb98cd21a0260d9babb6a4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204643"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="8e9f7-102">UncurriedOp 함수</span><span class="sxs-lookup"><span data-stu-id="8e9f7-102">UncurriedOp function</span></span>

<span data-ttu-id="8e9f7-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8e9f7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8e9f7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e9f7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e9f7-105">작업을 반환 하는 함수가 지정 된 경우 두 입력을 튜플로 받는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9f7-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="8e9f7-106">입력</span><span class="sxs-lookup"><span data-stu-id="8e9f7-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="8e9f7-107">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e9f7-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8e9f7-108">작업을 반환 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="8e9f7-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="8e9f7-109">출력: (' t, ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e9f7-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8e9f7-110">에 해당 하는 새 작업입니다 `op` `op(t, u)` `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="8e9f7-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8e9f7-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e9f7-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e9f7-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="8e9f7-112">'T</span></span>

<span data-ttu-id="8e9f7-113">변환 작업에 대 한 첫 번째 입력의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8e9f7-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="8e9f7-114">' U</span><span class="sxs-lookup"><span data-stu-id="8e9f7-114">'U</span></span>

<span data-ttu-id="8e9f7-115">커리 된 작업에 대 한 두 번째 입력의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8e9f7-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e9f7-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8e9f7-116">See Also</span></span>

- [<span data-ttu-id="8e9f7-117">Microsoft. 양자. UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="8e9f7-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="8e9f7-118">Microsoft. 양자. UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="8e9f7-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="8e9f7-119">Microsoft. 양자. UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="8e9f7-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)