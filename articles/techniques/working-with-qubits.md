---
title: 이상 비트 사용 | Microsoft Docs
description: 이상 비트 작업
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 477b358c3eba58b62926b4e9094770c9741cac92
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864256"
---
# <a name="working-with-qubits"></a><span data-ttu-id="0fed5-103">이상 비트 작업</span><span class="sxs-lookup"><span data-stu-id="0fed5-103">Working with Qubits</span></span> #

<span data-ttu-id="0fed5-104">이제는 Q # 언어의 다양 한 부분을 살펴보았습니다 .이를 통해 더 많은 부분을 소개 하 고,이를 사용 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="0fed5-105">비트 할당</span><span class="sxs-lookup"><span data-stu-id="0fed5-105">Allocating Qubits</span></span> ##

<span data-ttu-id="0fed5-106">첫째, Q #에서 사용할 수 있는 이상 비트를 얻기 위해 `using` 블록 내에서 다음과 같은 작업을 *할당* 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="0fed5-107">이 방법으로 할당 된 모든 모든 비트는 $ \ket{0}$ state;에서 시작 됩니다. 위의 예에서는 `register`가 $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cst\otimes \ket{0}$ 상태에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="0fed5-108">`using` 블록의 끝에서 해당 블록에 의해 할당 된 모든 요소는 즉시 할당 취소 되며 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="0fed5-109">대상 컴퓨터는 할당을 위해 다른 `using` 블록으로 다시 사용 하 고 제공할 수 있도록 \ket가 할당 취소 바로 앞에 ${0}$ 상태에 있을 것으로 간주 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="0fed5-110">가능 하면 항상 단일 작업을 사용 하 여 할당 된 모든 비트를 $ \ket{0}$로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="0fed5-111">이 필요한 경우에는 @"microsoft.quantum.intrinsic.reset" 작업을 사용 하 여 대신 원하는 비트를 측정 하 고 해당 측정 결과를 사용 하 여 측정 된 값이 $ \ket{0}$로 반환 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="0fed5-112">이러한 측정값을 사용 하면 잔여 비트를 사용 하 여 되거나 얽 히를 소멸 시킬 수 있으므로 계산에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span> 

## <a name="intrinsic-operations"></a><span data-ttu-id="0fed5-113">내장 작업</span><span class="sxs-lookup"><span data-stu-id="0fed5-113">Intrinsic Operations</span></span> ##

<span data-ttu-id="0fed5-114">할당 된 후에는 함수 및 작업에 이상 비트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="0fed5-115">어떤 경우에는이 작업을 수행할 수 있는 작업은 모두 작업으로 정의 되므로 Q # 프로그램은이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="0fed5-116">이러한 작업은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서 더 자세히 볼 수 있지만 지금은이 작업에 대 한 몇 가지 유용한 작업을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="0fed5-117">첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 Q #에서 각각 `Y`형식의 내장 작업 `X`, `Z`및 `(Qubit => Unit is Adj + Ctl)`로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="0fed5-118">[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 대로 $X $ 등의 `X`를 비트 대칭 작업으로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="0fed5-119">이를 통해 일부 기존 비트 문자열 $s $에 대해 $ \ket{s_0 s_1 \dots . s_n} $ 형식의 상태를 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-119">This lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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

