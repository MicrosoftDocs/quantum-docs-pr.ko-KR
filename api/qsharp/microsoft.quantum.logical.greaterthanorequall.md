---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: GreaterThanOrEqualL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: f33a7f17f3391d87e3eff9fb31939586036e83f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815855"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="1d428-102">GreaterThanOrEqualL 함수</span><span class="sxs-lookup"><span data-stu-id="1d428-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="1d428-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1d428-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1d428-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d428-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d428-105">숫자가 다른 숫자 보다 크거나 같은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d428-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="1d428-106">입력</span><span class="sxs-lookup"><span data-stu-id="1d428-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="1d428-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1d428-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1d428-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1d428-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="1d428-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1d428-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1d428-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1d428-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1d428-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1d428-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1d428-112">`true``a`가 보다 크거나가와 같은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="1d428-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d428-113">설명</span><span class="sxs-lookup"><span data-stu-id="1d428-113">Remarks</span></span>

<span data-ttu-id="1d428-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d428-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```