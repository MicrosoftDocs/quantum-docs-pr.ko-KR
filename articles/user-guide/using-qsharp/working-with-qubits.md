---
title: 큐비트 사용
description: 채우기 설명
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: e89b9ccfe2a0796e01eedfc99f7ce71038d85f38
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430937"
---
# <a name="working-with-qubits"></a><span data-ttu-id="00b18-103">큐비트 사용</span><span class="sxs-lookup"><span data-stu-id="00b18-103">Working with qubits</span></span>

<span data-ttu-id="00b18-104">이제는 Q # 언어의 다양 한 부분을 살펴보았습니다 .이를 통해 더 많은 부분을 소개 하 고,이를 사용 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

<span data-ttu-id="00b18-105">이러한 문은 함수 본문 내에서 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-105">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="00b18-106">작업 내 에서만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-106">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="00b18-107">비트 할당</span><span class="sxs-lookup"><span data-stu-id="00b18-107">Allocating Qubits</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="00b18-108">정리 비트</span><span class="sxs-lookup"><span data-stu-id="00b18-108">Clean qubits</span></span>

<span data-ttu-id="00b18-109">`using`문은 문 블록 중에 사용할 새 요소를 *할당* 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-109">The `using` statement is used to *allocate* new qubits for use during a statement block.</span></span>

<span data-ttu-id="00b18-110">문은 키워드로 구성 되 고, 여는 `using` 괄호 `(` , 바인딩, 닫는 괄호 `)` 및 계산 된 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-110">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="00b18-111">바인딩은 문과 동일한 패턴을 따릅니다 `let` . 단일 기호 또는 기호 튜플, 등호 `=` , 단일 값 또는 *이니셜라이저의*일치 하는 튜플 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-111">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="00b18-112">이니셜라이저는로 표시 된 단일의 비트 또는의 배열 ( `Qubit()` `Qubit[n]` 여기서 `n` 는 `Int` 식)으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-112">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="00b18-113">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-113">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="00b18-114">위의 예에서 $ \ket $ state;에 할당 된 것 처럼이 방법으로 할당 된 모든 {0} `register` 것은 $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cst\otimes \ket $ 상태에 {0} 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-114">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="00b18-115">블록의 끝에서 `using` 해당 블록에 의해 할당 된 모든 요소는 즉시 할당 취소 되며 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-115">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="00b18-116">대상 컴퓨터는 {0} 할당을 위해 다른 블록으로 다시 사용 하 고 제공할 수 있도록 해당 사용자가 할당 취소 직전에 $ \ket $ 상태에 있는 것으로 간주 `using` 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-116">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="00b18-117">가능 하면 항상 단일 작업을 사용 하 여 할당 된 모든 비트를 $ \ket $로 반환 {0} 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-117">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="00b18-118">필요한 경우 작업을 사용 하 여 @"microsoft.quantum.intrinsic.reset" 대신 원하는 비트를 측정 하 고 해당 측정 결과를 사용 하 여 측정 된 값이 $ \ket $로 반환 되도록 할 수 있습니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="00b18-118">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="00b18-119">이러한 측정값을 사용 하면 잔여 비트를 사용 하 여 되거나 얽 히를 소멸 시킬 수 있으므로 계산에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-119">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="00b18-120">빌려의 비트</span><span class="sxs-lookup"><span data-stu-id="00b18-120">Borrowed Qubits</span></span>

<span data-ttu-id="00b18-121">`borrowing`문을 사용 하 여 특정 상태에 있지 않아도 되는 임시 사용에 대 한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-121">The `borrowing` statement is used to make qubits available for temporary use, which do not need be in a specific state.</span></span>

<span data-ttu-id="00b18-122">Borrowing 메커니즘을 사용 하면 계산 중에 스크래치 공간으로 사용할 수 있는 원하는 비트를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-122">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span>
<span data-ttu-id="00b18-123">이러한 기능은 일반적으로 깨끗 한 상태가 아닙니다. 즉, $ \ket $와 같은 알려진 상태로 반드시 초기화 되는 것은 아닙니다. {0}</span><span class="sxs-lookup"><span data-stu-id="00b18-123">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="00b18-124">이러한 경우는 상태를 알 수 없으며 퀀텀 컴퓨터 메모리의 다른 부분과 함께 사용할 수 있기 때문에이를 "더티" 이상으로 지칭 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-124">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="00b18-125">바인딩은 문에 있는 것과 동일한 패턴 및 규칙을 따릅니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="00b18-125">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>
<span data-ttu-id="00b18-126">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-126">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="00b18-127">인 중 한 비트는 알 수 없는 상태 이며 문 블록의 끝에 있는 범위를 벗어났습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-127">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="00b18-128">대출자는가 중에 있던 상태와 동일한 상태를 유지 하도록 커밋 합니다. 즉, 문 블록의 시작과 끝에 있는 상태는 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-128">The borrower commits to leaving the qubits in the same state they were in when they were borrowed,  i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="00b18-129">특히 borrowing 범위에는 측정값이 포함 되지 않아야 하는 일반적인 상태가 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-129">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="00b18-130">Borrowing를 사용 하는 경우 시스템은 먼저 사용 중이 고 문의 본문 중에는 액세스 하지 않는 대신에 요청을 채우려고 시도 `borrowing` 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-130">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="00b18-131">이러한 것이 충분 하지 않은 경우 요청을 완료 하기 위해 새 비트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-131">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>


