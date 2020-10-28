---
uid: Microsoft.Quantum.Logical.LessThanL
title: LessThanL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: fde57bcd9960056461bddac54300c298def8f7d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709955"
---
# <a name="lessthanl-function"></a><span data-ttu-id="72f40-102">LessThanL 함수</span><span class="sxs-lookup"><span data-stu-id="72f40-102">LessThanL function</span></span>

<span data-ttu-id="72f40-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="72f40-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="72f40-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="72f40-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="72f40-105">숫자가 다른 숫자 보다 작은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72f40-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="72f40-106">입력</span><span class="sxs-lookup"><span data-stu-id="72f40-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="72f40-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="72f40-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="72f40-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="72f40-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="72f40-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="72f40-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="72f40-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="72f40-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="72f40-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="72f40-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="72f40-112">`true``a`가 보다 작거나 같은 경우에만 `b` 입니다.</span><span class="sxs-lookup"><span data-stu-id="72f40-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f40-113">설명</span><span class="sxs-lookup"><span data-stu-id="72f40-113">Remarks</span></span>

<span data-ttu-id="72f40-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="72f40-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```