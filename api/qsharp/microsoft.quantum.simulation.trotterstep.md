---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: TrotterStep 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 7a1a27ba4dc4b8b7bbc4da6a378d4a1494bc9415
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725352"
---
# <a name="trotterstep-function"></a><span data-ttu-id="9b21f-102">TrotterStep 함수</span><span class="sxs-lookup"><span data-stu-id="9b21f-102">TrotterStep function</span></span>

<span data-ttu-id="9b21f-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9b21f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9b21f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9b21f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9b21f-105">`EvolutionGenerator`Trotter – Suzuki 분해를 사용 하 여에 설명 된 시스템의 시간 진화의 단일 시간 단계를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b21f-105">Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.</span></span>

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9b21f-106">입력</span><span class="sxs-lookup"><span data-stu-id="9b21f-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="9b21f-107">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="9b21f-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="9b21f-108">시뮬레이트할 시스템에 대 한 전체 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9b21f-108">A complete description of the system to be simulated.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="9b21f-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b21f-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b21f-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="9b21f-110">Order of Trotter integrator.</span></span> <span data-ttu-id="9b21f-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b21f-111">This must be either 1 or an even number.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="9b21f-112">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9b21f-112">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9b21f-113">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b21f-113">Duration of simulated time-evolution in single Trotter step.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="9b21f-114">출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="9b21f-114">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="9b21f-115">기간에 대 한 단일 시간 진화의 단일 단계를 대략적으로 나타내는 단일 작업입니다 `trotterStepSize` .</span><span class="sxs-lookup"><span data-stu-id="9b21f-115">Unitary operation that approximates a single step of time-evolution for duration `trotterStepSize`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b21f-116">설명</span><span class="sxs-lookup"><span data-stu-id="9b21f-116">Remarks</span></span>

<span data-ttu-id="9b21f-117">Trotter – Suzuki 분해에 대 한 자세한 내용은 [시간이 지정 된 컴퍼지션](/quantum/libraries/control-flow#time-ordered-composition)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b21f-117">For more on the Trotter–Suzuki decomposition, see [Time-Ordered Composition](/quantum/libraries/control-flow#time-ordered-composition).</span></span>