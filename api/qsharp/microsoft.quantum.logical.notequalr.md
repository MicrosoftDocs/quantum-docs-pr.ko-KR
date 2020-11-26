---
uid: Microsoft.Quantum.Logical.NotEqualR
title: NotEqualR 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197197"
---
# <a name="notequalr-function"></a><span data-ttu-id="85f3a-102">NotEqualR 함수</span><span class="sxs-lookup"><span data-stu-id="85f3a-102">NotEqualR function</span></span>

<span data-ttu-id="85f3a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="85f3a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="85f3a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85f3a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85f3a-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="85f3a-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="85f3a-106">입력</span><span class="sxs-lookup"><span data-stu-id="85f3a-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="85f3a-107">a: __잘못 <Result> 된__</span><span class="sxs-lookup"><span data-stu-id="85f3a-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="85f3a-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85f3a-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="85f3a-109">b: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="85f3a-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="85f3a-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85f3a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="85f3a-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="85f3a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="85f3a-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="85f3a-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="85f3a-113">설명</span><span class="sxs-lookup"><span data-stu-id="85f3a-113">Remarks</span></span>

<span data-ttu-id="85f3a-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="85f3a-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```