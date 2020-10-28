---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: MappedOverRange 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719041"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="f03ac-102">MappedOverRange 함수</span><span class="sxs-lookup"><span data-stu-id="f03ac-102">MappedOverRange function</span></span>

<span data-ttu-id="f03ac-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f03ac-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f03ac-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f03ac-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f03ac-105">정수를 입력으로 사용 하는 범위와 함수가 지정 된 경우 함수 아래 범위 값의 이미지로 구성 된 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f03ac-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f03ac-106">입력</span><span class="sxs-lookup"><span data-stu-id="f03ac-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="f03ac-107">매퍼: [Int](xref:microsoft.quantum.lang-ref.int) -> ' t</span><span class="sxs-lookup"><span data-stu-id="f03ac-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="f03ac-108">범위 값을 매핑하는 데 사용 되는의 함수입니다 `Int` `'T` .</span><span class="sxs-lookup"><span data-stu-id="f03ac-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="f03ac-109">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="f03ac-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="f03ac-110">정수 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f03ac-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="f03ac-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="f03ac-111">Output : 'T[]</span></span>

<span data-ttu-id="f03ac-112">`'T[]`함수로 매핑되는 요소의 배열입니다 `mapper` .</span><span class="sxs-lookup"><span data-stu-id="f03ac-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f03ac-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f03ac-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f03ac-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f03ac-114">'T</span></span>

<span data-ttu-id="f03ac-115">함수의 결과 형식 `mapper` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f03ac-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f03ac-116">설명</span><span class="sxs-lookup"><span data-stu-id="f03ac-116">Remarks</span></span>

<span data-ttu-id="f03ac-117">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 함수가 있을 때마다 `mapper: Int -> 'T` 범위의 값을 매핑하고 형식의 배열을 생성할 수 있습니다 `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="f03ac-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="f03ac-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f03ac-118">See Also</span></span>

- [<span data-ttu-id="f03ac-119">Microsoft 양자. 배열 매핑</span><span class="sxs-lookup"><span data-stu-id="f03ac-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)