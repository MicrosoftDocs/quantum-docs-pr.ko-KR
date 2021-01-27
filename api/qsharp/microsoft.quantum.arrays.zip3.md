---
uid: Microsoft.Quantum.Arrays.Zip3
title: List.zip3 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: b41b0789cdf90db534ee7a50ff25eb3a931ec683
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845363"
---
# <a name="zip3-function"></a><span data-ttu-id="7b02f-102">List.zip3 함수</span><span class="sxs-lookup"><span data-stu-id="7b02f-102">Zip3 function</span></span>

<span data-ttu-id="7b02f-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7b02f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7b02f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b02f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="7b02f-105">List.zip3는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="7b02f-106">대신 <xref:Microsoft.Quantum.Arrays.Zipped3>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="7b02f-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="7b02f-107">3 개의 배열이 지정 된 경우 각 3 튜플은 각 원래 배열의 요소를 포함 하도록 3 튜플의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="7b02f-108">입력</span><span class="sxs-lookup"><span data-stu-id="7b02f-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="7b02f-109">first: ' t 1 []</span><span class="sxs-lookup"><span data-stu-id="7b02f-109">first : 'T1[]</span></span>

<span data-ttu-id="7b02f-110">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="7b02f-111">second: ' 2 []</span><span class="sxs-lookup"><span data-stu-id="7b02f-111">second : 'T2[]</span></span>

<span data-ttu-id="7b02f-112">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="7b02f-113">세 번째: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="7b02f-113">third : 'T3[]</span></span>

<span data-ttu-id="7b02f-114">각 튜플의 세 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="7b02f-115">출력: (' 0 ', ' 2 ', ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="7b02f-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="7b02f-116">각각에 대 한 폼의 3 개 튜플을 포함 하는 배열 `(first[idx], second[idx], third[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="7b02f-117">세 배열의 길이가 같지 않은 경우 출력은 입력 중 짧은 값 만큼 길어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7b02f-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b02f-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="7b02f-119">' 1 '</span><span class="sxs-lookup"><span data-stu-id="7b02f-119">'T1</span></span>

<span data-ttu-id="7b02f-120">첫 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="7b02f-121">' 2 '</span><span class="sxs-lookup"><span data-stu-id="7b02f-121">'T2</span></span>

<span data-ttu-id="7b02f-122">두 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="7b02f-123">' T 3</span><span class="sxs-lookup"><span data-stu-id="7b02f-123">'T3</span></span>

<span data-ttu-id="7b02f-124">세 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7b02f-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b02f-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7b02f-125">See Also</span></span>

- [<span data-ttu-id="7b02f-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="7b02f-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="7b02f-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="7b02f-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)