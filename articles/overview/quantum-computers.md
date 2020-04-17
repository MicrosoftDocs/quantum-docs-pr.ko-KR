---
title: 양자 컴퓨터에서 수행할 수 있는 작업은 무엇인가요?
description: 새 양자 알고리즘부터 클래식 컴퓨터에서 실행되는 양자 유도 알고리즘에 이르기까지 양자 컴퓨팅의 영향에 대해 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: article
uid: microsoft.quantum.overview.computers
ms.openlocfilehash: 9d8ba90a504f298f9465ebf564c43625a4d43168
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "73529945"
---
# <a name="what-can-a-quantum-computer-do"></a><span data-ttu-id="67f41-103">양자 컴퓨터에서 수행할 수 있는 작업은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="67f41-103">What can a quantum computer do?</span></span>

<span data-ttu-id="67f41-104">클래식 컴퓨터에서 수행할 수는 없지만 양자 컴퓨터에서 수행할 수 있는 작업은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="67f41-104">What can we do with a quantum computer that can't be done with a classical one?</span></span>

<span data-ttu-id="67f41-105">현재 솔루션을 찾는 데 수십억 년이 걸리는 세계에서 가장 어려운 문제 중 일부를 풀기 위해 양자 컴퓨터는 며칠, 몇 시간 또는 몇 분 안에 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-105">To solve some of the world's most challenging problems, where finding a solution would take current computers billions of years, a quantum computer could do so in days, hours, or even minutes.</span></span>

<span data-ttu-id="67f41-106">양자 컴퓨팅을 사용하면 연구자들이 새로운 촉매와 재료를 개발하고, 의약품을 개선하고, AI의 발전을 가속화하고, 우주의 기원에 대한 기본적인 질문에 답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-106">Quantum computing will enable researchers to develop new catalysts and materials, improve medicines, accelerate advances in artificial intelligence, and answer fundamental questions about the origins of our universe.</span></span>

## <a name="quantum-simulation"></a><span data-ttu-id="67f41-107">양자 시뮬레이션</span><span class="sxs-lookup"><span data-stu-id="67f41-107">Quantum simulation</span></span>

<span data-ttu-id="67f41-108">양자 프로그램을 사용하여 양자 시스템을 모델링하면 여러 산업에서 혁신으로 이어지는 인사이트를 발견할 가능성이 매우 높습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-108">Using quantum programs to model quantum systems themselves has vast potential for unlocking insights leading to innovations across many industries.</span></span> <span data-ttu-id="67f41-109">광합성, 초전도체, 복합 분자는 양자 프로그램을 사용하여 시뮬레이션할 수 있는 양자 시스템의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-109">Photosynthesis, superconductors, and complex molecules are examples of quantum systems that can be simulated using quantum programs.</span></span>

<span data-ttu-id="67f41-110">양자 역학의 법칙에 따라 작동하는 미세한 시스템을 시뮬레이션하는 것은 계산 비용이 많이 듭니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-110">Simulating microscopic systems that behave according to the laws of quantum mechanics is computationally expensive.</span></span> <span data-ttu-id="67f41-111">중첩될 수 있는 모든 가능한 상태를 고려해야 하며, 상태의 수는 시스템의 크기에 따라 기하 급수적으로 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-111">We need to take into account all the possible states that can be in superposition and the number of states grows exponentially with the size of the system.</span></span> <span data-ttu-id="67f41-112">양자 컴퓨터에서는 시스템의 모든 상태를 모델링할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-112">In a quantum computer, we don’t need to model all of the states of the system.</span></span> <span data-ttu-id="67f41-113">대신, 컴퓨터 자체의 큐비트에서 시뮬레이션하려는 시스템의 양자 상태를 포함하고, 특정 양자 게이트 세트를 사용하여 시뮬레이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-113">Instead, we embed the quantum state of the system that we want to simulate in the qubits of the computer itself, and run the simulation with a specific set of quantum gates.</span></span> <span data-ttu-id="67f41-114">즉 양자 컴퓨터를 사용하여 양자 시스템을 시뮬레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-114">In other words, we use a quantum computer to simulate a quantum system.</span></span>

