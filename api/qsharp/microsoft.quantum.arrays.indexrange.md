---
uid: Microsoft.Quantum.Arrays.IndexRange
title: IndexRange 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845789"
---
# <a name="indexrange-function"></a><span data-ttu-id="9c854-102">IndexRange 함수</span><span class="sxs-lookup"><span data-stu-id="9c854-102">IndexRange function</span></span>

<span data-ttu-id="9c854-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9c854-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9c854-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9c854-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9c854-105">배열이 지정 된 경우 for 루프에서 사용 하기에 적합 한 해당 배열의 인덱스에 대해 범위를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c854-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="9c854-106">입력</span><span class="sxs-lookup"><span data-stu-id="9c854-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="9c854-107">배열: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="9c854-107">array : 'TElement[]</span></span>

<span data-ttu-id="9c854-108">인덱스 범위가 반환 되어야 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9c854-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="9c854-109">출력: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="9c854-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="9c854-110">배열의 모든 인덱스에 대 한 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="9c854-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9c854-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c854-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="9c854-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="9c854-112">'TElement</span></span>

<span data-ttu-id="9c854-113">배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9c854-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="9c854-114">예</span><span class="sxs-lookup"><span data-stu-id="9c854-114">Example</span></span>

<span data-ttu-id="9c854-115">다음 `for` 루프는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c854-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```