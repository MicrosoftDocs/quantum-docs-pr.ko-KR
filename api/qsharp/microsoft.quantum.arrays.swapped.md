---
uid: Microsoft.Quantum.Arrays.Swapped
title: 교환 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 173fb32b5a41ce054f19548a7fcca18c11c4c4cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220130"
---
# <a name="swapped-function"></a><span data-ttu-id="5dff7-102">교환 함수</span><span class="sxs-lookup"><span data-stu-id="5dff7-102">Swapped function</span></span>

<span data-ttu-id="5dff7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5dff7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5dff7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5dff7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5dff7-105">배열에 두 요소의 교환을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dff7-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="5dff7-106">입력</span><span class="sxs-lookup"><span data-stu-id="5dff7-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="5dff7-107">firstIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5dff7-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5dff7-108">교환할 첫 번째 요소의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="5dff7-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="5dff7-109">secondIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5dff7-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5dff7-110">스왑할 두 번째 요소의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="5dff7-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="5dff7-111">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="5dff7-111">arr : 'T[]</span></span>

<span data-ttu-id="5dff7-112">스왑할 요소가 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5dff7-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="5dff7-113">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="5dff7-113">Output : 'T[]</span></span>

<span data-ttu-id="5dff7-114">내부 교환이 적용 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5dff7-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="5dff7-115">예제</span><span class="sxs-lookup"><span data-stu-id="5dff7-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="5dff7-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5dff7-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5dff7-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="5dff7-117">'T</span></span>

