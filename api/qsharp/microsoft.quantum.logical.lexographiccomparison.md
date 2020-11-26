---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: LexographicComparison 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: 4d8596c52b0fc8082a2b766d95d4052a4964b8b9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197587"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="d6f08-102">LexographicComparison 함수</span><span class="sxs-lookup"><span data-stu-id="d6f08-102">LexographicComparison function</span></span>

<span data-ttu-id="d6f08-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d6f08-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d6f08-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6f08-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6f08-105">비교 함수가 지정 된 경우 lexographically는 두 배열을 비교 하는 새 함수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="d6f08-106">입력</span><span class="sxs-lookup"><span data-stu-id="d6f08-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="d6f08-107">elementComparison: (' ' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d6f08-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d6f08-108">두 요소를 비교 하 고 `x` `y` `x` 가 보다 작거나 같은 경우을 반환 하는 함수입니다 `y` .</span><span class="sxs-lookup"><span data-stu-id="d6f08-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="d6f08-109">Output: (' ' ' ' ' t [])-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d6f08-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d6f08-110">두 배열을 비교 하 고 `xs` `ys` `xs` lexographical 정렬에서 이전 또는 같은 경우을 반환 하는 함수입니다 `ys` .</span><span class="sxs-lookup"><span data-stu-id="d6f08-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d6f08-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6f08-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d6f08-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="d6f08-112">'T</span></span>

<span data-ttu-id="d6f08-113">비교할 배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f08-114">설명</span><span class="sxs-lookup"><span data-stu-id="d6f08-114">Remarks</span></span>

<span data-ttu-id="d6f08-115">두 배열과 lexographic 비교는 `xs` `ys` 다음 절차에 따라 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="d6f08-116">`x` `y` `elementComparison(x, y)` 및가 모두 true 인 경우 두 개의 요소 및가 동일 하다는 것을 알 수 `elementComparison(y, x)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="d6f08-117">두 배열 모두 동일 하지 않은 요소의 첫 번째 쌍까지 요소 별로 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="d6f08-118">에 따라 먼저 발생 하는 요소를 포함 하는 배열을 `elementComparison` 먼저 lexographical 정렬에서 발생 한다고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="d6f08-119">Inequivalent 요소가 없고 한 배열이 다른 배열 보다 길면 짧은 배열이 먼저 발생 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f08-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6f08-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d6f08-120">See Also</span></span>

- [<span data-ttu-id="d6f08-121">Microsoft 양자 배열 정렬</span><span class="sxs-lookup"><span data-stu-id="d6f08-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)