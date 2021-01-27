---
uid: Microsoft.Quantum.Arrays.Sorted
title: 정렬 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845436"
---
# <a name="sorted-function"></a><span data-ttu-id="7c27b-102">정렬 된 함수</span><span class="sxs-lookup"><span data-stu-id="7c27b-102">Sorted function</span></span>

<span data-ttu-id="7c27b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7c27b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7c27b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c27b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c27b-105">배열이 지정 된 경우 지정 된 비교 함수를 기준으로 정렬 된 해당 배열의 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27b-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="7c27b-106">입력</span><span class="sxs-lookup"><span data-stu-id="7c27b-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="7c27b-107">비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c27b-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c27b-108">`a`가 이면 보다 작거나 같은 두 요소를 비교 하는 함수입니다 `b` `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="7c27b-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="7c27b-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="7c27b-109">array : 'T[]</span></span>

<span data-ttu-id="7c27b-110">정렬할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7c27b-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="7c27b-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="7c27b-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7c27b-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c27b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7c27b-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="7c27b-113">'T</span></span>

<span data-ttu-id="7c27b-114">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="7c27b-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="7c27b-115">예</span><span class="sxs-lookup"><span data-stu-id="7c27b-115">Example</span></span>

<span data-ttu-id="7c27b-116">다음 코드 조각은 오름차순으로 발생 하는 정수 배열을 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27b-116">The following snippet sorts an array of integers to occur in ascending order:</span></span>

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a><span data-ttu-id="7c27b-117">설명</span><span class="sxs-lookup"><span data-stu-id="7c27b-117">Remarks</span></span>

<span data-ttu-id="7c27b-118">함수는 `comparison` 전이적으로 간주 됩니다. 예를 들어 및 인 경우에는를로 `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27b-118">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="7c27b-119">이 속성이 없으면이 함수의 출력이 올바르지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27b-119">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="7c27b-120">이는 함수 이기 때문에 두 요소가 같은 것으로 간주 되는 경우에도 결과는 완전히 결정적 `comparison` . 즉, `comparison(a, b)` 와 `comparison(b, a)` 가 둘 다 `true` 인 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="7c27b-120">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="7c27b-121">특히이 함수에서 수행 하는 정렬의 안정성은 안정적인 것으로 간주 되므로 및 내에서 두 개의 요소가 및에서 동일한 순서로 발생 하는 경우에는 `a` `b` `array` `comparison` `a` 출력의 앞에도 표시 됩니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="7c27b-121">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="7c27b-122">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="7c27b-122">For example:</span></span>

```qsharp
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```