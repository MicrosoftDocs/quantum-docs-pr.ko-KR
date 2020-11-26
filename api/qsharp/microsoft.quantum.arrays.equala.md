---
uid: Microsoft.Quantum.Arrays.EqualA
title: EqualA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 176e15139a27d375fb047c07fa1ee778dc8cc2ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221371"
---
# <a name="equala-function"></a><span data-ttu-id="a64fa-102">EqualA 함수</span><span class="sxs-lookup"><span data-stu-id="a64fa-102">EqualA function</span></span>

<span data-ttu-id="a64fa-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a64fa-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a64fa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a64fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a64fa-105">동일한 형식의 두 배열과 배열의 요소 쌍에 대해 정의 된 조건자가 지정 된 경우 배열이 같은지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="a64fa-106">입력</span><span class="sxs-lookup"><span data-stu-id="a64fa-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="a64fa-107">같음: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a64fa-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a64fa-108">튜플의 `('T, 'T)` `Bool` 두 요소가 같은지 여부를 확인 하는 데 사용 되는 튜플의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="a64fa-109">: ' t []</span><span class="sxs-lookup"><span data-stu-id="a64fa-109">array1 : 'T[]</span></span>

<span data-ttu-id="a64fa-110">비교할 첫 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="a64fa-111">: ' t []</span><span class="sxs-lookup"><span data-stu-id="a64fa-111">array2 : 'T[]</span></span>

<span data-ttu-id="a64fa-112">비교할 두 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a64fa-113">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a64fa-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a64fa-114">와가 같으면 값이이 고, 그렇지 않으면 `true` `array1` `array2` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="a64fa-115">즉, 두 배열의 길이가 같고 모든 요소가에서 정의한 것과 같은 경우입니다 `equal` .</span><span class="sxs-lookup"><span data-stu-id="a64fa-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a64fa-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a64fa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a64fa-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="a64fa-117">'T</span></span>

<span data-ttu-id="a64fa-118">각 배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-118">The type of each array's elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="a64fa-119">설명</span><span class="sxs-lookup"><span data-stu-id="a64fa-119">Remarks</span></span>

<span data-ttu-id="a64fa-120">이 함수는 제네릭 형식에 대해 정의 됩니다. 즉, 두 개의 배열과 함수가 있을 때마다 `'T[]` `equal: ('T, 'T) -> Bool` 이 함수는 `Bool` 배열이 같은지 여부를 나타내는 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-120">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="a64fa-121">두 배열이 동일한 것으로 간주 되려면 길이가 같아야 하 고 배열의 같은 위치에 있는 요소가 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a64fa-121">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>