<span data-ttu-id="00b18-132">더티 비트의 알려진 사용 사례 중에는 incrementers의 구현이 매우 거의 필요 하지 않은 다중 제어 CNOT 게이트의 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-132">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="00b18-133">Q #에서의 사용 [예를 확인](#borrowing-qubits-example) 하거나, [*2n + 2를 사용 하 여 Toffoli 기반 모듈식 곱하기*](https://arxiv.org/abs/1611.07995) (Haner, RoetBorrowing er 및 svs2017)를 사용 하는 백서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00b18-133">See the [Borrowing Qubits Example](#borrowing-qubits-example) below to see an example of their use in Q#, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>


## <a name="intrinsic-operations"></a><span data-ttu-id="00b18-134">내장 작업</span><span class="sxs-lookup"><span data-stu-id="00b18-134">Intrinsic Operations</span></span>

<span data-ttu-id="00b18-135">할당 된 후에는 함수 및 작업에 이상 비트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-135">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="00b18-136">어떤 경우에는이 작업을 수행할 수 있는 작업은 모두 작업으로 정의 되므로 Q # 프로그램은이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-136">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="00b18-137">이러한 작업은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서 더 자세히 볼 수 있지만 지금은이 작업에 대 한 몇 가지 유용한 작업을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-137">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="00b18-138">첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 Q #에서 `X` `Y` `Z` 각각 형식이 있는 내장 작업, 및로 표시 됩니다 `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="00b18-138">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="00b18-139">[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 것 처럼, $X $ 등의 작업을 수행 하는 것으로 간주할 수 있습니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="00b18-139">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="00b18-140">`X`작업을 사용 하면 몇 가지 기존 비트 문자열 $s $에 대해 $ \ket{s_0 s_1 \dots .. s_n} $ 형식의 상태를 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-140">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="00b18-141">나중에이 작업을 작성 하는 보다 간단한 방법으로 수동 흐름 제어를 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-141">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="00b18-142">\Ket transform $H $를 사용 하 여 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left $ {2} 및 $ \ket {-} = \left (\ket-Hadamard \left)/\left $와 같은 상태를 준비할 수도 있습니다 {0} {1} {2} .이는 내장 작업으로 Q #에서 표시 됩니다 `H : (Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="00b18-142">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="00b18-143">측정</span><span class="sxs-lookup"><span data-stu-id="00b18-143">Measurements</span></span>

<span data-ttu-id="00b18-144">`Measure`기본 제공 되는 기본이 아닌 작업 인 작업을 사용 하 여 형식의 개체에서 기존 정보를 추출 하 고, 결과는 `Qubit` `Result` 더 이상 퀀텀 상태가 아님을 나타내는 예약 된 형식을 포함 하는 기존 값을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-144">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="00b18-145">에 대 한 입력은 `Measure` 형식 `Pauli` (예의 경우 `PauliX` ) 및 형식의 값으로 표현 되는 Bloch 구의 pauli 축입니다 `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="00b18-145">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="00b18-146">간단한 예는 $ \ket $ 상태에서 1 개의 한 비트를 할당 하 {0} 고, Hadamard 작업을 적용 하 고, 결과를 측정 하는 다음 작업입니다 `H` `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="00b18-146">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

<span data-ttu-id="00b18-147">조금 더 복잡 한 예는 다음 연산에서 제공 됩니다 .이 경우에는 `true` 레지스터의 모든 모든 비트가 `Qubit[]` 지정 된 pai로 측정 될 때 0 상태에 있는 경우 부울 값을 반환 하 고, 그렇지 않으면를 반환 `false` 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-147">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

## <a name="borrowing-qubits-example"></a><span data-ttu-id="00b18-148">Borrowing  Bits 예제</span><span class="sxs-lookup"><span data-stu-id="00b18-148">Borrowing Qubits Example</span></span>

<span data-ttu-id="00b18-149">에는 아래 정의 된 함수와 같이 키워드를 사용 하는 예제가 있습니다 `borrowing` `MultiControlledXBorrow` .</span><span class="sxs-lookup"><span data-stu-id="00b18-149">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="00b18-150">가 `controls` 작업에 추가 해야 하는 컨트롤의 비트를 나타내는 경우 `X` `Length(controls)-2` 이 구현에서 많은 더티 ancillas의 전체를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-150">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

<span data-ttu-id="00b18-151">`With`조합 기---는 adjoint를 지 원하는 작업 (예:---)에 적용할 수 있는 형식으로 되어 있습니다. `WithA`</span><span class="sxs-lookup"><span data-stu-id="00b18-151">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example.</span></span>
<span data-ttu-id="00b18-152">이는를 포함 하는 구조에 컨트롤을 추가 하 `With` 는 작업을 내부 작업에만 전파 하므로 좋은 프로그래밍 스타일입니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-152">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="00b18-153">또한 여기에서는 작업의에 대 한 추가 작업을 수행 하는 `body` `controlled` 대신 작업 본문의 구현이 명시적으로 제공 되었습니다 `controlled auto` .</span><span class="sxs-lookup"><span data-stu-id="00b18-153">Further, note that here in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="00b18-154">이에 대 한 이유는의 각 및 모든 개별 게이트에 컨트롤을 추가 하는 것과 비교 하 여 유용한 추가 컨트롤을 쉽게 추가 하는 방법에 대 한 것입니다 `body` .</span><span class="sxs-lookup"><span data-stu-id="00b18-154">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="00b18-155">그러나이 코드는 곱하기 제어 작업을 구현 하는 것과 동일한 목표를 달성 하는 다른 라고 함수와 비교 하는 것이 좋습니다 .이는 `MultiControlledXClean` `X` 메커니즘을 사용 하 여 여러 가지 깨끗 한 비트를 사용 합니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="00b18-155">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="whats-next"></a><span data-ttu-id="00b18-156">다음 단계</span><span class="sxs-lookup"><span data-stu-id="00b18-156">What's Next?</span></span>
<span data-ttu-id="00b18-157">Q #의 [제어 흐름](xref:microsoft.quantum.guide.controlflow) 에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="00b18-157">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>