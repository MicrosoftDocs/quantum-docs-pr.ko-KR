---
title: 의 작업 및 함수Q#
description: 작업 및 함수를 정의 하 고 호출 하는 방법 뿐만 아니라 제어 된 및 adjoint 작업 특수화입니다.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: 76437c83df894fa86409e680f961d97e267c6869
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867882"
---
# <a name="operations-and-functions-in-no-locq"></a><span data-ttu-id="910ef-103">의 작업 및 함수Q#</span><span class="sxs-lookup"><span data-stu-id="910ef-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="910ef-104">새 작업 정의</span><span class="sxs-lookup"><span data-stu-id="910ef-104">Defining New Operations</span></span>

<span data-ttu-id="910ef-105">작업은의 핵심입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="910ef-106">선언 되 면 기존 .NET 응용 프로그램에서 호출할 수 있습니다. 예를 들어 시뮬레이터를 사용 하거나 내에서 다른 작업을 수행할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-106">Once declared, they can either be called from classical .NET applications, for example, using a simulator or by other operations within Q#.</span></span>
<span data-ttu-id="910ef-107">에 정의 된 각 작업은 Q# 언어로 정의 된 기본 제공 기본 작업을 포함 하 여 원하는 수의 다른 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-107">Each operation defined in Q# can call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="910ef-108">이러한 내장 작업을 정의 하는 특정 방법은 Q# 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-108">The particular way in which Q# defines these intrinsic operations depends on the target machine.</span></span>
<span data-ttu-id="910ef-109">컴파일되는 경우 각 작업은 대상 컴퓨터에 제공할 수 있는 .NET 클래스 형식으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="910ef-110">각 Q# 소스 파일은 원하는 수의 작업을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-110">Each Q# source file can define any number of operations.</span></span>
<span data-ttu-id="910ef-111">작업 이름은 네임 스페이스 내에서 고유 해야 하며 형식 또는 함수 이름과 충돌 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-111">Operation names must be unique within a namespace and can not conflict with type or function names.</span></span>

<span data-ttu-id="910ef-112">작업 선언은 키워드, 작업의 `operation` 인수를 정의 하는 형식화 된 식별자 튜플, 작업에 대 한 인수를 정의 하는 형식화 된 식별자 튜플, 작업의 결과 형식에 대 한 인수를 정의 하는 형식화 된 식별자 튜플, `:` 선택적으로 작업 특성을 포함 하는 주석, 여는 중괄호, 작업 선언의 본문 (중괄호로 묶)으로 구성 됩니다 `{ }` .</span><span class="sxs-lookup"><span data-stu-id="910ef-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace, and then the body of the operation declaration, enclosed in braces `{ }`.</span></span>

<span data-ttu-id="910ef-113">각 작업은 입력을 가져오고, 출력을 생성 하 고, 하나 이상의 작업 특수화에 대해 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="910ef-114">가능한 특수화와이를 정의 하 고 호출 하는 방법은이 문서의 다른 섹션에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-114">The possible specializations, and how to define and call them, are detailed in the different sections of this article.</span></span>
<span data-ttu-id="910ef-115">지금은 기본 본문 특수화만 정의 하 고 단일 비트를 입력으로 사용 하 고 <xref:microsoft.quantum.intrinsic.x> 해당 입력에 대 한 기본 제공 작업을 호출 하는 다음 작업을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="910ef-116">키워드는 `operation` 작업 정의를 시작 하 고 그 뒤에 이름을 입력 `BitFlip` 합니다. 여기서는입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-116">The keyword `operation` begins the operation definition, followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="910ef-117">그런 다음 입력의 형식이 `Qubit` `target` 새 작업 내의 입력을 참조 하는 이름과 함께 정의 됩니다 ().</span><span class="sxs-lookup"><span data-stu-id="910ef-117">Next, the type of input is defined (`Qubit`), along with a name, `target`, for referring to the input within the new operation.</span></span>
<span data-ttu-id="910ef-118">마지막으로,는 `Unit` 작업의 출력이 비어 있음을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-118">Lastly, `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="910ef-119">`Unit`는 `void` c # 및 기타 명령형 언어에서와 유사 하 게 사용 되며 `unit` F # 및 다른 기능 언어에서와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-119">`Unit` is used similarly to `void` in C# and other imperative languages and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="910ef-120">작업은 보다 더 흥미로운 형식을 반환할 수도 있습니다 `Unit` .</span><span class="sxs-lookup"><span data-stu-id="910ef-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="910ef-121">예를 들어 <xref:microsoft.quantum.intrinsic.m> 작업은 측정을 수행 하는 `Result` 것을 나타내는 형식의 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span>  <span data-ttu-id="910ef-122">작업에서 다른 작업으로 전달 하거나 키워드와 함께 사용 하 여 `let` 새 변수를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-122">You can pass it from an operation to another operation or use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="910ef-123">이 접근 방식을 사용 하면 [슈퍼 조밀한 코딩](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)의 경우와 같이 낮은 수준에서 퀀텀 작업과 상호 작용 하는 기존 계산을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-123">This approach allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> <span data-ttu-id="910ef-124">의 각 작업 Q# 은 정확히 하나의 입력을 받아 정확히 하나의 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="910ef-125">여러 값을 단일 값으로 수집 하는 *튜플을*사용 하 여 여러 입력 및 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-125">Multiple inputs and outputs are represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="910ef-126">이와 관련 하 Q# 여은 "튜플 인 튜플" 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-126">In this regard, Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="910ef-127">이 개념에 따라 빈 괄호 집합은 `()` 형식을 가진 "empty" 튜플로 읽어야 합니다 `Unit` .</span><span class="sxs-lookup"><span data-stu-id="910ef-127">Following this concept, a set of empty parentheses, `()`, should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="910ef-128">제어 된 및 Adjoint 작업</span><span class="sxs-lookup"><span data-stu-id="910ef-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="910ef-129">에서 많은 작업을 수행 하는 경우 처럼 작업에서 단일 변환을 구현 하는 경우 Q# *adjointed* 또는 *제어*될 때 작업의 작동 방식을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="910ef-130">작업의 *adjoint* 특수화는 작업의 "역"이 작동 하는 방식을 지정 하는 반면, *제어* 되는 특수화는 응용 프로그램이 특정 퀀텀 레지스터의 상태에서 조건 화 된 때 작업이 작동 하는 방식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="910ef-131">퀀텀 작업의 adjoints는 퀀텀 컴퓨팅의 많은 측면에서 매우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="910ef-132">유용한 프로그래밍 기법을 함께 설명 하는 이러한 상황에 대 한 예는 Q# 이 문서의 [변화](#conjugations) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="910ef-132">For an example of one such situation discussed alongside a useful Q# programming technique, see [Conjugations](#conjugations) in this article.</span></span> 

