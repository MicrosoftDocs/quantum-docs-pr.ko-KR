---
uid: Microsoft.Quantum.Arrays.IndexRange
title: IndexRange 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719149"
---
# <a name="indexrange-function"></a><span data-ttu-id="a7652-102">IndexRange 함수</span><span class="sxs-lookup"><span data-stu-id="a7652-102">IndexRange function</span></span>

<span data-ttu-id="a7652-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a7652-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a7652-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7652-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7652-105">배열이 지정 된 경우 for 루프에서 사용 하기에 적합 한 해당 배열의 인덱스에 대해 범위를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7652-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="a7652-106">입력</span><span class="sxs-lookup"><span data-stu-id="a7652-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="a7652-107">배열: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="a7652-107">array : 'TElement[]</span></span>

<span data-ttu-id="a7652-108">인덱스 범위가 반환 되어야 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a7652-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="a7652-109">출력: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a7652-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="a7652-110">배열의 모든 인덱스에 대 한 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a7652-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a7652-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7652-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="a7652-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="a7652-112">'TElement</span></span>

<span data-ttu-id="a7652-113">배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a7652-113">The type of elements of the array.</span></span>