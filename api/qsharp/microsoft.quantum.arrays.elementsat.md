---
uid: Microsoft.Quantum.Arrays.ElementsAt
title: ElementsAt 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementsAt
qsharp.summary: Returns the array's elements at a given range of indices.
ms.openlocfilehash: 295aa4e2d79857405186b835d9788f59db83d1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842786"
---
# <a name="elementsat-function"></a><span data-ttu-id="c324e-102">ElementsAt 함수</span><span class="sxs-lookup"><span data-stu-id="c324e-102">ElementsAt function</span></span>

<span data-ttu-id="c324e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c324e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c324e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c324e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c324e-105">지정 된 인덱스 범위에서 배열의 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c324e-105">Returns the array's elements at a given range of indices.</span></span>

```qsharp
function ElementsAt<'T> (range : Range, array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="c324e-106">입력</span><span class="sxs-lookup"><span data-stu-id="c324e-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="c324e-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="c324e-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="c324e-108">배열 인덱스의 범위</span><span class="sxs-lookup"><span data-stu-id="c324e-108">Range of array indexes</span></span>


### <a name="array--t"></a><span data-ttu-id="c324e-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="c324e-109">array : 'T[]</span></span>

<span data-ttu-id="c324e-110">Array</span><span class="sxs-lookup"><span data-stu-id="c324e-110">Array</span></span>



## <a name="output--t"></a><span data-ttu-id="c324e-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="c324e-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c324e-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c324e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c324e-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="c324e-113">'T</span></span>

<span data-ttu-id="c324e-114">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="c324e-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="c324e-115">예</span><span class="sxs-lookup"><span data-stu-id="c324e-115">Example</span></span>

<span data-ttu-id="c324e-116">유명한 정수 시퀀스에서 홀수 인덱스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c324e-116">Get the odd indexes in famous integer sequences.</span></span> <span data-ttu-id="c324e-117">0 인덱스는 시퀀스의 _첫 번째_ 값에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c324e-117">(note that the 0 index corresponds to the _first_ value of the sequence.)</span></span>

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famousOdd = Mapped(ElementsAt<Int>(0..2..9, _), [lucas, prime, fibonacci, catalan]);
// same as: famousOdd = [[2, 3, 7, 18, 47], [2, 5, 11, 17, 23], [0, 1, 3, 8, 21], [1, 2, 14, 132, 1430]]
```

## <a name="see-also"></a><span data-ttu-id="c324e-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c324e-118">See Also</span></span>

- [<span data-ttu-id="c324e-119">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="c324e-119">Microsoft.Quantum.Arrays.ElementAt</span></span>](xref:Microsoft.Quantum.Arrays.ElementAt)
- [<span data-ttu-id="c324e-120">Microsoft 양자 함수</span><span class="sxs-lookup"><span data-stu-id="c324e-120">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)