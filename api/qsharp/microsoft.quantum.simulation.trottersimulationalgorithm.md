---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: TrotterSimulationAlgorithm 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: aa8338ab359441765db72a12f84a3a51e5bee3ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192539"
---
# <a name="trottersimulationalgorithm-function"></a><span data-ttu-id="9a7fb-102">TrotterSimulationAlgorithm 함수</span><span class="sxs-lookup"><span data-stu-id="9a7fb-102">TrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="9a7fb-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9a7fb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9a7fb-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9a7fb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9a7fb-105">`SimulationAlgorithm` Trotter – Suzuki 분해를 사용 하 여 시간-진화 연산자 _exp (-iHt)_ 에 근사치를 적용 하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7fb-105">`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.</span></span>

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="9a7fb-106">입력</span><span class="sxs-lookup"><span data-stu-id="9a7fb-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="9a7fb-107">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9a7fb-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9a7fb-108">시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7fb-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="9a7fb-109">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a7fb-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9a7fb-110">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7fb-110">Order of Trotter integrator.</span></span> <span data-ttu-id="9a7fb-111">이 값은 1 또는 짝수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7fb-111">This must be either 1 or an even number.</span></span>



## <a name="output--simulationalgorithm"></a><span data-ttu-id="9a7fb-112">출력: [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="9a7fb-112">Output : [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span></span>

<span data-ttu-id="9a7fb-113">`SimulationAlgorithm` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7fb-113">A `SimulationAlgorithm` type.</span></span>