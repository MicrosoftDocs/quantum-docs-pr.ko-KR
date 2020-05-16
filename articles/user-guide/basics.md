---
title: 'Q # 기본 사항'
description: 'Q의 기본 개념 #'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
ms.openlocfilehash: fd0ea47f00b1456ec460808ef7d451c8427677cd
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431158"
---
# <a name="q-basics"></a><span data-ttu-id="f0ff8-103">Q # 기본 사항</span><span class="sxs-lookup"><span data-stu-id="f0ff8-103">Q# Basics</span></span>

<span data-ttu-id="f0ff8-104">이 섹션에서는 Q #의 기본 구성 요소에 대 한 간략 한 소개를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-104">In this section we present a brief introduction to the basic building blocks of Q#.</span></span>

<span data-ttu-id="f0ff8-105">Q #가 무엇 인지와 이러한 항목이 퀀텀 개발 키트의 기본 구성 요소로 적합 한지에 대 한 간략 한 개요는 [q #?를](xref:microsoft.quantum.overview.q-sharp)확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-105">For a quick overview of what Q# is and where it fits in as a fundamental component of the Quantum Development Kit, you can check out [What is Q#?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="f0ff8-106">퀀텀 프로그램 이란?</span><span class="sxs-lookup"><span data-stu-id="f0ff8-106">What is a quantum program?</span></span>

