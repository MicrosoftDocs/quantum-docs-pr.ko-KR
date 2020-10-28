---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: Motail 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 8786250cf2f78ce2e9ff8baddc856d0bc07cb9a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718993"
---
# <a name="mostandtail-function"></a><span data-ttu-id="3661e-102">Motail 함수</span><span class="sxs-lookup"><span data-stu-id="3661e-102">MostAndTail function</span></span>

<span data-ttu-id="3661e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3661e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3661e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3661e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3661e-105">배열의 모든 및 마지막 요소에 대 한 튜플을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3661e-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="3661e-106">입력</span><span class="sxs-lookup"><span data-stu-id="3661e-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="3661e-107">array: ' A []</span><span class="sxs-lookup"><span data-stu-id="3661e-107">array : 'A[]</span></span>

<span data-ttu-id="3661e-108">요소가 하나 이상 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3661e-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="3661e-109">Output: (' A [], ' A)</span><span class="sxs-lookup"><span data-stu-id="3661e-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="3661e-110">배열의 모든 및 마지막 요소에 대 한 튜플</span><span class="sxs-lookup"><span data-stu-id="3661e-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3661e-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3661e-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="3661e-112">' A</span><span class="sxs-lookup"><span data-stu-id="3661e-112">'A</span></span>

<span data-ttu-id="3661e-113">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3661e-113">The type of the array elements.</span></span>