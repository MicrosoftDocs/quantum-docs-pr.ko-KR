---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: IterateThroughCartesianProduct 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: e4fc71f6f707639f6f89eece8546ec2fb434a15a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716038"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="8c544-102">IterateThroughCartesianProduct 작업</span><span class="sxs-lookup"><span data-stu-id="8c544-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="8c544-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8c544-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8c544-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8c544-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8c544-105">여러 범위의 데카르트 곱에서 각 인덱스에 대 한 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c544-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="8c544-106">Description</span><span class="sxs-lookup"><span data-stu-id="8c544-106">Description</span></span>

<span data-ttu-id="8c544-107">`0..(bounds[0] - 1)`, `0..(bounds[1] - 1)` , ...,,, ...,의 데카르트 곱의 각 요소에 대 한 작업을 반복적으로 적용 합니다.`0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="8c544-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="8c544-108">입력</span><span class="sxs-lookup"><span data-stu-id="8c544-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="8c544-109">범위: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8c544-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8c544-110">반복할 범위를 지정 하 고 각 범위를 정수 길이로 지정 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8c544-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="8c544-111">op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c544-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8c544-112">지정 된 데카르트 곱의 각 요소에 대해 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8c544-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8c544-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8c544-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8c544-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8c544-114">See Also</span></span>

- [<span data-ttu-id="8c544-115">IterateThroughCartesianPower입니다.</span><span class="sxs-lookup"><span data-stu-id="8c544-115">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)