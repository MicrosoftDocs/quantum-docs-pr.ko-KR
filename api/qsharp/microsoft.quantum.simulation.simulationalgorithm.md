---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: SimulationAlgorithm 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: 9127a936bbf7a212e712645eabdf49fefc7a97d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725569"
---
# <a name="simulationalgorithm-user-defined-type"></a><span data-ttu-id="bb517-102">SimulationAlgorithm 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="bb517-102">SimulationAlgorithm user defined type</span></span>

<span data-ttu-id="bb517-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="bb517-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="bb517-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bb517-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bb517-105">시간 독립적 시뮬레이션 알고리즘을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bb517-105">Represents a time-independent simulation algorithm.</span></span>

<span data-ttu-id="bb517-106">시간 독립적 시뮬레이션 기술은를 변환 합니다. <xref:microsoft.quantum.simulation.evolutiongenerator></span><span class="sxs-lookup"><span data-stu-id="bb517-106">A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator></span></span>
<span data-ttu-id="bb517-107">일정 시간 간격에 대 한 단일 시간 진화</span><span class="sxs-lookup"><span data-stu-id="bb517-107">to unitary time evolution for some time-interval.</span></span>

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```
