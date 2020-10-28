---
uid: Microsoft.Quantum.Arrays.Mapped
title: Mapped 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 1abb9d6fb1a921b49554bef968442f4f2b346b71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719077"
---
# <a name="mapped-function"></a><span data-ttu-id="285fd-102">Mapped 함수</span><span class="sxs-lookup"><span data-stu-id="285fd-102">Mapped function</span></span>

<span data-ttu-id="285fd-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="285fd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="285fd-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="285fd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="285fd-105">배열의 요소에 대해 정의 된 배열과 함수가 지정 된 경우 함수에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="285fd-105">Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="285fd-106">입력</span><span class="sxs-lookup"><span data-stu-id="285fd-106">Input</span></span>

### <a name="mapper--t---u"></a><span data-ttu-id="285fd-107">매퍼: ' t > ' U</span><span class="sxs-lookup"><span data-stu-id="285fd-107">mapper : 'T -> 'U</span></span>

<span data-ttu-id="285fd-108">요소를 매핑하는 데 사용 되는의 함수입니다 `'T` `'U` .</span><span class="sxs-lookup"><span data-stu-id="285fd-108">A function from `'T` to `'U` that is used to map elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="285fd-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="285fd-109">array : 'T[]</span></span>

<span data-ttu-id="285fd-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="285fd-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="285fd-111">출력: ' U []</span><span class="sxs-lookup"><span data-stu-id="285fd-111">Output : 'U[]</span></span>

<span data-ttu-id="285fd-112">`'U[]`함수로 매핑되는 요소의 배열입니다 `mapper` .</span><span class="sxs-lookup"><span data-stu-id="285fd-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="285fd-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="285fd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="285fd-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="285fd-114">'T</span></span>

<span data-ttu-id="285fd-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="285fd-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="285fd-116">' U</span><span class="sxs-lookup"><span data-stu-id="285fd-116">'U</span></span>

<span data-ttu-id="285fd-117">함수의 결과 형식 `mapper` 입니다.</span><span class="sxs-lookup"><span data-stu-id="285fd-117">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="285fd-118">설명</span><span class="sxs-lookup"><span data-stu-id="285fd-118">Remarks</span></span>

<span data-ttu-id="285fd-119">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 함수가 있을 때마다 `'T[]` `mapper: 'T -> 'U` 배열의 요소를 매핑하고 형식의 새 배열을 생성할 수 있습니다 `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="285fd-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `mapper: 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>