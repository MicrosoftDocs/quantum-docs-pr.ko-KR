---
uid: Microsoft.Quantum.Arrays.Reversed
title: 반전 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 50699465711de45ff994095e6c098550d637d608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845467"
---
# <a name="reversed-function"></a><span data-ttu-id="f64b7-102">반전 함수</span><span class="sxs-lookup"><span data-stu-id="f64b7-102">Reversed function</span></span>

<span data-ttu-id="f64b7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f64b7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f64b7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f64b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f64b7-105">입력 배열과 동일한 요소가 포함 된 배열을 역순으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f64b7-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f64b7-106">입력</span><span class="sxs-lookup"><span data-stu-id="f64b7-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="f64b7-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="f64b7-107">array : 'T[]</span></span>

<span data-ttu-id="f64b7-108">요소가 역순으로 복사 될 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f64b7-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="f64b7-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="f64b7-109">Output : 'T[]</span></span>

<span data-ttu-id="f64b7-110">요소가 포함 된 배열입니다 `array[Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="f64b7-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="f64b7-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="f64b7-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f64b7-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f64b7-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f64b7-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="f64b7-113">'T</span></span>

<span data-ttu-id="f64b7-114">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f64b7-114">The type of the array elements.</span></span>