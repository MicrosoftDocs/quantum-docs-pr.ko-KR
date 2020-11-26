---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: ResultArrayAsBoolArray 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: f3af3abd4ee58f495d4ea60ec4f21a2690abec1d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224227"
---
# <a name="resultarrayasboolarray-function"></a><span data-ttu-id="e739a-102">ResultArrayAsBoolArray 함수</span><span class="sxs-lookup"><span data-stu-id="e739a-102">ResultArrayAsBoolArray function</span></span>

<span data-ttu-id="e739a-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="e739a-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="e739a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e739a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e739a-105">`Result[]`형식을 형식으로 변환 `Bool[]` `One` 합니다. 여기서은로 매핑되고는 `true` `Zero` 에 매핑됩니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="e739a-105">Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.</span></span>

```qsharp
function ResultArrayAsBoolArray (input : Result[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="e739a-106">입력</span><span class="sxs-lookup"><span data-stu-id="e739a-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="e739a-107">입력: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="e739a-107">input : __invalid<Result>__[]</span></span>

<span data-ttu-id="e739a-108">`Result[]` 변환 될입니다.</span><span class="sxs-lookup"><span data-stu-id="e739a-108">`Result[]` to be converted.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e739a-109">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e739a-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e739a-110">`input`를 나타내는 `Bool[]`입니다.</span><span class="sxs-lookup"><span data-stu-id="e739a-110">A `Bool[]` representing the `input`.</span></span>