---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: RectangularArrayFact 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: 8cf6b85da6e8fee7fc255a173753a6468d8134b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845497"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="1ae03-102">RectangularArrayFact 함수</span><span class="sxs-lookup"><span data-stu-id="1ae03-102">RectangularArrayFact function</span></span>

<span data-ttu-id="1ae03-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1ae03-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1ae03-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1ae03-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1ae03-105">2 차원 배열에 사각형 모양이 있는 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ae03-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="1ae03-106">설명</span><span class="sxs-lookup"><span data-stu-id="1ae03-106">Description</span></span>

<span data-ttu-id="1ae03-107">이 함수는 배열의 각 행 길이가 동일 함을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae03-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="1ae03-108">입력</span><span class="sxs-lookup"><span data-stu-id="1ae03-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="1ae03-109">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="1ae03-109">array : 'T[][]</span></span>

<span data-ttu-id="1ae03-110">요소의 2 차원 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae03-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="1ae03-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="1ae03-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="1ae03-112">배열이 사각형 배열이 아닌 경우 인쇄 될 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae03-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="1ae03-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1ae03-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1ae03-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ae03-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1ae03-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="1ae03-115">'T</span></span>

<span data-ttu-id="1ae03-116">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="1ae03-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="1ae03-117">예제</span><span class="sxs-lookup"><span data-stu-id="1ae03-117">Example</span></span>

```qsharp
RectangularArrayFact([[1, 2], [3, 4]], "Array is not rectangular");       // okay
RectangularArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not rectangular"); // okay
RectangularArrayFact([[1, 2], [3, 4, 5]], "Array is not rectangular");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="1ae03-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1ae03-118">See Also</span></span>

- [<span data-ttu-id="1ae03-119">SquareArrayFact.</span><span class="sxs-lookup"><span data-stu-id="1ae03-119">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)