---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: 헤드 Andrest 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848554"
---
# <a name="headandrest-function"></a><span data-ttu-id="8dcf9-102">헤드 Andrest 함수</span><span class="sxs-lookup"><span data-stu-id="8dcf9-102">HeadAndRest function</span></span>

<span data-ttu-id="8dcf9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8dcf9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8dcf9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8dcf9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8dcf9-105">배열의 첫 번째 및 나머지 모든 요소에 대 한 튜플을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf9-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="8dcf9-106">입력</span><span class="sxs-lookup"><span data-stu-id="8dcf9-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="8dcf9-107">array: ' A []</span><span class="sxs-lookup"><span data-stu-id="8dcf9-107">array : 'A[]</span></span>

<span data-ttu-id="8dcf9-108">요소가 하나 이상 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf9-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="8dcf9-109">Output: (' A, ' A [])</span><span class="sxs-lookup"><span data-stu-id="8dcf9-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="8dcf9-110">배열의 첫 번째 및 나머지 모든 요소에 대 한 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf9-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8dcf9-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8dcf9-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="8dcf9-112">' A</span><span class="sxs-lookup"><span data-stu-id="8dcf9-112">'A</span></span>

<span data-ttu-id="8dcf9-113">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf9-113">The type of the array elements.</span></span>