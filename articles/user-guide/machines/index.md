---
title: 퀀텀 시뮬레이터 및 Q# 프로그램
description: Q# 프로그램의 대상 컴퓨터로 사용할 수 있는 퀀텀 시뮬레이터에 대해 설명합니다.
author: QuantumWriter
ms.author: v-benbra
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6a2a4bb829301f9db9bd14f3240556a403b9a54f
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833430"
---
# <a name="quantum-simulators"></a><span data-ttu-id="7fb58-103">퀀텀 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="7fb58-103">Quantum simulators</span></span>

<span data-ttu-id="7fb58-104">퀀텀 시뮬레이터는 클래식 컴퓨터에서 실행되고 Q# 프로그램을 위한 *대상 컴퓨터* 역할을 하는 소프트웨어 프로그램으로, 큐비트가 다른 작업에 반응하는 방식을 예측하는 환경에서 퀀텀 프로그램을 실행하고 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-104">Quantum simulators are software programs that run on classical computers and act as the *target machine* for a Q# program, making it possible to run and test quantum programs in an environment that predicts how qubits will react to different operations.</span></span> <span data-ttu-id="7fb58-105">이 문서에서는 QDK(Quantum Development Kit)에 포함된 퀀텀 시뮬레이터와 명령줄을 통하거나 기존 언어로 작성된 드라이버 코드를 사용하여 Q# 프로그램을 퀀텀 시뮬레이터에 전달할 수 있는 다양한 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-105">This article describes which quantum simulators are included with the Quantum Development Kit (QDK), and different ways that you can pass a Q# program to the quantum simulators, for example, via the command line or by using driver code written in a classical language.</span></span>  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a><span data-ttu-id="7fb58-106">QDK(Quantum Development Kit) 퀀텀 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="7fb58-106">The Quantum Development Kit (QDK) quantum simulators</span></span>

<span data-ttu-id="7fb58-107">퀀텀 시뮬레이터는 알고리즘을 위한 퀀텀 기본 형식을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-107">The quantum simulator is responsible for providing implementations of quantum primitives for an algorithm.</span></span> <span data-ttu-id="7fb58-108">여기에는 `H`, `CNOT` 및 `Measure`와 같은 기본 작업뿐만 아니라, 큐비트 관리와 추적도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-108">This includes primitive operations such as `H`, `CNOT`, and `Measure`, as well as qubit management and tracking.</span></span> <span data-ttu-id="7fb58-109">QDK에는 동일한 퀀텀 알고리즘에 대해 여러 실행 모델을 나타내는 여러 클래스의 퀀텀 시뮬레이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-109">The QDK includes different classes of quantum simulators representing different run models for the same quantum algorithm.</span></span> 


