---
uid: Microsoft.Quantum.Arrays.Interleaved
title: 인터리브 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220963"
---
# <a name="interleaved-function"></a><span data-ttu-id="9d51b-102">인터리브 함수</span><span class="sxs-lookup"><span data-stu-id="9d51b-102">Interleaved function</span></span>

<span data-ttu-id="9d51b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9d51b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9d51b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d51b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d51b-105">인터리브 하며는 거의 동일한 크기의 두 배열을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="9d51b-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="9d51b-106">Description</span><span class="sxs-lookup"><span data-stu-id="9d51b-106">Description</span></span>

<span data-ttu-id="9d51b-107">이 함수는 첫 번째 배열에서 첫 번째 요소부터 시작 하 여 두 배열의 인터리빙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51b-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="9d51b-108">첫 번째 배열의 길이는 두 번째 배열의 길이와 동일 하거나 하나 이상의 요소를 가질 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51b-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="9d51b-109">입력</span><span class="sxs-lookup"><span data-stu-id="9d51b-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="9d51b-110">first: ' t []</span><span class="sxs-lookup"><span data-stu-id="9d51b-110">first : 'T[]</span></span>

<span data-ttu-id="9d51b-111">인터리브 될 첫 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9d51b-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="9d51b-112">second: ' t []</span><span class="sxs-lookup"><span data-stu-id="9d51b-112">second : 'T[]</span></span>

<span data-ttu-id="9d51b-113">인터리브 될 두 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9d51b-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="9d51b-114">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="9d51b-114">Output : 'T[]</span></span>

<span data-ttu-id="9d51b-115">인터리브 배열</span><span class="sxs-lookup"><span data-stu-id="9d51b-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9d51b-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9d51b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d51b-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="9d51b-117">'T</span></span>

<span data-ttu-id="9d51b-118">및의 각 요소 형식입니다 `first` `second` .</span><span class="sxs-lookup"><span data-stu-id="9d51b-118">The type of each element of `first` and `second`.</span></span>