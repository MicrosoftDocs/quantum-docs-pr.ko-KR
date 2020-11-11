---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: ResultArrayAsBoolArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 0356fe9c98306ee3e1857f4af311aef9b3789a7d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713357"
---
# <a name="resultarrayasboolarray-function"></a><span data-ttu-id="c386d-102">ResultArrayAsBoolArray 함수</span><span class="sxs-lookup"><span data-stu-id="c386d-102">ResultArrayAsBoolArray function</span></span>

<span data-ttu-id="c386d-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="c386d-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="c386d-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c386d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c386d-105">`Result[]`형식을 형식으로 변환 `Bool[]` `One` 합니다. 여기서은로 매핑되고는 `true` `Zero` 에 매핑됩니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="c386d-105">Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.</span></span>

```qsharp
function ResultArrayAsBoolArray (input : Result[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="c386d-106">입력</span><span class="sxs-lookup"><span data-stu-id="c386d-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="c386d-107">입력: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="c386d-107">input : __invalid<Result>__ []</span></span>

<span data-ttu-id="c386d-108">`Result[]` 변환 될입니다.</span><span class="sxs-lookup"><span data-stu-id="c386d-108">`Result[]` to be converted.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c386d-109">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c386d-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c386d-110">`input`를 나타내는 `Bool[]`입니다.</span><span class="sxs-lookup"><span data-stu-id="c386d-110">A `Bool[]` representing the `input`.</span></span>