<span data-ttu-id="910ef-133">제어 되는 작업 버전은 모든 컨트롤이 지정 된 상태에 있는 경우에만 기본 작업을 효과적으로 적용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="910ef-134">컨트롤의 superposition에 있는 경우 기본 작업은 superposition의 해당 부분에 coherently 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="910ef-135">따라서 제어 된 작업은 종종 되거나 얽 히을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="910ef-136">물론, *제어 된 adjoint* 특수화도 존재할 수 있으며, 작업의 adjoint의 제어 된 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="910ef-137">$U $가 연산에 의해 구현 되는 단일 변환 인 경우는 `U` `Adjoint U` 복소수 (복소수)가 복소수 인 단일 변환을 $U 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="910ef-138">작업을 연속적으로 적용 한 다음, 해당 adjoint를 상태에 적용 하면 ^ \a턴 = U ^ \A턴 U = \dagger $, id 매트릭스를 $UU 하는 것 처럼 상태가 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="910ef-139">제어 된 작업에 대 한 단일 표현은 약간 더 미묘한 [퀀텀 컴퓨팅 개념: 여러 가지](xref:microsoft.quantum.concepts.multiple-qubits)추가 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="910ef-140">다음 섹션에서는 코드에서 이러한 다양 한 특수화를 호출 하는 방법과 이러한 특수화를 지 원하는 작업을 정의 하는 방법을 설명 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-140">The following section describes how to call these various specializations in your Q# code, and how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="910ef-141">작업 특수화 호출</span><span class="sxs-lookup"><span data-stu-id="910ef-141">Calling operation specializations</span></span>

<span data-ttu-id="910ef-142">의 *함수* 는 Q# 다른 작업에서 새 작업을 정의 하는 팩터리입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-142">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="910ef-143">의 두 표준 함수 Q# 는 `Adjoint` 및 `Controlled` 입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-143">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="910ef-144">함수는 새 작업의 구현을 정의할 때 기본 작업의 구현에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-144">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="910ef-145">따라서 함수는 기존의 상위 수준 함수 보다 더 복잡 한 함수를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-145">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="910ef-146">함수에 형식 시스템에 대 한 표현이 없습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-146">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="910ef-147">따라서 현재 변수를 변수에 바인딩하거나 인수로 전달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-147">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="910ef-148">새 작업을 반환 하는 작업에 적용 하 여 함수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-148">Use a functor by applying it to an operation, which returns a new operation.</span></span>
<span data-ttu-id="910ef-149">예를 들어 `Adjoint` 작업에 함수를 적용 하면 `Y` 새 작업이 반환 `Adjoint Y` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-149">For example, applying the `Adjoint` functor to the `Y` operation returns the new operation `Adjoint Y`.</span></span> <span data-ttu-id="910ef-150">다른 작업과 마찬가지로 새 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-150">You can invoke the new operation like any other operation.</span></span>
<span data-ttu-id="910ef-151">또는 함수의 응용 프로그램을 지 원하는 작업의 경우 `Adjoint` `Controlled` 반환 형식은 여야 `Unit` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-151">For an operation to support the application of the `Adjoint` or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="910ef-152">`Adjoint`함수</span><span class="sxs-lookup"><span data-stu-id="910ef-152">`Adjoint` functor</span></span>

<span data-ttu-id="910ef-153">따라서에서는 `Adjoint Y(q1)` 작업에 함수를 적용 하 여 `Adjoint` `Y` 새 작업을 생성 하 고 새 작업을에 적용 `q1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-153">Thus, `Adjoint Y(q1)` applies the `Adjoint` functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="910ef-154">새 작업의 시그니처와 형식이 기본 작업과 동일 합니다 `Y` .</span><span class="sxs-lookup"><span data-stu-id="910ef-154">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="910ef-155">특히, 새 작업은를 지원 하 `Adjoint` 고, `Controlled` 기본 작업이 수행한 경우에만를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-155">In particular, the new operation also supports `Adjoint`, and supports `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="910ef-156">`Adjoint`함수는 자체적으로 반전 됩니다. 즉, `Adjoint Adjoint Op` 는 항상와 동일 합니다 `Op` .</span><span class="sxs-lookup"><span data-stu-id="910ef-156">The `Adjoint` functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="910ef-157">`Controlled`함수</span><span class="sxs-lookup"><span data-stu-id="910ef-157">`Controlled` functor</span></span>

<span data-ttu-id="910ef-158">마찬가지로에서는 `Controlled X(controls, target)` 작업에 함수를 적용 하 여 `Controlled` `X` 새 작업을 생성 하 고 해당 새 작업을 및에 적용 합니다 `controls` `target` .</span><span class="sxs-lookup"><span data-stu-id="910ef-158">Similarly, `Controlled X(controls, target)` applies the `Controlled` functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="910ef-159">에서 Q# 제어 되는 버전은 항상 컨트롤의 배열을 사용 하며, 제어는 항상 계산 ( `PauliZ` ) `One` 상태 ($ \ket $)에 있는 모든 컨트롤을 기반으로 합니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="910ef-159">In Q#, controlled versions always take an array of control qubits, and the controlling is always based on all of the control qubits being in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="910ef-160">제어 된 작업 이전에 적절 한 단일 작업을 제어 된 작업 이전에 적용 한 다음 제어 된 작업 후에 단일 작업의 반대을 적용 하 여 다른 상태를 기반으로 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-160">Controlling based on other states is achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="910ef-161">예를 들면 제어 된 `X` 작업 전후에 컨트롤에 작업을 적용 하면 작업에서 `Zero` 해당 기능에 대해 상태 ($ \ket $)를 제어 하 {0} 고, 상태에서 컨트롤 전후에 작업을 적용 합니다. `H` `PauliX` `One` 즉,-1 Eigenvalue는 pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt $ (상태 아님)입니다 {2} `PauliZ` `One` .</span><span class="sxs-lookup"><span data-stu-id="910ef-161">For example, applying an `X` operation to a control qubit before and after a controlled operation causes the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after controls on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="910ef-162">작업 식이 지정 된 경우 함수를 사용 하 여 새 작업 식을 만들 수 있습니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-162">Given an operation expression, you can form a new operation expression by using the `Controlled` functor.</span></span>
<span data-ttu-id="910ef-163">새 작업의 서명은 원래 작업의 서명을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-163">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="910ef-164">결과 형식은 동일 하지만 입력 형식은 두 번째 요소로 서, 컨트롤의 요소를 첫 번째 요소로 사용 하 고 원래 작업의 인수를 두 번째 요소로 보유 하 고 있는 두 번째 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-164">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="910ef-165">새 작업은 `Controlled` 를 지원 하 고, `Adjoint` 원래 작업이 수행한 경우에만를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-165">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="910ef-166">원래 작업에 단일 인수만 사용한 경우 단일 [튜플 동등성](xref:microsoft.quantum.guide.types) 은 여기에서 재생 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-166">If the original operation took only a single argument, then [singleton tuple equivalence](xref:microsoft.quantum.guide.types) comes into play here.</span></span>
<span data-ttu-id="910ef-167">예를 들어 `Controlled X` 는 작업의 제어 된 버전입니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="910ef-167">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="910ef-168">`X`에는 형식이 `(Qubit => Unit is Adj + Ctl)` 있으므로 `Controlled X` 형식이 있습니다 `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` . 단일 튜플 동치로 인해와 동일 합니다 `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="910ef-168">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="910ef-169">기본 작업에서 여러 인수를 사용한 경우에는 작업의 제어 되는 버전에 대 한 해당 인수를 괄호로 묶어 튜플로 변환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-169">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="910ef-170">예를 들어 `Controlled Rz` 는 작업의 제어 된 버전입니다 `Rz` .</span><span class="sxs-lookup"><span data-stu-id="910ef-170">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="910ef-171">`Rz`형식에는 `((Double, Qubit) => Unit is Adj + Ctl)` `Controlled Rz` 형식이 `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-171">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="910ef-172">따라서는 `Controlled Rz(controls, (0.1, target))` 의 유효한 호출입니다 `Controlled Rz` (괄호로 묶인 괄호 `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="910ef-172">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="910ef-173">또 다른 예로는를 `CNOT(control, target)` 로 구현할 수 있습니다 `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="910ef-173">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="910ef-174">대상이 CCNOT (두 제어 비트)로 제어 되어야 하는 경우 `Controlled X([control1, control2], target)` 문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-174">If a target should be controlled by two control qubits (CCNOT), use a `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="910ef-175">`Controlled`및 `Adjoint` 함수 commute을 적용 하는 경우에는 또는를 적용 하는 것에 차이가 없습니다 `Controlled Adjoint Op` `Adjoint Controlled Op` .</span><span class="sxs-lookup"><span data-stu-id="910ef-175">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="910ef-176">제어 된 및 Adjoint 구현 정의</span><span class="sxs-lookup"><span data-stu-id="910ef-176">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="910ef-177">앞의 예제에서 첫 번째 작업 선언에서 작업 및는 `BitFlip` `DecodeSuperdense` 각각 시그니처와로 정의 되었습니다 `(Qubit => Unit)` `((Qubit, Qubit) => (Result, Result))` .</span><span class="sxs-lookup"><span data-stu-id="910ef-177">In the first operation declaration in the previous examples, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="910ef-178">`DecodeSuperdense`에는 측정값이 포함 되어 있으므로 단일 연산이 아니므로 adjoint 특수화를 제어 하지 않습니다 (해당 작업이 반환 하는 관련 요구 사항 회수 `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="910ef-178">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="910ef-179">그러나는 `BitFlip` 단순히 단일 <xref:microsoft.quantum.intrinsic.x> 작업을 수행 하므로 두 가지 특수화를 모두 사용 하 여 정의 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-179">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, you could have defined it with both specializations.</span></span>

