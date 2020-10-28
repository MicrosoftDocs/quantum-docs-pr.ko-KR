---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: 헤드 Andrest 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719180"
---
# <a name="headandrest-function"></a><span data-ttu-id="bd263-102">헤드 Andrest 함수</span><span class="sxs-lookup"><span data-stu-id="bd263-102">HeadAndRest function</span></span>

<span data-ttu-id="bd263-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bd263-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bd263-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bd263-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bd263-105">배열의 첫 번째 및 나머지 모든 요소에 대 한 튜플을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd263-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="bd263-106">입력</span><span class="sxs-lookup"><span data-stu-id="bd263-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="bd263-107">array: ' A []</span><span class="sxs-lookup"><span data-stu-id="bd263-107">array : 'A[]</span></span>

<span data-ttu-id="bd263-108">요소가 하나 이상 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="bd263-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="bd263-109">Output: (' A, ' A [])</span><span class="sxs-lookup"><span data-stu-id="bd263-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="bd263-110">배열의 첫 번째 및 나머지 모든 요소에 대 한 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="bd263-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bd263-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd263-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="bd263-112">' A</span><span class="sxs-lookup"><span data-stu-id="bd263-112">'A</span></span>

<span data-ttu-id="bd263-113">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bd263-113">The type of the array elements.</span></span>