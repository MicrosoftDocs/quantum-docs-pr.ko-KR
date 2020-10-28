---
uid: Microsoft.Quantum.Arrays.Swapped
title: 교환 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: fa5b37b4caf5d8f19ed05075ddd7bc4217036bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718825"
---
# <a name="swapped-function"></a><span data-ttu-id="ecb03-102">교환 함수</span><span class="sxs-lookup"><span data-stu-id="ecb03-102">Swapped function</span></span>

<span data-ttu-id="ecb03-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ecb03-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ecb03-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ecb03-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ecb03-105">배열에 두 요소의 교환을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb03-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="ecb03-106">입력</span><span class="sxs-lookup"><span data-stu-id="ecb03-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="ecb03-107">firstIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ecb03-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ecb03-108">교환할 첫 번째 요소의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb03-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="ecb03-109">secondIndex: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ecb03-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ecb03-110">스왑할 두 번째 요소의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb03-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="ecb03-111">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="ecb03-111">arr : 'T[]</span></span>

<span data-ttu-id="ecb03-112">스왑할 요소가 포함 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb03-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="ecb03-113">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="ecb03-113">Output : 'T[]</span></span>

<span data-ttu-id="ecb03-114">내부 교환이 적용 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb03-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="ecb03-115">예제</span><span class="sxs-lookup"><span data-stu-id="ecb03-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="ecb03-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecb03-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ecb03-117">없습니다</span><span class="sxs-lookup"><span data-stu-id="ecb03-117">'T</span></span>

