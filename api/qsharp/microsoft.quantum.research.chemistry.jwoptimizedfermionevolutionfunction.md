---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: JWOptimizedFermionEvolutionFunction 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: 952f3dc4ab0595ace0ee34c040cb21969afa111f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710802"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="0c976-102">JWOptimizedFermionEvolutionFunction 함수</span><span class="sxs-lookup"><span data-stu-id="0c976-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="0c976-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="0c976-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="0c976-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0c976-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0c976-105">동적 생성기를 simulatable 게이트 집합으로 나타내고 JWOptimized 된 단위로 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c976-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="0c976-106">입력</span><span class="sxs-lookup"><span data-stu-id="0c976-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="0c976-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="0c976-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="0c976-108">JWOptimized 된 기준에서 단일 진화로 나타낼 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="0c976-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="0c976-109">Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0c976-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0c976-110">시간 진화의 부호를 결정 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="0c976-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="0c976-111">출력: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="0c976-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="0c976-112">`EvolutionUnitary`' GeneratorIndex '에서 참조 되는 용어의 시간-진화를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="0c976-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>