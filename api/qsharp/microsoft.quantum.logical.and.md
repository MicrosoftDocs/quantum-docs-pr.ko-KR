---
uid: Microsoft.Quantum.Logical.And
title: And 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 6c405bdb4182cc7f32bd04952dec25a974c03445
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849235"
---
# <a name="and-function"></a><span data-ttu-id="533c4-102">And 함수</span><span class="sxs-lookup"><span data-stu-id="533c4-102">And function</span></span>

<span data-ttu-id="533c4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="533c4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="533c4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="533c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="533c4-105">두 값의 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="533c4-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="533c4-106">입력</span><span class="sxs-lookup"><span data-stu-id="533c4-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="533c4-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="533c4-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="533c4-108">고려해 야 할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="533c4-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="533c4-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="533c4-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="533c4-110">고려할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="533c4-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="533c4-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="533c4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="533c4-112">`true``a`및 `b` 가 둘 다 인 경우에만 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="533c4-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="533c4-113">설명</span><span class="sxs-lookup"><span data-stu-id="533c4-113">Remarks</span></span>

<span data-ttu-id="533c4-114">연산자와 달리 `and` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="533c4-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="533c4-115">단기 동작으로, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="533c4-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a and b;
let x = And(a, b);
```