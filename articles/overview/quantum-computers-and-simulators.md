---
title: 양자 컴퓨터 및 양자 시뮬레이터
description: 양자 하드웨어, 양자 시뮬레이터 및 양자 연산의 작동 방식에 대해 알아봅니다.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.simulators
ms.openlocfilehash: 04f90e9f88cf17259f96532617ef6f092b56b859
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430750"
---
# <a name="quantum-computers-and-quantum-simulators"></a><span data-ttu-id="8f9df-103">양자 컴퓨터 및 양자 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="8f9df-103">Quantum computers and quantum simulators</span></span>

<span data-ttu-id="8f9df-104">양자 컴퓨터는 아직 개발 초기 단계에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-104">Quantum computers are still in the infancy of their development.</span></span> <span data-ttu-id="8f9df-105">하드웨어 및 유지 관리 비용이 많이 들고 대부분의 시스템은 대학과 연구소에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-105">The hardware and maintenance are expensive, and most systems are located in universities and research labs.</span></span> <span data-ttu-id="8f9df-106">그러나 이 기술은 발전하고 있으며 일부 시스템에 대한 퍼블릭 액세스는 제한되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-106">The technology is advancing, though, and limited public access to some systems is available.</span></span>

<span data-ttu-id="8f9df-107">양자 시뮬레이터는 클래식 컴퓨터에서 실행되며 큐비트가 다른 작업에 반응하는 방식을 예측하는 환경에서 양자 프로그램을 실행하고 테스트할 수 있도록 하는 소프트웨어 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-107">Quantum simulators are software programs that run on classical computers and make it possible to run and test quantum programs in an environment that predicts how qubits will react to different operations.</span></span>

## <a name="quantum-hardware"></a><span data-ttu-id="8f9df-108">양자 하드웨어</span><span class="sxs-lookup"><span data-stu-id="8f9df-108">Quantum hardware</span></span>

<span data-ttu-id="8f9df-109">양자 컴퓨터에는 큐비트를 저장하는 영역, 신호를 큐비트에 전송하는 방법 및 프로그램을 실행하고 명령을 보내는 클래식 컴퓨터의 세 가지 주요 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-109">A quantum computer has three primary parts: an area that houses the qubits, a method for transferring signals to the qubits, and a classical computer to run a program and send instructions.</span></span>

- <span data-ttu-id="8f9df-110">큐비트에 사용되는 양자 물질은 취약하고 환경 간섭에 매우 민감합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-110">The quantum material used for qubits is fragile and highly sensitive to environmental interferences.</span></span> <span data-ttu-id="8f9df-111">큐비트를 저장하는 일부 방법의 경우 큐비트를 저장하는 장치는 결집을 최대화하기 위해 절대 0(영)도 바로 위의 온도로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-111">For some methods of qubit storage, the unit that houses the qubits is kept at a temperature just above absolute zero to maximize their coherence.</span></span> <span data-ttu-id="8f9df-112">다른 유형의 큐비트 저장에서는 진동을 최소화하고 큐비트를 안정화하는 데 도움이 되는 진공 챔버를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-112">Other types of qubit housing use a vacuum chamber to help minimize vibrations and stabilize the qubits.</span></span>  
- <span data-ttu-id="8f9df-113">신호는 극초단파, 레이저 및 전압을 포함한 다양한 방법을 사용하여 큐비트에 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-113">Signals can be sent to the qubits using a variety of methods including microwaves, laser, and voltage.</span></span>

<span data-ttu-id="8f9df-114">양자 컴퓨터는 올바르게 작동하기 위한 많은 과제를 마주하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-114">Quantum computers face a multitude of challenges to operate correctly.</span></span> <span data-ttu-id="8f9df-115">양자 컴퓨터의 오류 수정은 중요한 문제이며, 확장(더 많은 큐비트 추가)은 오류 비율을 높입니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-115">Error correction in quantum computers is a significant issue, and scaling up (adding more qubits) increases the error rate.</span></span> <span data-ttu-id="8f9df-116">이러한 제한으로 인해 데스크톱용 양자 PC는 아직 멀지만 상업적으로 실행 가능한 랩 기반 양자 컴퓨터는 가까이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-116">Because of these limitations, a quantum PC for your desktop is far in the future, but a commercially-viable lab-based quantum computer is closer.</span></span>

## <a name="quantum-simulators"></a><span data-ttu-id="8f9df-117">양자 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="8f9df-117">Quantum simulators</span></span>