<span data-ttu-id="67f41-115">화학 분자는 양자 시스템이므로 이 방법으로 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-115">Chemical molecules are quantum systems and therefore can be analyzed in this way.</span></span> <span data-ttu-id="67f41-116">이러한 특정 화학 물질 중 하나가 _니트로게나아제_(nitrogenase) 효소이며, 이 물질의 해당 속성을 더 잘 이해하면 현재 화학 비료의 에너지 소비와 온실 가스 배출을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-116">One such specific chemical is the _nitrogenase_ enzyme, which, with a better understanding of its properties, could have the potential to reduce the energy consumption and greenhouse gas emission of current fertilizers.</span></span>

## <a name="cryptography"></a><span data-ttu-id="67f41-117">암호화</span><span class="sxs-lookup"><span data-stu-id="67f41-117">Cryptography</span></span>

<span data-ttu-id="67f41-118">양자 컴퓨터의 가장 유명한 애플리케이션은 암호화입니다. 1994년에 Peter Shor는 널리 사용되는 모든 암호화 기술을 확장 가능한 양자 컴퓨터로 뚫을 수 있다는 것을 보여주었습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-118">Perhaps the most famous application of quantum computers is in cryptography, where Peter Shor showed in 1994 that a scalable quantum computer can break every widely used encryption technique.</span></span>  <span data-ttu-id="67f41-119">기존 암호화는 대수를 두 개의 소수로 인수분해하는 것처럼 까다로운 대수에 대한 연산에 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-119">Classical cryptography relies on the intractability of operations on large numbers, such as factorization of large numbers into two prime numbers.</span></span>

