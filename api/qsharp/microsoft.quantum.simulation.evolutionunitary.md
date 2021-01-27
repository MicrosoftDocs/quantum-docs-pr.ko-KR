---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: EvolutionUnitary 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: ea160bb9a0a8bb5106c3e37a6a16155bad71dd25
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856054"
---
# <a name="evolutionunitary-user-defined-type"></a><span data-ttu-id="c7fe7-102">EvolutionUnitary 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="c7fe7-102">EvolutionUnitary user defined type</span></span>

<span data-ttu-id="c7fe7-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c7fe7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c7fe7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7fe7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7fe7-105">단일 시간 진화 연산자를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c7fe7-105">Represents a unitary time-evolution operator.</span></span>

<span data-ttu-id="c7fe7-106">첫 번째 매개 변수는 시간 진화의 기간 이며 두 번째 매개 변수는 단일에 의해 처리 되는 고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="c7fe7-106">The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.</span></span>

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

