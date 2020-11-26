---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: GreaterThanOrEqualL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 5536c009d6e78eac9ab2320b42aec7d2d82946eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197758"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="2b60e-102">GreaterThanOrEqualL 함수</span><span class="sxs-lookup"><span data-stu-id="2b60e-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="2b60e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2b60e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2b60e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b60e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b60e-105">숫자가 다른 숫자 보다 크거나 같은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b60e-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="2b60e-106">입력</span><span class="sxs-lookup"><span data-stu-id="2b60e-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="2b60e-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2b60e-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2b60e-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b60e-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="2b60e-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2b60e-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2b60e-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b60e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2b60e-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2b60e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2b60e-112">`true``a`가 보다 크거나가와 같은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="2b60e-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b60e-113">설명</span><span class="sxs-lookup"><span data-stu-id="2b60e-113">Remarks</span></span>

<span data-ttu-id="2b60e-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b60e-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```