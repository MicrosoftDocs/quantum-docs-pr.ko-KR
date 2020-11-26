---
uid: Microsoft.Quantum.Simulation.PauliEvolutionFunction
title: PauliEvolutionFunction 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: e581cd4d0a3caf96bece9979a1d850aad7842727
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230364"
---
# <a name="paulievolutionfunction-function"></a><span data-ttu-id="6f077-102">PauliEvolutionFunction 함수</span><span class="sxs-lookup"><span data-stu-id="6f077-102">PauliEvolutionFunction function</span></span>

<span data-ttu-id="6f077-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6f077-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6f077-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f077-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6f077-105">동적 생성기를 simulatable 게이트 집합으로 나타내고 Pauli로 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f077-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="6f077-106">입력</span><span class="sxs-lookup"><span data-stu-id="6f077-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="6f077-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="6f077-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="6f077-108">Pauli 단위로 단일 진화로 나타낼 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="6f077-108">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="6f077-109">출력: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="6f077-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="6f077-110">`EvolutionUnitary`' GeneratorIndex '에서 참조 되는 용어의 시간-진화를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="6f077-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>