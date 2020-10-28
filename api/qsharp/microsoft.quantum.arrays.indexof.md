---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719173"
---
# <a name="indexof-function"></a><span data-ttu-id="8abbf-102">IndexOf 함수</span><span class="sxs-lookup"><span data-stu-id="8abbf-102">IndexOf function</span></span>

<span data-ttu-id="8abbf-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8abbf-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8abbf-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8abbf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8abbf-105">배열에서 지정 된 조건자를 만족 하는 첫 번째 요소의 첫 번째 인덱스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8abbf-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="8abbf-106">이러한 요소가 없는 경우-1을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8abbf-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="8abbf-107">입력</span><span class="sxs-lookup"><span data-stu-id="8abbf-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="8abbf-108">조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8abbf-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8abbf-109">배열의 요소에 대해 작동 하는 조건자 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="8abbf-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="8abbf-110">arr: ' t []</span><span class="sxs-lookup"><span data-stu-id="8abbf-110">arr : 'T[]</span></span>

<span data-ttu-id="8abbf-111">지정 된 조건자를 사용 하 여 검색할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8abbf-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="8abbf-112">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8abbf-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8abbf-113">True 인 가장 작은 인덱스 이거나 `idx` `predicate(arr[idx])` , 이러한 요소가 없는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="8abbf-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8abbf-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8abbf-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8abbf-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="8abbf-115">'T</span></span>