<span data-ttu-id="8f9df-118">클래식 컴퓨터에서 실행되는 양자 시뮬레이터를 사용하면 양자 시스템에서 양자 알고리즘 실행을 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-118">Quantum simulators that run on classical computers allow you to simulate the execution of quantum algorithms on a quantum system.</span></span>  <span data-ttu-id="8f9df-119">Microsoft의 QDK(Qualumer Development Kit)에는 특수한 다른 양자 시뮬레이터와 함께 전체 상태 벡터 시뮬레이터가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-119">Microsoft’s Quantum Development Kit (QDK) includes a full-state vector simulator along with other specialized quantum simulators.</span></span>

## <a name="topological-qubit"></a><span data-ttu-id="8f9df-120">위상 큐비트</span><span class="sxs-lookup"><span data-stu-id="8f9df-120">Topological qubit</span></span>

<span data-ttu-id="8f9df-121">Microsoft는 위상 큐비트를 기반으로 하는 양자 컴퓨터를 개발하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-121">Microsoft is developing a quantum computer based on topological qubits.</span></span> <span data-ttu-id="8f9df-122">위상 큐비트는 환경 변화의 영향을 덜 받으므로 필요한 외부 오류 수정의 정도를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-122">A topological qubit will be less impacted by changes in its environment, therefore reducing the degree of external error correction required.</span></span>

<span data-ttu-id="8f9df-123">위상 큐비트는 환경 소음에 대한 안정성과 저항성이 향상되어 더 쉽게 크기 조정하고 더 오래 안정적으로 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-123">Topological qubits feature increased stability and resistance to environmental noise, which means they can more readily scale and remain reliable longer.</span></span>

## <a name="microsoft-and-quantum-hardware-partnerships"></a><span data-ttu-id="8f9df-124">Microsoft 및 양자 하드웨어의 파트너 관계</span><span class="sxs-lookup"><span data-stu-id="8f9df-124">Microsoft and quantum hardware partnerships</span></span>

<span data-ttu-id="8f9df-125">Microsoft는 양자 하드웨어 제조업체인 IonQ, Honeywell 및 QCI와 협력하여 나중에 개발자가 양자 컴퓨터에 액세스할 수 있도록 하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-125">Microsoft is partnering with quantum hardware manufacturers IonQ, Honeywell, and QCI to make quantum computers accessible to developers in the future.</span></span> <span data-ttu-id="8f9df-126">개발자는 Azure Quantum 플랫폼을 활용하여 Microsoft의 QDK(Quality Development Kit) 및 Q#에서 양자 프로그램을 작성하고 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-126">Leveraging the Azure Quantum platform, developers will be able to use Microsoft’s Quantum Development Kit (QDK) and Q# to write quantum programs and run them remotely.</span></span>

## <a name="quantum-computations"></a><span data-ttu-id="8f9df-127">양자 계산</span><span class="sxs-lookup"><span data-stu-id="8f9df-127">Quantum computations</span></span>

<span data-ttu-id="8f9df-128">양자 컴퓨터 또는 양자 시뮬레이터에서 계산을 수행하는 작업은 다음과 같은 기본 프로세스를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-128">Performing computations on a quantum computer or quantum simulator follow a basic process:</span></span>

- <span data-ttu-id="8f9df-129">큐비트에 액세스</span><span class="sxs-lookup"><span data-stu-id="8f9df-129">Access the qubits</span></span>
- <span data-ttu-id="8f9df-130">큐비트를 원하는 상태로 초기화</span><span class="sxs-lookup"><span data-stu-id="8f9df-130">Initialize the qubits to the desired state</span></span>
- <span data-ttu-id="8f9df-131">큐비트 상태를 변환하는 작업수행</span><span class="sxs-lookup"><span data-stu-id="8f9df-131">Perform operations to transform the states of the qubits</span></span>
- <span data-ttu-id="8f9df-132">새 큐비트 상태 측정</span><span class="sxs-lookup"><span data-stu-id="8f9df-132">Measure the new states of the qubits</span></span>

