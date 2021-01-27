---
uid: Microsoft.Quantum.Arrays.Padded
title: 채워진 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845557"
---
# <a name="padded-function"></a><span data-ttu-id="01106-102">채워진 함수</span><span class="sxs-lookup"><span data-stu-id="01106-102">Padded function</span></span>

<span data-ttu-id="01106-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="01106-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="01106-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="01106-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="01106-105">지정 된 값을 사용 하 여 지정 된 길이까지 채워진 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="01106-105">Returns an array padded at with specified values up to a specified length.</span></span>

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="01106-106">입력</span><span class="sxs-lookup"><span data-stu-id="01106-106">Input</span></span>

### <a name="nelementstotal--int"></a><span data-ttu-id="01106-107">nElementsTotal: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01106-107">nElementsTotal : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01106-108">패딩 된 배열의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="01106-108">The length of the padded array.</span></span> <span data-ttu-id="01106-109">이가 양수인 경우 `inputArray` 는 헤드에 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="01106-109">If this is positive, `inputArray` is padded at the head.</span></span> <span data-ttu-id="01106-110">이가 음수 이면 `inputArray` 꼬리에 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="01106-110">If this is negative, `inputArray` is padded at the tail.</span></span>


### <a name="defaultelement--t"></a><span data-ttu-id="01106-111">defaultElement: ' '</span><span class="sxs-lookup"><span data-stu-id="01106-111">defaultElement : 'T</span></span>

<span data-ttu-id="01106-112">요소 패딩에 사용할 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="01106-112">Default value to use for padding elements.</span></span>


### <a name="inputarray--t"></a><span data-ttu-id="01106-113">inputArray: ' t []</span><span class="sxs-lookup"><span data-stu-id="01106-113">inputArray : 'T[]</span></span>

<span data-ttu-id="01106-114">출력 배열의 헤드에 값이 있는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="01106-114">Array whose values are at the head of the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="01106-115">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="01106-115">Output : 'T[]</span></span>

<span data-ttu-id="01106-116">에 `output` `inputArray` `defaultElement` 길이가 있을 때까지 s로 채워진의 배열입니다. `output``nElementsTotal`</span><span class="sxs-lookup"><span data-stu-id="01106-116">An array `output` that is the `inputArray` padded at the head with `defaultElement`s until `output` has length `nElementsTotal`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="01106-117">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="01106-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="01106-118">없습니다</span><span class="sxs-lookup"><span data-stu-id="01106-118">'T</span></span>

<span data-ttu-id="01106-119">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="01106-119">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="01106-120">예제</span><span class="sxs-lookup"><span data-stu-id="01106-120">Example</span></span>

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```