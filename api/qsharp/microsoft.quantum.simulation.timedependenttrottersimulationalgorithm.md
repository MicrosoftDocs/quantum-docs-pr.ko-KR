---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: TimeDependentTrotterSimulationAlgorithm 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 94bc606fdc46d77e8beb1470c78102a63e6d4e81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192777"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="ba173-102">TimeDependentTrotterSimulationAlgorithm 함수</span><span class="sxs-lookup"><span data-stu-id="ba173-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="ba173-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ba173-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ba173-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba173-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba173-105">`TimeDependentSimulationAlgorithm` Trotter – Suzuki 분해를 사용 하 여 시간 종속 Schrodinger 수식을 해결 하는 단일 연산자를 대략적으로 계산 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="ba173-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="ba173-106">입력</span><span class="sxs-lookup"><span data-stu-id="ba173-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="ba173-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ba173-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ba173-108">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba173-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="ba173-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ba173-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ba173-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="ba173-110">Order of Trotter integrator.</span></span> <span data-ttu-id="ba173-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba173-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="ba173-112">출력: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="ba173-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="ba173-113">`TimeDependentSimulationAlgorithm` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ba173-113">A `TimeDependentSimulationAlgorithm` type.</span></span>