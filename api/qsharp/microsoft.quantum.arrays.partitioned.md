---
uid: Microsoft.Quantum.Arrays.Partitioned
title: 분할 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718976"
---
# <a name="partitioned-function"></a><span data-ttu-id="431d9-102">분할 된 함수</span><span class="sxs-lookup"><span data-stu-id="431d9-102">Partitioned function</span></span>

<span data-ttu-id="431d9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="431d9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="431d9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="431d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="431d9-105">배열을 여러 부분으로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="431d9-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="431d9-106">입력</span><span class="sxs-lookup"><span data-stu-id="431d9-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="431d9-107">nElements: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="431d9-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="431d9-108">배열의 각 부분에 있는 요소 수</span><span class="sxs-lookup"><span data-stu-id="431d9-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="431d9-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="431d9-109">arr : 'T[]</span></span>

<span data-ttu-id="431d9-110">분할할 입력 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="431d9-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="431d9-111">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="431d9-111">Output : 'T[][]</span></span>

<span data-ttu-id="431d9-112">첫 번째 배열이 첫 번째 배열이 `nElements[0]` `arr` 고 두 번째 배열이 그 다음 `nElements[1]` 인 여러 배열 `arr` 마지막 배열은 나머지 모든 요소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="431d9-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="431d9-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="431d9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="431d9-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="431d9-114">'T</span></span>

