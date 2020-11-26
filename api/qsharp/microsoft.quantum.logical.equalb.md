---
uid: Microsoft.Quantum.Logical.EqualB
title: EqualB 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: b566f5ba8548eadeecf63a1e91956d936e7e9a20
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198472"
---
# <a name="equalb-function"></a><span data-ttu-id="fd4a9-102">EqualB 함수</span><span class="sxs-lookup"><span data-stu-id="fd4a9-102">EqualB function</span></span>

<span data-ttu-id="fd4a9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="fd4a9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="fd4a9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd4a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd4a9-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="fd4a9-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="fd4a9-106">입력</span><span class="sxs-lookup"><span data-stu-id="fd4a9-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="fd4a9-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fd4a9-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fd4a9-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4a9-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="fd4a9-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fd4a9-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fd4a9-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4a9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="fd4a9-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fd4a9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fd4a9-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="fd4a9-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd4a9-113">설명</span><span class="sxs-lookup"><span data-stu-id="fd4a9-113">Remarks</span></span>

<span data-ttu-id="fd4a9-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4a9-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```