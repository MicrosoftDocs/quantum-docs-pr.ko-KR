---
uid: Microsoft.Quantum.Simulation.IdentityTimeDependentGeneratorSystem
title: IdentityTimeDependentGeneratorSystem 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a time-dependent generator system consistent with the Hamiltonian `H(s) = 0`.
ms.openlocfilehash: e25e01a1f16182ea55fabd325d200c8489df5953
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846797"
---
# <a name="identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="db9fc-102">IdentityTimeDependentGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="db9fc-102">IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="db9fc-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="db9fc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="db9fc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="db9fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="db9fc-105">Hamiltonian와 일치 하는 시간 종속 생성기 시스템을 반환 합니다 `H(s) = 0` .</span><span class="sxs-lookup"><span data-stu-id="db9fc-105">Returns a time-dependent generator system consistent with the Hamiltonian `H(s) = 0`.</span></span>

```qsharp
function IdentityTimeDependentGeneratorSystem () : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="db9fc-106">출력: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="db9fc-106">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="db9fc-107">모든 $s $에 대해 Hamiltonian $H (s) = $0의 진화를 나타내는 시간 종속 생성기 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-107">A time dependent generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>