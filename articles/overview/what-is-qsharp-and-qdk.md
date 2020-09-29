---
title: Q# 프로그래밍 언어 및 QDK란?
description: Microsoft Quantum Development Kit, Q# 프로그래밍 언어 및 퀀텀 프로그램을 만드는 방법에 대해 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.q-sharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: 21adfcc1c5321d87665adb39a3c838bbda0b8861
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834570"
---
# <a name="what-are-the-no-locq-programming-language-and-qdk"></a><span data-ttu-id="1f6f3-103">Q# 프로그래밍 언어 및 QDK란?</span><span class="sxs-lookup"><span data-stu-id="1f6f3-103">What are the Q# programming language and QDK?</span></span>

<span data-ttu-id="1f6f3-104">Q#은 퀀텀 알고리즘을 개발하고 실행하기 위한 Microsoft의 오픈 소스 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-104">Q# is Microsoft’s open-source programming language for developing and running quantum algorithms.</span></span> <span data-ttu-id="1f6f3-105">이는 [Q#Q# 라이브러리](xref:microsoft.quantum.libraries), [퀀텀 시뮬레이터](xref:microsoft.quantum.machines), [다른 프로그래밍 환경용 확장](xref:microsoft.quantum.install) 및 [API 설명서](xref:microsoft.quantum.apiref-intro)가 포함된 QDK(Qualument Development Kit)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-105">It’s part of the Quantum Development Kit (QDK), which includes [Q# libraries](xref:microsoft.quantum.libraries), [quantum simulators](xref:microsoft.quantum.machines), [extensions for other programming environments](xref:microsoft.quantum.install), and [API documentation](xref:microsoft.quantum.apiref-intro).</span></span> <span data-ttu-id="1f6f3-106">QDK에는 표준 Q# 라이브러리 외에도 화학, Machine Learning 및 숫자 라이브러리가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-106">In addition to the Standard Q# library, the QDK includes Chemistry, Machine Learning, and Numeric libraries.</span></span>

<span data-ttu-id="1f6f3-107">프로그래밍 언어인 Q#은 Python, C# 및 F#에서 친숙한 요소를 가져오고 반복, if/then 문 및 공통 데이터 형식을 사용하여 프로그램을 작성하는 기본 절차 모델을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-107">As a programming language, Q# draws familiar elements from Python, C#, and F# and supports a basic procedural model for writing programs with loops, if/then statements, and common data types.</span></span> <span data-ttu-id="1f6f3-108">또한 새로운 양자 관련 데이터 구조 및 연산도 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-108">It also introduces new quantum-specific data structures and operations.</span></span>

## <a name="what-can-i-do-with-the-qdk"></a><span data-ttu-id="1f6f3-109">QDK에서 수행할 수 있는 작업은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="1f6f3-109">What can I do with the QDK?</span></span>

<span data-ttu-id="1f6f3-110">완전한 기능을 갖춘 Q#용 개발 키트인 QDK는 일반적인 도구 및 언어와 함께 사용하여 다양한 환경에서 실행할 수 있는 퀀텀 애플리케이션을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-110">The QDK is a full-featured development kit for Q# that you can use with common tools and languages to develop quantum applications that you can run in various environments.</span></span> <span data-ttu-id="1f6f3-111">Q# 프로그램은 Jupyter Notebook을 통해 콘솔 애플리케이션으로 실행하거나 Python 또는 .NET 호스트 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-111">Q# programs can run as a console application, through Jupyter Notebooks, or use a Python or .NET host program.</span></span>

### <a name="develop-in-common-tools-and-environments"></a><span data-ttu-id="1f6f3-112">일반적인 도구 및 환경에서 개발</span><span class="sxs-lookup"><span data-stu-id="1f6f3-112">Develop in common tools and environments</span></span>

<span data-ttu-id="1f6f3-113">양자 개발을 [Visual Studio, Visual Studio Code](xref:microsoft.quantum.install.standalone) 및 [Jupyter Notebook](xref:microsoft.quantum.install.jupyter)과 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-113">Integrate your quantum development with [Visual Studio, Visual Studio Code](xref:microsoft.quantum.install.standalone), and [Jupyter Notebooks](xref:microsoft.quantum.install.jupyter).</span></span> <span data-ttu-id="1f6f3-114">기본 제공 API를 사용하여 프로그램을 [Python](xref:microsoft.quantum.install.python) 및 [.NET](xref:microsoft.quantum.install.cs) 호스트 언어와 페어링합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-114">Use the built-in APIs for pairing your programs with [Python](xref:microsoft.quantum.install.python) and [.NET](xref:microsoft.quantum.install.cs) host languages.</span></span>

