---
title: 'Q # 표준 라이브러리-진단 | Microsoft Docs'
description: 'Q # 표준 라이브러리-진단'
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 67ec6780d8cbbda7223d46026a9df97cebc92b33
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820983"
---
# <a name="diagnostics"></a><span data-ttu-id="0e362-103">진단</span><span class="sxs-lookup"><span data-stu-id="0e362-103">Diagnostics</span></span> #

<span data-ttu-id="0e362-104">기존 개발과 마찬가지로 퀀텀 프로그램에서 실수 및 오류를 진단할 수 있는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-104">As with classical development, it is important to be able to diagnose mistakes and errors in quantum programs.</span></span>
<span data-ttu-id="0e362-105">Q # 표준 라이브러리는 <xref:microsoft.quantum.techniques.testing-and-debugging>에 설명 된 대로 퀀텀 프로그램의 정확성을 보장 하는 다양 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-105">The Q# standard libraries provide a variety of different ways to ensure the correctness of quantum programs, as detailed in <xref:microsoft.quantum.techniques.testing-and-debugging>.</span></span>
<span data-ttu-id="0e362-106">이러한 지원은 대부분 호스트 프로그램 또는 개발자에 게 추가 진단 정보를 제공 하도록 대상 컴퓨터에 지시 하거나 조건 및 고정의 정확성을 강제 적용 하는 함수 및 작업 형식으로 제공 됩니다. 함수 또는 작업 호출을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-106">Largely speaking, this support comes in the form of functions and operations that either instruct the target machine to provide additional diagnostic information to the host program or developer, or enforce the correctness of conditions and invariants expressed by the function or operation call.</span></span>

## <a name="machine-diagnostics"></a><span data-ttu-id="0e362-107">컴퓨터 진단</span><span class="sxs-lookup"><span data-stu-id="0e362-107">Machine Diagnostics</span></span> ##

<span data-ttu-id="0e362-108"><xref:microsoft.quantum.intrinsic.message> 함수를 사용 하 여 컴퓨터 종속 방식으로 메시지를 기록 하 여 기존 값에 대 한 진단 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-108">Diagnostics about classical values can be obtained by using the <xref:microsoft.quantum.intrinsic.message> function to log a message in a machine-dependent way.</span></span>
<span data-ttu-id="0e362-109">기본적으로이 문자열은 콘솔에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-109">By default, this writes the string to the console.</span></span>
<span data-ttu-id="0e362-110"><xref:microsoft.quantum.intrinsic.message> 보간된 문자열과 함께 사용 하 여 기존 값에 대 한 진단 정보를 쉽게 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-110">Used together with interpolated strings, <xref:microsoft.quantum.intrinsic.message> makes it easy to report diagnostic information about classical values:</span></span>

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> <span data-ttu-id="0e362-111">`Message`에는 시그니처 `(String -> Unit)`있으며,이는 디버그 로그 메시지 내보내기가 Q # 내에서 관찰 될 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-111">`Message` has signature `(String -> Unit)`, again representing that emitting a debug log message cannot be observed from within Q#.</span></span>

