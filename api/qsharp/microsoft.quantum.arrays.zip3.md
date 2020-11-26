---
uid: Microsoft.Quantum.Arrays.Zip3
title: List.zip3 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: a6e7519755c4d473f6ba255ac5f877b2a3894d71
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219824"
---
# <a name="zip3-function"></a><span data-ttu-id="ad270-102">List.zip3 함수</span><span class="sxs-lookup"><span data-stu-id="ad270-102">Zip3 function</span></span>

<span data-ttu-id="ad270-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ad270-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ad270-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad270-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="ad270-105">List.zip3는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="ad270-106">대신 <xref:Microsoft.Quantum.Arrays.Zipped3>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="ad270-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="ad270-107">3 개의 배열이 지정 된 경우 각 3 튜플은 각 원래 배열의 요소를 포함 하도록 3 튜플의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="ad270-108">입력</span><span class="sxs-lookup"><span data-stu-id="ad270-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="ad270-109">first: ' t 1 []</span><span class="sxs-lookup"><span data-stu-id="ad270-109">first : 'T1[]</span></span>

<span data-ttu-id="ad270-110">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="ad270-111">second: ' 2 []</span><span class="sxs-lookup"><span data-stu-id="ad270-111">second : 'T2[]</span></span>

<span data-ttu-id="ad270-112">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="ad270-113">세 번째: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="ad270-113">third : 'T3[]</span></span>

<span data-ttu-id="ad270-114">각 튜플의 세 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="ad270-115">출력: (' 0 ', ' 2 ', ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="ad270-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="ad270-116">각각에 대 한 폼의 3 개 튜플을 포함 하는 배열 `(first[idx], second[idx], third[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="ad270-117">세 배열의 길이가 같지 않은 경우 출력은 입력 중 짧은 값 만큼 길어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ad270-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ad270-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="ad270-119">' 1 '</span><span class="sxs-lookup"><span data-stu-id="ad270-119">'T1</span></span>

<span data-ttu-id="ad270-120">첫 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="ad270-121">' 2 '</span><span class="sxs-lookup"><span data-stu-id="ad270-121">'T2</span></span>

<span data-ttu-id="ad270-122">두 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="ad270-123">' T 3</span><span class="sxs-lookup"><span data-stu-id="ad270-123">'T3</span></span>

<span data-ttu-id="ad270-124">세 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ad270-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad270-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ad270-125">See Also</span></span>

- [<span data-ttu-id="ad270-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="ad270-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="ad270-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="ad270-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)