---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: IsPermutation 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220929"
---
# <a name="ispermutation-function"></a><span data-ttu-id="1453a-102">IsPermutation 함수</span><span class="sxs-lookup"><span data-stu-id="1453a-102">IsPermutation function</span></span>

<span data-ttu-id="1453a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1453a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1453a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1453a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1453a-105">지정 된 배열이 순열을 나타내는 경우에만 true를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1453a-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="1453a-106">Description</span><span class="sxs-lookup"><span data-stu-id="1453a-106">Description</span></span>

<span data-ttu-id="1453a-107">길이가 인 배열이 지정 된 경우에는의 `array` `n` 각 정수가에서 정확히 한 번 표시 되는 경우에만 true를 반환 합니다 `0` `n - 1` . 예를 들어 `array` `array` 요소에 대 한 순열으로 해석 될 수 있습니다 `n` .</span><span class="sxs-lookup"><span data-stu-id="1453a-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="1453a-108">입력</span><span class="sxs-lookup"><span data-stu-id="1453a-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="1453a-109">permuation: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1453a-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1453a-110">순열을 나타낼 수 있거나 나타내지 않을 수 있는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1453a-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1453a-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1453a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="1453a-112">설명</span><span class="sxs-lookup"><span data-stu-id="1453a-112">Remarks</span></span>

<span data-ttu-id="1453a-113">길이가 0 인 배열은 순열 일반적으로 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1453a-113">An array of length zero is trivially a permutation.</span></span>