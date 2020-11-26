---
uid: Microsoft.Quantum.Logical.NotEqualL
title: 참고
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: e138a8def30bc77499662ffa6bc214d0c6a38893
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197231"
---
# <a name="notequall-function"></a><span data-ttu-id="ec0e9-102">참고</span><span class="sxs-lookup"><span data-stu-id="ec0e9-102">NotEqualL function</span></span>

<span data-ttu-id="ec0e9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ec0e9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ec0e9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec0e9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec0e9-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e9-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="ec0e9-106">입력</span><span class="sxs-lookup"><span data-stu-id="ec0e9-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="ec0e9-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ec0e9-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ec0e9-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e9-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="ec0e9-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ec0e9-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ec0e9-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ec0e9-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ec0e9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ec0e9-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="ec0e9-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0e9-113">설명</span><span class="sxs-lookup"><span data-stu-id="ec0e9-113">Remarks</span></span>

<span data-ttu-id="ec0e9-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec0e9-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualL(a, b);
```