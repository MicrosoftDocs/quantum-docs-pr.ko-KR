---
uid: Microsoft.Quantum.Arrays.Enumerated
title: 열거 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: adb13d8b25c9e4a6011ade119ffa3cb2783f60e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848137"
---
# <a name="enumerated-function"></a><span data-ttu-id="06ae9-102">열거 함수</span><span class="sxs-lookup"><span data-stu-id="06ae9-102">Enumerated function</span></span>

<span data-ttu-id="06ae9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="06ae9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="06ae9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="06ae9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="06ae9-105">배열이 지정 된 경우 각 요소의 인덱스와 함께 원래 배열의 요소를 포함 하는 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ae9-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="06ae9-106">입력</span><span class="sxs-lookup"><span data-stu-id="06ae9-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="06ae9-107">배열: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="06ae9-107">array : 'TElement[]</span></span>

<span data-ttu-id="06ae9-108">해당 요소를 열거할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="06ae9-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="06ae9-109">Output: ([Int](xref:microsoft.quantum.lang-ref.int), ' TElement) []</span><span class="sxs-lookup"><span data-stu-id="06ae9-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="06ae9-110">인덱스와 함께 원래 배열의 요소를 포함 하는 새 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="06ae9-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="06ae9-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="06ae9-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="06ae9-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="06ae9-112">'TElement</span></span>

<span data-ttu-id="06ae9-113">배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="06ae9-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="06ae9-114">예</span><span class="sxs-lookup"><span data-stu-id="06ae9-114">Example</span></span>

<span data-ttu-id="06ae9-115">다음 `for` 루프는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ae9-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) {
    let element = array[idx];
    ...
}
for ((idx, element) in Enumerated(array)) { ... }
```