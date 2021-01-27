---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: SimulationAlgorithm 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: d7b233ee76d79072f59ecfd001245848cb780eec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851038"
---
# <a name="simulationalgorithm-user-defined-type"></a><span data-ttu-id="ec1fb-102">SimulationAlgorithm 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="ec1fb-102">SimulationAlgorithm user defined type</span></span>

<span data-ttu-id="ec1fb-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ec1fb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ec1fb-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec1fb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec1fb-105">시간 독립적 시뮬레이션 알고리즘을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-105">Represents a time-independent simulation algorithm.</span></span>

<span data-ttu-id="ec1fb-106">시간 독립적 시뮬레이션 기술은를 변환 합니다. <xref:microsoft.quantum.simulation.evolutiongenerator></span><span class="sxs-lookup"><span data-stu-id="ec1fb-106">A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator></span></span>
<span data-ttu-id="ec1fb-107">일정 시간 간격에 대 한 단일 시간 진화</span><span class="sxs-lookup"><span data-stu-id="ec1fb-107">to unitary time evolution for some time-interval.</span></span>

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```

