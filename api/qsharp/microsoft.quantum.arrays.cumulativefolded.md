---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: CumulativeFolded 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: 95cd5233a09a1234bba4de9fe870b9d93c0f86a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846232"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="4004c-102">CumulativeFolded 함수</span><span class="sxs-lookup"><span data-stu-id="4004c-102">CumulativeFolded function</span></span>

<span data-ttu-id="4004c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4004c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4004c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4004c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4004c-105">매핑된 및 접기를 단일 함수로 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="4004c-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="4004c-106">설명</span><span class="sxs-lookup"><span data-stu-id="4004c-106">Description</span></span>

<span data-ttu-id="4004c-107">이 함수는 초기 상태 `fn` 에서 시작 하 여 배열을 통해 함수를 반복 하 `state` 고 초기 상태를 포함 하지 않고 모든 중간 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4004c-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="4004c-108">입력</span><span class="sxs-lookup"><span data-stu-id="4004c-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="4004c-109">fn: (' State, t)-> ' 상태</span><span class="sxs-lookup"><span data-stu-id="4004c-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="4004c-110">배열에 대해 접힌 함수</span><span class="sxs-lookup"><span data-stu-id="4004c-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="4004c-111">상태: ' 상태 '</span><span class="sxs-lookup"><span data-stu-id="4004c-111">state : 'State</span></span>

<span data-ttu-id="4004c-112">접은 초기 상태</span><span class="sxs-lookup"><span data-stu-id="4004c-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="4004c-113">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="4004c-113">array : 'T[]</span></span>

<span data-ttu-id="4004c-114">접기 될 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4004c-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="4004c-115">출력: ' State []</span><span class="sxs-lookup"><span data-stu-id="4004c-115">Output : 'State[]</span></span>

<span data-ttu-id="4004c-116">최종 상태를 포함 하지만 초기 상태를 포함 하지 않는 모든 중간 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4004c-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="4004c-117">출력 배열의 길이가와 같은 길이입니다 `array` .</span><span class="sxs-lookup"><span data-stu-id="4004c-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4004c-118">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4004c-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="4004c-119">' 상태</span><span class="sxs-lookup"><span data-stu-id="4004c-119">'State</span></span>

<span data-ttu-id="4004c-120">함수가 작동 하는 상태 유형 (예:)은 `fn` 첫 번째 입력으로 수락 하 고를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4004c-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="4004c-121">없습니다</span><span class="sxs-lookup"><span data-stu-id="4004c-121">'T</span></span>

<span data-ttu-id="4004c-122">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4004c-122">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="4004c-123">예제</span><span class="sxs-lookup"><span data-stu-id="4004c-123">Example</span></span>

```qsharp
// same as sums = [1, 3, 6, 10, 15]
let sums = CumulativeFolded(PlusI, 0, SequenceI(1, 5));
```