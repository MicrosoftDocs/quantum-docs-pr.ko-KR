---
title: Q# 기본 사항
description: 의 기본 개념 Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 86f6538cf383f4e7c14255b38cfb1c141c8f991b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835522"
---
# <a name="no-locq-basics"></a><span data-ttu-id="d4fdd-103">Q# 기본 사항</span><span class="sxs-lookup"><span data-stu-id="d4fdd-103">Q# Basics</span></span>

<span data-ttu-id="d4fdd-104">이 문서에서는의 기본 구성 요소에 대 한 간략 한 소개를 제공 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-104">This article presents a brief introduction to the basic building blocks of Q#.</span></span>

<span data-ttu-id="d4fdd-105">에 대 한 개요 Q# 와 퀀텀 개발 키트의 기본 구성 요소로 사용할 수 있는 위치에 대 한 개요는 [무엇 Q# 인가요?](xref:microsoft.quantum.overview.q-sharp)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-105">For an overview of what Q# is and where it fits in as a fundamental component of the Quantum Development Kit, see [What is Q#?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="d4fdd-106">퀀텀 프로그램 이란?</span><span class="sxs-lookup"><span data-stu-id="d4fdd-106">What is a quantum program?</span></span>

<span data-ttu-id="d4fdd-107">기술적 측면에서 퀀텀 프로그램은 호출 시 퀀텀 시스템에서 특정 작업을 수행 하는 특별 한 특정 서브루틴 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-107">From a technical perspective, a quantum program is a particular set of classical subroutines which, when called, perform certain operations on a quantum system.</span></span>
<span data-ttu-id="d4fdd-108">이 보기의 중요 한 결과는 프로그램에서 Q# 직접 직접 모델링 하지 않고 일반적으로 제어 컴퓨터가 해당 하는 비트와 상호 작용 하는 방식을 설명 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-108">An important consequence of that view is that a Q# program does not directly model qubits themselves, but rather describes how a classically controlled computer interacts with those qubits.</span></span>
<span data-ttu-id="d4fdd-109">의도적으로는 퀀텀 Q# 상태 또는 퀀텀 메커니즘의 다른 속성을 직접 정의 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-109">By design, Q# does not define quantum states or other properties of quantum mechanics directly.</span></span>
<span data-ttu-id="d4fdd-110">예를 들어 퀀텀 컴퓨팅 개념 가이드에 설명 된 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left {2} $ [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) 상태를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-110">For instance, consider the state $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ discussed in the [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) guide.</span></span>
<span data-ttu-id="d4fdd-111">에서이 상태를 준비 하려면 Q# 먼저 $ \ket $ 상태에서이를 초기화 하 {0} 고 $ \ket{+} = H\ket {0} $를 사용 합니다. 여기서 $H $은 [ `H` 작업](xref:microsoft.quantum.intrinsic.h)에 의해 구현 되는 [Hadamard 변환](xref:microsoft.quantum.glossary#hadamard)입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-111">To prepare this state in Q#, start with the facts that the qubits are initialized in the $\ket{0}$ state, and that $\ket{+} = H\ket{0}$, where $H$ is the [Hadamard transform](xref:microsoft.quantum.glossary#hadamard), implemented by the [`H` operation](xref:microsoft.quantum.intrinsic.h).</span></span> <span data-ttu-id="d4fdd-112">을 Q# 초기화 하 고이를 변환 하는 기본 코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-112">The basic Q# code to initialize and transform a qubit, then, looks like this:</span></span>

```qsharp
using (qubit = Qubit()) {
    // At this point, the qubit is in the state |0⟩.
    H(qubit);
    // H is now applied, such that the qubit is in H|0⟩ = |+⟩, as desired.
}
```
<span data-ttu-id="d4fdd-113">을 초기화 하거나 *할당*하는 방법에 대 한 자세한 내용은 [작업](xref:microsoft.quantum.guide.qubits)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-113">For more information on initializing, or *allocating*, qubits, see [Working with qubits](xref:microsoft.quantum.guide.qubits).</span></span>

## <a name="quantum-states-in-no-locq"></a><span data-ttu-id="d4fdd-114">퀀텀 상태 Q#</span><span class="sxs-lookup"><span data-stu-id="d4fdd-114">Quantum states in Q#</span></span>

