---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: InterpolatedEvolution 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 18026b9872f6a3344a1e5c2122f55927975ccb59
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710585"
---
# <a name="interpolatedevolution-function"></a><span data-ttu-id="ebf9f-102">InterpolatedEvolution 함수</span><span class="sxs-lookup"><span data-stu-id="ebf9f-102">InterpolatedEvolution function</span></span>

<span data-ttu-id="ebf9f-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ebf9f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ebf9f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ebf9f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ebf9f-105">균일 한 일정을 사용 하 여 두 생성기 간을 보간합니다. 결과 시간 종속 생성기에서 시뮬레이션 된 진화를 원하는 비트 레지스터에 적용 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebf9f-105">Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.</span></span>

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="ebf9f-106">입력</span><span class="sxs-lookup"><span data-stu-id="ebf9f-106">Input</span></span>

### <a name="interpolationtime--double"></a><span data-ttu-id="ebf9f-107">interpolationTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ebf9f-107">interpolationTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ebf9f-108">보간을 수행할 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf9f-108">Time to perform the interpolation over.</span></span>


### <a name="evolutiongeneratorstart--evolutiongenerator"></a><span data-ttu-id="ebf9f-109">evolutionGeneratorStart: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="ebf9f-109">evolutionGeneratorStart : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="ebf9f-110">진화를 시뮬레이션 하는 초기 생성기입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf9f-110">Initial generator to simulate evolution under.</span></span>


### <a name="evolutiongeneratorend--evolutiongenerator"></a><span data-ttu-id="ebf9f-111">evolutionGeneratorEnd: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="ebf9f-111">evolutionGeneratorEnd : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="ebf9f-112">에서 발전을 시뮬레이트하는 최종 생성기입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf9f-112">Final generator to simulate evolution under.</span></span>


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a><span data-ttu-id="ebf9f-113">timeDependentSimulationAlgorithm: [timeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="ebf9f-113">timeDependentSimulationAlgorithm : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="ebf9f-114">균일 한 보간 일정 중에 진화를 시뮬레이션 하는 데 사용 되는 시간 종속 시뮬레이션 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="ebf9f-114">A time-dependent simulation algorithm that will be used to simulate evolution during the uniform interpolation schedule.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="ebf9f-115">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="ebf9f-115">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="ebf9f-116">설명</span><span class="sxs-lookup"><span data-stu-id="ebf9f-116">Remarks</span></span>

<span data-ttu-id="ebf9f-117">보간 시간이 adiabatic 조건을 충족 하도록 선택 된 경우이 함수는 최종 동적 생성기에 대해 adiabatic 상태 준비를 수행 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebf9f-117">If the interpolation time is chosen to meet the adiabatic conditions, then this function returns an operation which performs adiabatic state preparation for the final dynamical generator.</span></span>