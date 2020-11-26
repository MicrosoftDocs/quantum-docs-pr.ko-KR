---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219892"
---
# <a name="windows-function"></a><span data-ttu-id="a415a-102">Windows 함수</span><span class="sxs-lookup"><span data-stu-id="a415a-102">Windows function</span></span>

<span data-ttu-id="a415a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a415a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a415a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a415a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a415a-105">길이의 연속 subarrays 모두 반환 합니다 `size` .</span><span class="sxs-lookup"><span data-stu-id="a415a-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="a415a-106">설명</span><span class="sxs-lookup"><span data-stu-id="a415a-106">Description</span></span>

<span data-ttu-id="a415a-107">이 함수는의 길이에 대 한 모든 `n - size + 1` subarrays을 순서 대로 반환 합니다 `size` `n` . 여기서은의 길이입니다 `arr` .</span><span class="sxs-lookup"><span data-stu-id="a415a-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="a415a-108">첫 번째 subarrays는 `arr[0..size - 1], arr[1..size], arr[2..size + 1]` 마지막 하위 배열까지 `arr[n - size..n - 1]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a415a-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="a415a-109">또는 인 경우 `size <= 0` `size > n` 빈 배열이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a415a-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="a415a-110">입력</span><span class="sxs-lookup"><span data-stu-id="a415a-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="a415a-111">크기: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a415a-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a415a-112">Subarrays의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="a415a-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="a415a-113">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="a415a-113">array : 'T[]</span></span>

<span data-ttu-id="a415a-114">요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a415a-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="a415a-115">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="a415a-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a415a-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a415a-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a415a-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="a415a-117">'T</span></span>

<span data-ttu-id="a415a-118">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a415a-118">The type of `array` elements.</span></span>