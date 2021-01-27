---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: TrotterStepImpl 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: 33dc922cd5a60590a1306369fb99615fc6575b22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856737"
---
# <a name="trotterstepimpl-operation"></a><span data-ttu-id="688d5-102">TrotterStepImpl 작업</span><span class="sxs-lookup"><span data-stu-id="688d5-102">TrotterStepImpl operation</span></span>

<span data-ttu-id="688d5-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="688d5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="688d5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="688d5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="688d5-105">에 포함 된 용어에의 한 시간 혁신을 구현 `GeneratorSystem` 합니다.</span><span class="sxs-lookup"><span data-stu-id="688d5-105">Implements time-evolution by a term contained in a `GeneratorSystem`.</span></span>

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="688d5-106">입력</span><span class="sxs-lookup"><span data-stu-id="688d5-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="688d5-107">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="688d5-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="688d5-108">시뮬레이트할 시스템에 대 한 전체 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="688d5-108">A complete description of the system to be simulated.</span></span>


### <a name="idx--int"></a><span data-ttu-id="688d5-109">idx: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="688d5-109">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="688d5-110">설명 된 시스템의 용어에 대 한 정수 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="688d5-110">Integer index to a term in the described system.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="688d5-111">stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="688d5-111">stepsize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="688d5-112">시간 (시간)에 대 한 승수-로 인덱싱된 용어로 진화 `idx` 합니다.</span><span class="sxs-lookup"><span data-stu-id="688d5-112">Multiplier on duration of time-evolution by term indexed by `idx`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="688d5-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="688d5-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="688d5-114">이벤트가 시뮬레이션에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="688d5-114">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="688d5-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="688d5-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

