---
uid: Microsoft.Quantum.Logical.NotEqualI
title: NotEqualI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualI
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 68e0e105a6b3742ec11e80ff92c39578a786aa85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709829"
---
# <a name="notequali-function"></a><span data-ttu-id="aaee3-102">NotEqualI 함수</span><span class="sxs-lookup"><span data-stu-id="aaee3-102">NotEqualI function</span></span>

<span data-ttu-id="aaee3-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="aaee3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="aaee3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aaee3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aaee3-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaee3-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="aaee3-106">입력</span><span class="sxs-lookup"><span data-stu-id="aaee3-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="aaee3-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aaee3-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aaee3-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="aaee3-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="aaee3-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aaee3-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aaee3-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="aaee3-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="aaee3-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="aaee3-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="aaee3-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="aaee3-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaee3-113">설명</span><span class="sxs-lookup"><span data-stu-id="aaee3-113">Remarks</span></span>

<span data-ttu-id="aaee3-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaee3-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualI(a, b);
```