---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: GreaterThanOrEqualI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 292599c18d2aac44cef8f0eecca38eb1fbe22061
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723497"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="ccbb9-102">GreaterThanOrEqualI 함수</span><span class="sxs-lookup"><span data-stu-id="ccbb9-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="ccbb9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ccbb9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ccbb9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ccbb9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ccbb9-105">숫자가 다른 숫자 보다 크거나 같은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="ccbb9-106">입력</span><span class="sxs-lookup"><span data-stu-id="ccbb9-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="ccbb9-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ccbb9-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ccbb9-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="ccbb9-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ccbb9-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ccbb9-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ccbb9-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ccbb9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ccbb9-112">`true``a`가 보다 크거나가와 같은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="ccbb9-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccbb9-113">설명</span><span class="sxs-lookup"><span data-stu-id="ccbb9-113">Remarks</span></span>

<span data-ttu-id="ccbb9-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```