---
uid: Microsoft.Quantum.Logical.Or
title: Or 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848475"
---
# <a name="or-function"></a><span data-ttu-id="465af-102">Or 함수</span><span class="sxs-lookup"><span data-stu-id="465af-102">Or function</span></span>

<span data-ttu-id="465af-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="465af-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="465af-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="465af-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="465af-105">두 값의 부울 분리를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="465af-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="465af-106">입력</span><span class="sxs-lookup"><span data-stu-id="465af-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="465af-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="465af-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="465af-108">고려해 야 할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="465af-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="465af-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="465af-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="465af-110">고려할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="465af-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="465af-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="465af-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="465af-112">`true``a`또는가 인 경우에만 `b` `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="465af-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="465af-113">설명</span><span class="sxs-lookup"><span data-stu-id="465af-113">Remarks</span></span>

<span data-ttu-id="465af-114">연산자와 달리 `or` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="465af-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="465af-115">단기 동작으로, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="465af-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a or b;
let x = Or(a, b);
```