<span data-ttu-id="d4fdd-115">중요 한 점은 이전 프로그램은 내에서 상태를 명시적으로 참조 하지 Q# 않지만 프로그램이 상태를 *변환* 하는 방법을 설명 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-115">Importantly, the previous program does not explicitly refer to the state within Q# but described how our program *transformed* the state.</span></span>
<span data-ttu-id="d4fdd-116">이 접근 방식을 사용 하면 각 대상 컴퓨터 *에도 있는 퀀텀 상태를 완전히* 제어할 수 없으며, 컴퓨터에 따라 서로 다른 해석이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-116">With this approach, you can be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="d4fdd-117">Q#프로그램은 introspect의 상태로 전환 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-117">A Q# program cannot introspect into the state of a qubit.</span></span>
<span data-ttu-id="d4fdd-118">대신, 프로그램은 등의 작업을 호출 하 여이를 [`Measure`](xref:microsoft.quantum.intrinsic.measure) 통해 정보를 파악 하 고, 등의 작업을 호출 하 여 해당 [`X`](xref:microsoft.quantum.intrinsic.x) 상태에 대 한 작업을 수행할 수 있습니다 [`H`](xref:microsoft.quantum.intrinsic.h) .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-118">Instead, a program can call operations such as [`Measure`](xref:microsoft.quantum.intrinsic.measure) to learn information from a qubit, and call operations such as [`X`](xref:microsoft.quantum.intrinsic.x) and [`H`](xref:microsoft.quantum.intrinsic.h) to act on the state of a qubit.</span></span>
<span data-ttu-id="d4fdd-119">이러한 작업은 실제로 *수행* 하는 작업은 특정 프로그램을 실행 하는 데 사용 되는 대상 컴퓨터에 의해서만 구체적으로 적용 됩니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-119">What these operations actually *do* is only made concrete by the target machine used to run the particular Q# program.</span></span>
<span data-ttu-id="d4fdd-120">예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)에서 프로그램을 실행 하는 경우 시뮬레이터는 시뮬레이션 된 퀀텀 시스템에 해당 하는 수치 연산을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-120">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="d4fdd-121">하지만 나중에 대상 컴퓨터가 실제 퀀텀 컴퓨터인 경우에서 이러한 작업을 호출 하면 Q# *실제* 퀀텀 시스템에서 해당 하는 *실제* 작업을 수행 하도록 퀀텀 컴퓨터가 지시 합니다 (예: 정확히 시간이 지정 된 레이저 펄스).</span><span class="sxs-lookup"><span data-stu-id="d4fdd-121">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# directs the quantum computer to perform the corresponding *real* operations on the *real* quantum system, for example, precisely timed laser pulses).</span></span>

<span data-ttu-id="d4fdd-122">Q#프로그램은 대상 컴퓨터에서 정의한 대로 이러한 작업을 다시 결합 하 여 퀀텀 계산을 표현할 수 있는 새로운 수준의 새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-122">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="d4fdd-123">이러한 방식으로를 사용 하면 Q# 대상 컴퓨터 또는 시뮬레이터의 구조와 관련 하 여 일반적으로 사용 되는 논리 퀀텀 및 하이브리드 퀀텀 – 기존 알고리즘을 쉽게 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-123">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

## <a name="no-locq-operations-and-functions"></a><span data-ttu-id="d4fdd-124">Q# 작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="d4fdd-124">Q# operations and functions</span></span>

<span data-ttu-id="d4fdd-125">구체적으로 프로그램은 Q# *작업*, *함수*및 사용자 정의 형식으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-125">Concretely, a Q# program comprises *operations*, *functions*, and any user-defined types.</span></span> 

<span data-ttu-id="d4fdd-126">작업은 퀀텀 시스템의 변환을 설명 하는 데 사용 되며 가장 기본적인 프로그램 구성 요소입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-126">Operations are used to describe the transformations of quantum systems and are the most fundamental building block of Q# programs.</span></span> <span data-ttu-id="d4fdd-127">에서 정의 된 각 작업 Q# 은 다른 작업을 원하는 수 만큼 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-127">Each operation defined in Q# may then call any number of other operations.</span></span>

<span data-ttu-id="d4fdd-128">연산과는 달리 함수는 순수 하 게 *결정적인* 클래식 동작을 설명 하는 데 사용 되며, 기존 값을 계산 하는 것 외에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-128">In contrast to operations, functions are used to describe purely *deterministic* classical behavior and do not have any effects besides computing classical values.</span></span> <span data-ttu-id="d4fdd-129">예를 들어 프로그램의 끝에서 원하는 비트를 측정 하 고 배열에 측정 결과를 추가 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-129">For example, suppose you want to measure the qubits at the end of a program and add the measurement results to an array.</span></span>
<span data-ttu-id="d4fdd-130">이 경우 `Measure` 는 대상 컴퓨터에서 (실제 또는 시뮬레이트된)의 측정을 수행 하도록 지시 하는 *작업* 입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-130">In this case, `Measure` is an *operation* that instructs the target machine to perform a measurement on the (real or simulated) qubits.</span></span> <span data-ttu-id="d4fdd-131">동시에 *함수* 는 반환 된 결과를 배열에 추가 하는 기존 프로세스를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-131">At the same time, *functions* handle the classical process of adding the returned results to an array.</span></span>

