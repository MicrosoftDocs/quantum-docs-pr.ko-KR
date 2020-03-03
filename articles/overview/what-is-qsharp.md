---
title: Q# 및 QDK란?
description: 양자 컴퓨터 애플리케이션을 개발하기 위해 Microsoft에서 만든 프로그래밍 언어인 Q#과 Microsoft Quantum Development Kit의 주요 구성 요소에 대해 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: a4bf21887e34ac85f75e5e0b9a033138464fd09d
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907004"
---
# <a name="what-are-q-and-the-qdk"></a><span data-ttu-id="2b2c4-103">Q# 및 QDK란?</span><span class="sxs-lookup"><span data-stu-id="2b2c4-103">What are Q# and the QDK?</span></span>

<span data-ttu-id="2b2c4-104">Q#은 양자 컴퓨팅에 사용하도록 특별히 설계된 기능을 포함하고 있는 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-104">Q# is a programming language with features specifically designed for use with quantum computing.</span></span>
<span data-ttu-id="2b2c4-105">Microsoft QDK(Quantum Development Kit)의 주요 구성 요소인 Q#은 양자 프로그래머에게 게이트 시퀀스 최적화 또는 양자 컴퓨터의 물리적 구현과 같은 기술적 세부 정보에 구애받지 않고 알고리즘에 집중하도록 지원하는 프레임워크를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-105">As a key component of Microsoft's Quantum Development Kit (QDK), it provides quantum programmers a framework that allows you to focus on the algorithms without having to worry about technical details like gate sequence optimization or the physical implementation of a quantum computer.</span></span>

<span data-ttu-id="2b2c4-106">QDK는 개발자에게 양자 프로그램 작성을 시작하는 데 필요한 모든 기능을 제공하는 다양한 도구로 구성되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-106">The QDK comprises a wide range of tools which give developers everything they need to start writing quantum programs.</span></span>
<span data-ttu-id="2b2c4-107">Q# 언어 외에도, QDK에는 다음과 같은 것들이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-107">Alongside the Q# language, the QDK includes:</span></span>
* <span data-ttu-id="2b2c4-108">개발자가 양자 컴퓨팅을 시작하고 실제 양자 애플리케이션을 만들 수 있는 *Q# 라이브러리*</span><span class="sxs-lookup"><span data-stu-id="2b2c4-108">the *Q# libraries*, which allow developers to hit the ground running and create real-world quantum applications today</span></span>
* <span data-ttu-id="2b2c4-109">Q# 프로그램을 실행할 수 있는 다양한 *대상 머신*</span><span class="sxs-lookup"><span data-stu-id="2b2c4-109">various *target machines* on which Q# programs can be run.</span></span> <span data-ttu-id="2b2c4-110">여기에는 대형 양자 프로그램을 위한 리소스 추정 및 시뮬레이터와 노이즈 없는 양자 컴퓨터로 작동하는 전체 상태 양자 시뮬레이터가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-110">These include resource estimators and simulators for larger quantum programs, as well as a full-state quantum simulator, which behaves as a noise-free quantum computer.</span></span> <span data-ttu-id="2b2c4-111">후자는 아이디어를 수정하고, 프로그램을 디버깅하고, 양자 물리학을 배우는 데 매우 유용하지만, 큐비트 수가 비교적 적은 프로그램에만 효율적입니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-111">The latter is very useful for tinkering with ideas, debugging programs, and learning about quantum physics, but only efficient for programs with relatively few qubits.</span></span> <span data-ttu-id="2b2c4-112">대상 머신으로 양자 컴퓨팅 하드웨어를 사용할 수 있는 날이 빨리 왔으면 좋겠습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-112">We're very much looking forward to making quantum computing hardware available as target machines in the future.</span></span>
* <span data-ttu-id="2b2c4-113">Visual Studio 및 VS Code용 확장과 Python 및 Jupyter Notebook에 사용되는 패키지처럼 Q# 작업을 최대한 원활하게 만들어주는 *도구*</span><span class="sxs-lookup"><span data-stu-id="2b2c4-113">*tools* for making work with Q# as seamless as possible, such as extensions for Visual Studio and VS Code, and packages for use with Python and Jupyter Notebooks.</span></span>
* <span data-ttu-id="2b2c4-114">Q#을 Python이나 C# 같은 클래식 호스트 언어와 페어링하는 방법에 대한 *API 설명서*</span><span class="sxs-lookup"><span data-stu-id="2b2c4-114">*API documentation* for pairing Q# with classical host languages such as Python and C#</span></span>

