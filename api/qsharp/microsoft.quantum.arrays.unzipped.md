---
uid: Microsoft.Quantum.Arrays.Unzipped
title: 압축이 풀린 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845377"
---
# <a name="unzipped-function"></a><span data-ttu-id="39cdb-102">압축이 풀린 함수</span><span class="sxs-lookup"><span data-stu-id="39cdb-102">Unzipped function</span></span>

<span data-ttu-id="39cdb-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="39cdb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="39cdb-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39cdb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39cdb-105">2 튜플 배열이 지정 된 경우 각각 입력 배열의 튜플 요소를 포함 하는 두 배열의 튜플을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cdb-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="39cdb-106">입력</span><span class="sxs-lookup"><span data-stu-id="39cdb-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="39cdb-107">arr: (' t ', ' U) []</span><span class="sxs-lookup"><span data-stu-id="39cdb-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="39cdb-108">2 개의 튜플을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="39cdb-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="39cdb-109">Output: (' ' ', ' U [])</span><span class="sxs-lookup"><span data-stu-id="39cdb-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="39cdb-110">첫 번째 배열은 입력 튜플의 모든 첫 번째 요소를 포함 하 고 두 번째 배열은 입력 튜플의 두 번째 요소를 모두 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="39cdb-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="39cdb-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="39cdb-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="39cdb-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="39cdb-112">'T</span></span>

<span data-ttu-id="39cdb-113">각 튜플에 있는 첫 번째 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="39cdb-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="39cdb-114">' U</span><span class="sxs-lookup"><span data-stu-id="39cdb-114">'U</span></span>

<span data-ttu-id="39cdb-115">각 튜플에서 두 번째 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="39cdb-115">The type of the second element in each tuple</span></span>

## <a name="example"></a><span data-ttu-id="39cdb-116">예제</span><span class="sxs-lookup"><span data-stu-id="39cdb-116">Example</span></span>

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a><span data-ttu-id="39cdb-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="39cdb-117">See Also</span></span>

- [<span data-ttu-id="39cdb-118">Microsoft.Quantum.Arrays.Zip예: ped</span><span class="sxs-lookup"><span data-stu-id="39cdb-118">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)