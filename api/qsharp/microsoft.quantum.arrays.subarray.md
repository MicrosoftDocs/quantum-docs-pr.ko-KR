---
uid: Microsoft.Quantum.Arrays.Subarray
title: 하위 배열 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: cf72f04421b277ce64354d1eccec11cbc61d78cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220164"
---
# <a name="subarray-function"></a><span data-ttu-id="326e1-102">하위 배열 함수</span><span class="sxs-lookup"><span data-stu-id="326e1-102">Subarray function</span></span>

<span data-ttu-id="326e1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="326e1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="326e1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="326e1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="326e1-105">배열 및 위치 목록을 가져오고, 지정 된 위치와 일치 하는 원래 배열의 요소에서 형성 된 새 배열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-105">Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.</span></span>

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="326e1-106">입력</span><span class="sxs-lookup"><span data-stu-id="326e1-106">Input</span></span>

### <a name="indices--int"></a><span data-ttu-id="326e1-107">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="326e1-107">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="326e1-108">하위 배열을 정의 하는 데 사용 되는 정수 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-108">A list of integers that is used to define the subarray.</span></span>


### <a name="array--t"></a><span data-ttu-id="326e1-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="326e1-109">array : 'T[]</span></span>

<span data-ttu-id="326e1-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="326e1-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="326e1-111">Output : 'T[]</span></span>

<span data-ttu-id="326e1-112">`out`해당 인덱스가 하위 배열에 해당 하는 요소의 배열입니다 `out[idx] == array[indices[idx]]` .</span><span class="sxs-lookup"><span data-stu-id="326e1-112">An array `out` of elements whose indices correspond to the subarray, such that `out[idx] == array[indices[idx]]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="326e1-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="326e1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="326e1-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="326e1-114">'T</span></span>

<span data-ttu-id="326e1-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="326e1-116">설명</span><span class="sxs-lookup"><span data-stu-id="326e1-116">Remarks</span></span>

<span data-ttu-id="326e1-117">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 하위 배열을 정의 하는 `'T[]` 위치 목록이 있을 때마다입니다. `Int[]`</span><span class="sxs-lookup"><span data-stu-id="326e1-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a list of locations `Int[]` defining the subarray.</span></span>
<span data-ttu-id="326e1-118">하위 배열의 구성은 참조를 유지 관리 하는 대신 지정 된 배열의 새 전체 복사본을 생성 하는 것을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-118">The construction of the subarray is a based on generating a new, deep copy of the given array as opposed to maintaining references.</span></span>

<span data-ttu-id="326e1-119">인 경우 `Length(indices) < Length(array)` 이 함수는의 하위 집합을 반환 `array` 합니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-119">If `Length(indices) < Length(array)`, this function will return a subset of `array`.</span></span> <span data-ttu-id="326e1-120">반면에 반복 되는 요소가 포함 된 경우에는 `indices` 의 해당 요소도 `array` 반복 됩니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-120">On the other hand, if `indices` contains repeated elements, the corresponding elements of `array` will likewise be repeated.</span></span>
<span data-ttu-id="326e1-121">`indices`및 `array` 의 길이가 같은 경우이 함수는의 순열을 제공 `array` 합니다.</span><span class="sxs-lookup"><span data-stu-id="326e1-121">If `indices` and `array` are the same length, this function provides permutations of `array`.</span></span>