<span data-ttu-id="2b2c4-115">Microsoft Quantum Development Kit를 사용하여 개발된 애플리케이션은 일반적으로 다음 두 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-115">Applications developed with Microsoft's Quantum Development Kit typically consist of two parts:</span></span>
1. <span data-ttu-id="2b2c4-116">하나 이상의 양자 알고리즘 - Q# 양자 프로그래밍 언어를 사용하여 구현되고 클래식 호스트 프로그램을 통해 호출됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-116">One or more quantum algorithms, implemented using the Q# quantum programming language, and invoked by the classical host program.</span></span> <span data-ttu-id="2b2c4-117">양자 알고리즘은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-117">These consist of</span></span> 
    - <span data-ttu-id="2b2c4-118">Q# 연산: 양자 작업을 포함하는 서브루틴</span><span class="sxs-lookup"><span data-stu-id="2b2c4-118">Q# operations: subroutines containing quantum operations, and</span></span> 
    - <span data-ttu-id="2b2c4-119">Q# 함수: 양자 알고리즘 내에서 사용되는 클래식 서브루틴</span><span class="sxs-lookup"><span data-stu-id="2b2c4-119">Q# functions: classical subroutines used within the quantum algorithm.</span></span>
2. <span data-ttu-id="2b2c4-120">클래식 프로그램 - Python 또는 C# 같은 클래식 프로그래밍 언어로 구현되어 주 진입점 역할을 수행하며, 양자 알고리즘을 실행해야 할 때는 Q# 연산을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-120">A classical program, implemented in a classical programming language like Python or C#, that serves as the main entry point and will invoke Q# operations when it wants to execute a quantum algorithm.</span></span>

## <a name="write-quantum-programs-not-quantum-circuits"></a><span data-ttu-id="2b2c4-121">양자 회로가 아닌 양자 프로그램 작성</span><span class="sxs-lookup"><span data-stu-id="2b2c4-121">Write quantum programs, not quantum circuits</span></span>

<span data-ttu-id="2b2c4-122">초기 시대의 양자 컴퓨팅 알고리즘은 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-122">In the early days of quantum computing algorithms were visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>
<span data-ttu-id="2b2c4-123">회로 모델은 Microsoft에서 수년간 양자 컴퓨팅 연구에 유용했지만, 개발자는 양자 회로를 넘어서 Q#을 사용하여 양자 알고리즘과 애플리케이션을 개발할 수 있다고 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-123">While the circuit model has been useful for many years in quantum computing research, here at Microsoft, we believe that developers can go beyond quantum circuits and develop quantum algorithms and applications using Q#.</span></span>
<span data-ttu-id="2b2c4-124">Q# 언어는 수십 년간 클래식 소프트웨어 개발을 통해 습득한 것을 활용하고, 양자 컴퓨팅을 대상으로 하는 고급 언어 기능을 양자 개발자에게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-124">The Q# language was built to take advantage of what we’ve learned through decades of classical software development, and empower quantum developers with high-level language functionality targeted for quantum computing.</span></span>

## <a name="how-does-q-work"></a><span data-ttu-id="2b2c4-125">Q#은 어떻게 작동하나요?</span><span class="sxs-lookup"><span data-stu-id="2b2c4-125">How does Q# work?</span></span>

<span data-ttu-id="2b2c4-126">Q#프로그래밍 언어는 양자 컴퓨터의 내부의 논리에 대해 걱정할 필요 없이 알고리즘을 개발할 수 있도록 형식, 연산 및 논리 식의 직관적인 세트를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-126">The Q# programming language provides you with an intuitive set of types, operations, and logic expressions to develop algorithms without having to worry about the internal logic of the quantum computer.</span></span>

