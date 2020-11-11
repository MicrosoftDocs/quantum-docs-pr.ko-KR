---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: MappedByIndex 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 07ca523248c363f2229551a14e77803dc4f4f82e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719053"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="ac6c7-102">MappedByIndex 함수</span><span class="sxs-lookup"><span data-stu-id="ac6c7-102">MappedByIndex function</span></span>

<span data-ttu-id="ac6c7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ac6c7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ac6c7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ac6c7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ac6c7-105">배열의 인덱싱된 요소에 대해 정의 된 배열과 함수가 지정 된 경우 함수에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac6c7-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="ac6c7-106">입력</span><span class="sxs-lookup"><span data-stu-id="ac6c7-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="ac6c7-107">매퍼: ([Int](xref:microsoft.quantum.lang-ref.int), ' t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="ac6c7-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="ac6c7-108">`(Int, 'T)` `'U` 요소와 해당 인덱스를 매핑하는 데 사용 되는의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="ac6c7-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="ac6c7-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="ac6c7-109">array : 'T[]</span></span>

<span data-ttu-id="ac6c7-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ac6c7-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="ac6c7-111">출력: ' U []</span><span class="sxs-lookup"><span data-stu-id="ac6c7-111">Output : 'U[]</span></span>

<span data-ttu-id="ac6c7-112">`'U[]`함수로 매핑되는 요소의 배열입니다 `mapper` .</span><span class="sxs-lookup"><span data-stu-id="ac6c7-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ac6c7-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac6c7-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ac6c7-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="ac6c7-114">'T</span></span>

<span data-ttu-id="ac6c7-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ac6c7-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="ac6c7-116">' U</span><span class="sxs-lookup"><span data-stu-id="ac6c7-116">'U</span></span>

<span data-ttu-id="ac6c7-117">함수의 결과 형식 `mapper` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ac6c7-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac6c7-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ac6c7-118">See Also</span></span>

- [<span data-ttu-id="ac6c7-119">Microsoft 양자. 배열 매핑</span><span class="sxs-lookup"><span data-stu-id="ac6c7-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)