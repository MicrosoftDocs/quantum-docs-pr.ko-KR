---
uid: Microsoft.Quantum.Arrays.Prefixes
title: 전위 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718940"
---
# <a name="prefixes-function"></a><span data-ttu-id="dc4ee-102">전위 함수</span><span class="sxs-lookup"><span data-stu-id="dc4ee-102">Prefixes function</span></span>

<span data-ttu-id="dc4ee-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dc4ee-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dc4ee-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc4ee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc4ee-105">배열이 지정 된 경우 모든 접두사를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc4ee-105">Given an array, returns all its prefixes.</span></span>

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="dc4ee-106">Description</span><span class="sxs-lookup"><span data-stu-id="dc4ee-106">Description</span></span>

<span data-ttu-id="dc4ee-107">전체 배열까지 첫 번째 요소만 포함 하는 배열부터 시작 하 여 모든 접두사의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc4ee-107">Returns an array of all prefixes, starting with an array that only has the first element until the complete array.</span></span>

## <a name="input"></a><span data-ttu-id="dc4ee-108">입력</span><span class="sxs-lookup"><span data-stu-id="dc4ee-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="dc4ee-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="dc4ee-109">array : 'T[]</span></span>

<span data-ttu-id="dc4ee-110">요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="dc4ee-110">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="dc4ee-111">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="dc4ee-111">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dc4ee-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc4ee-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dc4ee-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="dc4ee-113">'T</span></span>

<span data-ttu-id="dc4ee-114">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dc4ee-114">The type of `array` elements.</span></span>