<span data-ttu-id="2b2c4-127">Q#의 기본 구성 요소 중 하나는 `Qubit` 형식이며, 실제 큐비트처럼 복사하거나 직접 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-127">One of the fundamental building blocks of Q# is the `Qubit` type, which cannot be copied or directly accessed, just like a real qubit.</span></span>
<span data-ttu-id="2b2c4-128">대신, 이를 측정하여 `Zero` 및 `One`의 두 가지 가능한 값을 사용할 수 있는 Q# 형식의 `Result` 변수에 측정 결과를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-128">Instead, we can measure it and store the outcome of the measurement in a `Result` variable, a Q# type that can take two possible values: `Zero` and `One`.</span></span>
<span data-ttu-id="2b2c4-129">이와 같은 구문을 통해 알고리즘은 항상 양자 물리학의 법칙을 준수하며 양자 컴퓨터 또는 시뮬레이터에서 올바르게 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-129">Constructs like this one guarantee that algorithms always respect the laws of quantum physics and can run correctly on quantum computers or simulators.</span></span>

<span data-ttu-id="2b2c4-130">또한 Q#에는 모든 양자 규칙이 적용될 수 있도록 조건 및 루프 같은 클래식 논리 기능도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-130">Q# also includes classical logic features like conditionals and loops with some subtleties to make sure that all the quantum rules are being respected.</span></span>
<span data-ttu-id="2b2c4-131">예를 들어, 결정적 클래식 서브루틴만 포함할 수 있는 함수 내에서 퀀텀 작업이 호출되지 않도록 루프가 실행되는 방식을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-131">For example, constraining the way loops are executed to ensure that quantum operations are not called within functions which may only contain deterministic classical subroutines.</span></span>

<span data-ttu-id="2b2c4-132">Q# 프로그램은 종종 C# 또는 Python으로 작성된 호스트 프로그램과 쌍을 이루어 클래식 코드와 양자 코드를 편리하게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-132">Q# programs are often paired with a host program written in C# or Python, which can provide convenient organization of classical and quantum code.</span></span>
<span data-ttu-id="2b2c4-133">QDK는 C# 및 Python과 같은 언어를 지원하는 것 외에도 IQ# Juppyter 커널을 사용하여 Jupyter Notebook을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-133">In addition to supporting languages such as C# and Python, the QDK provides Jupyter Notebook support with the IQ# Jupyter kernel.</span></span>

## <a name="what-can-i-use-q-for"></a><span data-ttu-id="2b2c4-134">Q#은 어디에 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="2b2c4-134">What can I use Q# for?</span></span>

### <a name="use-q-to-learn-quantum-computing"></a><span data-ttu-id="2b2c4-135">Q#을 사용하여 양자 컴퓨팅 학습</span><span class="sxs-lookup"><span data-stu-id="2b2c4-135">Use Q# to learn quantum computing</span></span>

<span data-ttu-id="2b2c4-136">지금까지 양자 컴퓨팅을 학습하려면 순서가 지정된 양자 게이트와 측정의 시퀀스 형식으로 알고리즘을 이해하기 위해 회로 모델을 학습해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-136">Until now, to learn quantum computing you needed to learn the circuit model to understand the algorithms in the form of ordered sequences of quantum gates and measurements.</span></span> <span data-ttu-id="2b2c4-137">Q#을 사용하면 양자 프로그램을 작성하여 양자 컴퓨팅을 학습할 수 있는 다른 경로를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-137">With Q# you can take another path: learn quantum computing by writing quantum programs.</span></span>

### <a name="use-q-to-design-quantum-algorithms"></a><span data-ttu-id="2b2c4-138">Q#을 사용하여 양자 알고리즘 디자인</span><span class="sxs-lookup"><span data-stu-id="2b2c4-138">Use Q# to design quantum algorithms</span></span>

