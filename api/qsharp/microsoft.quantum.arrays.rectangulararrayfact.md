---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: RectangularArrayFact 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: f0d3f4d6bfa9e86f1c7a91792c09e16fe86433a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718921"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="07228-102">RectangularArrayFact 함수</span><span class="sxs-lookup"><span data-stu-id="07228-102">RectangularArrayFact function</span></span>

<span data-ttu-id="07228-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="07228-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="07228-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="07228-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="07228-105">2 차원 배열에 사각형 모양이 있는 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07228-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="07228-106">Description</span><span class="sxs-lookup"><span data-stu-id="07228-106">Description</span></span>

<span data-ttu-id="07228-107">이 함수는 배열의 각 행 길이가 동일 함을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="07228-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="07228-108">입력</span><span class="sxs-lookup"><span data-stu-id="07228-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="07228-109">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="07228-109">array : 'T[][]</span></span>

<span data-ttu-id="07228-110">요소의 2 차원 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="07228-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="07228-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="07228-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="07228-112">배열이 사각형 배열이 아닌 경우 인쇄 될 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="07228-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="07228-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="07228-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="07228-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="07228-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="07228-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="07228-115">'T</span></span>

<span data-ttu-id="07228-116">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="07228-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="07228-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="07228-117">See Also</span></span>

- [<span data-ttu-id="07228-118">SquareArrayFact.</span><span class="sxs-lookup"><span data-stu-id="07228-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)