---
title: Q# 사용자 가이드
description: 사용자 가이드의 용도 및 내용 개요
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430614"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="df845-103">Q# 사용자 가이드</span><span class="sxs-lookup"><span data-stu-id="df845-103">The Q# User Guide</span></span>

<span data-ttu-id="df845-104">Q# 사용자 가이드 시작!</span><span class="sxs-lookup"><span data-stu-id="df845-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="df845-105">여기에서는 Q# 언어의 핵심 개념과 양자 프로그램을 작성하는 데 필요한 모든 정보를 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-105">Here we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="df845-106">사용자 가이드 내용</span><span class="sxs-lookup"><span data-stu-id="df845-106">User Guide Contents</span></span>

- <span data-ttu-id="df845-107">[Q# 기본 사항](xref:microsoft.quantum.guide.basics): Q# 프로그래밍 언어의 목적과 기능에 대한 소개 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="df845-107">[Q# Basics](xref:microsoft.quantum.guide.basics): an introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="df845-108">Q# 언어</span><span class="sxs-lookup"><span data-stu-id="df845-108">Q# Language</span></span>

- <span data-ttu-id="df845-109">[Q#의 형식](xref:microsoft.quantum.guide.types): Q# 형식 모델을 배치하고 형식을 지정하고 사용하는 구문을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-109">[Types in Q#](xref:microsoft.quantum.guide.types): lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="df845-110">[Type 식](xref:microsoft.quantum.guide.expressions): Q#에서 각 형식의 값을 지정하고, 참조하고, 결합하고, 연산하는 방법을 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="df845-111">Q# 사용</span><span class="sxs-lookup"><span data-stu-id="df845-111">Using Q#</span></span>

- <span data-ttu-id="df845-112">[Q# 파일 구조](xref:microsoft.quantum.guide.filestructure): `*.qs` Q# 파일의 구문과 구조를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="df845-113">[연산 및 함수](xref:microsoft.quantum.guide.operationsfunctions): Q# 언어의 두 가지 호출 가능 형식, 즉, 큐비트 레지스터에 대한 동작을 포함하는 *연산* 및 클래식 정보와 엄격하게 작동하는 *함수*에 대해 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): details the two callable types of the Q# language: *operations*, which include action on qubit registers and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="df845-114">여기에서는 수반(adjoint) 및 제어된 양자 연산 버전을 포함하여 이러한 형식을 정의하고 호출하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="df845-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="df845-115">[변수](xref:microsoft.quantum.guide.variables): Q# 프로그램 내 변수의 역할 및 변수를 효과적으로 활용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-115">[Variables](xref:microsoft.quantum.guide.variables): describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="df845-116">예를 들어, 바인딩 범위에 대한 정보는 물론 변경 불가능/변경 가능 변수의 차이와 이러한 변수를 할당/재할당하는 방법에 대한 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df845-116">For example, you can find information about binding scopes, as well as the difference between immutable/mutable variables and how to assign/re-assign them.</span></span>

- <span data-ttu-id="df845-117">[큐비트 사용](xref:microsoft.quantum.guide.qubits): 개별 큐비트 및 큐비트 시스템을 처리하는 데 사용되는 Q#의 기능을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): describes the features of Q# used to address individual qubits and systems of qubits.</span></span> 
    <span data-ttu-id="df845-118">구체적으로 말하자면, 큐비트를 할당하고, 큐비트에 대한 작업을 수행하고, 궁극적으로 큐비트를 측정하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-118">Specifically, that entails their allocation, performing operations on them, and ultimately their measurement.</span></span> 

- <span data-ttu-id="df845-119">[제어 흐름](xref:microsoft.quantum.guide.controlflow): Q# 에서 사용 가능한 프로그래밍 제어 흐름 패턴에 대해 자세히 설명합니다. 여기에는 다양한 표준 기술(조건부 실행, for 루프, while 루프 등)은 물론 양자 관련 "Repeat-Until-Success"(성공할 때까지 반복) 패턴이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="df845-119">[Control Flow](xref:microsoft.quantum.guide.controlflow): details the programming control flow patterns available in Q#, which includes many standard techniques (conditional execution, for loops, while loops, etc.) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="df845-120">[테스트 및 디버그](xref:microsoft.quantum.guide.testingdebugging): 코드가 수행해야 하는 작업을 수행하도록 만드는 몇 가지 기술을 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-120">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="df845-121">양자 정보는 일반적으로 불투명하기 때문에 양자 프로그램을 디버깅하려면 특수 기술이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df845-121">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="df845-122">다행히 Q#은 양자 관련 기술 외에도 프로그래머들에게 익숙한 여러 기존 디버깅 기술을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-122">Fortunately, Q# supports many of the classical debugging techniques programmers are used to, as well as those that are quantum-specific.</span></span> <span data-ttu-id="df845-123">여기에는 Q#에서 단위 테스트를 만들고/실행하는 기능, 그리고 코드의 값 및 확률과 대상 머신의 상태를 출력하는 `Dump` 함수에 대한 *어설션*을 포함하는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="df845-123">These include creating/running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the state of target machine.</span></span> 
    <span data-ttu-id="df845-124">후자는 전체 상태 시뮬레이터와 함께 사용하여 일부 양자 제한을 회피(예: 복사 불가능성 정리)하는 방식으로 계산의 특정 부분을 디버그할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df845-124">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations (e.g. the no-cloning theorem).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="df845-125">양자 시뮬레이터 및 리소스 예측 도구</span><span class="sxs-lookup"><span data-stu-id="df845-125">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="df845-126">[양자 시뮬레이터 및 호스트 애플리케이션](xref:microsoft.quantum.machines): 사용 가능한 여러 시뮬레이터에 대한 개요 및 호스트 프로그램과 대상 머신 간의 일반적인 실행 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="df845-126">[Quantum simulators and host applications](xref:microsoft.quantum.machines): an overview of the different simulators available, as well as the general execution model between host program and target machines.</span></span>

- <span data-ttu-id="df845-127">[전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator): 전체 양자 상태를 시뮬레이션하는 대상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="df845-127">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): the target machine which simulates the full quantum state.</span></span> <span data-ttu-id="df845-128">소규모 프로그램(수십 큐비트 미만)을 완전히 실행하거나 디버그하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-128">Useful for fully executing or debugging smaller scale programs (less than a couple dozen qubits)</span></span>

- <span data-ttu-id="df845-129">[리소스 예측 도구](xref:microsoft.quantum.machines.resources-estimator): 양자 컴퓨터에서 지정된 Q# 연산 인스턴스를 실행하는 데 필요한 리소스를 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-129">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="df845-130">[추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro): 실제로 양자 컴퓨터의 상태를 시뮬레이션하지 않고 양자 프로그램을 실행하기 때문에 수천 큐비트를 사용하는 양자 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df845-130">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="df845-131">양자 프로그램 내에서 클래식 코드를 디버그하는 것은 물론 필요한 리소스를 예측하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="df845-131">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="df845-132">[Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator): 수백만 큐비트에 사용할 수 있는 특수 목적의 양자 시뮬레이터입니다. 단, 제한된 양자 연산 세트(즉, X, CNOT 및 다중 제어 X)가 있는 프로그램에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df845-132">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): a special purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations (namely X, CNOT, and multi-controlled X).</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="df845-133">빠른 참조 페이지</span><span class="sxs-lookup"><span data-stu-id="df845-133">Quick Reference Pages</span></span>

- <span data-ttu-id="df845-134">[IQ# 매직 명령](xref:microsoft.quantum.guide.quickref.iqsharp): Q# Jupyter Notebook 내 IQ# 매직 명령에 대한 빠른 참조 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="df845-134">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