<span data-ttu-id="7fb58-110">각 유형의 퀀텀 시뮬레이터는 이러한 기본 형식의 다른 구현을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-110">Each type of quantum simulator can provide different implementations of these primitives.</span></span> <span data-ttu-id="7fb58-111">예를 들어, [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)는 [퀀텀 상태 벡터](xref:microsoft.quantum.glossary#quantum-state)를 완전히 시뮬레이션하여 퀀텀 알고리즘을 실행하는 반면 [양자 컴퓨터 추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)는 실제 퀀텀 상태를 전혀 고려하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-111">For example, the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator) runs the quantum algorithm by fully simulating the [quantum state vector](xref:microsoft.quantum.glossary#quantum-state), whereas the [quantum computer trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) doesn't consider the actual quantum state at all.</span></span> <span data-ttu-id="7fb58-112">대신 알고리즘에 대한 게이트, 큐비트 및 기타 리소스 사용을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-112">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machine-classes"></a><span data-ttu-id="7fb58-113">양자 컴퓨터 클래스</span><span class="sxs-lookup"><span data-stu-id="7fb58-113">Quantum machine classes</span></span>

<span data-ttu-id="7fb58-114">향후, QDK는 다른 유형의 시뮬레이션을 지원하고 퀀텀 하드웨어에서 실행할 수 있도록 지원하는 추가 퀀텀 머신 클래스를 정의할 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-114">In the future, the QDK will define additional quantum machine classes to support other types of simulation and to support running on quantum hardware.</span></span> <span data-ttu-id="7fb58-115">기본 컴퓨터 구현을 변경하면서 알고리즘은 일정하게 유지하면 시뮬레이션에서 알고리즘을 쉽게 테스트하고 디버그한 다음, 알고리즘이 변경되지 않았다는 확신을 가지고 실제 하드웨어에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-115">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

<span data-ttu-id="7fb58-116">QDK에는 `Microsoft.Quantum.Simulation.Simulators` 네임스페이스에 모두 정의된 여러 양자 컴퓨터 클래스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-116">The QDK includes several quantum machine classes, all defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

|<span data-ttu-id="7fb58-117">시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="7fb58-117">Simulator</span></span> |<span data-ttu-id="7fb58-118">클래스</span><span class="sxs-lookup"><span data-stu-id="7fb58-118">Class</span></span>|<span data-ttu-id="7fb58-119">Description</span><span class="sxs-lookup"><span data-stu-id="7fb58-119">Description</span></span>|
|-----|------|---|
|[<span data-ttu-id="7fb58-120">전체 상태 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="7fb58-120">Full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | <span data-ttu-id="7fb58-121">퀀텀 알고리즘을 실행 및 디버그하고 약 30큐비트로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-121">Runs and debugs quantum algorithms, and is limited to about 30 qubits.</span></span> |
|[<span data-ttu-id="7fb58-122">단순 리소스 예측 도구</span><span class="sxs-lookup"><span data-stu-id="7fb58-122">Simple resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | <span data-ttu-id="7fb58-123">퀀텀 알고리즘을 실행하는 데 필요한 리소스를 최상위 수준에서 분석하고 수천 큐비트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-123">Performs a top level analysis of the resources needed to run a quantum algorithm, and supports thousands of qubits.</span></span>|
|[<span data-ttu-id="7fb58-124">추적 기반 리소스 예측 도구</span><span class="sxs-lookup"><span data-stu-id="7fb58-124">Trace-based resource estimator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |<span data-ttu-id="7fb58-125">알고리즘의 전체 호출 그래프에 대해 리소스 사용량을 자세히 분석하고 수천 큐비트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-125">Runs advanced analysis of resources consumptions for the algorithm's entire call-graph, and supports thousands of qubits.</span></span>|
|[<span data-ttu-id="7fb58-126">Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="7fb58-126">Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |<span data-ttu-id="7fb58-127">`X`, `CNOT` 및 다중 제어 `X` 퀀텀 작업으로 제한되는 퀀텀 알고리즘을 시뮬레이션하고 수백만 큐비트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-127">Simulates quantum algorithms that are limited to `X`, `CNOT`, and multi-controlled `X` quantum operations, and supports million of qubits.</span></span> |

## <a name="invoking-the-quantum-simulator"></a><span data-ttu-id="7fb58-128">퀀텀 시뮬레이터 호출</span><span class="sxs-lookup"><span data-stu-id="7fb58-128">Invoking the quantum simulator</span></span>

<span data-ttu-id="7fb58-129">[Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)에서는 Q# 코드를 퀀텀 시뮬레이터에 전달하는 세 가지 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-129">In [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs), three ways of passing the Q# code to the quantum simulator are demonstrated:</span></span> 

* <span data-ttu-id="7fb58-130">명령줄 사용</span><span class="sxs-lookup"><span data-stu-id="7fb58-130">Using the command line</span></span>
* <span data-ttu-id="7fb58-131">Python 호스트 프로그램 사용</span><span class="sxs-lookup"><span data-stu-id="7fb58-131">Using a Python host program</span></span>
* <span data-ttu-id="7fb58-132">C# 호스트 프로그램 사용</span><span class="sxs-lookup"><span data-stu-id="7fb58-132">Using a C# host program</span></span>

<span data-ttu-id="7fb58-133">양자 컴퓨터는 일반적인 .NET 클래스의 인스턴스로, .NET 클래스와 마찬가지로 해당 생성자를 호출하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-133">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span> <span data-ttu-id="7fb58-134">이 작업을 수행하는 방법은 Q# 프로그램을 실행하는 방법에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="7fb58-134">How you do this depends on how you run the Q# program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7fb58-135">다음 단계</span><span class="sxs-lookup"><span data-stu-id="7fb58-135">Next steps</span></span>

* <span data-ttu-id="7fb58-136">서로 다른 환경에서 Q# 프로그램에 대한 대상 컴퓨터를 호출하는 방법에 대한 자세한 내용은 [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7fb58-136">For details about how to invoke target machines for Q# programs in different environments, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
