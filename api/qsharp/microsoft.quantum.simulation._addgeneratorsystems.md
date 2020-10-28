---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: _AddGeneratorSystems 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: 3bce9faf229f3b1f683e060437ec08da795ef185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710711"
---
# <a name="_addgeneratorsystems-function"></a><span data-ttu-id="51204-102">_AddGeneratorSystems 함수</span><span class="sxs-lookup"><span data-stu-id="51204-102">_AddGeneratorSystems function</span></span>

<span data-ttu-id="51204-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="51204-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="51204-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51204-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51204-105">새를 `GeneratorSystem` 만드는 두 개의를 추가 `GeneratorSystem` 합니다.</span><span class="sxs-lookup"><span data-stu-id="51204-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="51204-106">입력</span><span class="sxs-lookup"><span data-stu-id="51204-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="51204-107">idxTerm: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51204-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsa--int"></a><span data-ttu-id="51204-108">nTermsA: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51204-108">nTermsA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsb--int"></a><span data-ttu-id="51204-109">nTermsB: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51204-109">nTermsB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="generatorindexfunctiona--int---generatorindex"></a><span data-ttu-id="51204-110">generatorIndexFunctionA: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="51204-110">generatorIndexFunctionA : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="generatorindexfunctionb--int---generatorindex"></a><span data-ttu-id="51204-111">generatorIndexFunctionB: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="51204-111">generatorIndexFunctionB : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>





## <a name="output--generatorindex"></a><span data-ttu-id="51204-112">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="51204-112">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>



## <a name="remarks"></a><span data-ttu-id="51204-113">설명</span><span class="sxs-lookup"><span data-stu-id="51204-113">Remarks</span></span>

<span data-ttu-id="51204-114">이는 중간 단계 이며 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51204-114">This is an intermediate step and should not be called.</span></span>