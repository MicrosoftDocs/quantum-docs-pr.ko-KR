---
uid: Microsoft.Quantum.Logical.NotEqualL
title: 참고
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: b19de2e4e8052c77118f341700357b212e20af53
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849037"
---
# <a name="notequall-function"></a><span data-ttu-id="9bed2-102">참고</span><span class="sxs-lookup"><span data-stu-id="9bed2-102">NotEqualL function</span></span>

<span data-ttu-id="9bed2-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9bed2-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9bed2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9bed2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9bed2-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bed2-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="9bed2-106">입력</span><span class="sxs-lookup"><span data-stu-id="9bed2-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="9bed2-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9bed2-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9bed2-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9bed2-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="9bed2-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9bed2-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9bed2-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9bed2-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9bed2-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9bed2-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9bed2-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="9bed2-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bed2-113">설명</span><span class="sxs-lookup"><span data-stu-id="9bed2-113">Remarks</span></span>

<span data-ttu-id="9bed2-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bed2-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualL(a, b);
```