operation Example() : Unit {

    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
    }
}
```

> [!TIP]
> <span data-ttu-id="0fed5-120">나중에이 작업을 작성 하는 보다 간단한 방법으로 수동 흐름 제어를 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="0fed5-121">\Ket transform{0} $를 사용 하 여 $ \ket{+} = \left (\ket{0} + \ket{1}\left)/\left{2}$ 및 $ \ket{-} = \left (\ket{1}-Hadamard{2}\left)/\left $H $와 같은 상태를 준비할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="0fed5-122">측정값</span><span class="sxs-lookup"><span data-stu-id="0fed5-122">Measurements</span></span> ##

<span data-ttu-id="0fed5-123">기본 제공 되는 내장 형식이 아닌 작업 인 `Measure` 작업을 사용 하 여 `Qubit` 형식의 개체에서 클래식 정보를 추출 하 고 `Result`예약 된 형식이 포함 된 기존 값을 할당 하 여 결과가 더 이상 퀀텀 상태가 아님을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-123">Using the `Measure` operation, which is a built in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span> <span data-ttu-id="0fed5-124">`Measure`에 대 한 입력은 `Pauli` 형식의 개체 (예: `PauliX`) 및 `Qubit`형식의 개체에 의해 표현 되는 Bloch 구의 Pauli 축입니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by an object of type `Pauli` (i.e., for instance `PauliX`) and an object of type `Qubit`.</span></span> 

<span data-ttu-id="0fed5-125">간단한 예는 $ \ket{0}$ 상태에서 하나 비트를 만든 다음 Hadamard gate ``H``를 적용 한 다음 `PauliZ` 기준으로 결과를 측정 하는 다음 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-125">A simple example is the following operation which creates one qubit in the $\ket{0}$ state, then applies a Hadamard gate ``H`` to it and then measures the result in the `PauliZ` basis.</span></span> 

```qsharp
operation MeasurementOneQubit () : Result {

    // The following using block creates a fresh qubit and initializes it 
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby creating the 
        // state 1/sqrt(2)(|0〉+|1〉). 
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

<span data-ttu-id="0fed5-126">약간 더 복잡 한 예는 다음 연산에 의해 지정 됩니다 .이는 지정 된 형식으로 측정 될 때 `Qubit[]` 형식 레지스터의 모든 값이 0 인 경우 `true` 부울 값을 반환 하 고 그렇지 않으면 `false` 하는 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-126">A slightly more complicated example is given by the following operation which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero, when measured in a specified Pauli basis and `false` otherwise.</span></span> 

```qsharp
operation AllMeasurementsZero (qs : Qubit[], pauli : Pauli) : Bool {

    mutable value = true;
    for (q in qs) {
        if ( Measure([pauli], [q]) == One ) {
            set value = false;
        }
    }
    return value;
}
```

<span data-ttu-id="0fed5-127">Q # 언어를 사용 하면 기존 제어 흐름에 대 한 종속성을 사용 하 여 값을 측정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-127">The Q# language allows dependencies of classical control flow on measurement results of qubits.</span></span> <span data-ttu-id="0fed5-128">이를 통해에서는 unitaries 구현을 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-128">This in turn enables to implement powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span> <span data-ttu-id="0fed5-129">예를 들어, Q #의 *반복* 을 구현 하는 것은 간단 합니다. Q #의 경우에는 기본 게이트를 기준으로 낮은 비용을 *예상* 하는 확률 회로 이지만 실제 실행 및 가능한 여러 가지 branchings의 실제 인터리브에 따라 실질적인 비용이 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-129">As an example, it is easy to implement so-called *Repeat-Until-Success* in Q# which are probabilistic circuits that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span> 

<span data-ttu-id="0fed5-130">반복-성공 (RUS) 패턴을 용이 하 게 하기 위해 Q #에서 구문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-130">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>
```qsharp
repeat {
    statementBlock1 
}
until (expression)
fixup {
    statementBlock2
}
```
<span data-ttu-id="0fed5-131">여기서 `statementBlock1` 및 `statementBlock2`은 0 개 이상의 Q # 문이 고 `Bool`형식의 값으로 계산 되는 유효한 식을 `expression` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-131">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span> <span data-ttu-id="0fed5-132">일반적인 사용 사례에서 다음 회로는 Bloch 구의 $ (I + 2i Z)/\sqrt{5}$의 무리 축을 중심으로 회전을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-132">In a typical use case, the following circuit implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="0fed5-133">이 작업은 알려진 RUS 패턴을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-133">This is accomplished by using a known RUS pattern:</span></span> 

```qsharp
operation RUScircuit (qubit : Qubit) : Unit {

    using(ancillas = Qubit[2]) {
        ApplyToEachA(H, ancillas);
        mutable finished = false;
        repeat {
            Controlled X(ancillas, qubit);
            S(qubit);
            Controlled X(ancillas, qubit);
            Z(qubit);
        }
        until(finished)
        fixup {
            if AllMeasurementsZero(ancillas, Xpauli) {
                set finished = true;
            }
        }
    }
}
```

<span data-ttu-id="0fed5-134">이 예에서는 전체 반복 전-픽스업 루프의 범위에 있고 루프에서 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수 `finished`를 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-134">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="0fed5-135">마지막으로, $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $를 준비 하는 RUS 패턴의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-135">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span> <span data-ttu-id="0fed5-136">[표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)도 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0fed5-136">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span> 

```qsharp
operation RepeatUntilSuccessStatePreparation( target : Qubit ) : Unit {

    using( ancilla = Qubit() ) {
        H(ancilla);
        repeat {
            // We expect target and ancilla qubit to be in |+⟩ state.
            AssertProb( 
                [PauliX], [target], Zero, 1.0, 
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb( 
                [PauliX], [ancilla], Zero, 1.0,
                "ancilla qubit should be in the |+⟩ state", 1e-10 );
                
            Adjoint T(ancilla);
            CNOT(target, ancilla);
            T(ancilla);

            // The probability of measuring |+⟩ state on ancilla is 3/4.
            AssertProb( 
                [PauliX], [ancilla], Zero, 3. / 4., 
                "Error: the probability to measure |+⟩ in the first 
                ancilla must be 3/4",
                1e-10);

            // If we get measurement outcome Zero, we prepare the required state 
            let outcome = Measure([PauliX], [ancilla]);
        }
        until( outcome == Zero )
        fixup {
            // Bring ancilla and target back to |+⟩ state
            if( outcome == One ) {
                Z(ancilla);
                X(target);
                H(target);
            }
        }
        // Return ancilla back to Zero state
        H(ancilla);
    }
}
```
 
<span data-ttu-id="0fed5-137">이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 퀀텀 작업과 관련 된 루프의 더 복잡 한 `fixup` 부분으로, `AssertProb` 문을 사용 하 여 프로그램의 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fed5-137">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span> <span data-ttu-id="0fed5-138">`Assert` 및 `AssertProb` 문에 대 한 자세한 내용은 [테스트 및 디버깅](xref:microsoft.quantum.techniques.testing-and-debugging) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0fed5-138">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about `Assert` and `AssertProb` statements.</span></span> 
