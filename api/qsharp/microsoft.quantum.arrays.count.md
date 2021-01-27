---
uid: Microsoft.Quantum.Arrays.Count
title: Count 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: e178ee63526e3485e8cc83a3ba8f827d8ecac552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842846"
---
# <a name="count-function"></a><span data-ttu-id="1718a-102">Count 함수</span><span class="sxs-lookup"><span data-stu-id="1718a-102">Count function</span></span>

<span data-ttu-id="1718a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1718a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1718a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1718a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1718a-105">배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우 조건자를 충족 하는 요소로 구성 된 배열의 요소 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1718a-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="1718a-106">입력</span><span class="sxs-lookup"><span data-stu-id="1718a-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="1718a-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1718a-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1718a-108">에서 요소를 `'T` 필터링 하는 데 사용 되는 부울로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="1718a-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="1718a-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="1718a-109">array : 'T[]</span></span>

<span data-ttu-id="1718a-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1718a-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="1718a-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1718a-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1718a-112">조건자를 만족 하는의 요소 수입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="1718a-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1718a-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1718a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1718a-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="1718a-114">'T</span></span>

<span data-ttu-id="1718a-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1718a-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="1718a-116">예</span><span class="sxs-lookup"><span data-stu-id="1718a-116">Example</span></span>

<span data-ttu-id="1718a-117">다음 코드에서는 "Count" 함수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1718a-117">The following code demonstrates the "Count" function.</span></span>
<span data-ttu-id="1718a-118">조건자는 함수를 사용 하 여 정의 됩니다 @"microsoft.quantum.logical.greaterthani" .</span><span class="sxs-lookup"><span data-stu-id="1718a-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
 let predicate = GreaterThanI(_, 5);
 let count = Count(predicate, [2, 5, 9, 1, 8]);
 // count = 2
```

## <a name="remarks"></a><span data-ttu-id="1718a-119">설명</span><span class="sxs-lookup"><span data-stu-id="1718a-119">Remarks</span></span>

<span data-ttu-id="1718a-120">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열과 조건자가 있을 때마다 `'T[]` `'T -> Bool` 요소를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1718a-120">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>