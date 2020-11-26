---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: _SwapOrderToPermuteArray 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 9df2ec00d91c1124fae960efd15d576b15b0223c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221711"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="09da0-102">_SwapOrderToPermuteArray 함수</span><span class="sxs-lookup"><span data-stu-id="09da0-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="09da0-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="09da0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="09da0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09da0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09da0-105">배열에서 정렬 된 배열을 생성 하기 위해 교환 해야 하는 순서 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="09da0-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="09da0-106">에서 교체가 발생 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09da0-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="09da0-107">입력</span><span class="sxs-lookup"><span data-stu-id="09da0-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="09da0-108">newOrder: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="09da0-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="09da0-109">새 배열의 인덱스 순열이 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="09da0-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="09da0-110">$ Elements $n 해야 하며, 각각 $0 $에서 $n-$1 사이의 고유한 정수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09da0-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="09da0-111">Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="09da0-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="09da0-112">튜플은 교환 될 두 인덱스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09da0-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="09da0-113">교체는 가장 낮은 인덱스에서 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09da0-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="09da0-114">설명</span><span class="sxs-lookup"><span data-stu-id="09da0-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="09da0-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="09da0-115">Psuedocode</span></span>

<span data-ttu-id="09da0-116">의 경우 (인덱스는 0 ..1 (newOrder)-1) {newOrder [index]! = index {Switch newOrder [index] with newOrder [newOrder [인덱스]]}}</span><span class="sxs-lookup"><span data-stu-id="09da0-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>