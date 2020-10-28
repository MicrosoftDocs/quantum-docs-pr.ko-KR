---
uid: Microsoft.Quantum.Simulation.IdentityTimeDependentGeneratorSystem
title: IdentityTimeDependentGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a time-dependent generator system consistent with the Hamiltonian `H(s) = 0`.
ms.openlocfilehash: d51794aacbcf13ab567ff6be4f5d6b04581833bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724519"
---
# <a name="identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="15a41-102">IdentityTimeDependentGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="15a41-102">IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="15a41-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="15a41-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="15a41-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="15a41-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="15a41-105">Hamiltonian와 일치 하는 시간 종속 생성기 시스템을 반환 합니다 `H(s) = 0` .</span><span class="sxs-lookup"><span data-stu-id="15a41-105">Returns a time-dependent generator system consistent with the Hamiltonian `H(s) = 0`.</span></span>

```qsharp
function IdentityTimeDependentGeneratorSystem () : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="15a41-106">출력: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="15a41-106">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="15a41-107">모든 $s $에 대해 Hamiltonian $H (s) = $0의 진화를 나타내는 시간 종속 생성기 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="15a41-107">A time dependent generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>