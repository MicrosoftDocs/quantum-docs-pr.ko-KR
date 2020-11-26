---
uid: Microsoft.Quantum.Arrays.Unique
title: Unique 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: 7964d5d41eb68cb05f9414164d69496c1f76eb08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220011"
---
# <a name="unique-function"></a><span data-ttu-id="2e152-102">Unique 함수</span><span class="sxs-lookup"><span data-stu-id="2e152-102">Unique function</span></span>

<span data-ttu-id="2e152-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2e152-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2e152-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e152-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e152-105">인접 한 요소가 없는 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e152-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="2e152-106">Description</span><span class="sxs-lookup"><span data-stu-id="2e152-106">Description</span></span>

<span data-ttu-id="2e152-107">일부 요소 배열 및 테스트 같음을 지정 하는 경우이 함수는 요소의 상대 순서가 유지 되는 새 배열을 반환 하지만 동일한 모든 인접 요소가 단일 요소로만 필터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e152-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="2e152-108">입력</span><span class="sxs-lookup"><span data-stu-id="2e152-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="2e152-109">같음: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2e152-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2e152-110">`a`가 인 경우와 동일한 것으로 간주 되는 두 요소를 비교 하는 함수입니다 `b` `equal(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="2e152-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="2e152-111">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="2e152-111">array : 'T[]</span></span>

<span data-ttu-id="2e152-112">고유 요소에 대해 필터링 할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2e152-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="2e152-113">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="2e152-113">Output : 'T[]</span></span>

<span data-ttu-id="2e152-114">인접 한 요소가 없는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2e152-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2e152-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2e152-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2e152-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="2e152-116">'T</span></span>

<span data-ttu-id="2e152-117">에 있는 각 요소의 형식입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="2e152-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e152-118">설명</span><span class="sxs-lookup"><span data-stu-id="2e152-118">Remarks</span></span>

<span data-ttu-id="2e152-119">동일 하지만 서로 다른 여러 요소가 있는 경우 출력 배열에 여러 요소가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e152-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="2e152-120">과 함께이 함수 `Sorted` 를 사용 하 여 전체 고유 요소가 포함 된 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e152-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>