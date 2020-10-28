---
uid: Microsoft.Quantum.Logical.EqualR
title: EqualR 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710032"
---
# <a name="equalr-function"></a><span data-ttu-id="e1278-102">EqualR 함수</span><span class="sxs-lookup"><span data-stu-id="e1278-102">EqualR function</span></span>

<span data-ttu-id="e1278-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e1278-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e1278-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1278-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1278-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="e1278-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="e1278-106">입력</span><span class="sxs-lookup"><span data-stu-id="e1278-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="e1278-107">a: __잘못 <Result> 된__</span><span class="sxs-lookup"><span data-stu-id="e1278-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="e1278-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e1278-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="e1278-109">b: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="e1278-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="e1278-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e1278-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e1278-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e1278-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e1278-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="e1278-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1278-113">설명</span><span class="sxs-lookup"><span data-stu-id="e1278-113">Remarks</span></span>

<span data-ttu-id="e1278-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1278-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```