<span data-ttu-id="2b2c4-139">Q#은 고급 양자 알고리즘을 빌드하는 데 도움이 되는 라이브러리와 사용자 정의 형식을 점점 더 많이 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-139">Q# provides you with an increasing number of libraries and user-defined types that will help you to implement tools and build advanced quantum algorithms.</span></span> <span data-ttu-id="2b2c4-140">예를 들어 q1과 q2의 두 큐비트를 얽어야 할까요?</span><span class="sxs-lookup"><span data-stu-id="2b2c4-140">For example, you need to entangle two-qubits q1 and q2?</span></span> <span data-ttu-id="2b2c4-141">필요한 게이트를 개별적으로 적용하여 큐비트를 얽는 대신, 이미 기본 제공된 `PrepareEntangledState([q1], [q2])` 연산을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-141">Instead of applying individually the necessary gates to get the qubits entangled you can use the already built-in operation `PrepareEntangledState([q1], [q2])`.</span></span>

### <a name="use-q-to-estimate-quantum-resources"></a><span data-ttu-id="2b2c4-142">Q#을 사용하여 양자 리소스 예측</span><span class="sxs-lookup"><span data-stu-id="2b2c4-142">Use Q# to estimate quantum resources</span></span>

<span data-ttu-id="2b2c4-143">QDK(Quantum Development Kit)와 함께 제공되는 전체 상태 양자 시뮬레이터를 사용하여 Q# 프로그램 실행을 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-143">You can simulate the execution of your Q# program using the full state quantum simulator that is provided with the Quantum Development Kit (QDK).</span></span>  <span data-ttu-id="2b2c4-144">QDK는 너무 커서 시뮬레이터에서 실행할 수 없는 Q# 프로그램에 대한 인사이트를 제공하는 리소스 예측기도 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-144">The QDK also provides resource estimators that give you insights on the performance of Q# programs that are too large to be run on a simulator.</span></span>  <span data-ttu-id="2b2c4-145">알고리즘 디자이너는 더 적은 리소스를 사용하도록(즉, 더 적은 수의 작업에 대해 더 적은 수의 큐비트가 실행되도록), 초기에 더 작은 규모의 양자 하드웨어에서 실행되도록 프로그램을 튜닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-145">This is highly valuable for algorithm designers, because they can tune their programs to use fewer resources (e.g. fewer number of qubits running for fewer numbers of operations), to run on earlier smaller scale quantum hardware.</span></span>

### <a name="use-q-to-validate-hardware-performance"></a><span data-ttu-id="2b2c4-146">Q#을 사용하여 하드웨어 성능 확인</span><span class="sxs-lookup"><span data-stu-id="2b2c4-146">Use Q# to validate hardware performance</span></span>

<span data-ttu-id="2b2c4-147">Q#의 장점은 프로그램을 한 번 작성하여 양자 시뮬레이터에서 실행하면 여러 양자 컴퓨터 하드웨어에서 실행할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-147">The beauty of Q# is that a program can be written once and run on quantum simulators for debugging, and run on different quantum computer hardware.</span></span>  <span data-ttu-id="2b2c4-148">양자 컴퓨터가 진화하여 새로운 양자 컴퓨터를 사용할 수 있게 될 때 Q#으로 작성된 벤치마크 프로그램을 실행하여 하드웨어 성능을 확인하고 결과를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b2c4-148">Benchmark programs written in Q# can be run to validate hardware performance and compare results as quantum computers evolve and new quantum computers become available.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="2b2c4-149">다음 단계</span><span class="sxs-lookup"><span data-stu-id="2b2c4-149">Next steps</span></span>

* [<span data-ttu-id="2b2c4-150">양자 컴퓨팅을 학습하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="2b2c4-150">How do I learn about quantum computing?</span></span>](xref:microsoft.quantum.overview.learn)
* [<span data-ttu-id="2b2c4-151">Microsoft Quantum Development Kit 시작</span><span class="sxs-lookup"><span data-stu-id="2b2c4-151">Get started with the Microsoft Quantum Development Kit</span></span>](xref:microsoft.quantum.welcome)
