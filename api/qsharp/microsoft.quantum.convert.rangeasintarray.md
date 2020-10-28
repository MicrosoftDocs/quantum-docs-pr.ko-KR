---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: RangeAsIntArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713364"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="05e52-102">RangeAsIntArray 함수</span><span class="sxs-lookup"><span data-stu-id="05e52-102">RangeAsIntArray function</span></span>

<span data-ttu-id="05e52-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="05e52-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="05e52-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="05e52-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="05e52-105">`arr`Start .로 열거 된 정수 배열을 만듭니다. 단계. 종단.</span><span class="sxs-lookup"><span data-stu-id="05e52-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="05e52-106">입력</span><span class="sxs-lookup"><span data-stu-id="05e52-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="05e52-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="05e52-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="05e52-108">`Range`배열로 변환할 값의입니다 `start..step..end` .</span><span class="sxs-lookup"><span data-stu-id="05e52-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="05e52-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="05e52-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="05e52-110">에 의해 반복 되는 값에 해당 하는 정수의 새 배열입니다 `range` .</span><span class="sxs-lookup"><span data-stu-id="05e52-110">A new array of integers corresponding to values iterated over by `range`.</span></span>