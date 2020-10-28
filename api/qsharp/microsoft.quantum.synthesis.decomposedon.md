---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: DecomposedOn 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725219"
---
# <a name="decomposedon-function"></a><span data-ttu-id="68e95-102">DecomposedOn 함수</span><span class="sxs-lookup"><span data-stu-id="68e95-102">DecomposedOn function</span></span>

<span data-ttu-id="68e95-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="68e95-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="68e95-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="68e95-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="68e95-105">변수에서 순열 분해</span><span class="sxs-lookup"><span data-stu-id="68e95-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="68e95-106">Description</span><span class="sxs-lookup"><span data-stu-id="68e95-106">Description</span></span>

<span data-ttu-id="68e95-107">순열 $ \pi $ ( `perm` ) 및 인덱스 $i $ ( `index` )이 지정 된 경우이 메서드는 세 개의 순열 $ ((\ pi_l, \ pi_r), \pi ') $를 반환 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소의 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="68e95-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="68e95-108">입력</span><span class="sxs-lookup"><span data-stu-id="68e95-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="68e95-109">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="68e95-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="68e95-110">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="68e95-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="68e95-111">Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="68e95-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

