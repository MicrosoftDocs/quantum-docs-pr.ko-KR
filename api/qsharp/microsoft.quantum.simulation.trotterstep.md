---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: TrotterStep 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 516b40ac9920a4a8acc09ad7f558db88dbeb41e8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192811"
---
# <a name="trotterstep-function"></a><span data-ttu-id="a5195-102">TrotterStep 함수</span><span class="sxs-lookup"><span data-stu-id="a5195-102">TrotterStep function</span></span>

<span data-ttu-id="a5195-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a5195-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a5195-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5195-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5195-105">`EvolutionGenerator`Trotter – Suzuki 분해를 사용 하 여에 설명 된 시스템의 시간 진화의 단일 시간 단계를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5195-105">Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.</span></span>

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a5195-106">입력</span><span class="sxs-lookup"><span data-stu-id="a5195-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="a5195-107">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="a5195-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="a5195-108">시뮬레이트할 시스템에 대 한 전체 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a5195-108">A complete description of the system to be simulated.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="a5195-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a5195-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a5195-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="a5195-110">Order of Trotter integrator.</span></span> <span data-ttu-id="a5195-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5195-111">This must be either 1 or an even number.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="a5195-112">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a5195-112">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a5195-113">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5195-113">Duration of simulated time-evolution in single Trotter step.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="a5195-114">출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="a5195-114">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a5195-115">기간에 대 한 단일 시간 진화의 단일 단계를 대략적으로 나타내는 단일 작업입니다 `trotterStepSize` .</span><span class="sxs-lookup"><span data-stu-id="a5195-115">Unitary operation that approximates a single step of time-evolution for duration `trotterStepSize`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5195-116">설명</span><span class="sxs-lookup"><span data-stu-id="a5195-116">Remarks</span></span>

<span data-ttu-id="a5195-117">Trotter – Suzuki 분해에 대 한 자세한 내용은 [시간이 지정 된 컴퍼지션](/quantum/libraries/control-flow#time-ordered-composition)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5195-117">For more on the Trotter–Suzuki decomposition, see [Time-Ordered Composition](/quantum/libraries/control-flow#time-ordered-composition).</span></span>