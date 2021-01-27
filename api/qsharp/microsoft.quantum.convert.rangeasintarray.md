---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: RangeAsIntArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: 8c6b83d78e3b22ea1a17a48de66592950bf905a3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850095"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="c4b08-102">RangeAsIntArray 함수</span><span class="sxs-lookup"><span data-stu-id="c4b08-102">RangeAsIntArray function</span></span>

<span data-ttu-id="c4b08-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="c4b08-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="c4b08-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c4b08-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c4b08-105">`arr`Start .로 열거 된 정수 배열을 만듭니다. 단계. 종단.</span><span class="sxs-lookup"><span data-stu-id="c4b08-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="c4b08-106">입력</span><span class="sxs-lookup"><span data-stu-id="c4b08-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="c4b08-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="c4b08-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="c4b08-108">`Range`배열로 변환할 값의입니다 `start..step..end` .</span><span class="sxs-lookup"><span data-stu-id="c4b08-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="c4b08-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c4b08-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c4b08-110">에 의해 반복 되는 값에 해당 하는 정수의 새 배열입니다 `range` .</span><span class="sxs-lookup"><span data-stu-id="c4b08-110">A new array of integers corresponding to values iterated over by `range`.</span></span>

## <a name="example"></a><span data-ttu-id="c4b08-111">예제</span><span class="sxs-lookup"><span data-stu-id="c4b08-111">Example</span></span>

```qsharp
// The following returns [1,3,5,7];
let array = RangeAsIntArray(1..2..8);
```