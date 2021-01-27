---
uid: Microsoft.Quantum.Arrays.Where
title: Where 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 4a938114689177f7a9ee182e6e5f36debe4edac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842210"
---
# <a name="where-function"></a><span data-ttu-id="1d989-102">Where 함수</span><span class="sxs-lookup"><span data-stu-id="1d989-102">Where function</span></span>

<span data-ttu-id="1d989-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1d989-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1d989-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d989-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d989-105">조건자와 배열이 지정 된 경우 조건자가 true 인 배열의 인덱스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d989-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="1d989-106">입력</span><span class="sxs-lookup"><span data-stu-id="1d989-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="1d989-107">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1d989-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1d989-108">에서 요소를 `'T` 필터링 하는 데 사용 되는 부울로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="1d989-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="1d989-109">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="1d989-109">array : 'T[]</span></span>

<span data-ttu-id="1d989-110">에 있는 요소의 배열 `'T` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1d989-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="1d989-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1d989-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1d989-112">이 true 인 인덱스의 배열입니다 `predicate` .</span><span class="sxs-lookup"><span data-stu-id="1d989-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1d989-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d989-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1d989-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="1d989-114">'T</span></span>

<span data-ttu-id="1d989-115">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1d989-115">The type of `array` elements.</span></span>