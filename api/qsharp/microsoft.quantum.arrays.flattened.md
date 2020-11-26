---
uid: Microsoft.Quantum.Arrays.Flattened
title: 평면화 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 331b1714109259b21982e99d030aa0662e3aaadb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221218"
---
# <a name="flattened-function"></a><span data-ttu-id="db9ff-102">평면화 함수</span><span class="sxs-lookup"><span data-stu-id="db9ff-102">Flattened function</span></span>

<span data-ttu-id="db9ff-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="db9ff-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="db9ff-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="db9ff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="db9ff-105">배열의 배열이 지정 된 경우 모든 배열의 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9ff-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="db9ff-106">입력</span><span class="sxs-lookup"><span data-stu-id="db9ff-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="db9ff-107">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="db9ff-107">arrays : 'T[][]</span></span>

<span data-ttu-id="db9ff-108">배열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="db9ff-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="db9ff-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="db9ff-109">Output : 'T[]</span></span>

<span data-ttu-id="db9ff-110">모든 배열의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="db9ff-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="db9ff-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="db9ff-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="db9ff-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="db9ff-112">'T</span></span>

<span data-ttu-id="db9ff-113">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="db9ff-113">The type of `array` elements.</span></span>