---
uid: Microsoft.Quantum.Arrays.Chunks
title: 청크 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221609"
---
# <a name="chunks-function"></a><span data-ttu-id="4cf58-102">청크 함수</span><span class="sxs-lookup"><span data-stu-id="4cf58-102">Chunks function</span></span>

<span data-ttu-id="4cf58-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4cf58-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4cf58-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4cf58-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4cf58-105">배열을 같은 길이의 여러 요소로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf58-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="4cf58-106">입력</span><span class="sxs-lookup"><span data-stu-id="4cf58-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="4cf58-107">nElements: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4cf58-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4cf58-108">각 청크의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf58-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="4cf58-109">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="4cf58-109">arr : 'T[]</span></span>

<span data-ttu-id="4cf58-110">분할할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf58-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="4cf58-111">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="4cf58-111">Output : 'T[][]</span></span>

<span data-ttu-id="4cf58-112">원본 배열의 각 청크를 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf58-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4cf58-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4cf58-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4cf58-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="4cf58-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="4cf58-115">설명</span><span class="sxs-lookup"><span data-stu-id="4cf58-115">Remarks</span></span>

<span data-ttu-id="4cf58-116">`nElements`가로 나눌 수 없는 경우 출력의 마지막 요소는 보다 짧을 수 있습니다 `Length(arr)` `nElements` .</span><span class="sxs-lookup"><span data-stu-id="4cf58-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>