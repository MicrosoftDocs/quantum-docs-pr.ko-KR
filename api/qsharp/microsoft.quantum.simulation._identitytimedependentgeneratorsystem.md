---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: _IdentityTimeDependentGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710690"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="ad47b-102">_IdentityTimeDependentGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="ad47b-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="ad47b-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ad47b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ad47b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad47b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad47b-105">Hamiltonian와 일치 하는 생성기 시스템을 반환 합니다 `H(s) = 0` `s` . 여기서는 일정 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad47b-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="ad47b-106">입력</span><span class="sxs-lookup"><span data-stu-id="ad47b-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="ad47b-107">일정: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ad47b-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ad47b-108">이 입력은 무시 되며 사용자 정의 형식과의 일관성을 위해 정의 됩니다 <xref:microsoft.quantum.canon.timedependentgeneratorsystem> .</span><span class="sxs-lookup"><span data-stu-id="ad47b-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="ad47b-109">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="ad47b-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="ad47b-110">모든 $s $에 대해 Hamiltonian $H (s) = $0의 진화를 나타내는 생성기 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="ad47b-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>