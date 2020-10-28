---
uid: Microsoft.Quantum.Arrays.Excluding
title: 제외 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 8848c6e89da50efb4f7550168f1757b25a214a24
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719276"
---
# <a name="excluding-function"></a><span data-ttu-id="5bbb8-102">제외 함수</span><span class="sxs-lookup"><span data-stu-id="5bbb8-102">Excluding function</span></span>

<span data-ttu-id="5bbb8-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5bbb8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5bbb8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5bbb8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5bbb8-105">지정 된 인덱스 목록에서 요소를 제외 하 고 다른 배열의 요소를 포함 하는 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbb8-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="5bbb8-106">입력</span><span class="sxs-lookup"><span data-stu-id="5bbb8-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="5bbb8-107">remove: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5bbb8-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5bbb8-108">출력에서 제외 해야 하는 요소를 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbb8-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="5bbb8-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="5bbb8-109">array : 'T[]</span></span>

<span data-ttu-id="5bbb8-110">출력 배열의 값이 사용 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbb8-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="5bbb8-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="5bbb8-111">Output : 'T[]</span></span>

<span data-ttu-id="5bbb8-112">인덱스를 `output` `output[0]` 에 표시 하지 않는의 첫 번째 요소 (예: `array` `remove` `output[1]` 두 번째 요소 등) 인 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbb8-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5bbb8-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5bbb8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5bbb8-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="5bbb8-114">'T</span></span>

<span data-ttu-id="5bbb8-115">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbb8-115">The type of the array elements.</span></span>