---
uid: Microsoft.Quantum.Arrays.ElementsAt
title: ElementsAt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementsAt
qsharp.summary: Returns the array's elements at a given range of indices.
ms.openlocfilehash: b4bbba4dc83c4f9b89cdcb8ec32769f1c586357e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719341"
---
# <a name="elementsat-function"></a><span data-ttu-id="6ae7b-102">ElementsAt 함수</span><span class="sxs-lookup"><span data-stu-id="6ae7b-102">ElementsAt function</span></span>

<span data-ttu-id="6ae7b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6ae7b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6ae7b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6ae7b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6ae7b-105">지정 된 인덱스 범위에서 배열의 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ae7b-105">Returns the array's elements at a given range of indices.</span></span>

```qsharp
function ElementsAt<'T> (range : Range, array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="6ae7b-106">입력</span><span class="sxs-lookup"><span data-stu-id="6ae7b-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="6ae7b-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="6ae7b-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="6ae7b-108">배열 인덱스의 범위</span><span class="sxs-lookup"><span data-stu-id="6ae7b-108">Range of array indexes</span></span>


### <a name="array--t"></a><span data-ttu-id="6ae7b-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="6ae7b-109">array : 'T[]</span></span>

<span data-ttu-id="6ae7b-110">배열</span><span class="sxs-lookup"><span data-stu-id="6ae7b-110">Array</span></span>



## <a name="output--t"></a><span data-ttu-id="6ae7b-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="6ae7b-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6ae7b-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ae7b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6ae7b-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="6ae7b-113">'T</span></span>

<span data-ttu-id="6ae7b-114">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="6ae7b-114">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ae7b-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6ae7b-115">See Also</span></span>

- [<span data-ttu-id="6ae7b-116">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="6ae7b-116">Microsoft.Quantum.Arrays.ElementAt</span></span>](xref:Microsoft.Quantum.Arrays.ElementAt)
- [<span data-ttu-id="6ae7b-117">Microsoft 양자 함수</span><span class="sxs-lookup"><span data-stu-id="6ae7b-117">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)