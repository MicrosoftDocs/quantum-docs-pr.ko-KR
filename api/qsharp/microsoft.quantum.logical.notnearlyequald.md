---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: NotNearlyEqualD 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: d9e4cc5b0cfba3989ae64e494d0daa52069718a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720728"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="f6f24-102">NotNearlyEqualD 함수</span><span class="sxs-lookup"><span data-stu-id="f6f24-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="f6f24-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f6f24-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f6f24-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6f24-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6f24-105">두 입력이 거의 같지 않은 경우에만 true를 반환 합니다. 즉,의 허용 오차 범위 내에 없는 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f24-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="f6f24-106">입력</span><span class="sxs-lookup"><span data-stu-id="f6f24-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="f6f24-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f6f24-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f6f24-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f6f24-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="f6f24-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f6f24-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f6f24-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f6f24-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f6f24-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f6f24-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f6f24-112">`true``a`가와 거의 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="f6f24-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f24-113">설명</span><span class="sxs-lookup"><span data-stu-id="f6f24-113">Remarks</span></span>

<span data-ttu-id="f6f24-114">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f24-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```