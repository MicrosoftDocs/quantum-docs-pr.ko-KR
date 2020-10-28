---
uid: Microsoft.Quantum.Arrays.Unzipped
title: 압축이 풀린 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 37c960dc5dbdb8099fbebe1ad63cb44ce642733c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718789"
---
# <a name="unzipped-function"></a><span data-ttu-id="5f884-102">압축이 풀린 함수</span><span class="sxs-lookup"><span data-stu-id="5f884-102">Unzipped function</span></span>

<span data-ttu-id="5f884-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5f884-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5f884-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5f884-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5f884-105">2 튜플 배열이 지정 된 경우 각각 입력 배열의 튜플 요소를 포함 하는 두 배열의 튜플을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f884-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="5f884-106">입력</span><span class="sxs-lookup"><span data-stu-id="5f884-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="5f884-107">arr: (' t ', ' U) []</span><span class="sxs-lookup"><span data-stu-id="5f884-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="5f884-108">2 개의 튜플을 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5f884-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="5f884-109">Output: (' ' ', ' U [])</span><span class="sxs-lookup"><span data-stu-id="5f884-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="5f884-110">첫 번째 배열은 입력 튜플의 모든 첫 번째 요소를 포함 하 고 두 번째 배열은 입력 튜플의 두 번째 요소를 모두 포함 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5f884-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5f884-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5f884-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5f884-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="5f884-112">'T</span></span>

<span data-ttu-id="5f884-113">각 튜플에 있는 첫 번째 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f884-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="5f884-114">' U</span><span class="sxs-lookup"><span data-stu-id="5f884-114">'U</span></span>

<span data-ttu-id="5f884-115">각 튜플에서 두 번째 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f884-115">The type of the second element in each tuple</span></span>

## <a name="see-also"></a><span data-ttu-id="5f884-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5f884-116">See Also</span></span>

- [<span data-ttu-id="5f884-117">Microsoft.Quantum.Arrays.Zip예: ped</span><span class="sxs-lookup"><span data-stu-id="5f884-117">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)