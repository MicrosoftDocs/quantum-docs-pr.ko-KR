---
uid: Microsoft.Quantum.Arrays.Zipped4
title: Zipped4 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: 413b415288170b4a6bffbb773e3277cdb47bdbbe
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718681"
---
# <a name="zipped4-function"></a><span data-ttu-id="ef2f4-102">Zipped4 함수</span><span class="sxs-lookup"><span data-stu-id="ef2f4-102">Zipped4 function</span></span>

<span data-ttu-id="ef2f4-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ef2f4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ef2f4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ef2f4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ef2f4-105">4 개의 배열이 지정 된 경우 각 4 튜플은 각 원래 배열의 요소를 포함 하도록 4 튜플의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-105">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="ef2f4-106">입력</span><span class="sxs-lookup"><span data-stu-id="ef2f4-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="ef2f4-107">first: ' t 1 []</span><span class="sxs-lookup"><span data-stu-id="ef2f4-107">first : 'T1[]</span></span>

<span data-ttu-id="ef2f4-108">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="ef2f4-109">second: ' 2 []</span><span class="sxs-lookup"><span data-stu-id="ef2f4-109">second : 'T2[]</span></span>

<span data-ttu-id="ef2f4-110">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="ef2f4-111">세 번째: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="ef2f4-111">third : 'T3[]</span></span>

<span data-ttu-id="ef2f4-112">각 튜플의 세 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-112">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="ef2f4-113">네 번째: ' t 4 []</span><span class="sxs-lookup"><span data-stu-id="ef2f4-113">fourth : 'T4[]</span></span>

<span data-ttu-id="ef2f4-114">각 튜플의 네 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-114">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="ef2f4-115">출력: (' 0 ', ' 2 ', ' 2 ', 4) []</span><span class="sxs-lookup"><span data-stu-id="ef2f4-115">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="ef2f4-116">각에 대 한 형식의 4 개 튜플을 포함 하는 배열 `(first[idx], second[idx], third[idx], fourth[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-116">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="ef2f4-117">네 배열의 길이가 같지 않은 경우 출력은 입력 중 짧은 값 만큼 길어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-117">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ef2f4-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef2f4-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="ef2f4-119">' 1 '</span><span class="sxs-lookup"><span data-stu-id="ef2f4-119">'T1</span></span>

<span data-ttu-id="ef2f4-120">첫 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="ef2f4-121">' 2 '</span><span class="sxs-lookup"><span data-stu-id="ef2f4-121">'T2</span></span>

<span data-ttu-id="ef2f4-122">두 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="ef2f4-123">' T 3</span><span class="sxs-lookup"><span data-stu-id="ef2f4-123">'T3</span></span>

<span data-ttu-id="ef2f4-124">세 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-124">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="ef2f4-125">' 4 '</span><span class="sxs-lookup"><span data-stu-id="ef2f4-125">'T4</span></span>

<span data-ttu-id="ef2f4-126">네 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f4-126">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef2f4-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ef2f4-127">See Also</span></span>

- [<span data-ttu-id="ef2f4-128">Microsoft.Quantum.Arrays.Zip예: ped</span><span class="sxs-lookup"><span data-stu-id="ef2f4-128">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="ef2f4-129">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="ef2f4-129">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)