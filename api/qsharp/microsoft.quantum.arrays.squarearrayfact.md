---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: SquareArrayFact 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220198"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="1e06e-102">SquareArrayFact 함수</span><span class="sxs-lookup"><span data-stu-id="1e06e-102">SquareArrayFact function</span></span>

<span data-ttu-id="1e06e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1e06e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1e06e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1e06e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1e06e-105">2 차원 배열에 사각형 모양의 조건을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="1e06e-106">Description</span><span class="sxs-lookup"><span data-stu-id="1e06e-106">Description</span></span>

<span data-ttu-id="1e06e-107">이 함수는 배열의 각 행에 배열에 있는 행 (요소) 만큼의 요소가 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="1e06e-108">입력</span><span class="sxs-lookup"><span data-stu-id="1e06e-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="1e06e-109">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="1e06e-109">array : 'T[][]</span></span>

<span data-ttu-id="1e06e-110">요소의 2 차원 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="1e06e-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="1e06e-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="1e06e-112">배열이 정사각형 배열이 아닌 경우 인쇄 될 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="1e06e-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1e06e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1e06e-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1e06e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1e06e-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="1e06e-115">'T</span></span>

<span data-ttu-id="1e06e-116">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="1e06e-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e06e-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1e06e-117">See Also</span></span>

- [<span data-ttu-id="1e06e-118">RectangularArrayFact.</span><span class="sxs-lookup"><span data-stu-id="1e06e-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)