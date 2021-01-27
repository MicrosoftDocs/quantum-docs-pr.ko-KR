---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: IterateThroughCartesianProduct 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840272"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="a1cb6-102">IterateThroughCartesianProduct 작업</span><span class="sxs-lookup"><span data-stu-id="a1cb6-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="a1cb6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a1cb6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a1cb6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a1cb6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a1cb6-105">여러 범위의 데카르트 곱에서 각 인덱스에 대 한 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb6-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="a1cb6-106">설명</span><span class="sxs-lookup"><span data-stu-id="a1cb6-106">Description</span></span>

<span data-ttu-id="a1cb6-107">`0..(bounds[0] - 1)`, `0..(bounds[1] - 1)` , ...,,, ...,의 데카르트 곱의 각 요소에 대 한 작업을 반복적으로 적용 합니다.`0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="a1cb6-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="a1cb6-108">입력</span><span class="sxs-lookup"><span data-stu-id="a1cb6-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="a1cb6-109">범위: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a1cb6-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a1cb6-110">반복할 범위를 지정 하 고 각 범위를 정수 길이로 지정 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb6-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="a1cb6-111">op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1cb6-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a1cb6-112">지정 된 데카르트 곱의 각 요소에 대해 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb6-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a1cb6-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1cb6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="a1cb6-114">예</span><span class="sxs-lookup"><span data-stu-id="a1cb6-114">Example</span></span>

<span data-ttu-id="a1cb6-115">작업을 지정 하는 경우 `op` 다음 두 코드 조각이 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb6-115">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a><span data-ttu-id="a1cb6-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a1cb6-116">See Also</span></span>

- [<span data-ttu-id="a1cb6-117">IterateThroughCartesianPower입니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb6-117">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)