<span data-ttu-id="67f41-120">양자 컴퓨팅은 이러한 연산을 이론적으로 다루기 쉽게 만들어줍니다(Shor의 알고리즘을 통해).</span><span class="sxs-lookup"><span data-stu-id="67f41-120">Quantum computing makes these operations theoretically tractable (via Shor's algorithm).</span></span> <span data-ttu-id="67f41-121">이 알고리즘은 현재 규모의 양자 하드웨어로는 물리적으로 구현할 수 없지만, 암호화 및 암호화 키 분배를 위한 새 양자 알고리즘을 포함하여 향후에도 사용할 수 있는 데이터 보안에 대한 양자 저항 알고리즘을 개발할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-121">Whilst implementation of this algorithm is not physically possible with the current scale of quantum hardware, it has spawned development of quantum-resistant algorithms to future-proof data security, including novel quantum algorithms for encryption and cryptographic key distribution.</span></span>

<span data-ttu-id="67f41-122">Microsoft에는 세계 최고 수준의 양자 후 암호화 및 보안 팀이 양자 저항성 알고리즘을 개발하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-122">Here at Microsoft, we have the world's leading team in post-quantum cryptography and security developing quantum-resistant algorithms.</span></span>

## <a name="optimization"></a><span data-ttu-id="67f41-123">Optimization</span><span class="sxs-lookup"><span data-stu-id="67f41-123">Optimization</span></span>

<span data-ttu-id="67f41-124">최적화는 특정 비용 함수를 최소화하는 솔루션을 찾기 위해 고차원 공간에서 대량 검색을 수행하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-124">Optimization is the task of performing a large search over a high-dimensional space for a solution that minimizes a given cost function.</span></span>   <span data-ttu-id="67f41-125">양자 컴퓨터에서는 최적화 알고리즘의 속도를 높여서 양자 컴퓨터가 아니면 불가능한 솔루션을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-125">On a quantum computer, we can speed up optimization algorithms, enabling finding solutions that otherwise were not possible.</span></span> <span data-ttu-id="67f41-126">애플리케이션 범위는 교통부터 물류, 의료, 진단 및 재료 과학까지 매우 방대합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-126">Applications range from transportation and logistics, healthcare, diagnostics, and material science.</span></span> <span data-ttu-id="67f41-127">이러한 산업의 효율성을 향상시킬 수 있는 방법에 큰 영향이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-127">There can be a profound impact on how these industries can become more efficient.</span></span>

<span data-ttu-id="67f41-128">양자 컴퓨팅을 사용하여 최적화하면 현재의 기존 시스템으로는 불가능한 방식으로 교통 및 물류를 혁신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-128">Optimization with quantum computing allows us to innovate around transportation and logistics in a way that is not possible with today’s classical systems.</span></span>

<span data-ttu-id="67f41-129">교통 흐름을 최적화하여 정체를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-129">Optimizing traffic flow can reduce congestion.</span></span>  <span data-ttu-id="67f41-130">경로 계획 외에도 항공기 게이트 할당, 패키지 배달, 작업 예약 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-130">In addition to route planning, there is airplane gate assignment, package delivery, job scheduling and more.</span></span> <span data-ttu-id="67f41-131">재료 과학의 혁신을 통해 새로운 형태의 에너지, 더 큰 용량의 배터리, 더 가볍고 더 강한 재료를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-131">With breakthroughs in materials science, there will be new forms of energy, batteries with greater capacity, lighter and stronger materials.</span></span>

## <a name="machine-learning"></a><span data-ttu-id="67f41-132">Machine Learning</span><span class="sxs-lookup"><span data-stu-id="67f41-132">Machine learning</span></span>

<span data-ttu-id="67f41-133">기존의 컴퓨팅에서 다양한 수치 계산은 선형 연립방정식을 구하는 데 주로 적용되며, 특히 대부분의 계산 비용은 큰 행렬의 역을 계산하는 기계 학습 분야에서는 더욱 그렇습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-133">A great number of numerical calculations on classical computing consist mainly in solving linear systems of equations, especially true in the field of machine learning where most of the computation cost goes into calculating the inverse of huge matrices.</span></span>

<span data-ttu-id="67f41-134">다행히도, 대략적으로 클래식 컴퓨터보다 빠르게 기하급수적으로 시스템의 문제를 풀 수 있는 양자 알고리즘이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-134">Fortunately, there is a quantum algorithm that allows us to approximately solve the system exponentially faster than a classical computer.</span></span> <span data-ttu-id="67f41-135">이 알고리즘은 방정식의 선형 시스템에 대한 해법을 구하는 데 필요한 모든 문제에서 빠른 속도를 실현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-135">The algorithm opens the door to great speedups in every problem that needs the solution to linear systems of equations.</span></span>

<span data-ttu-id="67f41-136">이러한 영역에서 발생하는 문제에 대한 솔루션은 에너지 위기, 기후 변화, 식량 부족, 개인적이고 정확한 의료 진단을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-136">Solutions to problems in these areas will help address the energy crisis, climate change, food scarcity, and personal and precise medical diagnosis.</span></span>

## <a name="quantum-inspired-computing"></a><span data-ttu-id="67f41-137">양자 유도 컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="67f41-137">Quantum-inspired computing</span></span>

<span data-ttu-id="67f41-138">양자 유도 알고리즘은 클래식 소프트웨어를 사용하여 구현되지만, 속도와 정확도를 높이기 위해 양자 원칙을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-138">Quantum-inspired algorithms are implemented with classical software, but use quantum principles for increased speed and accuracy.</span></span>

<span data-ttu-id="67f41-139">양자 유도 알고리즘은 의학 연구에 적용되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-139">Quantum-inspired algorithms are being applied to medical research.</span></span> <span data-ttu-id="67f41-140">예를 들어 MRI(자기 공명 영상) 검사의 정확도를 향상시킵니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-140">For example, to improve the accuracy of Magnetic Resonance Imaging (MRI) scans.</span></span> <span data-ttu-id="67f41-141">양자 유도 컴퓨팅은 특정 질병을 식별하기 위해 MRI 머신의 구성을 최적화하는 데 사용되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f41-141">Quantum-inspired computing is being used to optimize the configuration of the MRI machines for identification of specific diseases.</span></span>

## <a name="next-steps"></a><span data-ttu-id="67f41-142">다음 단계</span><span class="sxs-lookup"><span data-stu-id="67f41-142">Next steps</span></span>

* [<span data-ttu-id="67f41-143">양자 컴퓨팅을 학습해야 하는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="67f41-143">Why should I learn quantum computing?</span></span>](xref:microsoft.quantum.overview.why)
* [<span data-ttu-id="67f41-144">Microsoft Quantum Development Kit 시작</span><span class="sxs-lookup"><span data-stu-id="67f41-144">Get started with the Microsoft Quantum Development Kit</span></span>](xref:microsoft.quantum.welcome)
