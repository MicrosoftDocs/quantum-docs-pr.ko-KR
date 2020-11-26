---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: d63b204334611f8f2c3860f9ee1d756f637780e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221014"
---
# <a name="indexof-function"></a><span data-ttu-id="6584e-102">IndexOf 함수</span><span class="sxs-lookup"><span data-stu-id="6584e-102">IndexOf function</span></span>

<span data-ttu-id="6584e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6584e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6584e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6584e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6584e-105">배열에서 지정 된 조건자를 만족 하는 첫 번째 요소의 첫 번째 인덱스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6584e-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="6584e-106">이러한 요소가 없는 경우-1을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6584e-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="6584e-107">입력</span><span class="sxs-lookup"><span data-stu-id="6584e-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="6584e-108">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6584e-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6584e-109">배열의 요소에 대해 작동 하는 조건자 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="6584e-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="6584e-110">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="6584e-110">arr : 'T[]</span></span>

<span data-ttu-id="6584e-111">지정 된 조건자를 사용 하 여 검색할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="6584e-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="6584e-112">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6584e-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6584e-113">True 인 가장 작은 인덱스 이거나 `idx` `predicate(arr[idx])` , 이러한 요소가 없는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="6584e-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6584e-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6584e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6584e-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="6584e-115">'T</span></span>

