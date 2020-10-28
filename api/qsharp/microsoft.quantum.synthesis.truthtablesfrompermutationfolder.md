---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: TruthTablesFromPermutationFolder 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 6b00c9e880ed7b7b3bf446dcb17dab3bab7a83a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724456"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="9a9ab-102">TruthTablesFromPermutationFolder 함수</span><span class="sxs-lookup"><span data-stu-id="9a9ab-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="9a9ab-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="9a9ab-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a9ab-105">단일 변수 인덱스의 분해 논리</span><span class="sxs-lookup"><span data-stu-id="9a9ab-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="9a9ab-106">Description</span><span class="sxs-lookup"><span data-stu-id="9a9ab-106">Description</span></span>

<span data-ttu-id="9a9ab-107">현재 상태를 사용 하 여 업데이트 된 순열을 생성 하 고 제어 되는 게이트에서 새 함수를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a9ab-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="9a9ab-108">입력</span><span class="sxs-lookup"><span data-stu-id="9a9ab-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="9a9ab-109">numVars: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="9a9ab-110">상태: [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="9a9ab-111">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="9a9ab-112">출력: [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>

