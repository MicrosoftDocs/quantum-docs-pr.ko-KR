---
uid: Microsoft.Quantum.Arrays.Padded
title: 채워진 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718981"
---
# <a name="padded-function"></a><span data-ttu-id="f8c1a-102">채워진 함수</span><span class="sxs-lookup"><span data-stu-id="f8c1a-102">Padded function</span></span>

<span data-ttu-id="f8c1a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f8c1a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f8c1a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f8c1a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f8c1a-105">지정 된 값을 사용 하 여 지정 된 길이까지 채워진 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f8c1a-106">입력</span><span class="sxs-lookup"><span data-stu-id="f8c1a-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="f8c1a-107">nElementsTotal: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f8c1a-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f8c1a-108">패딩 된 배열의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-108">The length of the padded array.</span></span> <span data-ttu-id="f8c1a-109">이가 양수인 경우 `inputArray` 는 헤드에 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="f8c1a-110">이가 음수 이면 `inputArray` 꼬리에 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="f8c1a-111">defaultElement: ' '</span><span class="sxs-lookup"><span data-stu-id="f8c1a-111">defaultElement : 'T</span></span>

<span data-ttu-id="f8c1a-112">요소 패딩에 사용할 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="f8c1a-113">inputArray: ' t []</span><span class="sxs-lookup"><span data-stu-id="f8c1a-113">inputArray : 'T[]</span></span>

<span data-ttu-id="f8c1a-114">출력 배열의 헤드에 값이 있는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="f8c1a-115">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="f8c1a-115">Output : 'T[]</span></span>

<span data-ttu-id="f8c1a-116">에 `output` `inputArray` `defaultElement` 길이가 있을 때까지 s로 채워진의 배열입니다. `output``nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="f8c1a-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f8c1a-117">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8c1a-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f8c1a-118">없습니다</span><span class="sxs-lookup"><span data-stu-id="f8c1a-118">'T</span></span>

<span data-ttu-id="f8c1a-119">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c1a-119">The type of the array elements.</span></span>