---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: TupleArrayAsNestedArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845384"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="8b7dc-102">TupleArrayAsNestedArray 함수</span><span class="sxs-lookup"><span data-stu-id="8b7dc-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="8b7dc-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8b7dc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8b7dc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b7dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b7dc-105">2 튜플의 목록을 중첩 된 배열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="8b7dc-106">입력</span><span class="sxs-lookup"><span data-stu-id="8b7dc-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="8b7dc-107">tupleList: (' ' ') []</span><span class="sxs-lookup"><span data-stu-id="8b7dc-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="8b7dc-108">중첩 배열로 전환 될 2 튜플의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="8b7dc-109">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="8b7dc-109">Output : 'T[][]</span></span>

<span data-ttu-id="8b7dc-110">길이가 tupleList와 일치 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="8b7dc-111">예</span><span class="sxs-lookup"><span data-stu-id="8b7dc-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="8b7dc-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b7dc-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8b7dc-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="8b7dc-113">'T</span></span>

