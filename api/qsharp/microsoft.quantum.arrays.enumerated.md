---
uid: Microsoft.Quantum.Arrays.Enumerated
title: 열거 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719305"
---
# <a name="enumerated-function"></a><span data-ttu-id="4b167-102">열거 함수</span><span class="sxs-lookup"><span data-stu-id="4b167-102">Enumerated function</span></span>

<span data-ttu-id="4b167-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4b167-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4b167-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4b167-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4b167-105">배열이 지정 된 경우 각 요소의 인덱스와 함께 원래 배열의 요소를 포함 하는 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b167-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="4b167-106">입력</span><span class="sxs-lookup"><span data-stu-id="4b167-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="4b167-107">배열: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="4b167-107">array : 'TElement[]</span></span>

<span data-ttu-id="4b167-108">해당 요소를 열거할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4b167-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="4b167-109">Output: ([Int](xref:microsoft.quantum.lang-ref.int), ' TElement) []</span><span class="sxs-lookup"><span data-stu-id="4b167-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="4b167-110">인덱스와 함께 원래 배열의 요소를 포함 하는 새 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4b167-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4b167-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b167-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="4b167-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="4b167-112">'TElement</span></span>

<span data-ttu-id="4b167-113">배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4b167-113">The type of elements of the array.</span></span>