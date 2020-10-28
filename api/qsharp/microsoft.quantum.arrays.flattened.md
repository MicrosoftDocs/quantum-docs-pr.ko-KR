---
uid: Microsoft.Quantum.Arrays.Flattened
title: 평면화 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 91a35f0ac2c2f8609bac07734265fcf4e88bf50b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719240"
---
# <a name="flattened-function"></a><span data-ttu-id="b9653-102">평면화 함수</span><span class="sxs-lookup"><span data-stu-id="b9653-102">Flattened function</span></span>

<span data-ttu-id="b9653-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b9653-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b9653-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b9653-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b9653-105">배열의 배열이 지정 된 경우 모든 배열의 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9653-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b9653-106">입력</span><span class="sxs-lookup"><span data-stu-id="b9653-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="b9653-107">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="b9653-107">arrays : 'T[][]</span></span>

<span data-ttu-id="b9653-108">배열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b9653-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="b9653-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="b9653-109">Output : 'T[]</span></span>

<span data-ttu-id="b9653-110">모든 배열의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="b9653-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b9653-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9653-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b9653-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="b9653-112">'T</span></span>

<span data-ttu-id="b9653-113">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b9653-113">The type of `array` elements.</span></span>