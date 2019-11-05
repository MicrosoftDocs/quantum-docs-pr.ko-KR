---
title: Q#이란?
description: 양자 컴퓨터 애플리케이션을 개발하기 위해 Microsoft에서 만든 프로그래밍 언어인 Q#에 대해 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: e04228ff62092a15c529297bd56b9ee48399f4a5
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443956"
---
# <a name="what-is-q"></a><span data-ttu-id="9de66-103">Q#이란?</span><span class="sxs-lookup"><span data-stu-id="9de66-103">What is Q#?</span></span>

<span data-ttu-id="9de66-104">Q#은 양자 컴퓨팅에 특화된 기능이 포함된 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-104">Q# is a programming language with features that are special to quantum computing.</span></span> <span data-ttu-id="9de66-105">Q#은 양자 프로그래머에게 게이트 시퀀스 최적화 또는 양자 컴퓨터의 물리적 구현과 같은 기술적 세부 정보를 고려하지 않고도 알고리즘에 집중할 수 있는 프레임워크를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-105">Q# provides quantum programmers a framework that allows you to focus on the algorithms without having to care about technical details like gate sequence optimization or the physical implementation of a quantum computer.</span></span>

<span data-ttu-id="9de66-106">Q#프로그래밍 언어는 양자 컴퓨터의 내부의 논리에 대해 걱정할 필요 없이 알고리즘을 개발할 수 있도록 형식, 연산 및 논리 식의 직관적인 세트를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-106">The Q# programming language provides you with an intuitive set of types, operations and logic expressions to develop algorithms without having to worry about the internal logic of the quantum computer.</span></span>

## <a name="code-algorithms"></a><span data-ttu-id="9de66-107">코드 알고리즘</span><span class="sxs-lookup"><span data-stu-id="9de66-107">Code algorithms</span></span>

<span data-ttu-id="9de66-108">초기 시대의 양자 컴퓨팅 알고리즘은 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-108">In the early days of quantum computing algorithms were visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>  <span data-ttu-id="9de66-109">회로 모델은 Microsoft에서 수년간 양자 컴퓨팅 연구에 매우 유용했지만, 개발자는 양자 회로를 넘어서 Q#을 사용하여 양자 알고리즘과 애플리케이션을 개발할 수 있다고 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-109">While the circuit model has been very useful for many years in quantum computing research, here at Microsoft, we believe that developers can go beyond quantum circuits and develop quantum algorithms and applications using Q#.</span></span> <span data-ttu-id="9de66-110">Q# 언어는 수십 년간 클래식 소프트웨어 개발을 통해 습득한 것을 활용하고, 특히 양자 컴퓨팅을 대상으로 하는 고급 언어 기능을 양자 개발자에게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-110">The Q# language was built to take advantage of what we’ve learned through decades of classical software development, and empower quantum developers with high-level language functionality specifically targeted for quantum computing.</span></span>


## <a name="how-does-q-work"></a><span data-ttu-id="9de66-111">Q#은 어떻게 작동하나요?</span><span class="sxs-lookup"><span data-stu-id="9de66-111">How does Q# work?</span></span>

<span data-ttu-id="9de66-112">Q#의 기본 구성 요소 중 하나는 `Qubit` 형식이며, 실제 큐비트처럼 복사하거나 직접 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-112">One of the fundamental building blocks of Q# is the `Qubit` type, which cannot be copied or directly accessed, just like a real qubit.</span></span> <span data-ttu-id="9de66-113">대신, 이를 측정하여 `Zero` 및 `One`의 두 가지 가능한 값을 사용할 수 있는 Q# 형식의 `Result` 변수에 측정 결과를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-113">Instead, we can measure it and store the outcome of the measurement in a `Result` variable, a Q# type that can take two possible values: `Zero` and `One`.</span></span> <span data-ttu-id="9de66-114">이와 같은 구문을 통해 알고리즘은 항상 양자 물리학의 법칙을 준수하며 양자 컴퓨터 또는 시뮬레이터에서 올바르게 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-114">Constructs like this one guarantee that algorithms always respect the laws of quantum physics and can run correctly on quantum computers or simulators.</span></span>

<span data-ttu-id="9de66-115">또한 Q#에는 모든 양자 규칙이 적용될 수 있도록 조건 또는 루프 같은 클래식 논리 기능도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-115">Q# also includes classical logic features like conditionals or loops with some subtleties to make sure that all the quantum rules are being respected.</span></span> <span data-ttu-id="9de66-116">예를 들어 양자 연산은 되돌릴 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-116">For example, quantum operations need to be reversible.</span></span> <span data-ttu-id="9de66-117">이렇게 하면 루프가 실행되는 방식에 일부 제약 조건이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-117">This enforces some constraints on the way loops are executed.</span></span>

<span data-ttu-id="9de66-118">Q# 프로그램은 종종 C# 또는 Python으로 작성된 호스트 프로그램과 쌍을 이루어 클래식 코드와 양자 코드를 편리하게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-118">Q# programs are often paired with a host program written in C# or Python, which can provide convenient organization of classical and quantum code.</span></span> <span data-ttu-id="9de66-119">QDK는 C# 및 Python과 같은 .NET 언어를 지원하는 것 외에도 IQ# Juppyter 커널을 사용하여 Jupyter Notebook을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-119">In addition to supporting .NET languages such as C# and Python, the QDK provides Jupyter Notebook support with the IQ# Jupyter kernel.</span></span>

