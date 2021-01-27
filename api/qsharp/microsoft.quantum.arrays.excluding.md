---
uid: Microsoft.Quantum.Arrays.Excluding
title: 제외 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: c117431e3d98bba4ed3d29cb0b171247bf77be0b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848662"
---
# <a name="excluding-function"></a><span data-ttu-id="8631f-102">제외 함수</span><span class="sxs-lookup"><span data-stu-id="8631f-102">Excluding function</span></span>

<span data-ttu-id="8631f-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8631f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8631f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8631f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8631f-105">지정 된 인덱스 목록에서 요소를 제외 하 고 다른 배열의 요소를 포함 하는 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8631f-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8631f-106">입력</span><span class="sxs-lookup"><span data-stu-id="8631f-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="8631f-107">remove: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8631f-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8631f-108">출력에서 제외 해야 하는 요소를 나타내는 인덱스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8631f-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="8631f-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="8631f-109">array : 'T[]</span></span>

<span data-ttu-id="8631f-110">출력 배열의 값이 사용 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8631f-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="8631f-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="8631f-111">Output : 'T[]</span></span>

<span data-ttu-id="8631f-112">인덱스를 `output` `output[0]` 에 표시 하지 않는의 첫 번째 요소 (예: `array` `remove` `output[1]` 두 번째 요소 등) 인 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8631f-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8631f-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8631f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8631f-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="8631f-114">'T</span></span>

<span data-ttu-id="8631f-115">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8631f-115">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="8631f-116">예제</span><span class="sxs-lookup"><span data-stu-id="8631f-116">Example</span></span>

```qsharp
let array = [10, 11, 12, 13, 14, 15];
// The following line returns [10, 12, 15].
let subarray = Excluding([1, 3, 4], array);
```