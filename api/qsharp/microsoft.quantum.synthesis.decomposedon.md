---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: DecomposedOn 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: 79f952e7bc7ba9f5337cf5e7a625e0d270a2e17a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203232"
---
# <a name="decomposedon-function"></a><span data-ttu-id="7a164-102">DecomposedOn 함수</span><span class="sxs-lookup"><span data-stu-id="7a164-102">DecomposedOn function</span></span>

<span data-ttu-id="7a164-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7a164-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7a164-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7a164-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7a164-105">변수에서 순열 분해</span><span class="sxs-lookup"><span data-stu-id="7a164-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="7a164-106">Description</span><span class="sxs-lookup"><span data-stu-id="7a164-106">Description</span></span>

<span data-ttu-id="7a164-107">순열 $ \pi $ ( `perm` ) 및 인덱스 $i $ ( `index` )이 지정 된 경우이 메서드는 세 개의 순열 $ ((\ pi_l, \ pi_r), \pi ') $를 반환 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소의 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7a164-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="7a164-108">입력</span><span class="sxs-lookup"><span data-stu-id="7a164-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="7a164-109">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7a164-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="7a164-110">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a164-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="7a164-111">Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="7a164-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

