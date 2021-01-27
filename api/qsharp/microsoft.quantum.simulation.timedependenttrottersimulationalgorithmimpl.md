---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: TimeDependentTrotterSimulationAlgorithmImpl 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: 3a23c14e8181eeaf1614dab6f8aa5a002364c2b8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847800"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a><span data-ttu-id="ccb40-102">TimeDependentTrotterSimulationAlgorithmImpl 작업</span><span class="sxs-lookup"><span data-stu-id="ccb40-102">TimeDependentTrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="ccb40-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ccb40-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ccb40-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ccb40-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ccb40-105">시간 종속 Schrödinger 방정식을 해결 하는 단일 연산자의 근사값을 위한 여러 Trotter 단계 구현.</span><span class="sxs-lookup"><span data-stu-id="ccb40-105">Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.</span></span>

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ccb40-106">입력</span><span class="sxs-lookup"><span data-stu-id="ccb40-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="ccb40-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ccb40-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ccb40-108">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb40-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="ccb40-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ccb40-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ccb40-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="ccb40-110">Order of Trotter integrator.</span></span> <span data-ttu-id="ccb40-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb40-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="ccb40-112">maxTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ccb40-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ccb40-113">$T 총 시뮬레이션 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="ccb40-113">Total duration of simulation $t$.</span></span>


### <a name="evolutionschedule--evolutionschedule"></a><span data-ttu-id="ccb40-114">evolutionSchedule: [evolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span><span class="sxs-lookup"><span data-stu-id="ccb40-114">evolutionSchedule : [EvolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span></span>

<span data-ttu-id="ccb40-115">시뮬레이트할 시간 종속 시스템의 전체 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ccb40-115">A complete description of the time-dependent system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="ccb40-116">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ccb40-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ccb40-117">이벤트가 시뮬레이션에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccb40-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ccb40-118">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ccb40-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

