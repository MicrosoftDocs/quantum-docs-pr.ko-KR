---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: TupleArrayAsNestedArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718808"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="7787e-102">TupleArrayAsNestedArray 함수</span><span class="sxs-lookup"><span data-stu-id="7787e-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="7787e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7787e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7787e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7787e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7787e-105">2 튜플의 목록을 중첩 된 배열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7787e-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="7787e-106">입력</span><span class="sxs-lookup"><span data-stu-id="7787e-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="7787e-107">tupleList: (' ' ') []</span><span class="sxs-lookup"><span data-stu-id="7787e-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="7787e-108">중첩 배열로 전환 될 2 튜플의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7787e-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="7787e-109">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="7787e-109">Output : 'T[][]</span></span>

<span data-ttu-id="7787e-110">길이가 tupleList와 일치 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7787e-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="7787e-111">예제</span><span class="sxs-lookup"><span data-stu-id="7787e-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="7787e-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7787e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7787e-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="7787e-113">'T</span></span>

