---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionFunction
title: JordanWignerFermionFunction 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 7d29393293acfc1748a1805f339951b1ff0f9b10
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714029"
---
# <a name="jordanwignerfermionfunction-function"></a><span data-ttu-id="23140-102">JordanWignerFermionFunction 함수</span><span class="sxs-lookup"><span data-stu-id="23140-102">JordanWignerFermionFunction function</span></span>

<span data-ttu-id="23140-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="23140-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="23140-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23140-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23140-105">동적 생성기를 simulatable 게이트 집합으로, JordanWigner 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="23140-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function JordanWignerFermionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="23140-106">입력</span><span class="sxs-lookup"><span data-stu-id="23140-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="23140-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="23140-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="23140-108">JordanWigner에서 단일 진화로 나타낼 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="23140-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="23140-109">출력: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="23140-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="23140-110">`EvolutionUnitary`' GeneratorIndex '에서 참조 되는 용어의 시간-진화를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="23140-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>