---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: _SwapOrderToPermuteArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719492"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="7e605-102">_SwapOrderToPermuteArray 함수</span><span class="sxs-lookup"><span data-stu-id="7e605-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="7e605-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7e605-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7e605-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e605-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7e605-105">배열에서 정렬 된 배열을 생성 하기 위해 교환 해야 하는 순서 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e605-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="7e605-106">에서 교체가 발생 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e605-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="7e605-107">입력</span><span class="sxs-lookup"><span data-stu-id="7e605-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="7e605-108">newOrder: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7e605-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="7e605-109">새 배열의 인덱스 순열이 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7e605-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="7e605-110">$ Elements $n 해야 하며, 각각 $0 $에서 $n-$1 사이의 고유한 정수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e605-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="7e605-111">Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="7e605-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="7e605-112">튜플은 교환 될 두 인덱스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e605-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="7e605-113">교체는 가장 낮은 인덱스에서 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e605-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e605-114">설명</span><span class="sxs-lookup"><span data-stu-id="7e605-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="7e605-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="7e605-115">Psuedocode</span></span>

<span data-ttu-id="7e605-116">의 경우 (인덱스는 0 ..1 (newOrder)-1) {newOrder [index]! = index {Switch newOrder [index] with newOrder [newOrder [인덱스]]}}</span><span class="sxs-lookup"><span data-stu-id="7e605-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>