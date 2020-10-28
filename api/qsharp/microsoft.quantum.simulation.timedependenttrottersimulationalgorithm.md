---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: TimeDependentTrotterSimulationAlgorithm 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 6129d768276b5c9d96a1b1ed9cd5a6a22d28e286
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719869"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="dba24-102">TimeDependentTrotterSimulationAlgorithm 함수</span><span class="sxs-lookup"><span data-stu-id="dba24-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="dba24-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="dba24-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="dba24-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dba24-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dba24-105">`TimeDependentSimulationAlgorithm` Trotter – Suzuki 분해를 사용 하 여 시간 종속 Schrodinger 수식을 해결 하는 단일 연산자를 대략적으로 계산 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="dba24-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="dba24-106">입력</span><span class="sxs-lookup"><span data-stu-id="dba24-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="dba24-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dba24-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dba24-108">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba24-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="dba24-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dba24-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dba24-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="dba24-110">Order of Trotter integrator.</span></span> <span data-ttu-id="dba24-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba24-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="dba24-112">출력: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="dba24-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="dba24-113">`TimeDependentSimulationAlgorithm` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dba24-113">A `TimeDependentSimulationAlgorithm` type.</span></span>