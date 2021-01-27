---
uid: Microsoft.Quantum.Arrays.IsSorted
title: IsSorted 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: a5916b5cbf36e1b6c421a81e04016a333e2b5be7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845729"
---
# <a name="issorted-function"></a><span data-ttu-id="37a69-102">IsSorted 함수</span><span class="sxs-lookup"><span data-stu-id="37a69-102">IsSorted function</span></span>

<span data-ttu-id="37a69-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="37a69-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="37a69-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37a69-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37a69-105">배열이 지정 된 경우 지정 된 비교 함수에 의해 정의 된 대로 배열이 정렬 되는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a69-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="37a69-106">입력</span><span class="sxs-lookup"><span data-stu-id="37a69-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="37a69-107">비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="37a69-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="37a69-108">`a`가 이면 보다 작거나 같은 두 요소를 비교 하는 함수입니다 `b` `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="37a69-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="37a69-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="37a69-109">array : 'T[]</span></span>

<span data-ttu-id="37a69-110">확인할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="37a69-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="37a69-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="37a69-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="37a69-112">`true` 각 요소 쌍에 대해 및이 순서 대로 발생 하는 경우에만 `a` `b` 가입니다 `array` `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="37a69-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="37a69-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37a69-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37a69-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="37a69-114">'T</span></span>

<span data-ttu-id="37a69-115">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="37a69-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a69-116">설명</span><span class="sxs-lookup"><span data-stu-id="37a69-116">Remarks</span></span>

<span data-ttu-id="37a69-117">함수는 `comparison` 전이적으로 간주 됩니다. 예를 들어 및 인 경우에는를로 `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a69-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="37a69-118">이 속성이 없으면이 함수의 출력이 올바르지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37a69-118">If this property does not hold, then the output of this function may be incorrect.</span></span>