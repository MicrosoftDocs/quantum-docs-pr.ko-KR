---
uid: Microsoft.Quantum.Arrays.Reversed
title: 반전 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 99244195e581dc00db24b938f5aa1c541cd4433a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718909"
---
# <a name="reversed-function"></a><span data-ttu-id="5fb8f-102">반전 함수</span><span class="sxs-lookup"><span data-stu-id="5fb8f-102">Reversed function</span></span>

<span data-ttu-id="5fb8f-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5fb8f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5fb8f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fb8f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5fb8f-105">입력 배열과 동일한 요소가 포함 된 배열을 역순으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="5fb8f-106">입력</span><span class="sxs-lookup"><span data-stu-id="5fb8f-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="5fb8f-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="5fb8f-107">array : 'T[]</span></span>

<span data-ttu-id="5fb8f-108">요소가 역순으로 복사 될 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="5fb8f-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="5fb8f-109">Output : 'T[]</span></span>

<span data-ttu-id="5fb8f-110">요소가 포함 된 배열입니다 `array[Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="5fb8f-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="5fb8f-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5fb8f-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fb8f-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5fb8f-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="5fb8f-113">'T</span></span>

<span data-ttu-id="5fb8f-114">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-114">The type of the array elements.</span></span>