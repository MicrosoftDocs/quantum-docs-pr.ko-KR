---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: _JordanWignerClusterOperatorFunction 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 58b0c7ad2216b1f58b9ea2765494b85fab4e1ff9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714659"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a><span data-ttu-id="b200c-102">_JordanWignerClusterOperatorFunction 함수</span><span class="sxs-lookup"><span data-stu-id="b200c-102">_JordanWignerClusterOperatorFunction function</span></span>

<span data-ttu-id="b200c-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="b200c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="b200c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b200c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b200c-105">동적 생성기를 simulatable 게이트 집합으로, JordanWigner 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b200c-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="b200c-106">입력</span><span class="sxs-lookup"><span data-stu-id="b200c-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="b200c-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="b200c-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="b200c-108">JordanWigner에서 단일 진화로 나타낼 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="b200c-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="b200c-109">출력: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="b200c-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="b200c-110">`EvolutionUnitary`' GeneratorIndex '에서 참조 되는 용어의 시간-진화를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="b200c-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>