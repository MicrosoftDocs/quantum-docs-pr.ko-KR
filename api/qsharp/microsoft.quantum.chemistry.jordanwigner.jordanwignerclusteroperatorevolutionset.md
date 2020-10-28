---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerClusterOperatorEvolutionSet
title: JordanWignerClusterOperatorEvolutionSet 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerClusterOperatorEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 81a2a109be0b19da5aa0a3feca76966deabeb665
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714078"
---
# <a name="jordanwignerclusteroperatorevolutionset-function"></a><span data-ttu-id="8e4de-102">JordanWignerClusterOperatorEvolutionSet 함수</span><span class="sxs-lookup"><span data-stu-id="8e4de-102">JordanWignerClusterOperatorEvolutionSet function</span></span>

<span data-ttu-id="8e4de-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="8e4de-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="8e4de-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8e4de-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8e4de-105">동적 생성기를 simulatable 게이트 집합으로, JordanWigner 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8e4de-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function JordanWignerClusterOperatorEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a><span data-ttu-id="8e4de-106">출력: [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="8e4de-106">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="8e4de-107">`EvolutionSet` `GeneratorIndex` JordanWigner 기준에 대 한를 ' EvolutionUnitary에 매핑하는입니다.</span><span class="sxs-lookup"><span data-stu-id="8e4de-107">An `EvolutionSet` that maps a `GeneratorIndex` for the JordanWigner basis to an \`EvolutionUnitary.</span></span>