<span data-ttu-id="f0ff8-107">기술적 측면에서 볼 때 퀀텀 프로그램은 특정 한 기존 서브루틴 집합으로 볼 수 있습니다 .이를 호출 하면 퀀텀 시스템에서 특정 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-107">From a technical perspective, a quantum program can be seen as a particular set of classical subroutines which, when called, perform certain operations on a quantum system.</span></span>
<span data-ttu-id="f0ff8-108">이 보기의 중요 한 결과는 Q #으로 작성 된 프로그램이 직접 직접 모델을 모델링 하는 것이 아니라 클래식 제어 컴퓨터가 해당 하는 비트와 상호 작용 하는 방식을 설명 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-108">An important consequence of that view is that a program written in Q# does not directly model qubits themselves, but rather describes how a classical control computer interacts with those qubits.</span></span>
<span data-ttu-id="f0ff8-109">따라서 Q #은 기본적으로 퀀텀 상태 또는 퀀텀 메커니즘의 다른 속성을 직접 정의 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-109">By design, Q# thus does not define quantum states or other properties of quantum mechanics directly.</span></span>
<span data-ttu-id="f0ff8-110">예를 들어 퀀텀 컴퓨팅 개념 가이드에 설명 된 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left {2} $ [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) 상태를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-110">For instance, consider the state $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ discussed in the [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) guide.</span></span>
<span data-ttu-id="f0ff8-111">Q #에서이 상태를 준비 하기 위해 $ \ket $ 상태에서이 상태를 초기화 하는 팩트와 $ {0} \ket{+} = H\ket {0} $를 사용 합니다. 여기서 $H $은 [ `H` operation] (] (f:)에 의해 구현 된 Hadamard 변환입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-111">To prepare this state in Q#, we use the facts that the qubits are initialized in the $\ket{0}$ state, and that $\ket{+} = H\ket{0}$, where $H$ is the Hadamard transform, implemented by the [`H` operation](](xref:microsoft.quantum.intrinsic.h):</span></span>

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0⟩.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0⟩ = |+⟩, as we wanted.
}
```

## <a name="quantum-states-in-q"></a><span data-ttu-id="f0ff8-112">Q의 퀀텀 상태 #</span><span class="sxs-lookup"><span data-stu-id="f0ff8-112">Quantum states in Q#</span></span>

<span data-ttu-id="f0ff8-113">중요 한 점은 위의 프로그램을 작성할 때 Q # 내에서 상태를 명시적으로 참조 하지 않고 프로그램에서 상태를 *변환* 하는 방법을 설명 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-113">Importantly, in writing the above program, we did not explicitly refer to the state within Q#, but rather described how the state was *transformed* by our program.</span></span>
<span data-ttu-id="f0ff8-114">이를 통해 각 대상 컴퓨터 *에도 있는 퀀텀 상태를 완전히* 제어할 수 있으며,이는 컴퓨터에 따라 서로 다르게 해석 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-114">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="f0ff8-115">Q # 프로그램에는 introspect의 상태로 전환 하는 기능이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-115">A Q# program has no ability to introspect into the state of a qubit.</span></span>
<span data-ttu-id="f0ff8-116">대신, 프로그램은 등의 작업을 호출 하 여이를 [`Measure`](xref:microsoft.quantum.intrinsic.measure) 통해 정보를 파악 하 고, 등의 작업을 호출 하 여 해당 [`X`](xref:microsoft.quantum.intrinsic.x) 상태에 대 한 작업을 수행할 수 있습니다 [`H`](xref:microsoft.quantum.intrinsic.h) .</span><span class="sxs-lookup"><span data-stu-id="f0ff8-116">Rather, a program can call operations such as [`Measure`](xref:microsoft.quantum.intrinsic.measure) to learn information from a qubit, and call operations such as [`X`](xref:microsoft.quantum.intrinsic.x) and [`H`](xref:microsoft.quantum.intrinsic.h) to act on the state of a qubit.</span></span>
<span data-ttu-id="f0ff8-117">이러한 작업은 실제로 *수행* 하는 작업은 특정 Q # 프로그램을 실행 하는 데 사용 하는 대상 컴퓨터에만 구체적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-117">What these operations actually *do* is only made concrete by the target machine we use to run the particular Q# program.</span></span>
<span data-ttu-id="f0ff8-118">예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)에서 프로그램을 실행 하는 경우 시뮬레이터는 시뮬레이션 된 퀀텀 시스템에 해당 하는 수학적 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-118">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator will perform the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="f0ff8-119">하지만 향후에는 대상 컴퓨터가 실제 퀀텀 컴퓨터인 경우 Q #에서 이러한 작업을 호출 하면 *실제* 퀀텀 시스템에서 해당 하는 *실제* 작업을 수행 하도록 퀀텀 컴퓨터가 지시 합니다 (예: 정확히 시간이 지정 된 레이저 펄스).</span><span class="sxs-lookup"><span data-stu-id="f0ff8-119">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# will direct the quantum computer to perform the corresponding *real* operations on the *real* quantum system (e.g. precisely timed laser pulses).</span></span>

<span data-ttu-id="f0ff8-120">Q # 프로그램은 대상 컴퓨터에서 정의한 대로 이러한 작업을 다시 결합 하 여 퀀텀 계산을 표현할 수 있는 새로운 수준의 새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-120">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="f0ff8-121">이러한 방식으로 Q #를 사용 하면 대상 컴퓨터 또는 시뮬레이터의 구조와 관련 하 여 일반적으로 사용 되는 논리 퀀텀 및 하이브리드 퀀텀 – 기존 알고리즘을 쉽게 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-121">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

## <a name="q-operations-and-functions"></a><span data-ttu-id="f0ff8-122">Q # 작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="f0ff8-122">Q# operations and functions</span></span>

<span data-ttu-id="f0ff8-123">구체적으로 Q # 프로그램은 *작업*, *함수*및 사용자 정의 형식으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-123">Concretely, a Q# program is comprised of *operations*, *functions*, and any user-defined types.</span></span> 

<span data-ttu-id="f0ff8-124">작업은 퀀텀 시스템의 변환을 설명 하는 데 사용 되며 Q # 프로그램의 가장 기본적인 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-124">Operations are used to describe the transformations of quantum systems and are the most basic building block of Q# programs.</span></span> <span data-ttu-id="f0ff8-125">Q #에 정의 된 각 작업은 원하는 수 만큼 다른 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-125">Each operation defined in Q# may then call any number of other operations.</span></span>

<span data-ttu-id="f0ff8-126">연산과는 달리 함수는 순수 하 게 *결정적인* 클래식 동작을 설명 하는 데 사용 되며, 기존 값을 계산 하는 것 외에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-126">In contrast to operations, functions are used to describe purely *deterministic* classical behavior and do not have any effects besides computing classical values.</span></span> <span data-ttu-id="f0ff8-127">예를 들어, 프로그램의 끝에서 원하는 비트를 측정 하 고 배열에 측정 결과를 추가 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-127">For example, suppose we would like to measure our qubits at the end of a program, and add the measurement results to an array.</span></span>
<span data-ttu-id="f0ff8-128">이 경우 `Measure` 대상 컴퓨터에서 (real 또는 시뮬레이션 된)의 측정을 수행 하도록 지시 하는 *연산이* 며 반환 된 결과를 배열에 추가 하는 기존 프로세스는 *함수*에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-128">In this case `Measure` is an *operation* which instructs the target machine to perform a measurement on the (real or simulated) qubits, and the classical process of adding the returned results to an array will be handled by *functions*.</span></span>

<span data-ttu-id="f0ff8-129">작업 및 함수를 함께 *callables*이라고 하며, [Q # 페이지의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 에 해당 기본 구조 및 동작이 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-129">Together, operations and functions are referred to as *callables*, and their underlying structure and behavior is introduced on the [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) page.</span></span>


## <a name="q-syntax-overview"></a><span data-ttu-id="f0ff8-130">Q # 구문 개요</span><span class="sxs-lookup"><span data-stu-id="f0ff8-130">Q# syntax overview</span></span>

<span data-ttu-id="f0ff8-131">언어의 구문은 구문상 올바른 프로그램을 구성 하는 기호의 여러 조합을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-131">The syntax of a language describes the different combinations of symbols that form a syntactically correct program.</span></span>
<span data-ttu-id="f0ff8-132">Q #에서는 형식, 식 및 문과 같은 세 가지 그룹의 구문 요소를 분류할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-132">In Q# we can classify the elements of its syntax in three different groups: types, expressions and statements.</span></span>

### <a name="types"></a><span data-ttu-id="f0ff8-133">형식</span><span class="sxs-lookup"><span data-stu-id="f0ff8-133">Types</span></span>
<span data-ttu-id="f0ff8-134">Q #은 강력한 형식의 언어 이며, 신중 하 게 형식을 사용 하면 컴파일러가 컴파일 시간에 Q # 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-134">Q# is a strongly-typed language, such that careful use of types can help the compiler provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="f0ff8-135">표준 및 퀀텀 관련 기본 제공 기본 형식 (예:,, `Int` 및) 외에 `Bool` 도 `Qubit` `Result` Q #에서는 사용자 정의 형식에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-135">In addition to standard and quantum-specific built-in primitive types (e.g. `Int`, `Bool`, `Qubit`, and `Result`), Q# provides support for user-defined types.</span></span>
<span data-ttu-id="f0ff8-136">Q #의 다양 한 기본 형식은 q # 페이지의 [형식](xref:microsoft.quantum.guide.types) , 배열 및 튜플 형식에 대 한 세부 정보 및 q # 파일 내에 새 형식을 정의 하는 방법에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-136">All of Q#'s various primitive types are described on the [Types in Q#](xref:microsoft.quantum.guide.types) page, along with details on array and tuple types, as well as how to define new types within a Q# file.</span></span>

### <a name="expressions"></a><span data-ttu-id="f0ff8-137">식</span><span class="sxs-lookup"><span data-stu-id="f0ff8-137">Expressions</span></span>
<span data-ttu-id="f0ff8-138">프로그래밍 언어의 식은 프로그래밍 언어가 해석 하 고 특정 값으로 평가 하는 하나 이상의 상수, 변수, 연산자 및 함수의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-138">An expression in a programming language is a combination of one or more constants, variables, operators, and functions that the programming language interprets and evaluates to a specific value.</span></span>
<span data-ttu-id="f0ff8-139">대부분의 경우 언어의 모든 형식에 대해 해당 형식의 식은 해당 형식의 값에 바인딩된 *리터럴* 또는 기호 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-139">Most simply, for every type in a language, expressions of that type can be either *literals* or symbols bound to a value of that type.</span></span>
<span data-ttu-id="f0ff8-140">예를 들어 `5` 는 `Int` 리터럴 (따라서 형식의 식 `Int` )이 고 기호가 `count` 정수 값에 바인딩되면는 `5` `count` 정수 식 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-140">For example, `5` is an `Int` literal (thus also an expression of type `Int`), and if the symbol `count` is bound to the integer value `5`, then `count` is also an integer expression.</span></span>

<span data-ttu-id="f0ff8-141">또한 식은 특정 연산자와 결합 된 다른 식으로 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-141">Additionally, an expression can consist of other expressions combined with certain operators.</span></span>
<span data-ttu-id="f0ff8-142">따라서로 계산 되는 식의 또 다른 예 `Int` `5` 는입니다 `2+3` .</span><span class="sxs-lookup"><span data-stu-id="f0ff8-142">Hence another example of an `Int` expression which evaluates to `5` is `2+3`.</span></span>

<span data-ttu-id="f0ff8-143">Q #에서 가능한 형식의 가능한 식과 이러한 연산자를 구성 하는 데 사용할 수 있는 호환 연산자는 [q # 페이지의 형식 식](xref:microsoft.quantum.guide.expressions) 에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-143">The possible expressions of types in Q#, as well as the compatible operators that can be used to form them, are detailed on the [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) page.</span></span> 

### <a name="statements"></a><span data-ttu-id="f0ff8-144">문</span><span class="sxs-lookup"><span data-stu-id="f0ff8-144">Statements</span></span> 
<span data-ttu-id="f0ff8-145">문은 수행할 작업을 표현 하는 명령형 프로그래밍 언어의 구문 단위입니다. 문은 결과를 반환 하지 않고 그 파생 작업에 대해서만 실행 되는 반면 식은 항상 결과를 반환 하며 부작용이 전혀 없는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-145">A statement is a syntactic unit of an imperative programming language that expresses some action to be carried out. Statements contrast with expressions in that statements do not return results and are executed solely for their side effects, while expressions always return a result and often do not have side effects at all.</span></span>
<span data-ttu-id="f0ff8-146">이러한 구분은 일반적으로 식이 계산 되는 반면 문이 실행 되는 경우에 자주 관찰 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-146">This distinction is frequently observed in wording: an expression is evaluated, whereas a statement is executed.</span></span>

<span data-ttu-id="f0ff8-147">Q #에 있는 문의 기본 예는 식에 기호를 할당 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-147">A very basic example of a statement in Q# is assigning a symbol to an expression:</span></span>
```qsharp
let count = 5;
```

<span data-ttu-id="f0ff8-148">약간 더 흥미로운 예는 반복을 `for` 지원 하 고 *문 블록*을 포함 하는 문입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-148">A slightly more interesting example is the `for` statement which supports iteration and includes a *statement block*.</span></span>
<span data-ttu-id="f0ff8-149">이 경우에 `qubits` 는 (형식 `Qubit[]` , 즉 형식의 배열)의 레지스터에 바인딩된 기호가 있다고 가정 합니다 `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="f0ff8-149">Suppose `qubits` is the symbol bound to a register of qubits (technically of type `Qubit[]`, i.e. an array of `Qubit` types).</span></span> <span data-ttu-id="f0ff8-150">결과</span><span class="sxs-lookup"><span data-stu-id="f0ff8-150">Then</span></span>
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
<span data-ttu-id="f0ff8-151">는 레지스터에서 각의 각 비트를 반복 하 여 `H` 각각에 대해 작업을 수행 하는 문입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-151">is a statement which iterates over each qubit in the register, performing the `H` operation on each.</span></span> <span data-ttu-id="f0ff8-152">는 `H(qubit);` 자체의 문입니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-152">Note that `H(qubit);` is a statement in itself as well.</span></span>

