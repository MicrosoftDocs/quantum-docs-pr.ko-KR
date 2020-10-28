---
uid: Microsoft.Quantum.Arrays.ForEach
title: ForEach 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719204"
---
# <a name="foreach-operation"></a><span data-ttu-id="7c599-102">ForEach 작업</span><span class="sxs-lookup"><span data-stu-id="7c599-102">ForEach operation</span></span>

<span data-ttu-id="7c599-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7c599-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7c599-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c599-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c599-105">배열의 요소에 대해 정의 된 배열과 작업이 지정 된 경우 작업에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c599-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="7c599-106">입력</span><span class="sxs-lookup"><span data-stu-id="7c599-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="7c599-107">작업: ' t => ' U</span><span class="sxs-lookup"><span data-stu-id="7c599-107">action : 'T => 'U</span></span> 

<span data-ttu-id="7c599-108">`'T` `'U` 각 요소에 적용 되는에서로의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7c599-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="7c599-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="7c599-109">array : 'T[]</span></span>

<span data-ttu-id="7c599-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="7c599-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="7c599-111">출력: ' U []</span><span class="sxs-lookup"><span data-stu-id="7c599-111">Output : 'U[]</span></span>

<span data-ttu-id="7c599-112">`'U[]`작업에 의해 매핑되는 요소의 배열입니다 `action` .</span><span class="sxs-lookup"><span data-stu-id="7c599-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7c599-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c599-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7c599-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="7c599-114">'T</span></span>

<span data-ttu-id="7c599-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7c599-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="7c599-116">' U</span><span class="sxs-lookup"><span data-stu-id="7c599-116">'U</span></span>

<span data-ttu-id="7c599-117">작업의 결과 형식 `action` 입니다.</span><span class="sxs-lookup"><span data-stu-id="7c599-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c599-118">설명</span><span class="sxs-lookup"><span data-stu-id="7c599-118">Remarks</span></span>

<span data-ttu-id="7c599-119">작업은 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 작업이 있을 때마다 `'T[]` `action : 'T -> 'U` 배열의 요소를 매핑하고 형식의 새 배열을 생성할 수 있습니다 `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="7c599-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>