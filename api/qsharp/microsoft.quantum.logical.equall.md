---
uid: Microsoft.Quantum.Logical.EqualL
title: 모든 기능
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f0a2bfa866068746e9c6e249573eb61c0d08c0f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710039"
---
# <a name="equall-function"></a><span data-ttu-id="41a11-102">모든 기능</span><span class="sxs-lookup"><span data-stu-id="41a11-102">EqualL function</span></span>

<span data-ttu-id="41a11-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="41a11-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="41a11-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41a11-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41a11-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="41a11-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="41a11-106">입력</span><span class="sxs-lookup"><span data-stu-id="41a11-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="41a11-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="41a11-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="41a11-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="41a11-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="41a11-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="41a11-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="41a11-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="41a11-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="41a11-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="41a11-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="41a11-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="41a11-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="41a11-113">설명</span><span class="sxs-lookup"><span data-stu-id="41a11-113">Remarks</span></span>

<span data-ttu-id="41a11-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a11-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```