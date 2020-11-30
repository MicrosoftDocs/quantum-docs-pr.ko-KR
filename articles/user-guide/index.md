---
title: Q# 사용자 가이드
description: 사용자 가이드의 용도 및 내용 개요
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231760"
---
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="6019d-103">Q# 사용자 가이드</span><span class="sxs-lookup"><span data-stu-id="6019d-103">The Q# User Guide</span></span>

<span data-ttu-id="6019d-104">Q# 사용자 가이드 시작!</span><span class="sxs-lookup"><span data-stu-id="6019d-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="6019d-105">이 가이드의 다른 항목에서는 Q#를 사용하여 퀀텀 프로그램을 개발하기 위한 몇 가지 기본 사항을 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-105">In the different topics of this guide, we introduce some of the basics for developing quantum programs using Q#.</span></span>

<span data-ttu-id="6019d-106">Q# 퀀텀 프로그래밍 언어에 대한 전체 사양과 설명서는 [Q# 언어 가이드](xref:microsoft.quantum.qsharp.index)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6019d-106">We refer to the [Q# language guide](xref:microsoft.quantum.qsharp.index) for a full specification and documentation of the Q# quantum programming language.</span></span> 

## <a name="user-guide-contents"></a><span data-ttu-id="6019d-107">사용자 가이드 내용</span><span class="sxs-lookup"><span data-stu-id="6019d-107">User Guide Contents</span></span>

- <span data-ttu-id="6019d-108">[Q# 프로그램](xref:microsoft.quantum.guide.programs): Q#의 퀀텀 프로그램에 대한 간략한 소개입니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-108">[Q# programs](xref:microsoft.quantum.guide.programs): An quick introduction to quantum programs in Q#.</span></span> 

- <span data-ttu-id="6019d-109">[Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs): Q# 프로그램을 실행하는 방법을 설명하고, 프로그램을 호출할 수 있는 다양한 방법(명령줄에서, Q# Jupyter Notebook에서 또는 Python이나 .NET 언어로 작성된 기존 호스트 프로그램에서)에 대한 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-109">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

- <span data-ttu-id="6019d-110">[테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging): 코드가 수행해야 하는 작업을 수행하도록 만드는 몇 가지 기술을 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-110">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="6019d-111">양자 정보는 일반적으로 불투명하기 때문에 양자 프로그램을 디버깅하려면 특수 기술이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-111">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="6019d-112">다행히 Q#은 퀀텀 관련 기술 외에도 프로그래머들에게 익숙한 여러 기존 디버깅 기술을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-112">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="6019d-113">여기에는 Q#에서 단위 테스트를 만들어 실행하는 기능, 그리고 코드의 값 및 확률과 대상 머신의 상태를 출력하는 `Dump` 함수에 대한 *어설션* 을 포함하는 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-113">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="6019d-114">후자는 전체 상태 시뮬레이터와 함께 사용하여 일부 퀀텀 제한을 회피(예: [복사 불가능성 정리](xref:microsoft.quantum.concepts.pauli))하는 방식으로 계산의 특정 부분을 디버그할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-114">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="6019d-115">양자 시뮬레이터 및 리소스 예측 도구</span><span class="sxs-lookup"><span data-stu-id="6019d-115">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="6019d-116">[퀀텀 시뮬레이터 및 호스트 애플리케이션](xref:microsoft.quantum.machines): 사용 가능한 여러 시뮬레이터와 호스트 프로그램 및 대상 머신이 함께 작동하여 Q# 프로그램을 실행하는 방법에 대한 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-116">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well of how host programs and target machines work together to run Q# programs.</span></span>

- <span data-ttu-id="6019d-117">[전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator): 전체 퀀텀 상태를 시뮬레이션하는 대상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-117">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="6019d-118">소규모 프로그램(몇십 큐비트 미만)을 완전히 실행하거나 디버그하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-118">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="6019d-119">[리소스 추정기](xref:microsoft.quantum.machines.resources-estimator): 퀀텀 컴퓨터에서 지정된 Q# 연산 인스턴스를 실행하는 데 필요한 리소스를 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-119">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="6019d-120">[추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro): 실제로 퀀텀 컴퓨터의 상태를 시뮬레이션하지 않고 퀀텀 프로그램을 실행하기 때문에 수천 큐비트를 사용하는 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-120">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="6019d-121">양자 프로그램 내에서 클래식 코드를 디버그하는 것은 물론 필요한 리소스를 예측하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-121">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="6019d-122">[Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator): 수백만 큐비트에 사용할 수 있는 특수 목적의 퀀텀 시뮬레이터입니다. 단, 제한된 퀀텀 연산 세트(X, CNOT 및 다중 제어 X)가 있는 프로그램에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-122">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="6019d-123">빠른 참조 페이지</span><span class="sxs-lookup"><span data-stu-id="6019d-123">Quick Reference Pages</span></span>

- <span data-ttu-id="6019d-124">[IQ# 매직 명령](xref:microsoft.quantum.guide.quickref.iqsharp): Q# Jupyter Notebook 내 IQ# 매직 명령에 대한 빠른 참조 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="6019d-124">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
