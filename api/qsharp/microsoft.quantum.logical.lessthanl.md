---
uid: Microsoft.Quantum.Logical.LessThanL
title: LessThanL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: d5753f9e1447fc1bd433703037fe44c86aaa659c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849142"
---
# <a name="lessthanl-function"></a><span data-ttu-id="94106-102">LessThanL 함수</span><span class="sxs-lookup"><span data-stu-id="94106-102">LessThanL function</span></span>

<span data-ttu-id="94106-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="94106-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="94106-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94106-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94106-105">숫자가 다른 숫자 보다 작은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94106-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="94106-106">입력</span><span class="sxs-lookup"><span data-stu-id="94106-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="94106-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="94106-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="94106-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="94106-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="94106-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="94106-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="94106-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="94106-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="94106-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="94106-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="94106-112">`true``a`가 보다 작거나 같은 경우에만 `b` 입니다.</span><span class="sxs-lookup"><span data-stu-id="94106-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="94106-113">설명</span><span class="sxs-lookup"><span data-stu-id="94106-113">Remarks</span></span>

<span data-ttu-id="94106-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="94106-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanL(a, b);
```