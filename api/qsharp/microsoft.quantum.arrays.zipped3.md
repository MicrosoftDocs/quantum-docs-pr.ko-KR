---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Zipped3 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: 6a4ffaeff8e6248a708ab9f8f9a6ff0c2e9e08d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842189"
---
# <a name="zipped3-function"></a><span data-ttu-id="5f226-102">Zipped3 함수</span><span class="sxs-lookup"><span data-stu-id="5f226-102">Zipped3 function</span></span>

<span data-ttu-id="5f226-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5f226-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5f226-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f226-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f226-105">3 개의 배열이 지정 된 경우 각 3 튜플은 각 원래 배열의 요소를 포함 하도록 3 튜플의 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="5f226-106">입력</span><span class="sxs-lookup"><span data-stu-id="5f226-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="5f226-107">first: ' t 1 []</span><span class="sxs-lookup"><span data-stu-id="5f226-107">first : 'T1[]</span></span>

<span data-ttu-id="5f226-108">각 튜플의 첫 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="5f226-109">second: ' 2 []</span><span class="sxs-lookup"><span data-stu-id="5f226-109">second : 'T2[]</span></span>

<span data-ttu-id="5f226-110">각 튜플의 두 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="5f226-111">세 번째: ' t 3 []</span><span class="sxs-lookup"><span data-stu-id="5f226-111">third : 'T3[]</span></span>

<span data-ttu-id="5f226-112">각 튜플의 세 번째 요소에 대 한 값을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="5f226-113">출력: (' 0 ', ' 2 ', ' t 3) []</span><span class="sxs-lookup"><span data-stu-id="5f226-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="5f226-114">각각에 대 한 폼의 3 개 튜플을 포함 하는 배열 `(first[idx], second[idx], third[idx])` `idx` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="5f226-115">세 배열의 길이가 같지 않은 경우 출력은 입력 중 짧은 값 만큼 길어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5f226-116">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5f226-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="5f226-117">' 1 '</span><span class="sxs-lookup"><span data-stu-id="5f226-117">'T1</span></span>

<span data-ttu-id="5f226-118">첫 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="5f226-119">' 2 '</span><span class="sxs-lookup"><span data-stu-id="5f226-119">'T2</span></span>

<span data-ttu-id="5f226-120">두 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="5f226-121">' T 3</span><span class="sxs-lookup"><span data-stu-id="5f226-121">'T3</span></span>

<span data-ttu-id="5f226-122">세 번째 배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f226-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f226-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5f226-123">See Also</span></span>

- [<span data-ttu-id="5f226-124">Microsoft.Quantum.Arrays.Zip예: ped</span><span class="sxs-lookup"><span data-stu-id="5f226-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="5f226-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="5f226-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)