### <a name="try-quantum-operations-and-domain-specific-libraries"></a><span data-ttu-id="1f6f3-115">양자 연산 및 도메인별 라이브러리 사용해 보기</span><span class="sxs-lookup"><span data-stu-id="1f6f3-115">Try quantum operations and domain-specific libraries</span></span>

<span data-ttu-id="1f6f3-116">중첩, 얽힘 및 기타 양자 연산을 검색하는 양자 알고리즘을 작성하고 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-116">Write and test quantum algorithms to explore superposition, entanglement, and other quantum operations.</span></span> <span data-ttu-id="1f6f3-117">Q# 라이브러리를 사용하면 하위 수준의 연산 순서를 설계하지 않고도 복잡한 퀀텀 연산을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-117">The Q# libraries enable you to run complex quantum operations without having to design low-level operation sequences.</span></span>

### <a name="run-programs-in-simulators"></a><span data-ttu-id="1f6f3-118">시뮬레이터에서 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="1f6f3-118">Run programs in simulators</span></span>

<span data-ttu-id="1f6f3-119">전체 상태 퀀텀 시뮬레이터, 제한된 범위의 Toffoli 시뮬레이터에서 퀀텀 프로그램을 실행하거나 다른 리소스 예측 도구에서 Q# 코드를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-119">Run your quantum programs on a full-state quantum simulator, a limited-scope Toffoli simulator, or test your Q# code in different resource estimators.</span></span> 

## <a name="where-can-i-learn-more"></a><span data-ttu-id="1f6f3-120">자세한 내용을 알아보려면 어떤 정보를 참조해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="1f6f3-120">Where can I learn more?</span></span>

|||
| ---- | ---- |
| <span data-ttu-id="1f6f3-121">**양자 컴퓨팅을 처음 접하는 경우**</span><span class="sxs-lookup"><span data-stu-id="1f6f3-121">**I'm new to quantum computing**</span></span> | <span data-ttu-id="1f6f3-122">[주요 개념](xref:microsoft.quantum.overview.understanding)에서 양자 물리학 및 양자 컴퓨팅에 대한 몇 가지 기본 사항을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-122">Review some basics of quantum physics and quantum computing in [Key Concepts](xref:microsoft.quantum.overview.understanding).</span></span>|
| <span data-ttu-id="1f6f3-123">**Q# 언어에 대해 자세히 알아보려는 경우**</span><span class="sxs-lookup"><span data-stu-id="1f6f3-123">**I want to dive deeper into the Q# language**</span></span> | <span data-ttu-id="1f6f3-124">[Q# 사용자 가이드](xref:microsoft.quantum.guide)에서 형식, 식, 변수 및 퀀텀 프로그램 구조를 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-124">Explore types, expressions, variables, and quantum program structure in the [Q# User Guide](xref:microsoft.quantum.guide).</span></span>|
| <span data-ttu-id="1f6f3-125">**양자 프로그램 작성을 시작하려는 경우**</span><span class="sxs-lookup"><span data-stu-id="1f6f3-125">**I just want to start writing quantum programs**</span></span> | <span data-ttu-id="1f6f3-126">Q# 환경을 설치하고, [빠른 시작](xref:microsoft.quantum.install)에서 퀀텀 프로그램 작성을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-126">Set up your Q# environment and start writing quantum programs in [QuickStarts](xref:microsoft.quantum.install).</span></span>|

## <a name="how-does-no-locq-work"></a><span data-ttu-id="1f6f3-127">Q# 작동 방식</span><span class="sxs-lookup"><span data-stu-id="1f6f3-127">How does Q# work?</span></span>

<span data-ttu-id="1f6f3-128">Q# 프로그램은 독립 실행형 애플리케이션으로 컴파일하거나 Python 또는 .NET 언어로 작성된 호스트 프로그램에서 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-128">A Q# program can compile into a standalone application or be called by a host program that is written either in Python or a .NET language.</span></span>

<span data-ttu-id="1f6f3-129">프로그램을 컴파일하고 실행하면 퀀텀 시뮬레이터의 인스턴스가 만들어지고 Q# 코드가 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-129">When you compile and run the program, it creates an instance of the quantum simulator and passes the Q# code to it.</span></span> <span data-ttu-id="1f6f3-130">시뮬레이터는 Q# 코드를 사용하여 큐비트를 만들고(퀀텀 입자 시뮬레이션), 변환을 적용하여 해당 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-130">The simulator uses the Q# code to create qubits (simulations of quantum particles) and apply transformations to modify their state.</span></span> <span data-ttu-id="1f6f3-131">그런 다음, 시뮬레이터의 양자 연산 결과가 프로그램에 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-131">The results of the quantum operations in the simulator are then returned to the program.</span></span>  

<span data-ttu-id="1f6f3-132">시뮬레이터에서 Q# 코드를 격리하면 알고리즘이 양자 물리학 법칙을 따르고 양자 컴퓨터에서 올바르게 실행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-132">Isolating the Q# code in the simulator ensures that the algorithms follow the laws of quantum physics and can run correctly on quantum computers.</span></span>

