---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: LookupFunction 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: c929054b96ee499db896cacf0e3ae4da6f6c4b98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719072"
---
# <a name="lookupfunction-function"></a><span data-ttu-id="ea822-102">LookupFunction 함수</span><span class="sxs-lookup"><span data-stu-id="ea822-102">LookupFunction function</span></span>

<span data-ttu-id="ea822-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ea822-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ea822-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ea822-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ea822-105">배열이 지정 된 경우 해당 배열의 요소를 반환 하는 함수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea822-105">Given an array, returns a function which returns elements of that array.</span></span>

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a><span data-ttu-id="ea822-106">입력</span><span class="sxs-lookup"><span data-stu-id="ea822-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="ea822-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="ea822-107">array : 'T[]</span></span>

<span data-ttu-id="ea822-108">조회 함수로 나타낼 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ea822-108">The array to be represented as a lookup function.</span></span>



## <a name="output--int---t"></a><span data-ttu-id="ea822-109">출력: [Int](xref:microsoft.quantum.lang-ref.int) > ' t '</span><span class="sxs-lookup"><span data-stu-id="ea822-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="ea822-110">이에 `f` 해당 하는 함수 `f(idx) == f[idx]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="ea822-110">A function `f` such that `f(idx) == f[idx]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ea822-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea822-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ea822-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="ea822-112">'T</span></span>

<span data-ttu-id="ea822-113">조회 함수로 표시 되는 배열의 요소 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ea822-113">The type of the elements of the array being represented as a lookup function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea822-114">설명</span><span class="sxs-lookup"><span data-stu-id="ea822-114">Remarks</span></span>

<span data-ttu-id="ea822-115">이 함수는 함수 및 함수를 인수로 사용 하는 작업과의 상호 운용을 위해 주로 유용 `Int -> 'T` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea822-115">This function is mainly useful for interoperating with functions and operations that take `Int -> 'T` functions as their arguments.</span></span> <span data-ttu-id="ea822-116">예를 들어, 함수를 사용 하 여 전체 배열을 메모리에 기록할 필요가 없도록 하는 생성기 표현 라이브러리에서 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="ea822-116">This is common, for instance, in the generator representation library, where functions are used to avoid the need to record an entire array in memory.</span></span>