<span data-ttu-id="910ef-180">이 섹션에서는 작업 선언에 특수화의 존재를 포함 하 여 Q# 또는 함수와 함께 호출할 수 있는 기능을 제공 하는 방법에 대해 자세히 설명 합니다 `Adjoint` `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-180">This section details how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` or `Controlled` functors.</span></span>
<span data-ttu-id="910ef-181">특정 특수화를 선언 하는 데 유효 하거나 유효 하지 않은 상황에 대 한 자세한 내용은이 문서에서 특수화를 올바르게 정의 하는 [상황](#circumstances-for-validly-defining-specializations) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="910ef-181">For more information about some of the situations in which it is either valid or not valid to declare certain specializations, see [Circumstances for validly defining specializations](#circumstances-for-validly-defining-specializations) in this article.</span></span>

<span data-ttu-id="910ef-182">작업 특성은 선언 된 작업에 적용할 수 있는 함수의 종류와 표시 되는 결과를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-182">Operation characteristics define what kinds of functors you can apply to the declared operation, and what effect they have.</span></span> <span data-ttu-id="910ef-183">이러한 특수화의 존재는 작업 시그니처의 일부로 선언 될 수 있으며, 특히 작업 특성이 포함 된 주석 (, 또는)을 통해 선언할 수 있습니다 `is Adj` `is Ctl` `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="910ef-183">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="910ef-184">각 특수화의 실제 구현은 *암시적* 또는 *명시적으로* 정의 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-184">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="910ef-185">암시적으로 구현 지정</span><span class="sxs-lookup"><span data-stu-id="910ef-185">Implicitly specifying implementations</span></span>

<span data-ttu-id="910ef-186">이 경우 작업 선언의 본문은 기본 구현 으로만 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-186">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="910ef-187">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="910ef-187">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="910ef-188">여기에서 암시적으로 선언 된 각 특수화에 해당 하는 구현은 `Adjoint` 또는 함수 사용 될 경우 컴파일러에 의해 자동으로 생성 됩니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-188">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="910ef-189">따라서를 호출 하면의 `Adjoint PrepareEntangledPair` adjoint와 adjoint의를 구현 하는 컴파일러가 생성 됩니다 `CNOT` `H` .</span><span class="sxs-lookup"><span data-stu-id="910ef-189">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="910ef-190">이러한 개별 작업은 둘 다 자체 작업 이므로 결과 `Adjoint PrepareEntangledPair` 작업은 단순히 적용 되 고 그 다음으로 구성 됩니다 `CNOT(here, there)` `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="910ef-190">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="910ef-191">따라서이를 사용 하면 `DecodeSuperdense` adjoint의를 사용 하 여 `PrepareEntangledPair` entangled 상태를 조밀로 다시 변환 하는 방법으로 앞의 예제에서를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-191">Hence you can use this to write the `DecodeSuperdense` in the previous example more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="910ef-192">선언에서 작업 특성이 포함 된 주석은 컴파일러가 기본 구현을 기반으로 하 여 다른 특수화를 자동으로 생성 하는지 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-192">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="910ef-193">함수와 함께 사용 하기 위한 작업을 디자인할 때 고려해 야 할 몇 가지 중요 한 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-193">There are several important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="910ef-194">다른 작업의 출력 값을 사용 하는 작업에 대 한 특수화는 컴파일러에서 자동으로 생성할 수 *없습니다* . 이러한 작업에서 문을 다시 정렬 하 여 동일한 효과를 얻는 방법은 모호 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-194">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="910ef-195">따라서 다양 한 구현을 명시적으로 지정 하는 것이 유용한 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-195">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="910ef-196">명시적으로 구현 지정</span><span class="sxs-lookup"><span data-stu-id="910ef-196">Explicitly specifying implementations</span></span>

<span data-ttu-id="910ef-197">컴파일러가 구현을 생성할 수 없는 경우 명시적으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-197">In the case where the compiler cannot generate the implementation, you can specify it explicitly.</span></span> <span data-ttu-id="910ef-198">이러한 명시적 특수화 선언은 적절 한 *세대 지시문* 또는 사용자 정의 구현으로 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-198">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="910ef-199">다음은 명시적 특수화의 몇 가지 예를 포함 한 모든 범위의 전체 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-199">Following are the full range of possibilities, with some examples of explicit specialization.</span></span> 


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="910ef-200">명시적 특수화 선언</span><span class="sxs-lookup"><span data-stu-id="910ef-200">Explicit specialization declarations</span></span>

<span data-ttu-id="910ef-201">Q#작업에는 다음과 같은 명시적 특수화 선언이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-201">Q# operations can contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="910ef-202">`body`특수화는 함수 적용 되지 않은 작업의 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-202">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="910ef-203">`adjoint`특수화는 적용 된 함수를 사용 하 여 작업의 구현을 지정 합니다 `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="910ef-203">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="910ef-204">`controlled`특수화는 적용 된 함수를 사용 하 여 작업의 구현을 지정 합니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-204">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="910ef-205">`controlled adjoint`특수화는 `Adjoint` 및 함수 적용 된 작업의 구현을 지정 합니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-205">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="910ef-206">두 함수 commute 이므로이 특수화의 이름을 지정할 수도 있습니다 `adjoint controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-206">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="910ef-207">작업 특수화는 특수화 태그 (예 `body` `adjoint` : 또는)와 다음 중 하나가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-207">An operation specialization consists of the specialization tag (for example, `body` or `adjoint`) followed by one of:</span></span>

- <span data-ttu-id="910ef-208">다음에 설명 된 명시적 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-208">An explicit declaration as described in the following.</span></span>
- <span data-ttu-id="910ef-209">다음 중 하나에 해당 하는 특수화를 생성 하는 *방법을* 컴파일러에 지시 하는 *지시문* 입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-209">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="910ef-210">`intrinsic`-대상 컴퓨터가 특수화를 제공 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-210">`intrinsic`, which indicates that the target machine provides the specialization.</span></span>
  - <span data-ttu-id="910ef-211">`distribute`및 특수화와 함께 `controlled` 사용 `controlled adjoint` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-211">`distribute`, used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="910ef-212">에서 사용 하는 경우 `controlled` 컴파일러는의 `Controlled` 모든 작업에를 적용 하 여 특수화를 계산 해야 함을 나타냅니다 `body` .</span><span class="sxs-lookup"><span data-stu-id="910ef-212">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="910ef-213">과 함께 사용 하는 경우 `controlled adjoint` `Controlled` 특수화의 모든 작업에를 적용 하 여 컴파일러가 특수화를 계산 해야 함을 나타냅니다 `adjoint` .</span><span class="sxs-lookup"><span data-stu-id="910ef-213">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="910ef-214">`invert`. 예를 들어 `adjoint` `body` 작업 순서를 반대로 하 고 각각에 adjoint를 적용 하 여 컴파일러가 특수화를 계산 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-214">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, for example, reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="910ef-215">이는와 함께 사용 될 때 `adjoint controlled` 컴파일러가 특수화를 반전 하 여 특수화를 계산 해야 함을 나타냅니다 `controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-215">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="910ef-216">`self`-adjoint 특수화가 특수화와 동일 함을 표시 `body` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-216">`self`, to indicate that the adjoint specialization is the same as the `body` specialization.</span></span>
    <span data-ttu-id="910ef-217">`self`및 특수화에는를 사용할 수 `adjoint` `adjoint controlled` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-217">Using `self` is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="910ef-218">의 `adjoint controlled` 경우 `self` `adjoint controlled` 특수화가 특수화와 동일 함을 의미 합니다 `controlled` .</span><span class="sxs-lookup"><span data-stu-id="910ef-218">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="910ef-219">`auto`-컴파일러가 적용할 적절 한 지시문을 선택 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-219">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="910ef-220">특수화에는를 사용할 수 없습니다 `auto` `body` .</span><span class="sxs-lookup"><span data-stu-id="910ef-220">You cannot use`auto` for the `body` specialization.</span></span>

<span data-ttu-id="910ef-221">지시문과 모두에는 `auto` 닫는 세미콜론이 필요 `;` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-221">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="910ef-222">`auto`의 명시적 선언이 제공 되는 경우 지시문은 다음과 같이 생성 된 지시문으로 확인 `body` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-222">The `auto` directive resolves to the following generated directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="910ef-223">`adjoint`특수화는 지시문에 따라 생성 `invert` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-223">The `adjoint` specialization generates according to the directive `invert`.</span></span>
- <span data-ttu-id="910ef-224">`controlled`특수화는 지시문에 따라 생성 `distribute` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-224">The `controlled` specialization generates according to the directive `distribute`.</span></span>
- <span data-ttu-id="910ef-225">`adjoint controlled`특수화는 `invert` 에 대 한 명시적 선언이 `controlled` 지정 되었지만에 대해 지정 되지 않은 경우 지시문에 따라 생성 되 `adjoint` 고 그렇지 않은 경우에는 `distribute` 입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-225">The `adjoint controlled` specialization  generates according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="910ef-226">작업이 자체 adjoint 인 경우 생성 지시문을 통해 adjoint 또는 제어 된 adjoint 특수화를 명시적으로 지정 `self` 하 여 컴파일러가 최적화를 위해 해당 정보를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-226">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="910ef-227">사용자 정의 구현을 포함 하는 특수화 선언은 인수 튜플 및 Q# 특수화를 구현 하는 코드를 포함 하는 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-227">A specialization declaration containing a user-defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="910ef-228">인수 목록에서 `...` 은 작업에 대해 전체적으로 선언 된 인수를 나타내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-228">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="910ef-229">및의 경우 `body` `adjoint` 인수 목록은 항상 이어야 합니다 `(...)` . 및의 `controlled` 경우 `adjoint controlled` 인수 목록은 컨트롤의 배열을 나타내는 기호 여야 합니다 ( `...` 예:) `(controls,...)` .</span><span class="sxs-lookup"><span data-stu-id="910ef-229">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="910ef-230">예</span><span class="sxs-lookup"><span data-stu-id="910ef-230">Examples</span></span>

<span data-ttu-id="910ef-231">작업 선언은 다음과 같이 간단할 수 있습니다 .이는 기본 Pauli X 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-231">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="910ef-232">Pauli X 작업의 adjoint는 `self` 정의에 따라 고유한 역함수 이기 때문에 지시문을 사용 하 여 정의 됩니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="910ef-232">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="910ef-233">이전 예제에서 `PrepareEntangledPair` 코드는 명시적 특수화 선언이 포함 된 다음 코드와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-233">In the earlier `PrepareEntangledPair` example, the code is equivalent to the following code containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="910ef-234">키워드는 `auto` 컴파일러가 특수화 구현을 생성 하는 방법을 결정 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-234">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="910ef-235">사용자 정의 특수화 구현</span><span class="sxs-lookup"><span data-stu-id="910ef-235">User-defined specialization implementation</span></span>

<span data-ttu-id="910ef-236">컴파일러가 특정 특수화에 대 한 구현을 자동으로 생성할 수 없거나 보다 효율적인 구현을 제공할 수 있는 경우에는 구현을 수동으로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-236">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then you can manually define the implementation.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="910ef-237">이전 예제에서는 `adjoint invert;` 본문 구현을 반전 하 여 adjoint 특수화를 생성 하 고, 제어 된 `controlled adjoint invert;` 특수화의 지정 된 구현을 반전 하 여 제어 된 adjoint 특수화가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-237">In the previous example, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="910ef-238">기본 본문 외에도 하나 이상의 특수화를 명시적으로 선언 해야 하는 경우 기본 본문의 구현은 적절 한 특수화 선언에도 래핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-238">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="910ef-239">특수화를 유효 하 게 정의 하는 상황</span><span class="sxs-lookup"><span data-stu-id="910ef-239">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="910ef-240">Adjoint/제어를 사용 하는 작업 선언</span><span class="sxs-lookup"><span data-stu-id="910ef-240">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="910ef-241">Adjoint 또는 제어 된 버전이 없는 작업을 지정 하는 것은 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-241">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="910ef-242">예를 들어, 측정 작업은 역 변환할 수 없거나 제어할 수 없기 때문에 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-242">For instance, measurement operations have neither because they are not invertible or controllable.</span></span>

<span data-ttu-id="910ef-243">작업은 선언에 `Adjoint` `Controlled` 각 특수화의 암시적 또는 명시적 선언이 포함 된 경우 및 함수을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-243">An operation supports the `Adjoint` and `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="910ef-244">명시적으로 선언 된 adjoint/제어 된 특수화는 adjoint/제어 된 특수화의 존재를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-244">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="910ef-245">본문이-success 루프, set 문, 측정값, return 문 또는 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우 `Adjoint` 또는 지시문 다음에 adjoint 특수화 자동 생성을 `invert` `auto` 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-245">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="910ef-246">해당 본문에서 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우 `Controlled` 또는 지시문 다음에 제어 된 특수화를 자동으로 생성할 `distribute` `auto` 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-246">For an operation whose body contains calls to other operations that do not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="910ef-247">제어 된 Adjoint</span><span class="sxs-lookup"><span data-stu-id="910ef-247">Controlled Adjoint</span></span>

<span data-ttu-id="910ef-248">작업의 제어 된 adjoint 버전은 작업의 adjoint의 퀀텀 제어 버전을 구현 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-248">The controlled adjoint version of an operation specifies how to implement a quantum-controlled version of the adjoint of the operation.</span></span>
<span data-ttu-id="910ef-249">제어 된 adjoint 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 제어 또는 반전할 수 없기 때문에 제어 되는 adjoint 버전이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-249">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="910ef-250">작업에 대 한 제어 된 adjoint 특수화는 adjoint와 제어 된 특수화가 모두 있는 경우에만 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-250">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="910ef-251">이 경우 제어 된 adjoint 특수화의 존재 여부가 유추 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-251">In that case, the existence of the controlled adjoint specialization is inferred.</span></span> <span data-ttu-id="910ef-252">명시적으로 정의 된 구현이 없는 경우 컴파일 시 적절 한 특수화가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-252">If no implementation is explicitly defined, the compile generates an appropriate specialization.</span></span>

<span data-ttu-id="910ef-253">해당 본문에 제어 된 adjoint 버전이 없는 다른 작업에 대 한 호출이 포함 된 작업의 경우, 또는 지시문 다음에 나오는 adjoint 특수화를 자동으로 생성할 `invert` `distribute` `auto` 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute`, or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="910ef-254">형식 호환성</span><span class="sxs-lookup"><span data-stu-id="910ef-254">Type Compatibility</span></span>

<span data-ttu-id="910ef-255">모든 위치에서 지원 되는 추가 함수와 함께 작업을 사용 합니다 .이 작업은 함수 더 적거나 동일한 서명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-255">Use an operation with additional functors supported anywhere you use an operation with fewer functors but the same signature.</span></span> <span data-ttu-id="910ef-256">예를 들어 형식의 작업을 사용 하는 모든 위치에서 형식의 작업을 사용 `(Qubit => Unit is Adj)` `(Qubit => Unit)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-256">For instance, use an operation of type `(Qubit => Unit is Adj)` anywhere you use an operation of type `(Qubit => Unit)`.</span></span>

<span data-ttu-id="910ef-257">Q#는 호출 가능 반환 형식과 관련 하 여 *공변 (covariant* )이 있습니다. 형식을 반환 하는 호출 가능은 `'A` 동일한 입력 형식 및와 호환 되는 결과 형식으로 호출할 수 있는와 호환 됩니다. `'A`</span><span class="sxs-lookup"><span data-stu-id="910ef-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that is compatible with `'A` .</span></span>

<span data-ttu-id="910ef-258">Q#입력 형식과 관련 하 여 *반공 변 (contravariant* ): 형식을 입력으로 사용 하는 호출할 수 있는는 `'A` 동일한 결과 형식 및와 호환 되는 입력 형식으로 호출할 수 있는와 호환 됩니다 `'A` .</span><span class="sxs-lookup"><span data-stu-id="910ef-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="910ef-259">즉, 다음과 같은 정의가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-259">That is, given the following definitions,</span></span>

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="910ef-260">당신은 할 수 있어요</span><span class="sxs-lookup"><span data-stu-id="910ef-260">you can</span></span>

- <span data-ttu-id="910ef-261">`ConjugateInvertWith`또는의 인수를 사용 하 여 함수를 호출 합니다 `inner` `Invert` `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="910ef-261">Invoke the function `ConjugateInvertWith` with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="910ef-262">`ConjugateUnitaryWith`의 인수를 사용 하 여 함수를 호출 `inner` `ApplyUnitary` `Invert` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-262">Invoke the function `ConjugateUnitaryWith` with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="910ef-263">에서 형식의 값을 반환 `(Qubit[] => Unit is Adj + Ctl)` `ConjugateInvertWith` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-263">Return a value of type `(Qubit[] => Unit is Adj + Ctl)` from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="910ef-264">Q#0.3에서는 사용자 정의 형식의 동작에 상당한 차이점이 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="910ef-265">사용자 정의 형식은 하위 형식이 아니라 기본 형식의 래핑된 버전으로 취급 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="910ef-266">이는 기본 형식의 값이 인 것으로 간주 되는 사용자 정의 형식의 값을 사용할 수 없음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-266">This means that a value of a user-defined type is not usable where you expect a value of the underlying type is.</span></span>


### <a name="conjugations"></a><span data-ttu-id="910ef-267">변화</span><span class="sxs-lookup"><span data-stu-id="910ef-267">Conjugations</span></span>

<span data-ttu-id="910ef-268">기존 비트와는 달리, 더 이상 필요 하지 않은 계산에 대 한 의도 하지 않은 영향이 있을 경우이를 무조건 다시 설정 하면 나머지 계산에 원치 않는 영향이 있을 수 있으므로 퀀텀 메모리 해제는 약간 더 복잡 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="910ef-269">메모리를 해제 하기 전에 수행 된 계산을 적절히 "실행 취소" 하 여 이러한 효과를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-269">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="910ef-270">따라서 퀀텀 컴퓨팅의 일반적인 패턴은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-270">A common pattern in quantum computing is hence the following:</span></span> 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

<span data-ttu-id="910ef-271">0.9 릴리스부터는 Q# 이전 변환을 구현 하는 활용 문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-271">Starting with our 0.9 release, Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="910ef-272">이 문을 사용 하 여 `ApplyWith` 다음과 같은 방법으로 작업을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
<span data-ttu-id="910ef-273">외부 및 내부 변환을 작업으로 쉽게 사용할 수 없지만 대신 여러 문으로 구성 된 블록에서 더 편리 하 게 설명 하는 경우 이러한 활용 문은 훨씬 더 유용 해 집니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-273">Such a conjugation statement becomes far more useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="910ef-274">블록 내에서 정의 된 문에 대 한 역 변환은 컴파일러에 의해 자동으로 생성 되 고 적용 블록이 완료 된 후에 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="910ef-275">블록 내에 사용 되는 변경할 수 있는 변수는 적용 블록에서 바인딩 가능 하지 않으므로 생성 된 변환은 블록 내에서 계산의 adjoint로 보장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="910ef-276">새 함수 정의</span><span class="sxs-lookup"><span data-stu-id="910ef-276">Defining New Functions</span></span>

<span data-ttu-id="910ef-277">함수는 순수 하 게 결정적 이며,이 루틴은 Q# 출력 값을 계산 하는 것 이상의 효과를 허용 하지 않는 작업과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="910ef-278">특히 함수는 작업을 호출할 수 없습니다. 작업 수행, 할당 또는 적용 샘플 난수 또는 함수에 대 한 입력 값 이상의 상태에 종속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="910ef-279">결과적으로 함수는 Q# 항상 동일한 입력 값을 동일한 출력 값에 매핑하기 때문에 *순수*합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="910ef-280">이 동작을 통해 Q# 컴파일러는 작업 특수화를 생성할 때 함수를 호출 하는 방법 및 시기를 안전 하 게 다시 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-280">This behavior allows the Q# compiler to safely reorder how and when to call functions when generating operation specializations.</span></span>

<span data-ttu-id="910ef-281">각 Q# 소스 파일은 원하는 수의 함수를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-281">Each Q# source file can define any number of functions.</span></span>
<span data-ttu-id="910ef-282">함수 이름은 네임 스페이스 내에서 고유 해야 하며 작업 또는 형식 이름과 충돌할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-282">Function names must be unique within a namespace and cannot conflict with operation or type names.</span></span>

<span data-ttu-id="910ef-283">함수 정의는 함수에 대해 adjoint 또는 제어 된 특수화를 정의할 수 없다는 점을 제외 하 고 작업을 정의 하는 것과 유사 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="910ef-284">예:</span><span class="sxs-lookup"><span data-stu-id="910ef-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="910ef-285">또는</span><span class="sxs-lookup"><span data-stu-id="910ef-285">or</span></span> 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="910ef-286">함수의 기존 논리 = = 양호</span><span class="sxs-lookup"><span data-stu-id="910ef-286">Classical logic in functions == good</span></span>

<span data-ttu-id="910ef-287">이렇게 할 수 있는 경우에는 작업 보다 더 쉽게 사용할 수 있도록 함수 대신 함수를 사용 하 여 기존 논리를 작성 하는 것이 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations so that operations can more readily use it.</span></span> <span data-ttu-id="910ef-288">예를 들어 이전 `Square` 선언을 *작업*으로 작성 한 경우 컴파일러는 동일한 입력을 사용 하 여 호출 하는 것이 일관 되 게 동일한 출력을 생성 하도록 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-288">For example, if you had written the earlier `Square` declaration as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="910ef-289">함수와 작업 사이의 차이를 표시 하려면 작업 내에서 난수를 샘플링 하 여 일반적으로 문제를 고려해 야 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="910ef-290">`U`가 호출 될 때마다에 대해 다른 작업을 수행 `target` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-290">Each time that `U` is called, it has a different action on `target`.</span></span>
<span data-ttu-id="910ef-291">특히 특수화 선언을에 추가 하는 경우 컴파일러는 `adjoint auto` `U` `U(target); Adjoint U(target);` id (즉, op)로 작동 하도록 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-291">In particular, the compiler cannot guarantee that if you add an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="910ef-292">이는 [벡터 및 행렬](xref:microsoft.quantum.concepts.vectors)에 정의 된 adjoint의 정의를 위반 합니다. 즉, 컴파일러가 작업을 호출 하는 작업에서 adjoint 특수화를 자동으로 생성 하 여 <xref:microsoft.quantum.math.randomreal> 컴파일러에서 제공 하는 보증을 중단 하는 것과 같이 <xref:microsoft.quantum.math.randomreal> adjoint 또는 제어 된 버전이 없는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-292">This violates the definition of the adjoint defined in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing the compiler to auto-generate an adjoint specialization in an operation where you call the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="910ef-293">반면,와 같은 함수 호출을 안전 하 게 허용 하 `Square` 고 `Square` 출력을 안정적으로 유지 하기 위해 입력을 유지 해야 한다는 것을 컴파일러에 게 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-293">On the other hand, allowing function calls such as `Square` is safe, and assures the compiler that it only needs to preserve the input to `Square` to keep its output stable.</span></span>
<span data-ttu-id="910ef-294">따라서 함수에서 최대한 많은 고전 논리를 격리 하면 다른 함수와 작업에서 해당 논리를 쉽게 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="910ef-295">제네릭 (형식 매개 변수화 된) Callables</span><span class="sxs-lookup"><span data-stu-id="910ef-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="910ef-296">정의할 수 있는 많은 함수와 연산은 실제로 해당 입력의 형식에 의존 하지 않고 다른 함수 또는 작업을 통해서만 암시적으로 해당 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-296">Many functions and operations that you might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="910ef-297">예를 들어 많은 기능 언어에 공통적인 *map* 개념을 살펴보겠습니다. 함수 $f (x) $ 및 값 $ \{ x_1, x_2, \dots, x_n \} $, map이 지정 된 경우 새 컬렉션 $ \{ f (x_1), f (x_2), \ 점, f (x_n) $를 반환 합니다 \} .</span><span class="sxs-lookup"><span data-stu-id="910ef-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="910ef-298">에서이를 구현 하려면 Q# 함수가 첫 번째 클래스 라는 사실을 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-298">To implement this in Q#, take advantage of the fact that functions are first class.</span></span>
<span data-ttu-id="910ef-299">`Map` `T` 필요한 형식을 확인 하는 동안를 자리 표시자로 사용 하는 간단한 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-299">Here is a quick example of `Map`, using `T` as a placeholder while you figure out what types you need.</span></span>

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="910ef-300">이 함수는에서 대체 하는 실제 형식에 관계 없이 거의 동일 하 게 보입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-300">Note that this function looks very much the same no matter what actual types you substitute in.</span></span>
<span data-ttu-id="910ef-301">예를 들어 정수에서 Paulis의 맵은 부동 소수점 숫자에서 문자열로의 맵과 거의 같습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="910ef-302">원칙적으로는 `Map` 발생 하는 모든 형식 쌍에 대해의 버전을 작성할 수 있지만이 경우 여러 가지 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-302">In principle, you could write a version of `Map` for every pair of types that you encounter, but this introduces several difficulties.</span></span>
<span data-ttu-id="910ef-303">예를 들어에서 버그를 발견 한 경우에는 `Map` 모든 버전의에서 일관 되 게 수정 사항을 적용 해야 합니다 `Map` .</span><span class="sxs-lookup"><span data-stu-id="910ef-303">For instance, if you find a bug in `Map`, then you must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="910ef-304">또한 새 튜플 또는 UDT를 생성 하는 경우 새 형식과 함께 새를 구성 해야 합니다 `Map` .</span><span class="sxs-lookup"><span data-stu-id="910ef-304">Moreover, if you construct a new tuple or UDT, then you must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="910ef-305">이러한 함수는 약간의 이러한 기능을 다루기가 하지만,와 동일한 폼의 더 많은 함수를 수집 하는 경우 `Map` 새 형식을 도입 하는 비용은 매우 짧은 순서로 지나치게 길면 커집니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-305">While this is tractable for a small number of such functions, as you collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="910ef-306">그러나 이러한 어려움의 대부분은 서로 다른 버전의와 관련 된 방법을 인식 하는 데 필요한 정보를 컴파일러에 제공 하지 않았기 때문에 발생 `Map` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-306">However, much of this difficulty results from the fact that you have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="910ef-307">효과적으로 컴파일러에서 `Map` Q# *형식* 에서 함수로 함수를 일종의 수학적 함수로 처리 하려고 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-307">Effectively, you want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="910ef-308">Q#는 함수 및 작업에 *형식 매개 변수와*일반적인 튜플 매개 변수를 포함 하도록 허용 하 여이 개념을 공식화 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-308">Q# formalizes this notion by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="910ef-309">앞의 예제에서는 `Map` `Int, Pauli` 첫 번째 경우와 두 번째 경우에 형식 매개 변수를 포함 한다고 생각 합니다 `Double, String` .</span><span class="sxs-lookup"><span data-stu-id="910ef-309">In the previous examples, you wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="910ef-310">대부분의 경우 이러한 형식 매개 변수를 일반적인 형식인 것 처럼 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-310">For the most part, use these type parameters as though they were ordinary types.</span></span> <span data-ttu-id="910ef-311">형식 매개 변수 값을 사용 하 여 배열 및 튜플을 만들고, 함수 및 작업을 호출 하 고, 일반 변수 또는 변경 가능한 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-311">Use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="910ef-312">간접적 종속성의 가장 극단적인 경우는 Q# 프로그램에서 형식의 구조를 직접 사용할 수 `Qubit` 없지만 이러한 형식을 다른 작업 및 함수에 전달 **해야** 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-312">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="910ef-313">이전 예제로 돌아가면에서 입력을 `Map` 나타내는 형식 매개 변수와 출력을 나타내는 하나를 표시 하는 형식 매개 변수가 있어야 합니다 `fn` `fn` .</span><span class="sxs-lookup"><span data-stu-id="910ef-313">Returning to the earlier example, then, you see that `Map` needs to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="910ef-314">에서는 Q# `<>` {} 선언에서 함수 또는 작업 이름 뒤에 꺾쇠 괄호 (brakets $ \braket $!)를 추가 하 고 각 형식 매개 변수를 나열 하 여이를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-314">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="910ef-315">각 형식 매개 변수의 이름은 틱으로 시작 해야 `'` 하며 일반 형식 ( *구체적* 형식이 라고도 함)이 아니라 형식 매개 변수 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-315">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="910ef-316">따라서 `Map` 는 다음과 같이 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-316">Thus, `Map`, is written:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="910ef-317">의 정의는 `Map<'Input, 'Output>` previoius 버전과 매우 유사 하 게 보입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-317">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the previoius versions.</span></span>
<span data-ttu-id="910ef-318">유일한 차이점은 컴파일러에 직접 의존 하지 않는 컴파일러에 명시적으로 알리는 것이 `Map` `'Input` 고 `'Output` ,이를 간접적으로 사용 하 여 두 가지 형식에 대해 작동 `fn` 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-318">The only difference is that you have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="910ef-319">이러한 방식으로를 정의한 후 `Map<'Input, 'Output>` 에는 일반적인 함수 처럼 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-319">Once you have defined `Map<'Input, 'Output>` in this way, you can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="910ef-320">제네릭 함수 및 작업을 작성 하는 것은 함수 및 작업에 대해 생각 하는 데 매우 유용한 방법입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-320">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="910ef-321">모든 함수는 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하므로 형식의 입력은 `'T -> 'U` *모든* Q# 함수와 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-321">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="910ef-322">마찬가지로 형식의 입력에 작업을 전달할 수 있습니다 `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="910ef-322">Similarly, you can pass any operation to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="910ef-323">두 번째 예는 다른 두 함수의 컴퍼지션을 반환 하는 함수를 작성 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-323">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="910ef-324">여기에서, 및가 무엇 인지 정확 하 게 지정 해야 `A` `B` `C` 하므로 새 함수의 유틸리티를 심각 하 게 제한 합니다 `Compose` .</span><span class="sxs-lookup"><span data-stu-id="910ef-324">Here, you must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="910ef-325">그 후에는 `Compose` 및를 `A` 통해, 및에만 의존 `B` `C` *via* `innerFn` `outerFn` 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-325">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="910ef-326">또는 `Compose` *any* `A` `B` `C` 이러한 매개 변수가 및에서 예상한 것과 일치 하는 경우, 및에 대해 작동 함을 나타내는 `innerFn` 형식 매개 변수를에 추가할 수 있습니다 `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="910ef-326">As an alternative, then, you can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="910ef-327">Q#표준 라이브러리는 이러한 형식의 매개 변수가 있는 작업 및 함수를 제공 하 여 더 높은 순서 제어 흐름을 보다 쉽게 표현할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-327">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="910ef-328">이러한 내용은 [ Q# 표준 라이브러리 가이드](xref:microsoft.quantum.libraries.standard.intro)에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-328">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="910ef-329">첫 번째 클래스 값으로 callables</span><span class="sxs-lookup"><span data-stu-id="910ef-329">Callables as First-Class Values</span></span>

<span data-ttu-id="910ef-330">작업 대신 함수를 사용 하는 제어 흐름과 기존 논리를 추론 하는 한 가지 중요 한 기술은의 작업 및 함수를 활용 하는 것입니다 Q# . *first-class*</span><span class="sxs-lookup"><span data-stu-id="910ef-330">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="910ef-331">즉, 해당 언어의 각 값은 고유한 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-331">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="910ef-332">예를 들어, 약간의 간접적인 경우 다음과 같은 코드는 완벽 하 게 유효 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-332">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="910ef-333">`ourH`이전 코드 조각의 변수 값은 <xref:microsoft.quantum.intrinsic.h> 다른 작업 처럼 해당 값을 호출할 수 있도록 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-333">The value of the variable `ourH` in the previous snippet is then the operation <xref:microsoft.quantum.intrinsic.h>, such that you can call that value like any other operation.</span></span>
<span data-ttu-id="910ef-334">이 기능을 사용 하면 작업을 수행 하는 작업을 작성 하 여 고차 제어 흐름 개념을 형성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-334">With this ability, you can write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="910ef-335">예를 들어 동일한 대상의 동일한 대상에 두 번 적용 하 여 작업을 "제곱" 하는 것을 생각해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-335">For instance, you could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="910ef-336">함수에서 작업 반환</span><span class="sxs-lookup"><span data-stu-id="910ef-336">Returning operations from a function</span></span>

<span data-ttu-id="910ef-337">작업을 출력의 일부로 반환 하는 것이 중요 합니다. 예를 들어 작업 형식으로 퀀텀 프로그램에 대 한 설명을 반환 하는 클래식 함수로 일부 종류의 클래식 조건부 논리를 격리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-337">It's important to emphasize that you can also return operations as a part of outputs, such that you can isolate some kinds of classical conditional logic as a classical function, which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="910ef-338">간단한 예로, 2 비트 클래식 메시지를 수신 하는 파티가 메시지를 사용 하 여 해당 teleportation를 적절 한 teleported 상태로 디코딩하는 경우를 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-338">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="910ef-339">이러한 두 개의 기존 비트를 사용 하 고 적절 한 디코딩 작업을 반환 하는 함수를 기준으로이를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-339">You could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

<span data-ttu-id="910ef-340">이 새로운 함수는 실제로 함수 이며, 같은 값을 사용 하 여이 함수를 호출 하는 경우 `hereBit` `thereBit` 항상 동일한 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-340">This new function is indeed a function, in that if you call it with the same values of `hereBit` and `thereBit`, you always get back the same operation.</span></span>
<span data-ttu-id="910ef-341">따라서 디코딩 논리가 다른 작업 특수화의 정의와 상호 작용 하는 방법에 대해 설명 하지 않고도 디코더를 작업 내에서 안전 하 게 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-341">Thus, the decoder can safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="910ef-342">즉, 함수 내의 기존 논리가 격리 되므로 입력이 유지 되는 한, 함수 호출을 사용 하 여 함수 호출을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-342">That is, the classical logic inside a function is isolated, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="910ef-343">부분 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="910ef-343">Partial Application</span></span>

<span data-ttu-id="910ef-344">*부분 응용 프로그램*을 사용 하 여 작업을 반환 하는 함수를 사용 하 여 작업을 반환 하는 함수를 사용 하 여 더 많은 작업을 수행할 수 있습니다. 이러한 함수는 실제로 호출 하지 않고 함수 또는 작업에 입력의</span><span class="sxs-lookup"><span data-stu-id="910ef-344">You can do significantly more with functions that return operations by using *partial application*, in which you provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="910ef-345">앞의 예제에서 입력 작업을 적용 해야 하는 것을 즉시 지정 하지 않으려는 경우를 `ApplyTwice` 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-345">In the earlier `ApplyTwice` example, you can indicate that you don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="910ef-346">이 경우 지역 변수는 `twiceOp` 부분적으로 적용 된 작업을 보유 합니다 `ApplyTwice(op, _)` . 여기서는 `_` 아직 지정 되지 않은 입력 부분을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-346">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where `_` indicates parts of the input that have not yet been specified.</span></span>
<span data-ttu-id="910ef-347">`twiceOp`다음 줄에서를 호출 하는 경우 입력의 나머지 부분을 모두 원래 작업에 적용 하 여 부분적으로 적용 된 작업에 입력으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-347">When you call `twiceOp` in the next line, you pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="910ef-348">따라서 이전 코드 조각은 실제로 직접 호출 하는 것과 동일 합니다 `ApplyTwice(op, target)` . 새 지역 변수를 도입 하 여 입력의 일부를 제공 하는 동안 호출을 지연할 수 있도록 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-348">Thus, the previous snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that you have introduced a new local variable so you can delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="910ef-349">부분적으로 적용 된 작업은 전체 입력이 제공 될 때까지 실제로 호출 되지 않으므로 함수 내 에서도 작업을 부분적으로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-349">Since an operation that has been partially applied is not actually called until its entire input has been provided, you can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="910ef-350">원칙적으로 내에서의 기존 논리는 `SquareOperation` 훨씬 더 많은 관련이 있었지만 컴파일러가 함수에 대해 제공할 수 있는 보증을 통해 작업의 나머지 부분과 여전히 격리 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-350">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span> <span data-ttu-id="910ef-351">Q#표준 라이브러리는 퀀텀 프로그램에서 쉽게 사용할 수 있는 방식으로 클래식 제어 흐름을 표현 하는 데이 접근 방식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-351">The Q# standard library uses this approach throughout for expressing classical control flow in a way that quantum programs can readily use.</span></span>


## <a name="recursion"></a><span data-ttu-id="910ef-352">재귀</span><span class="sxs-lookup"><span data-stu-id="910ef-352">Recursion</span></span>

<span data-ttu-id="910ef-353">Q#callables은 직접 또는 간접적으로 재귀적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-353">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="910ef-354">즉, 작업 또는 함수가 자신을 호출 하거나 호출 가능 작업을 직접 또는 간접적으로 호출 하는 다른 호출 가능 함수를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-354">That is, an operation or function can call itself, or it can call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="910ef-355">그러나 재귀 사용에 대 한 두 가지 중요 한 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-355">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="910ef-356">작업에서 재귀를 사용 하면 특정 최적화에 방해가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-356">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="910ef-357">이 간섭을 통해 알고리즘의 실행 시간에 상당한 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-357">This interference can have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="910ef-358">실제 퀀텀 장치에서 실행 되는 경우 스택 공간이 제한 될 수 있으므로 심층 재귀가 런타임 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-358">When running on an actual quantum device, stack space might be limited, and so deep recursion can lead to a runtime error.</span></span>
  <span data-ttu-id="910ef-359">특히 Q# 컴파일러와 런타임에서는 마무리 재귀를 식별 하 고 최적화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="910ef-359">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="next-steps"></a><span data-ttu-id="910ef-360">다음 단계</span><span class="sxs-lookup"><span data-stu-id="910ef-360">Next steps</span></span>

<span data-ttu-id="910ef-361">에서 [변수에](xref:microsoft.quantum.guide.variables) 대해 알아보세요 Q# .</span><span class="sxs-lookup"><span data-stu-id="910ef-361">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>