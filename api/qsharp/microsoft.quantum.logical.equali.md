---
uid: Microsoft.Quantum.Logical.EqualI
title: EqualI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: be92ef2b63981094e1a95c38e02de95c3c2bbf3a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198166"
---
# <a name="equali-function"></a><span data-ttu-id="e215a-102">EqualI 함수</span><span class="sxs-lookup"><span data-stu-id="e215a-102">EqualI function</span></span>

<span data-ttu-id="e215a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e215a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e215a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e215a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e215a-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="e215a-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="e215a-106">입력</span><span class="sxs-lookup"><span data-stu-id="e215a-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="e215a-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e215a-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e215a-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e215a-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="e215a-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e215a-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e215a-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e215a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e215a-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e215a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e215a-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="e215a-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e215a-113">설명</span><span class="sxs-lookup"><span data-stu-id="e215a-113">Remarks</span></span>

<span data-ttu-id="e215a-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="e215a-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```