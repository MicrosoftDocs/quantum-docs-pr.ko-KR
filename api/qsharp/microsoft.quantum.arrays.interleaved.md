---
uid: Microsoft.Quantum.Arrays.Interleaved
title: 인터리브 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848108"
---
# <a name="interleaved-function"></a><span data-ttu-id="466ae-102">인터리브 함수</span><span class="sxs-lookup"><span data-stu-id="466ae-102">Interleaved function</span></span>

<span data-ttu-id="466ae-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="466ae-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="466ae-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="466ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="466ae-105">인터리브 하며는 거의 동일한 크기의 두 배열을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="466ae-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="466ae-106">설명</span><span class="sxs-lookup"><span data-stu-id="466ae-106">Description</span></span>

<span data-ttu-id="466ae-107">이 함수는 첫 번째 배열에서 첫 번째 요소부터 시작 하 여 두 배열의 인터리빙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="466ae-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="466ae-108">첫 번째 배열의 길이는 두 번째 배열의 길이와 동일 하거나 하나 이상의 요소를 가질 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="466ae-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="466ae-109">입력</span><span class="sxs-lookup"><span data-stu-id="466ae-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="466ae-110">first: ' t []</span><span class="sxs-lookup"><span data-stu-id="466ae-110">first : 'T[]</span></span>

<span data-ttu-id="466ae-111">인터리브 될 첫 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="466ae-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="466ae-112">second: ' t []</span><span class="sxs-lookup"><span data-stu-id="466ae-112">second : 'T[]</span></span>

<span data-ttu-id="466ae-113">인터리브 될 두 번째 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="466ae-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="466ae-114">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="466ae-114">Output : 'T[]</span></span>

<span data-ttu-id="466ae-115">인터리브 배열</span><span class="sxs-lookup"><span data-stu-id="466ae-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="466ae-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="466ae-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="466ae-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="466ae-117">'T</span></span>

<span data-ttu-id="466ae-118">및의 각 요소 형식입니다 `first` `second` .</span><span class="sxs-lookup"><span data-stu-id="466ae-118">The type of each element of `first` and `second`.</span></span>

## <a name="example"></a><span data-ttu-id="466ae-119">예제</span><span class="sxs-lookup"><span data-stu-id="466ae-119">Example</span></span>

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```