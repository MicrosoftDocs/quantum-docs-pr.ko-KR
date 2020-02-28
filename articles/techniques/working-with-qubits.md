---
title: 이상 비트 작업
description: 기능을 할당 하 고, 작업 및 함수에서 사용 하 고, 결과를 측정 하는 방법에 대해 알아봅니다.
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 1aa2432996dda61d099e3b5bb4db78379ce43d97
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907650"
---
# <a name="working-with-qubits"></a><span data-ttu-id="921f9-103">이상 비트 작업</span><span class="sxs-lookup"><span data-stu-id="921f9-103">Working with Qubits</span></span>

<span data-ttu-id="921f9-104">이제는 Q # 언어의 다양 한 부분을 살펴보았습니다 .이를 통해 더 많은 부분을 소개 하 고,이를 사용 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="921f9-105">비트 할당</span><span class="sxs-lookup"><span data-stu-id="921f9-105">Allocating Qubits</span></span>

<span data-ttu-id="921f9-106">첫째, Q #에서 사용할 수 있는 이상 비트를 얻기 위해 `using` 블록 내에서 다음과 같은 작업을 *할당* 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="921f9-107">이 방법으로 할당 된 모든 모든 비트는 $ \ket{0}$ state;에서 시작 됩니다. 위의 예에서는 `register`가 $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cst\otimes \ket{0}$ 상태에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="921f9-108">`using` 블록의 끝에서 해당 블록에 의해 할당 된 모든 요소는 즉시 할당 취소 되며 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="921f9-109">대상 컴퓨터는 할당을 위해 다른 `using` 블록으로 다시 사용 하 고 제공할 수 있도록 \ket가 할당 취소 바로 앞에 ${0}$ 상태에 있을 것으로 간주 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="921f9-110">가능 하면 항상 단일 작업을 사용 하 여 할당 된 모든 비트를 $ \ket{0}$로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="921f9-111">이 필요한 경우에는 @"microsoft.quantum.intrinsic.reset" 작업을 사용 하 여 대신 원하는 비트를 측정 하 고 해당 측정 결과를 사용 하 여 측정 된 값이 $ \ket{0}$로 반환 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="921f9-112">이러한 측정값을 사용 하면 잔여 비트를 사용 하 여 되거나 얽 히를 소멸 시킬 수 있으므로 계산에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="921f9-113">내장 작업</span><span class="sxs-lookup"><span data-stu-id="921f9-113">Intrinsic Operations</span></span>

<span data-ttu-id="921f9-114">할당 된 후에는 함수 및 작업에 이상 비트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="921f9-115">어떤 경우에는이 작업을 수행할 수 있는 작업은 모두 작업으로 정의 되므로 Q # 프로그램은이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="921f9-116">이러한 작업은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서 더 자세히 볼 수 있지만 지금은이 작업에 대 한 몇 가지 유용한 작업을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="921f9-117">첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 Q #에서 각각 `Y`형식의 내장 작업 `X`, `Z`및 `(Qubit => Unit is Adj + Ctl)`로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="921f9-118">[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 대로 $X $ 등의 `X`를 비트 대칭 작업으로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="921f9-119">`X` 작업을 사용 하면 일부 클래식 비트 문자열 $s $에 대해 $ \ket{s_0 s_1 \dots . s_n} $ 형식의 상태를 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-119">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="921f9-120">나중에이 작업을 작성 하는 보다 간단한 방법으로 수동 흐름 제어를 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="921f9-121">\Ket transform{0} $를 사용 하 여 $ \ket{+} = \left (\ket{0} + \ket{1}\left)/\left{2}$ 및 $ \ket{-} = \left (\ket{1}-Hadamard{2}\left)/\left $H $와 같은 상태를 준비할 수도 있습니다.`H : (Qubit => Unit is Adj + Ctl)`</span><span class="sxs-lookup"><span data-stu-id="921f9-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="921f9-122">측정값</span><span class="sxs-lookup"><span data-stu-id="921f9-122">Measurements</span></span>

<span data-ttu-id="921f9-123">기본 제공 되는 기본 제공 비 작업 인 `Measure` 작업을 사용 하 여 `Qubit` 형식의 개체에서 기존 정보를 추출 하 고, 예약 된 형식 `Result`를 포함 하는 기존 값을 결과에 할당할 수 있습니다 .이는 결과가 더 이상 퀀텀 상태가 아님을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-123">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="921f9-124">`Measure`에 대 한 입력은 `Pauli` 형식의 값 (예 `PauliX`) 및 `Qubit`형식의 값으로 표현 되는 Bloch 구의 Pauli 축입니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="921f9-125">간단한 예는 $ \ket{0}$ 상태에서 하나 비트를 할당 한 다음 Hadamard 연산을 `H` 적용 하 고 결과를 `PauliZ` 기준으로 측정 하는 다음 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-125">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="921f9-126">약간 더 복잡 한 예는 다음 연산에서 제공 됩니다 .이 경우에는 `Qubit[]` 형식의 레지스터에 있는 모든 값이 지정 된 Pain으로 측정 될 때 `true` 상태이 고, 그렇지 않은 경우 `false`를 반환 하는 경우 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-126">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

<span data-ttu-id="921f9-127">Q # 언어를 사용 하면 기존 제어 흐름을 사용 하 여 다양 한 비트 측정 결과에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-127">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="921f9-128">이 기능을 사용 하면 unitaries을 구현 하기 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-128">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="921f9-129">예를 들어 Q #에서 쉽게 구현할 수 있습니다 (RUS ( *-성공-성공* ) 패턴 이라고 함).</span><span class="sxs-lookup"><span data-stu-id="921f9-129">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="921f9-130">이러한 RUS 패턴은 기본 게이트 측면에서 비용이 *저렴 한* 확률 프로그램 이지만 실제 실행 및 가능한 여러 가지 branchings의 실제 인터리브에 따라 실질적인 비용이 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-130">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="921f9-131">반복-성공 (RUS) 패턴을 용이 하 게 하기 위해 Q #에서 구문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-131">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

<span data-ttu-id="921f9-132">여기서 `statementBlock1` 및 `statementBlock2`은 0 개 이상의 Q # 문이 고 `Bool`형식의 값으로 계산 되는 유효한 식을 `expression` 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-132">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="921f9-133">일반적인 사용 사례에서 다음 Q # 연산은 Bloch 구의 $ (I + 2i Z)/\sqrt{5}$ 인 무리 축을 중심으로 회전을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-133">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="921f9-134">이 작업은 알려진 RUS 패턴을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-134">This is accomplished by using a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

<span data-ttu-id="921f9-135">이 예에서는 전체 반복 전-픽스업 루프의 범위에 있고 루프에서 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수 `finished`를 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-135">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="921f9-136">마지막으로, $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $를 준비 하는 RUS 패턴의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-136">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="921f9-137">[표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)도 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="921f9-137">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="921f9-138">이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 퀀텀 작업을 포함 하는 루프의 좀 더 복잡 한 `fixup` 부분으로, `AssertProb` 문을 사용 하 여 프로그램의 지정 된 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="921f9-138">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="921f9-139">또한 [`Assert`](xref:microsoft.quantum.intrinsic.assert) 및 [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) 작업에 대 한 자세한 내용은 [테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="921f9-139">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>