<span data-ttu-id="0e362-112"><xref:microsoft.quantum.diagnostics.dumpmachine> 및 <xref:microsoft.quantum.diagnostics.dumpregister> callables은 대상 컴퓨터에 현재 할당 된 모든 기능에 대 한 진단 정보를 제공 하거나 각각의 특정 기능에 대 한 진단 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-112">The <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister> callables instruct target machines to provide diagnostic information about all currently allocated qubits or about a specific register of qubits, respectively.</span></span>
<span data-ttu-id="0e362-113">각 대상 컴퓨터는 덤프 명령에 대 한 응답으로 제공 되는 진단 정보에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-113">Each target machine varies in what diagnostic information is provided in response to a dump instruction.</span></span>
<span data-ttu-id="0e362-114">예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator) 대상 컴퓨터는 내부에서 사용 하는 상태 vector를 호스트 프로그램에 제공 하 여 해당 기능을 내부적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-114">The [full state simulator](xref:microsoft.quantum.machines.full-state-simulator) target machine, for instance, provides the host program with the state vector that it uses internally to represent a register of qubits.</span></span>
<span data-ttu-id="0e362-115">비교 하 여 [Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator) 대상 컴퓨터는 각 고 비트에 대해 단일 고전 비트를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-115">By comparison, the [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator) target machine provides a single classical bit for each qubit.</span></span>

 <span data-ttu-id="0e362-116">[전체 상태 시뮬레이터의](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` 출력에 대해 자세히 알아보려면 [테스트 및 디버깅 문서의](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions)덤프 함수 섹션을 살펴보세요.</span><span class="sxs-lookup"><span data-stu-id="0e362-116">To learn more about the [full state simulator's](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` output, take a look at the dump functions section of our [testing and debugging article](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions).</span></span>


## <a name="facts-and-assertions"></a><span data-ttu-id="0e362-117">팩트 및 어설션</span><span class="sxs-lookup"><span data-stu-id="0e362-117">Facts and Assertions</span></span> ##

<span data-ttu-id="0e362-118">[테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging)에 설명 된 대로 시그니처 `Unit -> Unit` 또는 `Unit => Unit`를 사용 하는 함수 또는 작업은 각각 *단위 테스트*로 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-118">As discussed in [Testing and Debugging](xref:microsoft.quantum.techniques.testing-and-debugging), a function or operation with signature `Unit -> Unit` or `Unit => Unit`, respectively, can be marked as a *unit test*.</span></span>
<span data-ttu-id="0e362-119">각 단위 테스트는 일반적으로 해당 프로그램의 정확성을 확인 하는 하나 이상의 조건과 함께 작은 퀀텀 프로그램으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-119">Each unit test generally consists of a small quantum program, along with one or more conditions that check the correctness of that program.</span></span>
<span data-ttu-id="0e362-120">이러한 조건은 입력 값을 확인 하는 _팩트_형식 또는 입력으로 전달 된 하나 이상의 이상 상태를 확인 하는 _어설션_형식으로 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-120">These conditions can come in the form of either _facts_, which check the values of their inputs, or _assertions_, which check the states of one or more qubits passed as input.</span></span>

<span data-ttu-id="0e362-121">예를 들어 `EqualityFactI(1 + 1, 2, "1 + 1 != 2")`은 $1 + 1 = $2 이라는 수학적 팩트를 나타내며 `AssertQubit(One, qubit)`는 `qubit` 측정 하는 조건을 명확 하 게 `One` 반환 하는 조건을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-121">For example, `EqualityFactI(1 + 1, 2, "1 + 1 != 2")` represents the mathematical fact that $1 + 1 = 2$, while `AssertQubit(One, qubit)` represents the condition that measuring `qubit` will return a `One` with certainty.</span></span>
<span data-ttu-id="0e362-122">이전 경우에는 해당 값만 제공 된 조건의 정확성을 확인할 수 있습니다. 후자의 경우에는 어설션을 평가 하기 위해 해당 값에 대 한 정보를 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-122">In the former case, we can check the correctness of the condition given only its values, while in the latter, we must know something about the state of the qubit in order to evaluate the assertion.</span></span>

<span data-ttu-id="0e362-123">Q # 표준 라이브러리는 다음과 같은 여러 가지 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-123">The Q# standard libraries provide several different functions for representing facts, including:</span></span>

- <xref:microsoft.quantum.diagnostics.fact>
- <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact>
- <xref:microsoft.quantum.diagnostics.nearequalityfactc>
- <xref:microsoft.quantum.diagnostics.equalityfacti>


### <a name="testing-qubit-states"></a><span data-ttu-id="0e362-124">비트율 비트 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="0e362-124">Testing Qubit States</span></span> ###

<span data-ttu-id="0e362-125">실제로 어설션은 퀀텀 메커니즘의 클래식 시뮬레이션이 [복제 안 함 정리](https://arxiv.org/abs/quant-ph/9607018)을 준수 하지 않아도 된다는 사실에 의존 합니다 .이를 위해 대상 컴퓨터에 시뮬레이터를 사용 하는 경우 비 물리적 측정과 어설션을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-125">In practice, assertions rely on the fact that classical simulations of quantum mechanics need not obey the [no-cloning theorem](https://arxiv.org/abs/quant-ph/9607018), such that we can make unphysical measurements and assertions when using a simulator for our target machine.</span></span>
<span data-ttu-id="0e362-126">따라서 하드웨어에를 배포 하기 전에 기존 시뮬레이터에서 개별 작업을 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-126">Thus, we can test individual operations on a classical simulator before deploying on hardware.</span></span>
<span data-ttu-id="0e362-127">어설션 평가를 허용 하지 않는 대상 컴퓨터에서는 <xref:microsoft.quantum.intrinsic.assert>에 대 한 호출을 안전 하 게 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-127">On target machines which do not allow evaluation of assertions, calls to <xref:microsoft.quantum.intrinsic.assert> can be safely ignored.</span></span>

<span data-ttu-id="0e362-128">보다 일반적으로 지정 된의 지정 된 비트를 측정 하는 <xref:microsoft.quantum.intrinsic.assert> 작업에는 항상 지정 된 결과가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-128">More generally, the <xref:microsoft.quantum.intrinsic.assert> operation asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>
<span data-ttu-id="0e362-129">어설션이 실패 하면 지정 된 메시지와 함께 `fail`를 호출 하 여 실행이 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-129">If the assertion fails, the execution ends by calling `fail` with the given message.</span></span>
<span data-ttu-id="0e362-130">기본적으로이 작업은 구현 되지 않습니다. 이를 지원할 수 있는 시뮬레이터는 런타임 검사를 수행 하는 구현을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-130">By default, this operation is not implemented; simulators that can support it should provide an implementation that performs runtime checking.</span></span>
<span data-ttu-id="0e362-131">`Assert`에 `((Pauli[], Qubit[], Result, String) -> ())`시그니처가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-131">`Assert` has signature `((Pauli[], Qubit[], Result, String) -> ())`.</span></span>
<span data-ttu-id="0e362-132">`Assert`는 빈 튜플을 출력 형식으로 사용 하는 함수 이므로 `Assert`를 호출한 결과는 Q # 프로그램 내에서 관찰 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-132">Since `Assert` is a function with an empty tuple as its output type, no effects from having called `Assert` are observable within a Q# program.</span></span>

<span data-ttu-id="0e362-133"><xref:microsoft.quantum.intrinsic.assertprob> 작업 함수는 지정 된 Pauli의 지정 된 된 비트 수를 측정 하는 assert를 사용 하 여 지정 된 확률을 사용 하는 특정 결과를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-133">The <xref:microsoft.quantum.intrinsic.assertprob> operation function asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>
<span data-ttu-id="0e362-134">허용 오차는 덧셈입니다 (예: `abs(expected-actual) < tol`).</span><span class="sxs-lookup"><span data-stu-id="0e362-134">Tolerance is additive (e.g. `abs(expected-actual) < tol`).</span></span>
<span data-ttu-id="0e362-135">어설션이 실패 하면 지정 된 메시지와 함께 `fail`를 호출 하 여 실행이 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-135">If the assertion fails, the execution ends by calling `fail` with the given message.</span></span>
<span data-ttu-id="0e362-136">기본적으로이 작업은 구현 되지 않습니다. 이를 지원할 수 있는 시뮬레이터는 런타임 검사를 수행 하는 구현을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-136">By default, this operation is not implemented; simulators that can support it should provide an implementation that performs runtime checking.</span></span>
<span data-ttu-id="0e362-137">`AssertProb`에 `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)`시그니처가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-137">`AssertProb` has signature `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)`.</span></span> <span data-ttu-id="0e362-138">첫 번째 `Double` 매개 변수는 원하는 결과의 확률을 제공 하 고 두 번째 매개 변수는 허용 오차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-138">The first of `Double` parameters gives the desired probability of the result, and the second one the tolerance.</span></span>

<span data-ttu-id="0e362-139">단일 측정을 어설션하는 것 보다 더 많은 작업을 수행할 수 있습니다. 시뮬레이터에서 사용 되는 기존 정보를 복사 하는 것이 적합할,이를 통해 실제로 어설션을 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-139">We can do more than assert a single measurement, using that the classical information used by a simulator to represent the internal state of a qubit is amenable to copying, such that we do not need to actually perform a measurement to test our assertion.</span></span>
<span data-ttu-id="0e362-140">특히,이를 통해 실제 하드웨어에서 사용할 수 없는 *호환 되지* 않는 측정에 대해 설명할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-140">In particular, this allows us to reason about *incompatible* measurements that would be impossible on actual hardware.</span></span>

<span data-ttu-id="0e362-141">\Ket{\psi}가 $ \ket{0}$ 상태에 있을 때 $ $ 상태를 준비 하기 위한 작업 이라고 `P : Qubit => Unit` 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-141">Suppose that `P : Qubit => Unit` is an operation intended to prepare the state $\ket{\psi}$ when its input is in the state $\ket{0}$.</span></span>
<span data-ttu-id="0e362-142">$ \Ket{\psi '} $는 `P`에서 준비한 실제 상태가 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-142">Let $\ket{\psi'}$ be the actual state prepared by `P`.</span></span>
<span data-ttu-id="0e362-143">$ \Ket{\psi} $에서 설명 하는 축에서 $ \ket{\psi '} $를 측정 하는 경우에만 $ \ket{\psi} = \ket{\psi '} $가 항상 `Zero`을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-143">Then, $\ket{\psi} = \ket{\psi'}$ if and only if measuring $\ket{\psi'}$ in the axis described by $\ket{\psi}$ always returns `Zero`.</span></span>
<span data-ttu-id="0e362-144">즉, \begin{align} \ket{\psi} = \ket{\psi '} \text{} \braket{\psi | \psi '} = 1 인 경우에만 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-144">That is, \begin{align} \ket{\psi} = \ket{\psi'} \text{ if and only if } \braket{\psi | \psi'} = 1.</span></span>
<span data-ttu-id="0e362-145">prelude에 정의 된 기본 작업을 사용 하 여 \end{align} $ \ket{\psi} $가 Pauli 연산자 중 하나의 eigenstate 인 경우 `Zero`를 반환 하는 측정값을 직접 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-145">\end{align} Using the primitive operations defined in the prelude, we can directly perform a measurement that returns `Zero` if $\ket{\psi}$ is an eigenstate of one of the Pauli operators.</span></span>


<span data-ttu-id="0e362-146">작업 <xref:microsoft.quantum.diagnostics.assertqubit>에서는 어설션을 $ \ket{\psi} = \ket{0}$로 테스트 하려는 경우에 특히 유용한 약어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-146">The operation <xref:microsoft.quantum.diagnostics.assertqubit> provides a particularly useful shorthand to do so in the case that we wish to test the assertion $\ket{\psi} = \ket{0}$.</span></span>
<span data-ttu-id="0e362-147">예를 들어이를 해제 하기 전에 ancilla를 $ \ket{0}$로 반환 하기 위해 계산 되지 않은 경우에 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-147">This is common, for instance, when we have uncomputed to return ancilla qubits to $\ket{0}$ before releasing them.</span></span>
<span data-ttu-id="0e362-148">$ \Ket{0}$에 대 한 어설션은 두 상태 준비 `P` 및 `Q` 작업이 모두 동일한 상태를 준비 하 고 `Q` `Adjoint`를 지 원하는 경우에도 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-148">Asserting against $\ket{0}$ is also useful when we wish to assert that two state preparation `P` and `Q` operations both prepare the same state, and when `Q` supports `Adjoint`.</span></span>
<span data-ttu-id="0e362-149">특히,</span><span class="sxs-lookup"><span data-stu-id="0e362-149">In particular,</span></span>

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

<span data-ttu-id="0e362-150">그러나 일반적으로 Pauli 연산자의 eigenstates와 일치 하지 않는 상태에 대 한 어설션을 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-150">More generally, however, we may not have access to assertions about states that do not coincide with eigenstates of Pauli operators.</span></span>
<span data-ttu-id="0e362-151">예를 들어 $ \ket{\psi} = (\ket{0} + e ^ {i \pi/8} \ket{1})/\pi{2}$는 <xref:microsoft.quantum.intrinsic.assertprob>를 사용 하 여 $ \ket{\psi '} $ 상태가 $ \ket{\psi} $와 같은지를 고유 하 게 확인할 수 없는 경우와 같이 Pauli 연산자의 eigenstate가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-151">For example, $\ket{\psi} = (\ket{0} + e^{i \pi / 8} \ket{1}) / \sqrt{2}$ is not an eigenstate of any Pauli operator, such that we cannot use <xref:microsoft.quantum.intrinsic.assertprob> to uniquely determine that a state $\ket{\psi'}$ is equal to $\ket{\psi}$.</span></span>
<span data-ttu-id="0e362-152">대신, 시뮬레이터에서 지 원하는 기본 형식을 사용 하 여 직접 테스트할 수 있는 가정으로 assertion $ \ket{\psi '} = \ket{\psi} $를 분해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-152">Instead, we must decompose the assertion $\ket{\psi'} = \ket{\psi}$ into assumptions that can be directly tested using  the primitives supported by our simulator.</span></span>
<span data-ttu-id="0e362-153">이렇게 하려면 $ \ket{\psi} = \alpha \ket{0} + \alpha \ket{1}$ 복소수에 대해 $ \alpha = a\_r + a\_i i $ 및 $ \alpha $를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-153">To do so, let $\ket{\psi} = \alpha \ket{0} + \beta \ket{1}$ for complex numbers $\alpha = a\_r + a\_i i$ and $\beta$.</span></span>
<span data-ttu-id="0e362-154">이 식에는 각 복소수를 실수와 허수부의 합계로 표현할 수 있으므로 $\{\_r, a\_i, b\_r, b\_i\}$ 네 개의 실수 숫자가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-154">Note that this expression requires four real numbers $\{a\_r, a\_i, b\_r, b\_i\}$ to specify, as each complex number can be expressed as the sum of a real and imaginary part.</span></span>
<span data-ttu-id="0e362-155">그러나 글로벌 단계 때문에 $a\_i = $0를 선택할 수 있습니다. 예를 들어, 단일가 나 비트 상태를 고유 하 게 지정 하기 위해 세 가지 실수만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-155">Due to the global phase, however, we can choose $a\_i = 0$, such that we only need three real numbers to uniquely specify a single-qubit state.</span></span>

<span data-ttu-id="0e362-156">따라서 필요한 상태를 어설션할 수 있도록 서로 독립적인 세 가지 어설션을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-156">Thus, we need to specify three assertions which are independent of each other in order to assert the state that we expect.</span></span>
<span data-ttu-id="0e362-157">이를 위해 $ \alpha $ 및 $ \alpha $를 지정 하 고 각각을 독립적으로 어설션하는 각 Pauli에 대 한 `Zero` 관찰 확률을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-157">We do so by finding the probability of observing `Zero` for each Pauli measurement given $\alpha$ and $\beta$, and asserting each independently.</span></span>
<span data-ttu-id="0e362-158">$X $, $y $ 및 $z $를 각각 Pauli $X $, $Y $ 및 $Z $ 측정값에 대 한 `Result` 값으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-158">Let $x$, $y$, and $z$ be `Result` values for Pauli $X$, $Y$, and $Z$ measurements respectively.</span></span>
<span data-ttu-id="0e362-159">그런 다음 퀀텀 측정값에 대 한 유사도 함수를 사용 하 여 \begin{align} \Pr (x = \texttt{Zero} | \pr, \pr) & = \frac12 + a\_r b\_r + a\_i b\_\\\\ \Pr (y = \texttt{Zero} | \pr, \pr) & = \frac12 + a\_r b\_i-a\_i b\_r \\\\ \Pr (z = \texttt{Zero} | \pr, \pr) & = \frac12\left (1 + a\_r ^ 2 + a\_i ^ 2 + b\_r ^ 2 + b\_i ^ 2 \right).</span><span class="sxs-lookup"><span data-stu-id="0e362-159">Then, using the likelihood function for quantum measurements, \begin{align} \Pr(x = \texttt{Zero} | \alpha, \beta) & = \frac12 + a\_r b\_r + a\_i b\_i \\\\ \Pr(y = \texttt{Zero} | \alpha, \beta) & = \frac12 + a\_r b\_i - a\_i b\_r \\\\ \Pr(z = \texttt{Zero} | \alpha, \beta) & = \frac12\left( 1 + a\_r^2 + a\_i^2 + b\_r^2 + b\_i^2 \right).</span></span>
<span data-ttu-id="0e362-160">\end{align}</span><span class="sxs-lookup"><span data-stu-id="0e362-160">\end{align}</span></span>

<span data-ttu-id="0e362-161"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> 작업에서는 $ \alpha $ 및 $ \alpha $의 지정 된 표현이 <xref:microsoft.quantum.math.complex>형식의 값으로 지정 된 이러한 어설션을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-161">The <xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> operation implements these assertions given representations of $\alpha$ and $\beta$ as values of type <xref:microsoft.quantum.math.complex>.</span></span>
<span data-ttu-id="0e362-162">이는 예상 상태를 수학적으로 계산할 수 있는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-162">This is helpful when the expected state can be computed mathematically.</span></span>

### <a name="asserting-equality-of-quantum-operations"></a><span data-ttu-id="0e362-163">퀀텀 작업의 같음 어설션</span><span class="sxs-lookup"><span data-stu-id="0e362-163">Asserting Equality of Quantum Operations</span></span> ###

<span data-ttu-id="0e362-164">지금까지 특정 상태를 준비 하기 위한 테스트 작업과 관련 하 여 노력 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-164">Thus far, we have been concerned with testing operations which are intended to prepare particular states.</span></span>
<span data-ttu-id="0e362-165">그러나 종종 단일 고정 입력이 아닌 임의의 입력에 대해 작업을 수행 하는 방법에 관심이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-165">Often, however, we are interested in how an operation acts for arbitrary inputs rather than for a single fixed input.</span></span>
<span data-ttu-id="0e362-166">예를 들어 일련의 단일 연산자 $U (t) $에 해당 하는 작업 `U : ((Double, Qubit[]) => () : Adjoint)`를 구현 했으며 `adjoint auto`를 사용 하는 대신 명시적인 `adjoint` 블록을 제공 했다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-166">For example, suppose we have implemented an operation `U : ((Double, Qubit[]) => () : Adjoint)` corresponding to a family of unitary operators $U(t)$, and have provided an explicit `adjoint` block instead of using `adjoint auto`.</span></span>
<span data-ttu-id="0e362-167">$T $가 진화 시간을 나타내는 경우 예상 대로 ^ \aa&gt (t) = U (-t) $ $U를 어설션하는 데 관심이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-167">We may be interested in asserting that $U^\dagger(t) = U(-t)$, as expected if $t$ represents an evolution time.</span></span>

<span data-ttu-id="0e362-168">두 가지 작업을 `U` 하 고 `V` 동일 하 게 작동 하는 어설션을 만들기 위해 수행할 수 있는 두 가지 전략이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-168">Broadly speaking, there are two different strategies that we can follow in making the assertion that two operations `U` and `V` act identically.</span></span>
<span data-ttu-id="0e362-169">첫째, `U(target); (Adjoint V)(target);`이 지정 된 기준으로 각 상태를 유지 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-169">First, we can check that `U(target); (Adjoint V)(target);` preserves each state in a given basis.</span></span>
<span data-ttu-id="0e362-170">둘째, entangled의 절반에 대해 작동 하는 `U(target); (Adjoint V)(target);`이 해당을 유지 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-170">Second, we can check that `U(target); (Adjoint V)(target);` acting on half of an entangled state preserves that entanglement.</span></span>
<span data-ttu-id="0e362-171">이러한 전략은 각각 라고 작업 <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> 및 <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced>에 의해 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-171">These strategies are implemented by the canon operations <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> and <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced>, respectively.</span></span>

> [!NOTE]
> <span data-ttu-id="0e362-172">위에 설명 된 참조 어설션은 $2n $ Choi – $ Jamiłkowski isomorphism에 대 한 $n 작업을 연결 하는 수학적 프레임 워크인 [–](https://en.wikipedia.org/wiki/Channel-state_duality)을 기반으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-172">The referenced assertion discussed above works based on the [Choi–Jamiłkowski isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality), a mathematical framework which relates operations on $n$ qubits to entangled states on $2n$ qubits.</span></span>
> <span data-ttu-id="0e362-173">특히 $ \ket{\ beta_의 ${00}} \mathrel{: =} (\ket{00} + \ket{11})/\sqrt{2}$를 $n $에 $n 대 한 id 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-173">In particular, the identity operation on $n$ qubits is represented by $n$ copies of the entangled state $\ket{\beta_{00}} \mathrel{:=} (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span>
> <span data-ttu-id="0e362-174">작업 <xref:microsoft.quantum.preparation.preparechoistate>이 isomorphism를 구현 하 여 지정 된 작업을 나타내는 상태를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-174">The operation <xref:microsoft.quantum.preparation.preparechoistate> implements this isomorphism, preparing a state that represents a given operation.</span></span>

<span data-ttu-id="0e362-175">대략 이러한 전략은 시간 공간 균형에 따라 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-175">Roughly, these strategies are distinguished by a time–space tradeoff.</span></span>
<span data-ttu-id="0e362-176">각 입력 상태를 반복 하는 데는 추가 시간이 소요 되지만 되거나 얽 히를 참조로 사용 하는 경우 추가 추가 비트를 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-176">Iterating through each input state takes additional time, while using entanglement as a reference requires storing additional qubits.</span></span>
<span data-ttu-id="0e362-177">작업에서 해독 가능한 클래식 작업을 구현 하는 경우 (계산 기준 상태에만 관심이 있음)이 제한 된 입력 집합에 대 한 같음 테스트를 <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-177">In cases where an operation implements a reversible classical operation, such that we are only interested in its behavior on computational basis states, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> tests equality on this restricted set of inputs.</span></span>

> [!TIP]
> <span data-ttu-id="0e362-178">입력 상태 반복은 열거형 작업 <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> 및 <xref:microsoft.quantum.canon.iteratethroughcartesianpower>에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-178">The iteration over input states is handled by the enumeration operations <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> and <xref:microsoft.quantum.canon.iteratethroughcartesianpower>.</span></span>
> <span data-ttu-id="0e362-179">이러한 작업은 일반적으로 두 개 이상의 집합 사이에 있는 카티션 product의 각 요소에 작업을 적용 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-179">These operations are useful more generally for applying an operation to each element of the Cartesian product between two or more sets.</span></span>

<span data-ttu-id="0e362-180">그러나 두 가지 접근 방식은 검사 중인 작업의 다른 속성을 테스트 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-180">More critically, however, the two approaches test different properties of the operations under examination.</span></span>
<span data-ttu-id="0e362-181">내부 어설션은 각 작업을 여러 번 호출 하므로 입력 상태 마다 한 번씩 임의의 선택 및 측정 결과가 호출 사이에서 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-181">Since the in-place assertion calls each operation multiple times, once for each input state, any random choices and measurement results might change between calls.</span></span>
<span data-ttu-id="0e362-182">이와 대조적으로 참조 된 어설션은 각 작업을 정확히 한 번 호출 하 여 *단일 샷에*작업이 동일한 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-182">By contrast, the referenced assertion calls each operation exactly once, such that it checks that the operations are equal *in a single shot*.</span></span>
<span data-ttu-id="0e362-183">이러한 테스트는 모두 퀀텀 프로그램의 정확성을 보장 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e362-183">Both of these tests are useful in ensuring the correctness of quantum programs.</span></span>


## <a name="further-reading"></a><span data-ttu-id="0e362-184">추가 참고 자료</span><span class="sxs-lookup"><span data-stu-id="0e362-184">Further Reading</span></span> ##

- <xref:microsoft.quantum.techniques.testing-and-debugging>
- <xref:microsoft.quantum.diagnostics>
