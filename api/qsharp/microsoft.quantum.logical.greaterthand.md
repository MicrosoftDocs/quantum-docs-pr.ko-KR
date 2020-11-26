---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: GreaterThanD 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: c23d85cf513bb6d37e67260eeeb3b81b42e6771a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198030"
---
# <a name="greaterthand-function"></a><span data-ttu-id="6c1e4-102">GreaterThanD 함수</span><span class="sxs-lookup"><span data-stu-id="6c1e4-102">GreaterThanD function</span></span>

<span data-ttu-id="6c1e4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6c1e4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6c1e4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6c1e4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6c1e4-105">숫자가 다른 숫자 보다 큰 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="6c1e4-106">입력</span><span class="sxs-lookup"><span data-stu-id="6c1e4-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="6c1e4-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6c1e4-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6c1e4-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="6c1e4-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6c1e4-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6c1e4-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6c1e4-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6c1e4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6c1e4-112">`true``a`가 보다 엄격 하 게 큰 경우에만 `b` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1e4-113">설명</span><span class="sxs-lookup"><span data-stu-id="6c1e4-113">Remarks</span></span>

<span data-ttu-id="6c1e4-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanD(a, b);
```