<span data-ttu-id="8f9df-133">큐비트 초기화 및 변환은 **양자 연산**(때로는 양자 게이트라고도 함)을 사용하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-133">Initializing and transforming qubits is done using **quantum operations** (sometimes called quantum gates).</span></span> <span data-ttu-id="8f9df-134">양자 연산은 AND, OR, NOT 및 XOR과 같은 클래식 컴퓨팅의 논리 연산과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-134">Quantum operations are similar to logic operations in classical computing, such as AND, OR, NOT, and XOR.</span></span> <span data-ttu-id="8f9df-135">연산은 1에서 0으로 큐비트의 상태를 대칭 이동하거나 한 쌍의 큐비트를 얽는 것처럼 기본적으로 여러 개의 연산을 직렬로 사용하여 중첩된 큐비트가 한 방향 또는 다른 방향으로 붕괴될 확률에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-135">An operation can be as basic as flipping a qubit's state from 1 to 0 or entangling a pair of qubits, to using multiple operations in series to affect the probability of a superposed qubit collapsing one way or the other.</span></span>

> [!NOTE] 
> <span data-ttu-id="8f9df-136">[Q# 라이브러리](xref:microsoft.quantum.libraries)는 하위 수준 양자 연산의 복잡한 조합을 정의하는 기본 제공 연산을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-136">The [Q# libraries](xref:microsoft.quantum.libraries) provide built-in operations that define complex combinations of lower-level quantum operations.</span></span> <span data-ttu-id="8f9df-137">라이브러리 연산을 사용하여 큐비트를 변환하고 더 복잡한 사용자 정의 연산을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-137">You can use the library operations to transform qubits and to create more complex user-defined operations.</span></span>  

<span data-ttu-id="8f9df-138">계산 결과를 측정하면 답이 나오지만, 일부 양자 알고리즘의 경우 정답이 반드시 맞는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-138">Measuring the result of the computation tells us an answer, but for some quantum algorithms, not necessarily the correct answer.</span></span> <span data-ttu-id="8f9df-139">일부 양자 알고리즘의 결과는 양자 연산으로 구성된 확률을 기반으로 하므로 이러한 계산은 여러 번 실행되어 확률 분포를 얻고 결과의 정확도를 향상시킵니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-139">Because the result of some quantum algorithms is based on the probability that was configured by the quantum operations, these computations are run multiple times to get a probability distribution and refine the accuracy of the results.</span></span>  <span data-ttu-id="8f9df-140">연산에서 정답을 반환했는지 확인하는 작업은 양자 확인이라고 하며 양자 컴퓨팅에서 중요한 과제입니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-140">Assurance that an operation returned a correct answer is known as quantum verification and is a significant challenge in quantum computing.</span></span>

## <a name="summary"></a><span data-ttu-id="8f9df-141">요약</span><span class="sxs-lookup"><span data-stu-id="8f9df-141">Summary</span></span>

<span data-ttu-id="8f9df-142">양자 컴퓨팅은 클래식 컴퓨팅과 동일한 개념 중 일부를 공유하지만 몇 가지 새로운 방식이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-142">Quantum computing shares some of the same concepts as classical computing but adds a few new twists.</span></span> <span data-ttu-id="8f9df-143">몇 가지 주요 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-143">Here are some key takeaways:</span></span>

- <span data-ttu-id="8f9df-144">양자 하드웨어는 비용이 많이 들고 사용하기에 취약하므로 양자 시뮬레이터를 사용하여 프로그램을 작성하고 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-144">Quantum hardware is expensive and fragile to work with, so quantum simulators are used to write and test programs.</span></span>
- <span data-ttu-id="8f9df-145">클래식 컴퓨터와 양자 컴퓨터에서 모두 논리 연산(또는 게이트)을 사용하여 계산을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-145">Both classical and quantum computers use logic operations (or gates) to prepare computations.</span></span>
- <span data-ttu-id="8f9df-146">양자 계산에서 확률을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-146">Quantum computations return probabilities.</span></span>

<span data-ttu-id="8f9df-147">양자 하드웨어와 기술의 발전은 관련 분야를 빠르게 변화시키고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-147">Advancements in quantum hardware and techniques is rapidly changing the field.</span></span> <span data-ttu-id="8f9df-148">이는 [현재 개발](https://phys.org/search/?search=quantum+computer&s=0) 중 일부에 불과합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9df-148">Here are just a few of the [current developments](https://phys.org/search/?search=quantum+computer&s=0).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8f9df-149">다음 단계</span><span class="sxs-lookup"><span data-stu-id="8f9df-149">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8f9df-150">Q# 프로그래밍 언어 및 QDK란?</span><span class="sxs-lookup"><span data-stu-id="8f9df-150">What is the Q# programming language and QDK?</span></span>](xref:microsoft.quantum.overview.q-sharp)