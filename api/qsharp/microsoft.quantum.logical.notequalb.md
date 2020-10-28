---
uid: Microsoft.Quantum.Logical.NotEqualB
title: NotEqualB 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: d5a9819bf3baa7c914487277fef308abbc8d25bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709836"
---
# <a name="notequalb-function"></a><span data-ttu-id="52ead-102">NotEqualB 함수</span><span class="sxs-lookup"><span data-stu-id="52ead-102">NotEqualB function</span></span>

<span data-ttu-id="52ead-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="52ead-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="52ead-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="52ead-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="52ead-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ead-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="52ead-106">입력</span><span class="sxs-lookup"><span data-stu-id="52ead-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="52ead-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="52ead-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="52ead-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="52ead-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="52ead-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="52ead-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="52ead-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="52ead-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="52ead-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="52ead-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="52ead-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="52ead-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="52ead-113">설명</span><span class="sxs-lookup"><span data-stu-id="52ead-113">Remarks</span></span>

<span data-ttu-id="52ead-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ead-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```