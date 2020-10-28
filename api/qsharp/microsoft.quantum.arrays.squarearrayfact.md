---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: SquareArrayFact 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718856"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="e7182-102">SquareArrayFact 함수</span><span class="sxs-lookup"><span data-stu-id="e7182-102">SquareArrayFact function</span></span>

<span data-ttu-id="e7182-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e7182-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e7182-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e7182-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e7182-105">2 차원 배열에 사각형 모양의 조건을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7182-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="e7182-106">Description</span><span class="sxs-lookup"><span data-stu-id="e7182-106">Description</span></span>

<span data-ttu-id="e7182-107">이 함수는 배열의 각 행에 배열에 있는 행 (요소) 만큼의 요소가 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7182-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="e7182-108">입력</span><span class="sxs-lookup"><span data-stu-id="e7182-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="e7182-109">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="e7182-109">array : 'T[][]</span></span>

<span data-ttu-id="e7182-110">요소의 2 차원 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e7182-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="e7182-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e7182-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e7182-112">배열이 정사각형 배열이 아닌 경우 인쇄 될 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="e7182-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="e7182-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e7182-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e7182-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7182-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e7182-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="e7182-115">'T</span></span>

<span data-ttu-id="e7182-116">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="e7182-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7182-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e7182-117">See Also</span></span>

- [<span data-ttu-id="e7182-118">RectangularArrayFact.</span><span class="sxs-lookup"><span data-stu-id="e7182-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)