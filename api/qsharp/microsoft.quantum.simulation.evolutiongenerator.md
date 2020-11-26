---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: EvolutionGenerator 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: 9e0fc5a232070c238aad943ab73f064999237c15
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229446"
---
# <a name="evolutiongenerator-user-defined-type"></a><span data-ttu-id="f03ca-102">EvolutionGenerator 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="f03ca-102">EvolutionGenerator user defined type</span></span>

<span data-ttu-id="f03ca-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="f03ca-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="f03ca-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f03ca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f03ca-105">동적 생성기를 simulatable 게이트 집합으로 표시 하 고이를 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f03ca-105">Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.</span></span>

<span data-ttu-id="f03ca-106">용어 수의 마지막 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f03ca-106">Last parameter for number of terms.</span></span>

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```

