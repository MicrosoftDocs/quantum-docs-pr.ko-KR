---
uid: Microsoft.Quantum.Arrays.Head
title: Head 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 7b26a9c414ab2caad70f96f3c26c2d1cf0b03e95
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719185"
---
# <a name="head-function"></a><span data-ttu-id="faeb1-102">Head 함수</span><span class="sxs-lookup"><span data-stu-id="faeb1-102">Head function</span></span>

<span data-ttu-id="faeb1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="faeb1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="faeb1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="faeb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="faeb1-105">배열의 첫 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faeb1-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="faeb1-106">입력</span><span class="sxs-lookup"><span data-stu-id="faeb1-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="faeb1-107">array: ' A []</span><span class="sxs-lookup"><span data-stu-id="faeb1-107">array : 'A[]</span></span>

<span data-ttu-id="faeb1-108">첫 번째 요소를 가져올 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="faeb1-108">Array of which the first element is taken.</span></span> <span data-ttu-id="faeb1-109">배열의 길이는 1 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="faeb1-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="faeb1-110">출력: ' A</span><span class="sxs-lookup"><span data-stu-id="faeb1-110">Output : 'A</span></span>

<span data-ttu-id="faeb1-111">배열의 첫 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="faeb1-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="faeb1-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="faeb1-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="faeb1-113">' A</span><span class="sxs-lookup"><span data-stu-id="faeb1-113">'A</span></span>

<span data-ttu-id="faeb1-114">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="faeb1-114">The type of the array elements.</span></span>