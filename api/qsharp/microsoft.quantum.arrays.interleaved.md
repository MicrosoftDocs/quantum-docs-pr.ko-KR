---
uid: Microsoft.Quantum.Arrays.Interleaved
title: 인터리브 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719144"
---
# <a name="interleaved-function"></a><span data-ttu-id="1d2f6-102">인터리브 함수</span><span class="sxs-lookup"><span data-stu-id="1d2f6-102">Interleaved function</span></span>

<span data-ttu-id="1d2f6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1d2f6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1d2f6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1d2f6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1d2f6-105">인터리브 하며는 거의 동일한 크기의 두 배열을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="1d2f6-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="1d2f6-106">Description</span><span class="sxs-lookup"><span data-stu-id="1d2f6-106">Description</span></span>

<span data-ttu-id="1d2f6-107">이 함수는 첫 번째 배열에서 첫 번째 요소부터 시작 하 여 두 배열의 인터리빙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2f6-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="1d2f6-108">첫 번째 배열의 길이는 두 번째 배열의 길이와 동일 하거나 하나 이상의 요소를 가질 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2f6-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="1d2f6-109">입력</span><span class="sxs-lookup"><span data-stu-id="1d2f6-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="1d2f6-110">first: ' t []</span><span class="sxs-lookup"><span data-stu-id="1d2f6-110">first : 'T[]</span></span>

<span data-ttu-id="1d2f6-111">인터리브 될 첫 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1d2f6-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="1d2f6-112">second: ' t []</span><span class="sxs-lookup"><span data-stu-id="1d2f6-112">second : 'T[]</span></span>

<span data-ttu-id="1d2f6-113">인터리브 될 두 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1d2f6-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="1d2f6-114">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="1d2f6-114">Output : 'T[]</span></span>

<span data-ttu-id="1d2f6-115">인터리브 배열</span><span class="sxs-lookup"><span data-stu-id="1d2f6-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1d2f6-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d2f6-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1d2f6-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="1d2f6-117">'T</span></span>

<span data-ttu-id="1d2f6-118">및의 각 요소 형식입니다 `first` `second` .</span><span class="sxs-lookup"><span data-stu-id="1d2f6-118">The type of each element of `first` and `second`.</span></span>