---
uid: Microsoft.Quantum.Arrays.ElementsAt
title: ElementsAt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementsAt
qsharp.summary: Returns the array's elements at a given range of indices.
ms.openlocfilehash: 83b5e97085234e8249869f858400cba265d13058
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221456"
---
# <a name="elementsat-function"></a><span data-ttu-id="8cfe2-102">ElementsAt 함수</span><span class="sxs-lookup"><span data-stu-id="8cfe2-102">ElementsAt function</span></span>

<span data-ttu-id="8cfe2-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8cfe2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8cfe2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8cfe2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8cfe2-105">지정 된 인덱스 범위에서 배열의 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cfe2-105">Returns the array's elements at a given range of indices.</span></span>

```qsharp
function ElementsAt<'T> (range : Range, array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8cfe2-106">입력</span><span class="sxs-lookup"><span data-stu-id="8cfe2-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="8cfe2-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="8cfe2-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="8cfe2-108">배열 인덱스의 범위</span><span class="sxs-lookup"><span data-stu-id="8cfe2-108">Range of array indexes</span></span>


### <a name="array--t"></a><span data-ttu-id="8cfe2-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="8cfe2-109">array : 'T[]</span></span>

<span data-ttu-id="8cfe2-110">배열</span><span class="sxs-lookup"><span data-stu-id="8cfe2-110">Array</span></span>



## <a name="output--t"></a><span data-ttu-id="8cfe2-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="8cfe2-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8cfe2-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cfe2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8cfe2-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="8cfe2-113">'T</span></span>

<span data-ttu-id="8cfe2-114">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="8cfe2-114">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cfe2-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8cfe2-115">See Also</span></span>

- [<span data-ttu-id="8cfe2-116">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="8cfe2-116">Microsoft.Quantum.Arrays.ElementAt</span></span>](xref:Microsoft.Quantum.Arrays.ElementAt)
- [<span data-ttu-id="8cfe2-117">Microsoft 양자 함수</span><span class="sxs-lookup"><span data-stu-id="8cfe2-117">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)