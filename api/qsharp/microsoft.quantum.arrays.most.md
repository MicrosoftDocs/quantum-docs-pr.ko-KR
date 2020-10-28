---
uid: Microsoft.Quantum.Arrays.Most
title: 대부분 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719000"
---
# <a name="most-function"></a><span data-ttu-id="097b3-102">대부분 함수</span><span class="sxs-lookup"><span data-stu-id="097b3-102">Most function</span></span>

<span data-ttu-id="097b3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="097b3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="097b3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="097b3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="097b3-105">마지막 배열 요소가 삭제 된 경우를 제외 하 고 입력 배열과 같은 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="097b3-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="097b3-106">입력</span><span class="sxs-lookup"><span data-stu-id="097b3-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="097b3-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="097b3-107">array : 'T[]</span></span>

<span data-ttu-id="097b3-108">첫 번째-마지막 요소에 대 한 첫 번째 요소에서 출력 배열을 형성 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="097b3-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="097b3-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="097b3-109">Output : 'T[]</span></span>

<span data-ttu-id="097b3-110">요소를 포함 하는 배열 `array[0..Length(array) - 2]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="097b3-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="097b3-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="097b3-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="097b3-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="097b3-112">'T</span></span>

<span data-ttu-id="097b3-113">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="097b3-113">The type of the array elements.</span></span>