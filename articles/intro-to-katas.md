---
title: Quantum Katas 소개
description: Microsoft QDK(Quantum Development Kit)에서 제공하는 카타(학습 연습)에 대해 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/17/2019
ms.topic: overview
uid: microsoft.quantum.overview.katas
ms.openlocfilehash: af54a2260147b8ca07919b241548aac85ed0d8a1
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76821102"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a><span data-ttu-id="f3e94-103">Quantum Katas에서 양자 컴퓨팅 알아보기</span><span class="sxs-lookup"><span data-stu-id="f3e94-103">Learn quantum computing with the Quantum Katas</span></span>

<span data-ttu-id="f3e94-104">[Quantum Katas](https://github.com/Microsoft/QuantumKatas/)는 양자 컴퓨팅과 Q# 프로그래밍 요소를 동시에 가르치기 위한 자가 학습 자습서 및 프로그래밍 연습 세트로 구성된 오픈 소스 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-104">[The Quantum Katas](https://github.com/Microsoft/QuantumKatas/) is an open-source collection of self-paced tutorials and sets of programming exercises aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span>

## <a name="learning-by-doing"></a><span data-ttu-id="f3e94-105">작업을 통한 학습</span><span class="sxs-lookup"><span data-stu-id="f3e94-105">Learning by Doing</span></span>

<span data-ttu-id="f3e94-106">이 프로젝트에 수집되는 자습서와 연습은 작업을 수행하여 학습하는 방법을 강조합니다. 즉 매우 간단한 과제에서 상당히 까다로운 과제로 진행되는 특정 항목을 다루는 프로그래밍 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-106">The tutorials and exercises collected in this project emphasize learning by doing: they offer programming tasks that cover certain topics which progress from very simple to quite challenging.</span></span> <span data-ttu-id="f3e94-107">각 작업에서는 코드를 입력해야 합니다. 첫 번째 작업에서는 한 줄만 입력하면 되고, 마지막 작업에서는 상당한 크기의 코드 조각을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-107">Each task asks you to fill in some code; the first tasks might require just one line, and the later ones might require a sizable fragment of code.</span></span>

<span data-ttu-id="f3e94-108">가장 중요한 점으로, katas는 작업에 대한 솔루션을 설정하고 실행하고 유효성을 검사하는 테스트 프레임워크를 포함하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-108">Most importantly, the katas include testing frameworks that sets up, runs and validates the solutions to the tasks.</span></span> <span data-ttu-id="f3e94-109">따라서 자신의 솔루션에 대한 피드백을 즉시 받을 수 있으며, 접근 방식이 잘못된 경우 방법을 다시 생각해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-109">This allows you to get immediate feedback on your solution and to reconsider your approach if it is incorrect.</span></span>

<span data-ttu-id="f3e94-110">다음 중 원하는 환경을 선택하여 Katas를 학습에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-110">You can use the Katas for learning in your environment of choice:</span></span>

* <span data-ttu-id="f3e94-111">바인더 환경 내의 Jupyter Notebook 온라인</span><span class="sxs-lookup"><span data-stu-id="f3e94-111">Jupyter Notebooks online within the Binder environment</span></span>
* <span data-ttu-id="f3e94-112">로컬 머신에서 실행되는 Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="f3e94-112">Jupyter Notebooks running on your local machine</span></span>
* <span data-ttu-id="f3e94-113">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3e94-113">Visual Studio</span></span>
* <span data-ttu-id="f3e94-114">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="f3e94-114">Visual Studio Code</span></span>

## <a name="what-can-i-learn-with-the-quantum-katas"></a><span data-ttu-id="f3e94-115">Quantum Katas에서 배울 수 있는 내용</span><span class="sxs-lookup"><span data-stu-id="f3e94-115">What can I learn with the Quantum Katas?</span></span>

<span data-ttu-id="f3e94-116">다음은 Quantum Katas에서 다루는 주요 토픽의 요약 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-116">Here is a summary of the main topics covered in the Quantum Katas.</span></span> <span data-ttu-id="f3e94-117">처음에는 이 학습 경로를 따라 양자 컴퓨팅의 기본 개념을 확실하게 익히는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-117">We recommend you to follow this learning path in the beginning to make sure you have a solid grasp on the fundamental concepts of quantum computing.</span></span> <span data-ttu-id="f3e94-118">물론 복소수처럼 이미 잘 알고 있는 토픽을 건너뛰고, 원하는 순서로 알고리즘을 알아볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e94-118">Of course, you can skip the topics you're comfortable with, such as complex arithmetic, and learn the algorithms in any order you want.</span></span>

### <a name="introduction-to-quantum-computing-concepts"></a><span data-ttu-id="f3e94-119">양자 컴퓨팅 개념 소개</span><span class="sxs-lookup"><span data-stu-id="f3e94-119">Introduction to quantum computing concepts</span></span>

* [<span data-ttu-id="f3e94-120">복소수</span><span class="sxs-lookup"><span data-stu-id="f3e94-120">Complex arithmetic</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)
* [<span data-ttu-id="f3e94-121">선형 대수</span><span class="sxs-lookup"><span data-stu-id="f3e94-121">Linear algebra</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)
* [<span data-ttu-id="f3e94-122">큐비트의 개념</span><span class="sxs-lookup"><span data-stu-id="f3e94-122">The concept of a qubit</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/Qubit)
* [<span data-ttu-id="f3e94-123">단일 큐비트 양자 게이트</span><span class="sxs-lookup"><span data-stu-id="f3e94-123">Single-qubit quantum gates</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates)
* [<span data-ttu-id="f3e94-124">다중 큐비트 시스템</span><span class="sxs-lookup"><span data-stu-id="f3e94-124">Multi-qubit systems</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitSystems)
* [<span data-ttu-id="f3e94-125">다중 큐비트 게이트</span><span class="sxs-lookup"><span data-stu-id="f3e94-125">Multi-qubit gates</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitGates)

### <a name="quantum-computing-fundamentals"></a><span data-ttu-id="f3e94-126">양자 컴퓨팅 기본 사항</span><span class="sxs-lookup"><span data-stu-id="f3e94-126">Quantum computing fundamentals</span></span>

* [<span data-ttu-id="f3e94-127">양자 게이트 인식</span><span class="sxs-lookup"><span data-stu-id="f3e94-127">Recognizing quantum gates</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/BasicGates)
* [<span data-ttu-id="f3e94-128">양자 중첩 만들기</span><span class="sxs-lookup"><span data-stu-id="f3e94-128">Creating quantum superposition</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/Superposition)
* [<span data-ttu-id="f3e94-129">측정값을 사용하여 양자 상태 구별</span><span class="sxs-lookup"><span data-stu-id="f3e94-129">Distinguishing quantum states using measurements</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/Measurements)
* [<span data-ttu-id="f3e94-130">공동 측정값</span><span class="sxs-lookup"><span data-stu-id="f3e94-130">Joint measurements</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/JointMeasurements)

### <a name="algorithms"></a><span data-ttu-id="f3e94-131">알고리즘</span><span class="sxs-lookup"><span data-stu-id="f3e94-131">Algorithms</span></span>

* [<span data-ttu-id="f3e94-132">양자 순간 이동</span><span class="sxs-lookup"><span data-stu-id="f3e94-132">Quantum teleportation</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/Teleportation)
* [<span data-ttu-id="f3e94-133">초고밀도 코딩</span><span class="sxs-lookup"><span data-stu-id="f3e94-133">Superdense coding</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)
* [<span data-ttu-id="f3e94-134">도이치–조사 알고리즘</span><span class="sxs-lookup"><span data-stu-id="f3e94-134">Deutsch–Jozsa algorithm</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringDeutschJozsaAlgorithm)
* [<span data-ttu-id="f3e94-135">Grover 검색 알고리즘 구현</span><span class="sxs-lookup"><span data-stu-id="f3e94-135">Implementing Grover's search algorithm</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/GroversAlgorithm)
* [<span data-ttu-id="f3e94-136">Grover 검색 알고리즘의 상위 수준 속성 살펴보기</span><span class="sxs-lookup"><span data-stu-id="f3e94-136">Exploring high-level properties of Grover's search algorithm</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringGroversAlgorithm)
* <span data-ttu-id="f3e94-137">Grover 알고리즘을 사용하여 실제 문제 해결: [SAT 문제](https://github.com/microsoft/QuantumKatas/tree/master/SolveSATWithGrover) 및 [그래프 색 지정 문제](https://github.com/microsoft/QuantumKatas/tree/master/GraphColoring)</span><span class="sxs-lookup"><span data-stu-id="f3e94-137">Solving real problems using Grover's algorithm: [SAT problems](https://github.com/microsoft/QuantumKatas/tree/master/SolveSATWithGrover) and [graph coloring problems](https://github.com/microsoft/QuantumKatas/tree/master/GraphColoring)</span></span>

### <a name="protocols-and-libraries"></a><span data-ttu-id="f3e94-138">프로토콜 및 라이브러리</span><span class="sxs-lookup"><span data-stu-id="f3e94-138">Protocols and libraries</span></span>

* [<span data-ttu-id="f3e94-139">양자 키 배포용 BB84 프로토콜</span><span class="sxs-lookup"><span data-stu-id="f3e94-139">BB84 protocol for quantum key distribution</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/KeyDistribution_BB84)
* <span data-ttu-id="f3e94-140">양자 오류 수정: [비트 대칭 이동 오류 수정 코드](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)</span><span class="sxs-lookup"><span data-stu-id="f3e94-140">Quantum error correction: [bit-flip error correcting code](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)</span></span>
* [<span data-ttu-id="f3e94-141">단계 예측</span><span class="sxs-lookup"><span data-stu-id="f3e94-141">Phase estimation</span></span>](https://github.com/microsoft/QuantumKatas/blob/master/PhaseEstimation)
* <span data-ttu-id="f3e94-142">양자 산술: [리플 캐리 가산기 빌드](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)</span><span class="sxs-lookup"><span data-stu-id="f3e94-142">Quantum arithmetic: [building ripple-carry adders](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)</span></span>

### <a name="entanglement-games"></a><span data-ttu-id="f3e94-143">얽힘 게임</span><span class="sxs-lookup"><span data-stu-id="f3e94-143">Entanglement games</span></span>

* [<span data-ttu-id="f3e94-144">CHSH 게임</span><span class="sxs-lookup"><span data-stu-id="f3e94-144">CHSH game</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/CHSHGame)
* [<span data-ttu-id="f3e94-145">GHZ 게임</span><span class="sxs-lookup"><span data-stu-id="f3e94-145">GHZ game</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/GHZGame)
* [<span data-ttu-id="f3e94-146">머민-페레스 매직 스퀘어 게임</span><span class="sxs-lookup"><span data-stu-id="f3e94-146">Mermin-Peres magic square game</span></span>](https://github.com/microsoft/QuantumKatas/tree/master/MagicSquareGame)

## <a name="resources"></a><span data-ttu-id="f3e94-147">리소스</span><span class="sxs-lookup"><span data-stu-id="f3e94-147">Resources</span></span>

* <span data-ttu-id="f3e94-148">[Quantum Katas의 전체 시리즈 참조](https://github.com/microsoft/QuantumKatas)</span><span class="sxs-lookup"><span data-stu-id="f3e94-148">See the full series of [Quantum Katas](https://github.com/microsoft/QuantumKatas)</span></span>
* [<span data-ttu-id="f3e94-149">online에서 katas 실행</span><span class="sxs-lookup"><span data-stu-id="f3e94-149">Run the katas online</span></span>](https://aka.ms/try-quantum-katas)
