---
uid: Microsoft.Quantum.Arrays.Filtered
title: 필터링 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 4c786c69b0896b517f108611e32501867838aeb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719269"
---
# <a name="filtered-function"></a><span data-ttu-id="c355b-102">필터링 된 함수</span><span class="sxs-lookup"><span data-stu-id="c355b-102">Filtered function</span></span>

<span data-ttu-id="c355b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c355b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c355b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c355b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c355b-105">배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우 조건자를 충족 하는 요소로 구성 된 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c355b-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="c355b-106">입력</span><span class="sxs-lookup"><span data-stu-id="c355b-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="c355b-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c355b-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c355b-108">에서 요소를 `'T` 필터링 하는 데 사용 되는 부울로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="c355b-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="c355b-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="c355b-109">array : 'T[]</span></span>

<span data-ttu-id="c355b-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c355b-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="c355b-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="c355b-111">Output : 'T[]</span></span>

<span data-ttu-id="c355b-112">`'T[]`조건자를 만족 하는 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="c355b-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c355b-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c355b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c355b-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="c355b-114">'T</span></span>

<span data-ttu-id="c355b-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c355b-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="c355b-116">설명</span><span class="sxs-lookup"><span data-stu-id="c355b-116">Remarks</span></span>

<span data-ttu-id="c355b-117">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열과 조건자가 있을 때마다 `'T[]` `'T -> Bool` 요소를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c355b-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>