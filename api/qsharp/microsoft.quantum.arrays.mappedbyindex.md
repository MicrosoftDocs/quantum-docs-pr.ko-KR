---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: MappedByIndex 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845660"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="d634b-102">MappedByIndex 함수</span><span class="sxs-lookup"><span data-stu-id="d634b-102">MappedByIndex function</span></span>

<span data-ttu-id="d634b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d634b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d634b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d634b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d634b-105">배열의 인덱싱된 요소에 대해 정의 된 배열과 함수가 지정 된 경우 함수에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d634b-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="d634b-106">입력</span><span class="sxs-lookup"><span data-stu-id="d634b-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="d634b-107">매퍼: ([Int](xref:microsoft.quantum.lang-ref.int), ' t)-> ' U</span><span class="sxs-lookup"><span data-stu-id="d634b-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="d634b-108">`(Int, 'T)` `'U` 요소와 해당 인덱스를 매핑하는 데 사용 되는의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="d634b-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="d634b-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="d634b-109">array : 'T[]</span></span>

<span data-ttu-id="d634b-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d634b-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="d634b-111">출력: ' U []</span><span class="sxs-lookup"><span data-stu-id="d634b-111">Output : 'U[]</span></span>

<span data-ttu-id="d634b-112">`'U[]`함수로 매핑되는 요소의 배열입니다 `mapper` .</span><span class="sxs-lookup"><span data-stu-id="d634b-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d634b-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d634b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d634b-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="d634b-114">'T</span></span>

<span data-ttu-id="d634b-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d634b-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="d634b-116">' U</span><span class="sxs-lookup"><span data-stu-id="d634b-116">'U</span></span>

<span data-ttu-id="d634b-117">함수의 결과 형식 `mapper` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d634b-117">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="d634b-118">예</span><span class="sxs-lookup"><span data-stu-id="d634b-118">Example</span></span>

<span data-ttu-id="d634b-119">다음 두 줄은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d634b-119">The following two lines are equivalent:</span></span>

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

<span data-ttu-id="d634b-120">및</span><span class="sxs-lookup"><span data-stu-id="d634b-120">and</span></span>

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a><span data-ttu-id="d634b-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d634b-121">See Also</span></span>

- [<span data-ttu-id="d634b-122">Microsoft 양자. 배열 매핑</span><span class="sxs-lookup"><span data-stu-id="d634b-122">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)