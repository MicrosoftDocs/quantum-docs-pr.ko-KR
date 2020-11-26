---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: EvolutionSet 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: ee8f3c0716f035dcb0c4fad557092fbf8dd3c356
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229412"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="968fc-102">EvolutionSet 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="968fc-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="968fc-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="968fc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="968fc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="968fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="968fc-105">시뮬레이션 알고리즘을 구현 하는 데 쉽게 구현 하 고 사용할 수 있는 게이트 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="968fc-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="968fc-106">집합의 요소는로 인덱싱됩니다.  <xref:microsoft.quantum.simulation.generatorindex> 각 집합은에 대 한 함수에서로 설명 됩니다 .이 함수는 `GeneratorIndex` 시간을  <xref:microsoft.quantum.simulation.evolutionunitary> 나타내는 실수에 의해 매개 변수화 된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="968fc-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

