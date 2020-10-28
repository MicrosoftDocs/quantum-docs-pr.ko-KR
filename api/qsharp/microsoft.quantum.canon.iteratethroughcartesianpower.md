---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: IterateThroughCartesianPower 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716024"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="c211e-102">IterateThroughCartesianPower 작업</span><span class="sxs-lookup"><span data-stu-id="c211e-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="c211e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c211e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c211e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c211e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c211e-105">정수 범위의 데카르트 제곱에 있는 각 인덱스에 대해 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c211e-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="c211e-106">Description</span><span class="sxs-lookup"><span data-stu-id="c211e-106">Description</span></span>

<span data-ttu-id="c211e-107">범위에서 데카르트 제곱의 각 요소에 대 한 작업을 반복적으로 적용 `0..(bound - 1)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c211e-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="c211e-108">입력</span><span class="sxs-lookup"><span data-stu-id="c211e-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="c211e-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c211e-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c211e-110">범위가 발생 해야 하는 데카르트 제곱입니다 `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="c211e-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="c211e-111">바인딩: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c211e-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c211e-112">범위 길이로 지정 된 반복 될 범위에 대 한 사양입니다.</span><span class="sxs-lookup"><span data-stu-id="c211e-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="c211e-113">op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c211e-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c211e-114">지정 된 데카르트 거듭제곱의 각 요소에 대해 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c211e-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c211e-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c211e-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c211e-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c211e-116">See Also</span></span>

- [<span data-ttu-id="c211e-117">IterateThroughCartesianProduct입니다.</span><span class="sxs-lookup"><span data-stu-id="c211e-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)