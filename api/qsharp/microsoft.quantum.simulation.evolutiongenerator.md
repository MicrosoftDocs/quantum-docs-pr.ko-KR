---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: EvolutionGenerator 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: 98241f77bfbd73929896bb114fad060001016a86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856078"
---
# <a name="evolutiongenerator-user-defined-type"></a><span data-ttu-id="e9e95-102">EvolutionGenerator 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="e9e95-102">EvolutionGenerator user defined type</span></span>

<span data-ttu-id="e9e95-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e9e95-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e9e95-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e9e95-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e9e95-105">동적 생성기를 simulatable 게이트 집합으로 표시 하 고이를 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e9e95-105">Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.</span></span>

<span data-ttu-id="e9e95-106">용어 수의 마지막 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9e95-106">Last parameter for number of terms.</span></span>

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```

