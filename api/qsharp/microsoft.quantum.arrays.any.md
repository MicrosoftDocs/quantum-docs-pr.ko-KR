---
uid: Microsoft.Quantum.Arrays.Any
title: 모든 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: a05f9531168bf2b32977665d38cc00f3c8e64879
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846274"
---
# <a name="any-function"></a><span data-ttu-id="62b77-102">모든 함수</span><span class="sxs-lookup"><span data-stu-id="62b77-102">Any function</span></span>

<span data-ttu-id="62b77-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="62b77-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="62b77-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="62b77-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="62b77-105">배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우는 배열의 요소 중 하나 이상이 조건자를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="62b77-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="62b77-106">입력</span><span class="sxs-lookup"><span data-stu-id="62b77-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="62b77-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="62b77-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="62b77-108">에서 요소를 `'T` `Bool` 확인 하는 데 사용 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="62b77-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="62b77-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="62b77-109">array : 'T[]</span></span>

<span data-ttu-id="62b77-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="62b77-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="62b77-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="62b77-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="62b77-112">`Bool`모든 요소에 적용 되는 조건자의 또는 함수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="62b77-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="62b77-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="62b77-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="62b77-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="62b77-114">'T</span></span>

<span data-ttu-id="62b77-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="62b77-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="62b77-116">예</span><span class="sxs-lookup"><span data-stu-id="62b77-116">Example</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function IsThreePresent() : Bool {
    let arrayOfInts = [1, 2, 3, 4, 5];
    let is3Present = IsNumberPresentInArray(3, arrayOfInts);
    return is3Present;
}

function IsNumberPresentInArray(n : Int, array : Int[]) : Bool {
    return Any(EqualI(_, n), array);
}
```

## <a name="remarks"></a><span data-ttu-id="62b77-117">설명</span><span class="sxs-lookup"><span data-stu-id="62b77-117">Remarks</span></span>

<span data-ttu-id="62b77-118">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 함수가 있을 때마다 `'T[]` `predicate: 'T -> Bool` `Bool` 일부 요소가 충족 되는지 여부를 나타내는 값을 생성할 수 있습니다 `predicate` .</span><span class="sxs-lookup"><span data-stu-id="62b77-118">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>