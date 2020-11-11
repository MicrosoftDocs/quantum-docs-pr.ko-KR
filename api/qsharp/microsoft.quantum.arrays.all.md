---
uid: Microsoft.Quantum.Arrays.All
title: All 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 345c3fb92babd4ae2e54803b6c3b79b3313ef417
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719480"
---
# <a name="all-function"></a><span data-ttu-id="44f62-102">All 함수</span><span class="sxs-lookup"><span data-stu-id="44f62-102">All function</span></span>

<span data-ttu-id="44f62-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="44f62-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="44f62-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="44f62-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="44f62-105">배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우 및 배열의 모든 요소가 조건자를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="44f62-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="44f62-106">입력</span><span class="sxs-lookup"><span data-stu-id="44f62-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="44f62-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="44f62-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="44f62-108">에서 요소를 `'T` `Bool` 확인 하는 데 사용 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="44f62-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="44f62-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="44f62-109">array : 'T[]</span></span>

<span data-ttu-id="44f62-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="44f62-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="44f62-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="44f62-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="44f62-112">`Bool`모든 요소에 적용 되는 조건자의 AND 함수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="44f62-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="44f62-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="44f62-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="44f62-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="44f62-114">'T</span></span>

<span data-ttu-id="44f62-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="44f62-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f62-116">설명</span><span class="sxs-lookup"><span data-stu-id="44f62-116">Remarks</span></span>

<span data-ttu-id="44f62-117">함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 함수가 있을 때마다 `'T[]` `predicate: 'T -> Bool` `Bool` 모든 요소가 만족 하는지 여부를 나타내는 값을 생성할 수 있습니다 `predicate` .</span><span class="sxs-lookup"><span data-stu-id="44f62-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>