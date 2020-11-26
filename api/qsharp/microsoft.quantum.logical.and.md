---
uid: Microsoft.Quantum.Logical.And
title: And 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 279221ed785dd76e28146e4c22e70290936bf529
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198574"
---
# <a name="and-function"></a><span data-ttu-id="21ea0-102">And 함수</span><span class="sxs-lookup"><span data-stu-id="21ea0-102">And function</span></span>

<span data-ttu-id="21ea0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="21ea0-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="21ea0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="21ea0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="21ea0-105">두 값의 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ea0-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="21ea0-106">입력</span><span class="sxs-lookup"><span data-stu-id="21ea0-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="21ea0-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="21ea0-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="21ea0-108">고려해 야 할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="21ea0-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="21ea0-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="21ea0-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="21ea0-110">고려할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="21ea0-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="21ea0-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="21ea0-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="21ea0-112">`true``a`및 `b` 가 둘 다 인 경우에만 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="21ea0-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ea0-113">설명</span><span class="sxs-lookup"><span data-stu-id="21ea0-113">Remarks</span></span>

<span data-ttu-id="21ea0-114">연산자와 달리 `and` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="21ea0-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="21ea0-115">단기 동작으로, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ea0-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```