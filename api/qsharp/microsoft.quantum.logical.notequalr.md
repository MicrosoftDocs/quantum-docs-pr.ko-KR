---
uid: Microsoft.Quantum.Logical.NotEqualR
title: NotEqualR 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 06615c7ffb6aafc296077990dfca0ce25e1e00fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709794"
---
# <a name="notequalr-function"></a><span data-ttu-id="3e5f6-102">NotEqualR 함수</span><span class="sxs-lookup"><span data-stu-id="3e5f6-102">NotEqualR function</span></span>

<span data-ttu-id="3e5f6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="3e5f6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="3e5f6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3e5f6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3e5f6-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="3e5f6-106">입력</span><span class="sxs-lookup"><span data-stu-id="3e5f6-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="3e5f6-107">a: __잘못 <Result> 된__</span><span class="sxs-lookup"><span data-stu-id="3e5f6-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="3e5f6-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="3e5f6-109">b: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="3e5f6-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="3e5f6-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3e5f6-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3e5f6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3e5f6-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="3e5f6-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e5f6-113">설명</span><span class="sxs-lookup"><span data-stu-id="3e5f6-113">Remarks</span></span>

<span data-ttu-id="3e5f6-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e5f6-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```