---
uid: Microsoft.Quantum.Arrays.Filtered
title: 필터링 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 83336b7001ce1d8ab1f5340b194abdcf93588c31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847154"
---
# <a name="filtered-function"></a><span data-ttu-id="f89bd-102">필터링 된 함수</span><span class="sxs-lookup"><span data-stu-id="f89bd-102">Filtered function</span></span>

<span data-ttu-id="f89bd-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f89bd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f89bd-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f89bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f89bd-105">배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우 조건자를 충족 하는 요소로 구성 된 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f89bd-106">입력</span><span class="sxs-lookup"><span data-stu-id="f89bd-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="f89bd-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f89bd-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f89bd-108">에서 요소를 `'T` 필터링 하는 데 사용 되는 부울로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="f89bd-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="f89bd-109">array : 'T[]</span></span>

<span data-ttu-id="f89bd-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="f89bd-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="f89bd-111">Output : 'T[]</span></span>

<span data-ttu-id="f89bd-112">`'T[]`조건자를 만족 하는 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f89bd-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f89bd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f89bd-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f89bd-114">'T</span></span>

<span data-ttu-id="f89bd-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="f89bd-116">예</span><span class="sxs-lookup"><span data-stu-id="f89bd-116">Example</span></span>

<span data-ttu-id="f89bd-117">다음 코드에서는 "필터링 된" 함수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-117">The following code demonstrates the "Filtered" function.</span></span>
<span data-ttu-id="f89bd-118">조건자는 함수를 사용 하 여 정의 됩니다 @"microsoft.quantum.logical.greaterthani" .</span><span class="sxs-lookup"><span data-stu-id="f89bd-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function FilteredDemo() : Unit {
   let predicate = GreaterThanI(_, 5);
   let filteredArray = Filtered(predicate, [2, 5, 9, 1, 8]);
   Message($"{filteredArray}");
}
```

<span data-ttu-id="f89bd-119">이 예제에서 짐작할 수 있는 결과는 5 보다 큰 숫자의 배열이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-119">The outcome one should expect from this example will be an array of numbers greater than 5.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89bd-120">설명</span><span class="sxs-lookup"><span data-stu-id="f89bd-120">Remarks</span></span>

<span data-ttu-id="f89bd-121">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열과 조건자가 있을 때마다 `'T[]` `'T -> Bool` 요소를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f89bd-121">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>