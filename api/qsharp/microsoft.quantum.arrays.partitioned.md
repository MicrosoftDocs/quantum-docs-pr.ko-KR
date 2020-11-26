---
uid: Microsoft.Quantum.Arrays.Partitioned
title: 분할 된 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220504"
---
# <a name="partitioned-function"></a><span data-ttu-id="847ce-102">분할 된 함수</span><span class="sxs-lookup"><span data-stu-id="847ce-102">Partitioned function</span></span>

<span data-ttu-id="847ce-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="847ce-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="847ce-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="847ce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="847ce-105">배열을 여러 부분으로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="847ce-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="847ce-106">입력</span><span class="sxs-lookup"><span data-stu-id="847ce-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="847ce-107">nElements: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="847ce-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="847ce-108">배열의 각 부분에 있는 요소 수</span><span class="sxs-lookup"><span data-stu-id="847ce-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="847ce-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="847ce-109">arr : 'T[]</span></span>

<span data-ttu-id="847ce-110">분할할 입력 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="847ce-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="847ce-111">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="847ce-111">Output : 'T[][]</span></span>

<span data-ttu-id="847ce-112">첫 번째 배열이 첫 번째 배열이 `nElements[0]` `arr` 고 두 번째 배열이 그 다음 `nElements[1]` 인 여러 배열 `arr` 마지막 배열은 나머지 모든 요소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="847ce-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="847ce-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="847ce-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="847ce-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="847ce-114">'T</span></span>

