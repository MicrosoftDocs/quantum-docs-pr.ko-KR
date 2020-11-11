---
uid: Microsoft.Quantum.Arrays.Where
title: Where 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 1c9fa0463ed49788d12502257d735b965565d1ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718753"
---
# <a name="where-function"></a><span data-ttu-id="b7f0b-102">Where 함수</span><span class="sxs-lookup"><span data-stu-id="b7f0b-102">Where function</span></span>

<span data-ttu-id="b7f0b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b7f0b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b7f0b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b7f0b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b7f0b-105">조건자와 배열이 지정 된 경우 조건자가 true 인 배열의 인덱스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f0b-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="b7f0b-106">입력</span><span class="sxs-lookup"><span data-stu-id="b7f0b-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="b7f0b-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b7f0b-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b7f0b-108">에서 요소를 `'T` 필터링 하는 데 사용 되는 부울로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f0b-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="b7f0b-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="b7f0b-109">array : 'T[]</span></span>

<span data-ttu-id="b7f0b-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f0b-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="b7f0b-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b7f0b-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b7f0b-112">이 true 인 인덱스의 배열입니다 `predicate` .</span><span class="sxs-lookup"><span data-stu-id="b7f0b-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b7f0b-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7f0b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b7f0b-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="b7f0b-114">'T</span></span>

<span data-ttu-id="b7f0b-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f0b-115">The type of `array` elements.</span></span>