---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: TimeDependentTrotterSimulationAlgorithmImpl 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: f4f8a9265dc25305819da5ae1002f02b7efd1952
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203453"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a><span data-ttu-id="86e8a-102">TimeDependentTrotterSimulationAlgorithmImpl 작업</span><span class="sxs-lookup"><span data-stu-id="86e8a-102">TimeDependentTrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="86e8a-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="86e8a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="86e8a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="86e8a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="86e8a-105">시간 종속 Schrödinger 방정식을 해결 하는 단일 연산자의 근사값을 위한 여러 Trotter 단계 구현.</span><span class="sxs-lookup"><span data-stu-id="86e8a-105">Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.</span></span>

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="86e8a-106">입력</span><span class="sxs-lookup"><span data-stu-id="86e8a-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="86e8a-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86e8a-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86e8a-108">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="86e8a-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="86e8a-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86e8a-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86e8a-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="86e8a-110">Order of Trotter integrator.</span></span> <span data-ttu-id="86e8a-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86e8a-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="86e8a-112">maxTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86e8a-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86e8a-113">$T 총 시뮬레이션 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="86e8a-113">Total duration of simulation $t$.</span></span>


### <a name="evolutionschedule--evolutionschedule"></a><span data-ttu-id="86e8a-114">evolutionSchedule: [evolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span><span class="sxs-lookup"><span data-stu-id="86e8a-114">evolutionSchedule : [EvolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span></span>

<span data-ttu-id="86e8a-115">시뮬레이트할 시간 종속 시스템의 전체 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="86e8a-115">A complete description of the time-dependent system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="86e8a-116">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="86e8a-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="86e8a-117">이벤트가 시뮬레이션에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86e8a-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="86e8a-118">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86e8a-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

