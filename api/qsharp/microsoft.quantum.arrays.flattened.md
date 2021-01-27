---
uid: Microsoft.Quantum.Arrays.Flattened
title: 평면화 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848627"
---
# <a name="flattened-function"></a><span data-ttu-id="16198-102">평면화 함수</span><span class="sxs-lookup"><span data-stu-id="16198-102">Flattened function</span></span>

<span data-ttu-id="16198-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="16198-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="16198-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="16198-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="16198-105">배열의 배열이 지정 된 경우 모든 배열의 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16198-105">Given an array of arrays, returns the concatenation of all arrays.</span></span>

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="16198-106">입력</span><span class="sxs-lookup"><span data-stu-id="16198-106">Input</span></span>

### <a name="arrays--t"></a><span data-ttu-id="16198-107">배열: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="16198-107">arrays : 'T[][]</span></span>

<span data-ttu-id="16198-108">배열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="16198-108">Array of arrays.</span></span>



## <a name="output--t"></a><span data-ttu-id="16198-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="16198-109">Output : 'T[]</span></span>

<span data-ttu-id="16198-110">모든 배열의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="16198-110">Concatenation of all arrays.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="16198-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="16198-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="16198-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="16198-112">'T</span></span>

<span data-ttu-id="16198-113">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="16198-113">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="16198-114">예제</span><span class="sxs-lookup"><span data-stu-id="16198-114">Example</span></span>

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```