## <a name="use-q-to-learn-quantum-computing"></a><span data-ttu-id="9de66-120">Q#을 사용하여 양자 컴퓨팅 학습</span><span class="sxs-lookup"><span data-stu-id="9de66-120">Use Q# to learn quantum computing</span></span>

<span data-ttu-id="9de66-121">지금까지 양자 컴퓨팅을 학습하려면 순서가 지정된 양자 게이트와 측정의 시퀀스 형식으로 알고리즘을 이해하기 위해 회로 모델을 학습해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-121">Until now, to learn quantum computing you needed to learn the circuit model to understand the algorithms in the form of ordered sequences of quantum gates and measurements.</span></span> <span data-ttu-id="9de66-122">Q#을 사용하면 양자 프로그램을 작성하여 양자 컴퓨팅을 학습할 수 있는 다른 경로를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-122">With Q# you can take another path: learn quantum computing by writing quantum programs.</span></span>

## <a name="use-q-to-design-quantum-algorithms"></a><span data-ttu-id="9de66-123">Q#을 사용하여 양자 알고리즘 디자인</span><span class="sxs-lookup"><span data-stu-id="9de66-123">Use Q# to design quantum algorithms</span></span>

<span data-ttu-id="9de66-124">Q#은 고급 양자 알고리즘을 빌드하는 데 도움이 되는 라이브러리와 사용자 정의 형식을 점점 더 많이 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-124">Q# provides you with an increasing number of libraries and user-defined types that will help you to implement tools and build advanced quantum algorithms.</span></span> <span data-ttu-id="9de66-125">예를 들어 q1과 q2의 두 큐비트를 얽어야 할까요?</span><span class="sxs-lookup"><span data-stu-id="9de66-125">For example, you need to entangle two-qubits q1 and q2?</span></span> <span data-ttu-id="9de66-126">필요한 게이트를 개별적으로 적용하여 큐비트를 얽는 대신, 이미 기본 제공된 `PrepareEntangledState([q1], [q2])` 연산을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-126">Instead of applying individually the necessary gates to get the qubits entangled you can use the already built-in operation `PrepareEntangledState([q1], [q2])`.</span></span>

## <a name="use-q-to-estimate-quantum-resources"></a><span data-ttu-id="9de66-127">Q#을 사용하여 양자 리소스 예측</span><span class="sxs-lookup"><span data-stu-id="9de66-127">Use Q# to estimate quantum resources</span></span>

<span data-ttu-id="9de66-128">QDK(Quantum Development Kit)와 함께 제공되는 전체 상태 양자 시뮬레이터를 사용하여 Q# 프로그램 실행을 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-128">You can simulate the execution of your Q# program using the full state quantum simulator that is provided with the Quantum Development Kit (QDK).</span></span>  <span data-ttu-id="9de66-129">QDK는 너무 커서 시뮬레이터에서 실행할 수 없는 Q# 프로그램에 대한 인사이트를 제공하는 리소스 예측기도 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-129">The QDK also provides resource estimators that give you insights on the performance of Q# programs that are too big to be run on a simulator.</span></span>  <span data-ttu-id="9de66-130">알고리즘 디자이너는 더 적은 리소스를 사용하도록(즉, 더 적은 수의 작업에 대해 더 적은 수의 큐비트가 실행되도록), 초기에 더 작은 규모의 양자 하드웨어에서 실행되도록 프로그램을 튜닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-130">This is highly valuable for algorithm designers, because they can tune their programs to use fewer resources (e.g. fewer number of qubits running for fewer numbers of operations), to run on earlier smaller scale quantum hardware.</span></span>   

## <a name="use-q-to-validate-hardware-performance"></a><span data-ttu-id="9de66-131">Q#을 사용하여 하드웨어 성능 확인</span><span class="sxs-lookup"><span data-stu-id="9de66-131">Use Q# to validate hardware performance</span></span>

<span data-ttu-id="9de66-132">Q#의 장점은 프로그램을 한 번 작성하여 양자 시뮬레이터에서 실행하면 여러 양자 컴퓨터 하드웨어에서 실행할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-132">The beauty of Q# is that a program can be written once and run on quantum simulators for debugging, and run on multiple quantum computer hardware.</span></span>  <span data-ttu-id="9de66-133">양자 컴퓨터가 진화하여 새로운 양자 컴퓨터를 사용할 수 있게 될 때 Q#으로 작성된 벤치마크 프로그램을 실행하여 하드웨어 성능을 확인하고 결과를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de66-133">Benchmark programs written in Q# can be run to validate hardware performance and compare results as quantum computers evolve and new quantum computers become available.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="9de66-134">다음 단계</span><span class="sxs-lookup"><span data-stu-id="9de66-134">Next steps</span></span>

* [<span data-ttu-id="9de66-135">양자 컴퓨팅을 학습하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="9de66-135">How do I learn quantum computing?</span></span>](xref:microsoft.quantum.overview.learn)
* [<span data-ttu-id="9de66-136">Microsoft Quantum Development Kit 시작</span><span class="sxs-lookup"><span data-stu-id="9de66-136">Get started with the Microsoft Quantum Development Kit</span></span>](xref:microsoft.quantum.welcome)
