---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: LessThanOrEqualD 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 3f4ccb0888e7df7c43ff73be8a3140e3fa84d4dc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197639"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="6d4cb-102">LessThanOrEqualD 함수</span><span class="sxs-lookup"><span data-stu-id="6d4cb-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="6d4cb-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6d4cb-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6d4cb-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d4cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d4cb-105">숫자가 다른 숫자 보다 작거나 같은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="6d4cb-106">입력</span><span class="sxs-lookup"><span data-stu-id="6d4cb-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="6d4cb-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d4cb-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d4cb-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="6d4cb-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d4cb-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d4cb-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6d4cb-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6d4cb-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6d4cb-112">`true``a`가 보다 작거나 같은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="6d4cb-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4cb-113">설명</span><span class="sxs-lookup"><span data-stu-id="6d4cb-113">Remarks</span></span>

<span data-ttu-id="6d4cb-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```