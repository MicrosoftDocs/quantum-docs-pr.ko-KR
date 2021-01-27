---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: IterateThroughCartesianPower 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840291"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="38307-102">IterateThroughCartesianPower 작업</span><span class="sxs-lookup"><span data-stu-id="38307-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="38307-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="38307-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="38307-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="38307-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="38307-105">정수 범위의 데카르트 제곱에 있는 각 인덱스에 대해 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="38307-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="38307-106">설명</span><span class="sxs-lookup"><span data-stu-id="38307-106">Description</span></span>

<span data-ttu-id="38307-107">범위에서 데카르트 제곱의 각 요소에 대 한 작업을 반복적으로 적용 `0..(bound - 1)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="38307-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="38307-108">입력</span><span class="sxs-lookup"><span data-stu-id="38307-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="38307-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="38307-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="38307-110">범위가 발생 해야 하는 데카르트 제곱입니다 `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="38307-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="38307-111">바인딩: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="38307-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="38307-112">범위 길이로 지정 된 반복 될 범위에 대 한 사양입니다.</span><span class="sxs-lookup"><span data-stu-id="38307-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="38307-113">op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="38307-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="38307-114">지정 된 데카르트 거듭제곱의 각 요소에 대해 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="38307-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="38307-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="38307-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="38307-116">예</span><span class="sxs-lookup"><span data-stu-id="38307-116">Example</span></span>

<span data-ttu-id="38307-117">작업을 지정 하는 경우 `op` 다음 두 코드 조각이 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="38307-117">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a><span data-ttu-id="38307-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="38307-118">See Also</span></span>

- [<span data-ttu-id="38307-119">IterateThroughCartesianProduct입니다.</span><span class="sxs-lookup"><span data-stu-id="38307-119">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)