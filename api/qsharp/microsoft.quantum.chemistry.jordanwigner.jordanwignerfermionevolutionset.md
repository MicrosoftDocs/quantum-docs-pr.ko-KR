---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionEvolutionSet
title: JordanWignerFermionEvolutionSet 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: a43f9c27eb1e60fb072d5962c37816577a7b2879
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714036"
---
# <a name="jordanwignerfermionevolutionset-function"></a><span data-ttu-id="0014b-102">JordanWignerFermionEvolutionSet 함수</span><span class="sxs-lookup"><span data-stu-id="0014b-102">JordanWignerFermionEvolutionSet function</span></span>

<span data-ttu-id="0014b-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="0014b-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="0014b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0014b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0014b-105">동적 생성기를 simulatable 게이트 집합으로, JordanWigner 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0014b-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function JordanWignerFermionEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a><span data-ttu-id="0014b-106">출력: [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="0014b-106">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="0014b-107">`EvolutionSet` `GeneratorIndex` JordanWigner 기준에 대 한를 ' EvolutionUnitary에 매핑하는입니다.</span><span class="sxs-lookup"><span data-stu-id="0014b-107">An `EvolutionSet` that maps a `GeneratorIndex` for the JordanWigner basis to an \`EvolutionUnitary.</span></span>