<span data-ttu-id="f0ff8-153">실제로 형식의 호출 식 `Unit` (정보를 반환 하지 않는 callables)은 문으로 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-153">In fact, any call expression of type `Unit` (those callables that do not return any information) may be used as a statement.</span></span>
<span data-ttu-id="f0ff8-154">이는 `Unit` 문의 목적이 암시적 퀀텀 상태를 수정 하기 때문에를 반환 하는 stbits에 대 한 작업을 호출할 때 주로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-154">This is primarily of use when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="f0ff8-155">식 계산 문에는 종료 세미콜론이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-155">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="f0ff8-156">Q # 프로그램의 거의 모든 측면은 문을 사용 하 여 작성 되므로 단일 페이지에 관련 된 모든 정보가 포함 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-156">Nearly every aspect of a Q# program is built using statements, so no single page could encompass all the information relating to them.</span></span>
<span data-ttu-id="f0ff8-157">그러나 해당 어휘 구조와 서식 지정은 q # [파일 구조](xref:microsoft.quantum.guide.filestructure) 페이지, [q #의 변수](xref:microsoft.quantum.guide.variables)에서 기호 바인딩 할당 및 범위, q `for` #의 [제어 흐름](xref:microsoft.quantum.guide.controlflow)등의 제어 흐름 루프에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-157">However, their lexical structure and formatting is described on the [Q# File Structure](xref:microsoft.quantum.guide.filestructure) page, symbol binding assignment and scope at [Variables in Q#](xref:microsoft.quantum.guide.variables), and control flow loops such as `for` at [Control Flow in Q#](xref:microsoft.quantum.guide.controlflow).</span></span>


## <a name="whats-next"></a><span data-ttu-id="f0ff8-158">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f0ff8-158">What's next?</span></span>
<span data-ttu-id="f0ff8-159">이 가이드의 나머지 부분에서는 Q #을 사용 하 여 작업, 함수 및 형식의 기본 구성 요소를 통해 복잡 한 퀀텀 프로그램을 생성 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-159">Throughout the rest of this guide, we will show you how to use Q# to construct complex quantum programs through the basic building blocks of operations, functions, and types.</span></span>

<span data-ttu-id="f0ff8-160">시작 하려면 [Q #에서 형식](xref:microsoft.quantum.guide.types)에 대 한 학습을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-160">To get started, you can start learning about [Types in Q#](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="f0ff8-161">Q #의 기초 및 동기에 대해 자세히 알아보려면 [q #?가 필요한 이유](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0ff8-161">If you are interested in learning more about the foundations and motivation behind Q#, check out [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>
