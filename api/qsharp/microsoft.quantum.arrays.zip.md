---
uid: Microsoft.Quantum.Arrays.Zip
title: Zip 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 8ed658003f749efd31b8d841cecbb0a23a471af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850894"
---
# <a name="zip-function"></a><span data-ttu-id="908c2-102">Zip 함수</span><span class="sxs-lookup"><span data-stu-id="908c2-102">Zip function</span></span>

<span data-ttu-id="908c2-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="908c2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="908c2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="908c2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="908c2-105">Zip은 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-105">Zip has been deprecated.</span></span> <span data-ttu-id="908c2-106">대신 <xref:Microsoft.Quantum.Arrays.Zipped>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="908c2-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="908c2-107">두 배열이 지정 된 경우 각 쌍은 각 원래 배열의 요소를 포함 하도록 쌍의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="908c2-108">입력</span><span class="sxs-lookup"><span data-stu-id="908c2-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="908c2-109">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="908c2-109">left : 'T[]</span></span>

<span data-ttu-id="908c2-110">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="908c2-111">right: ' U []</span><span class="sxs-lookup"><span data-stu-id="908c2-111">right : 'U[]</span></span>

<span data-ttu-id="908c2-112">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="908c2-113">출력: (' t ', ' U) []</span><span class="sxs-lookup"><span data-stu-id="908c2-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="908c2-114">각에 대 한 폼의 쌍을 포함 하는 배열 `(left[idx], right[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="908c2-115">두 배열의 길이가 같지 않은 경우에는 입력 중 짧은 값 만큼 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="908c2-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="908c2-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="908c2-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="908c2-117">'T</span></span>

<span data-ttu-id="908c2-118">왼쪽 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="908c2-119">' U</span><span class="sxs-lookup"><span data-stu-id="908c2-119">'U</span></span>

<span data-ttu-id="908c2-120">오른쪽 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="908c2-120">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="908c2-121">예제</span><span class="sxs-lookup"><span data-stu-id="908c2-121">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zip(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="908c2-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="908c2-122">See Also</span></span>

- [<span data-ttu-id="908c2-123">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="908c2-123">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="908c2-124">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="908c2-124">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="908c2-125">Microsoft 양자. 배열 압축 해제</span><span class="sxs-lookup"><span data-stu-id="908c2-125">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)