![Qsharp 코드 흐름](~/media/qsharp-code-flow.png)

## <a name="how-do-i-use-the-qdk"></a><span data-ttu-id="1f6f3-134">QDK를 사용하려면 어떻게 할까요?</span><span class="sxs-lookup"><span data-stu-id="1f6f3-134">How do I use the QDK?</span></span>

<span data-ttu-id="1f6f3-135">Q# 컴파일러, Q# 라이브러리 및 퀀텀 시뮬레이터를 포함하여 Q# 프로그램을 작성하고 실행하는 데 필요한 모든 항목을 로컬 컴퓨터에서 설치하고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-135">Everything you need to write and run Q# programs, including the Q# compiler, the Q# libraries, and the quantum simulators, can be installed and run from your local computer.</span></span> <span data-ttu-id="1f6f3-136">결국에는 실제 양자 컴퓨터에서 Q# 프로그램을 원격으로 실행할 수 있지만, 그 후에는 QDK에서 제공되는 퀀텀 시뮬레이터에서 정확하고 신뢰할 수 있는 결과를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-136">Eventually you will be able to run your Q# programs remotely on an actual quantum computer, but until then the quantum simulators provided with the QDK provide accurate and reliable results.</span></span>

- <span data-ttu-id="1f6f3-137">[Q# 애플리케이션](xref:microsoft.quantum.install.standalone) 개발을 개발하는 것이 가장 빨리 시작하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-137">Developing [Q# applications](xref:microsoft.quantum.install.standalone) is the quickest way to get started.</span></span>

- <span data-ttu-id="1f6f3-138">Q# 프로그램을 컴파일, 시뮬레이션 및 시각화하는 Jupyter 확장인 [IQ#를 사용하여 독립 실행형 Jupyter Notebook을 실행](xref:microsoft.quantum.install.jupyter)합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-138">Run standalone [Jupyter Notebooks with IQ#](xref:microsoft.quantum.install.jupyter), a Jupyter extension for compiling, simulating, and visualizing Q# programs.</span></span>

- <span data-ttu-id="1f6f3-139">[Python](xref:microsoft.quantum.install.python)에 익숙한 경우 이를 호스트 프로그래밍 플랫폼으로 사용하여 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-139">If you are familiar with [Python](xref:microsoft.quantum.install.python), you can use it as a host programming platform to get started.</span></span> <span data-ttu-id="1f6f3-140">Python은 개발자뿐만 아니라 과학자, 연구원 및 교사 사이에서도 널리 사용되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-140">Python enjoys widespread use not only among developers, but also scientists, researchers and teachers.</span></span>

- <span data-ttu-id="1f6f3-141">이미 [C#, F# 또는 VB.NET](xref:microsoft.quantum.install.cs)을 사용한 경험이 있고 Visual Studio 개발 환경에 익숙한 경우 Q#을 준비하려면 몇 가지 확장만 Visual Studio에 추가하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-141">If you already have experience with [C#, F#, or VB.NET](xref:microsoft.quantum.install.cs) and are familiar with the Visual Studio development environment, there are just a few extensions you need to add to Visual Studio to prepare it for Q#.</span></span>  

## <a name="summary"></a><span data-ttu-id="1f6f3-142">요약</span><span class="sxs-lookup"><span data-stu-id="1f6f3-142">Summary</span></span>

<span data-ttu-id="1f6f3-143">Q#은 퀀텀 프로그램을 개발하기 위한 오픈 소스 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-143">Q# is an open-source programming language for developing quantum programs.</span></span> <span data-ttu-id="1f6f3-144">여기에는 복합 양자 연산을 만들 수 있는 라이브러리 및 프로그램을 정확하게 실행하고 테스트할 수 있는 양자 시뮬레이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-144">It has libraries that let you create complex quantum operations, and quantum simulators to accurately run and test your programs.</span></span> <span data-ttu-id="1f6f3-145">Q# 프로그램은 독립 실행형 앱으로 실행되거나 Python 또는 .NET 호스트 프로그램에서 호출될 수 있으며 로컬 컴퓨터에서 작성, 실행 및 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-145">Q# programs can run as standalone apps or be called from a Python or .NET host program, and can be written, run, and tested from your local computer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1f6f3-146">다음 단계</span><span class="sxs-lookup"><span data-stu-id="1f6f3-146">Next Steps</span></span>

[<span data-ttu-id="1f6f3-147">양자 컴퓨팅을 위한 선형 대수</span><span class="sxs-lookup"><span data-stu-id="1f6f3-147">Linear algebra for quantum computing</span></span>](xref:microsoft.quantum.overview.algebra)
