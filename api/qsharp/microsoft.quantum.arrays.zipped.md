---
uid: Microsoft.Quantum.Arrays.Zipped
title: 압축 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 56ed97d573bf29dddb7cdb1c3f360218bf97889a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219756"
---
# <a name="zipped-function"></a><span data-ttu-id="9b7d8-102">압축 함수</span><span class="sxs-lookup"><span data-stu-id="9b7d8-102">Zipped function</span></span>

<span data-ttu-id="9b7d8-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9b7d8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9b7d8-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b7d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b7d8-105">두 배열이 지정 된 경우 각 쌍은 각 원래 배열의 요소를 포함 하도록 쌍의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="9b7d8-106">입력</span><span class="sxs-lookup"><span data-stu-id="9b7d8-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="9b7d8-107">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="9b7d8-107">left : 'T[]</span></span>

<span data-ttu-id="9b7d8-108">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="9b7d8-109">right: ' U []</span><span class="sxs-lookup"><span data-stu-id="9b7d8-109">right : 'U[]</span></span>

<span data-ttu-id="9b7d8-110">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="9b7d8-111">출력: (' t ', ' U) []</span><span class="sxs-lookup"><span data-stu-id="9b7d8-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="9b7d8-112">각에 대 한 폼의 쌍을 포함 하는 배열 `(left[idx], right[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="9b7d8-113">두 배열의 길이가 같지 않은 경우에는 입력 중 짧은 값 만큼 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9b7d8-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b7d8-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9b7d8-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="9b7d8-115">'T</span></span>

<span data-ttu-id="9b7d8-116">왼쪽 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="9b7d8-117">' U</span><span class="sxs-lookup"><span data-stu-id="9b7d8-117">'U</span></span>

<span data-ttu-id="9b7d8-118">오른쪽 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9b7d8-118">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b7d8-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9b7d8-119">See Also</span></span>

- [<span data-ttu-id="9b7d8-120">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="9b7d8-120">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="9b7d8-121">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="9b7d8-121">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="9b7d8-122">Microsoft 양자. 배열 압축 해제</span><span class="sxs-lookup"><span data-stu-id="9b7d8-122">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)