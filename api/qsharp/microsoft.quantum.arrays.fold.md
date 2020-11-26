---
uid: Microsoft.Quantum.Arrays.Fold
title: 접기 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221167"
---
# <a name="fold-function"></a><span data-ttu-id="badd3-102">접기 함수</span><span class="sxs-lookup"><span data-stu-id="badd3-102">Fold function</span></span>

<span data-ttu-id="badd3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="badd3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="badd3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="badd3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="badd3-105">배열을 통해 함수를 반복 `f` `array` 하 여를 반환 `f(f(f(initialState, array[0]), array[1]), ...)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="badd3-106">입력</span><span class="sxs-lookup"><span data-stu-id="badd3-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="badd3-107">폴더: (' 상태, ' ')-> ' 상태</span><span class="sxs-lookup"><span data-stu-id="badd3-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="badd3-108">배열에 대해 접힌 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="badd3-109">상태: ' 상태 '</span><span class="sxs-lookup"><span data-stu-id="badd3-109">state : 'State</span></span>

<span data-ttu-id="badd3-110">폴더의 초기 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="badd3-111">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="badd3-111">array : 'T[]</span></span>

<span data-ttu-id="badd3-112">접을 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="badd3-113">출력: ' 상태</span><span class="sxs-lookup"><span data-stu-id="badd3-113">Output : 'State</span></span>

<span data-ttu-id="badd3-114">의 모든 요소를 반복한 후 폴더에서 반환 되는 최종 상태 `array` 입니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="badd3-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="badd3-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="badd3-116">' 상태</span><span class="sxs-lookup"><span data-stu-id="badd3-116">'State</span></span>

<span data-ttu-id="badd3-117">함수가 작동 하는 상태 유형 (예:)은 `folder` 첫 번째 인수로 수락 하 고를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="badd3-118">없습니다</span><span class="sxs-lookup"><span data-stu-id="badd3-118">'T</span></span>

<span data-ttu-id="badd3-119">`array`요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="badd3-119">The type of `array` elements.</span></span>