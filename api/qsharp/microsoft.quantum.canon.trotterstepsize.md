---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: TrotterStepSize 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204694"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="57393-102">TrotterStepSize 함수</span><span class="sxs-lookup"><span data-stu-id="57393-102">TrotterStepSize function</span></span>

<span data-ttu-id="57393-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="57393-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="57393-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="57393-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="57393-105">Trotter 시뮬레이션 알고리즘의 재귀적 구현에서 Trotter step 크기를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="57393-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="57393-106">입력</span><span class="sxs-lookup"><span data-stu-id="57393-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="57393-107">순서: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57393-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="57393-108">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="57393-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="57393-109">설명</span><span class="sxs-lookup"><span data-stu-id="57393-109">Remarks</span></span>

<span data-ttu-id="57393-110">이 [작업은 다른](https://arxiv.org/abs/quant-ph/0508139)인덱싱 규칙을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57393-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="57393-111">특히 `DecomposedIntoTimeStepsCA(_, 4)` 은 _2/0508139의 스칼라 $p (\lambda) $에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="57393-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>