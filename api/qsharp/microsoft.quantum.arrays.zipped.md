---
uid: Microsoft.Quantum.Arrays.Zipped
title: 압축 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 67170fa005675f0e5d788c9c3b350fb9a961a597
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718712"
---
# <a name="zipped-function"></a><span data-ttu-id="5fbe4-102">압축 함수</span><span class="sxs-lookup"><span data-stu-id="5fbe4-102">Zipped function</span></span>

<span data-ttu-id="5fbe4-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5fbe4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5fbe4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fbe4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5fbe4-105">두 배열이 지정 된 경우 각 쌍은 각 원래 배열의 요소를 포함 하도록 쌍의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="5fbe4-106">입력</span><span class="sxs-lookup"><span data-stu-id="5fbe4-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="5fbe4-107">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="5fbe4-107">left : 'T[]</span></span>

<span data-ttu-id="5fbe4-108">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="5fbe4-109">right: ' U []</span><span class="sxs-lookup"><span data-stu-id="5fbe4-109">right : 'U[]</span></span>

<span data-ttu-id="5fbe4-110">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="5fbe4-111">출력: (' t ', ' U) []</span><span class="sxs-lookup"><span data-stu-id="5fbe4-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="5fbe4-112">각에 대 한 폼의 쌍을 포함 하는 배열 `(left[idx], right[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="5fbe4-113">두 배열의 길이가 같지 않은 경우에는 입력 중 짧은 값 만큼 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5fbe4-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fbe4-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5fbe4-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="5fbe4-115">'T</span></span>

<span data-ttu-id="5fbe4-116">왼쪽 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="5fbe4-117">' U</span><span class="sxs-lookup"><span data-stu-id="5fbe4-117">'U</span></span>

<span data-ttu-id="5fbe4-118">오른쪽 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbe4-118">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fbe4-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5fbe4-119">See Also</span></span>

- [<span data-ttu-id="5fbe4-120">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="5fbe4-120">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="5fbe4-121">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="5fbe4-121">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="5fbe4-122">Microsoft 양자. 배열 압축 해제</span><span class="sxs-lookup"><span data-stu-id="5fbe4-122">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)