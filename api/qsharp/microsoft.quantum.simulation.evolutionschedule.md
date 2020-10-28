---
uid: Microsoft.Quantum.Simulation.EvolutionSchedule
title: EvolutionSchedule 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSchedule
qsharp.summary: >-
  Represents a time-dependent dynamical generator.

  The `Double` parameter is a schedule in $[0, 1]$.
ms.openlocfilehash: 4dc8bf4028e82d3e746779ae8c7d400dcbd3ea1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710620"
---
# <a name="evolutionschedule-user-defined-type"></a><span data-ttu-id="95d39-102">EvolutionSchedule 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="95d39-102">EvolutionSchedule user defined type</span></span>

<span data-ttu-id="95d39-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="95d39-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="95d39-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="95d39-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="95d39-105">시간 종속 동적 생성기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-105">Represents a time-dependent dynamical generator.</span></span>

<span data-ttu-id="95d39-106">`Double`매개 변수는 $ [0, 1] $의 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="95d39-106">The `Double` parameter is a schedule in $[0, 1]$.</span></span>

```qsharp

newtype EvolutionSchedule = (Microsoft.Quantum.Simulation.EvolutionSet, (Double -> Microsoft.Quantum.Simulation.GeneratorSystem));
```

