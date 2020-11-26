---
uid: Microsoft.Quantum.Simulation.EvolutionSchedule
title: EvolutionSchedule 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSchedule
qsharp.summary: >-
  Represents a time-dependent dynamical generator.

  The `Double` parameter is a schedule in $[0, 1]$.
ms.openlocfilehash: f99c72a44acc3fdcd9c0f182b51d9437b5e6606d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225298"
---
# <a name="evolutionschedule-user-defined-type"></a><span data-ttu-id="c5d16-102">EvolutionSchedule 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="c5d16-102">EvolutionSchedule user defined type</span></span>

<span data-ttu-id="c5d16-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c5d16-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c5d16-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c5d16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c5d16-105">시간 종속 동적 생성기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c5d16-105">Represents a time-dependent dynamical generator.</span></span>

<span data-ttu-id="c5d16-106">`Double`매개 변수는 $ [0, 1] $의 일정입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d16-106">The `Double` parameter is a schedule in $[0, 1]$.</span></span>

```qsharp

newtype EvolutionSchedule = (Microsoft.Quantum.Simulation.EvolutionSet, (Double -> Microsoft.Quantum.Simulation.GeneratorSystem));
```

