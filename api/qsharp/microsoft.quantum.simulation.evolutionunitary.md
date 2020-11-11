---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: EvolutionUnitary 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: 28ab492573b67e4aa42392e4ee499596b9c0225f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724855"
---
# <a name="evolutionunitary-user-defined-type"></a><span data-ttu-id="5d9d3-102">EvolutionUnitary 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="5d9d3-102">EvolutionUnitary user defined type</span></span>

<span data-ttu-id="5d9d3-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5d9d3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5d9d3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5d9d3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5d9d3-105">단일 시간 진화 연산자를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-105">Represents a unitary time-evolution operator.</span></span>

<span data-ttu-id="5d9d3-106">첫 번째 매개 변수는 시간 진화의 기간 이며 두 번째 매개 변수는 단일에 의해 처리 되는 고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-106">The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.</span></span>

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```