<span data-ttu-id="d4fdd-132">작업 및 함수를 함께 *callables*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-132">Together, operations and functions are known as *callables*.</span></span> <span data-ttu-id="d4fdd-133">의 기본 구조와 동작은 [의 Q# 작업 및 함수 ](xref:microsoft.quantum.guide.operationsfunctions)에서 도입 되 고 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-133">Their underlying structure and behavior are introduced and detailed in [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>


## <a name="no-locq-syntax-overview"></a><span data-ttu-id="d4fdd-134">Q# 구문 개요</span><span class="sxs-lookup"><span data-stu-id="d4fdd-134">Q# syntax overview</span></span>

<span data-ttu-id="d4fdd-135">언어의 구문은 구문상 올바른 프로그램을 구성 하는 기호의 여러 조합을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-135">The syntax of a language describes the different combinations of symbols that form a syntactically correct program.</span></span>
<span data-ttu-id="d4fdd-136">에서 Q# 구문 요소는 형식, 식 및 문과 같은 세 가지 그룹으로 분류 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-136">In Q#, syntax elements are classified into three different groups: types, expressions, and statements.</span></span>

### <a name="types"></a><span data-ttu-id="d4fdd-137">형식</span><span class="sxs-lookup"><span data-stu-id="d4fdd-137">Types</span></span>
<span data-ttu-id="d4fdd-138">Q# 는 강력한 형식의 언어 이며, 신중 하 게 형식을 사용 하면 컴파일러가 Q# 컴파일 시간에 프로그램에 대 한 강력한 보증을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-138">Q# is a strongly-typed language, such that careful use of types can help the compiler provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="d4fdd-139">표준 및 퀀텀 관련 기본 제공 기본 형식 (예:,, 및) 외에 `Int` 도 `Bool` `Qubit` `Result` Q# 사용자 정의 형식에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-139">In addition to standard and quantum-specific built-in primitive types, for example, `Int`, `Bool`, `Qubit`, and `Result`, Q# provides support for user-defined types.</span></span>

<span data-ttu-id="d4fdd-140">모든 기본 형식, 배열 및 튜플 형식에 대 한 자세한 내용 및 파일 내에 새 형식을 정의 하는 단계에 대 한 설명은 Q# [의 Q# 형식 ](xref:microsoft.quantum.guide.types)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-140">For descriptions of all the primitive types, details for array and tuple types, and steps to define new types within a Q# file, see [Types in Q#](xref:microsoft.quantum.guide.types).</span></span>

### <a name="expressions"></a><span data-ttu-id="d4fdd-141">표현식</span><span class="sxs-lookup"><span data-stu-id="d4fdd-141">Expressions</span></span>
<span data-ttu-id="d4fdd-142">프로그래밍 언어의 식은 프로그래밍 언어가 해석 하 고 특정 값으로 평가 하는 하나 이상의 상수, 변수, 연산자 및 함수의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-142">An expression in a programming language is a combination of one or more constants, variables, operators, and functions that the programming language interprets and evaluates to a specific value.</span></span>
<span data-ttu-id="d4fdd-143">대부분의 경우 언어의 모든 형식에 대해 해당 형식의 식은 해당 형식의 값에 바인딩된 *리터럴* 또는 기호 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-143">Most simply, for every type in a language, expressions of that type can be either *literals* or symbols bound to a value of that type.</span></span>
<span data-ttu-id="d4fdd-144">예를 들어 `5` 는 `Int` 리터럴 (따라서 형식의 식 `Int` )이 고 기호가 `count` 정수 값에 바인딩되면는 `5` `count` 정수 식 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-144">For example, `5` is an `Int` literal (thus also an expression of type `Int`), and if the symbol `count` is bound to the integer value `5`, then `count` is also an integer expression.</span></span>

<span data-ttu-id="d4fdd-145">또한 식은 특정 연산자에 의해 결합 된 다른 식으로 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-145">Additionally, an expression can consist of other expressions combined by certain operators.</span></span>
<span data-ttu-id="d4fdd-146">예를 들어 `Int` 로 계산 되는 다른 식은입니다 `5` `2+3` .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-146">For example, another `Int` expression that evaluates to `5` is `2+3`.</span></span>

<span data-ttu-id="d4fdd-147">의 식 및 호환 연산자에 대 한 자세한 내용은 Q# [의 Q# 형식 식 ](xref:microsoft.quantum.guide.expressions)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-147">For more information about expressions and compatible operators in Q#, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span> 

### <a name="statements"></a><span data-ttu-id="d4fdd-148">문</span><span class="sxs-lookup"><span data-stu-id="d4fdd-148">Statements</span></span> 
<span data-ttu-id="d4fdd-149">문은 수행할 작업을 표현 하는 명령형 프로그래밍 언어의 구문 단위입니다. 문에 있는 식과의 대조는 결과를 반환 하지 않으며 의도 하지 않은 결과에 대해서만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-149">A statement is a syntactic unit of an imperative programming language that expresses some action to carry out. Statements contrast with expressions in that statements do not return results and are run solely for their side effects.</span></span> <span data-ttu-id="d4fdd-150">그러나 식은 항상 결과를 반환 하며 부작용이 없는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-150">Expressions, however, always return a result and often do not have any side effects.</span></span> <span data-ttu-id="d4fdd-151">즉, Q# 식이 계산 되는 동안 문이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-151">In short, Q# statements are run, while expressions are evaluated.</span></span>

<span data-ttu-id="d4fdd-152">에서 문의 간단한 예는 Q# 식에 기호를 할당 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-152">A simple example of a statement in Q# is assigning a symbol to an expression:</span></span>
```qsharp
let count = 5;
```

<span data-ttu-id="d4fdd-153">더 흥미로운 예는 반복을 `for` 지원 하 고 *문 블록*을 포함 하는 문입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-153">A more interesting example is the `for` statement which supports iteration and includes a *statement block*.</span></span>
<span data-ttu-id="d4fdd-154">`qubits`는 (기술적으로는 형식 또는 형식의 배열인)의 레지스터에 바인딩된 기호가 있다고 가정 `Qubit[]` `Qubit` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-154">Suppose `qubits` is the symbol bound to a register of qubits (technically of type `Qubit[]`, or an array of `Qubit` types).</span></span> <span data-ttu-id="d4fdd-155">결과</span><span class="sxs-lookup"><span data-stu-id="d4fdd-155">Then</span></span>
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
<span data-ttu-id="d4fdd-156">는 레지스터의 각 비트를 반복 하 여 `H` 각각에 대해 작업을 수행 하는 문입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-156">is a statement that iterates over each qubit in the register, performing the `H` operation on each one.</span></span> <span data-ttu-id="d4fdd-157">는 `H(qubit);` 자체의 문입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-157">Note that `H(qubit);` is a statement in itself as well.</span></span>

<span data-ttu-id="d4fdd-158">형식 `Unit` (정보를 반환 하지 않는 형식)의 호출 식을 문으로 사용할 수 있습니다 `Unit` .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-158">You can use any call expression of type `Unit` (a `Unit` type does not return any information) as a statement.</span></span>
<span data-ttu-id="d4fdd-159">이 식 형식은 `Unit` 문의 목적이 암시적 퀀텀 상태를 수정 하기 때문에를 반환 하는 작업을 호출 하는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-159">This type of expression is useful when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="d4fdd-160">식 계산 문에는 종료 세미콜론이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-160">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="d4fdd-161">문을 사용 하 여 프로그램의 거의 모든 측면을 빌드할 수 Q# 있으며, 모든 정보를 포함 하는 모든 정보는 단일 페이지에 포함 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-161">You use statements to build nearly every aspect of a Q# program, and no single page could encompass all the information relating to them.</span></span>
<span data-ttu-id="d4fdd-162">해당 어휘 구조 및 서식에 대 한 자세한 내용은 [ Q# 파일 구조](xref:microsoft.quantum.guide.filestructure), 기호 바인딩 할당 및 범위에 대 한 자세한 내용은 [의 Q# 변수 ](xref:microsoft.quantum.guide.variables)를 참조 하 고,와 같은 제어 흐름 루프의 `for` 경우 [ Q# 제어 흐름 ](xref:microsoft.quantum.guide.controlflow)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-162">For more information about their lexical structure and formatting, see [Q# File Structure](xref:microsoft.quantum.guide.filestructure); for symbol binding assignment and scope, see [Variables in Q#](xref:microsoft.quantum.guide.variables); and for control flow loops such as `for`, see [Control Flow in Q#](xref:microsoft.quantum.guide.controlflow).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d4fdd-163">다음 단계</span><span class="sxs-lookup"><span data-stu-id="d4fdd-163">Next steps</span></span>

<span data-ttu-id="d4fdd-164">[의 형식 Q# ](xref:microsoft.quantum.guide.types)에 대 한 학습을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-164">Start learning about [Types in Q#](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="d4fdd-165">기반이 되는 것과 그에 대 한 자세한 배경 정보는 Q# [왜 필요 Q# 합니까?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-165">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>
