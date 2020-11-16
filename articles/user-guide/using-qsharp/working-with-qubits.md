---
title: 큐비트 사용
description: '에서의 작업에 대해 알아보기 Q#'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 9a3d7e03016332a04ac9d1610428b6fcd546d1f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691582"
---
# <a name="working-with-qubits"></a><span data-ttu-id="fb5e2-103">큐비트 사용</span><span class="sxs-lookup"><span data-stu-id="fb5e2-103">Working with qubits</span></span>

<span data-ttu-id="fb5e2-104">이는 퀀텀 컴퓨팅에서 정보의 기본적인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-104">Qubits are the fundamental object of information in quantum computing.</span></span> <span data-ttu-id="fb5e2-105">표준에 대 한 일반적인 소개는 [퀀텀 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding)및 수학적 표현에 대 한 자세한 내용은 [이 항목을 참조 하세요.](xref:microsoft.quantum.concepts.qubit)</span><span class="sxs-lookup"><span data-stu-id="fb5e2-105">For a general introduction to qubits, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding), and to dive deeper into their mathematical representation, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span> 

<span data-ttu-id="fb5e2-106">이 문서에서는 프로그램에서을 사용 하 고이를 사용 하는 방법을 살펴봅니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-106">This article explores how to use and work with qubits in a Q# program.</span></span> 

> [!IMPORTANT]
><span data-ttu-id="fb5e2-107">이 문서에서 설명 하는 문은 함수 본문 내에서 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-107">None of the statements discussed in this article are valid within the body of a function.</span></span> <span data-ttu-id="fb5e2-108">작업 내 에서만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-108">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="fb5e2-109">비트 할당</span><span class="sxs-lookup"><span data-stu-id="fb5e2-109">Allocating Qubits</span></span>

<span data-ttu-id="fb5e2-110">실제 리소스는 퀀텀 컴퓨터의 귀중 한 리소스 이기 때문에 컴파일러의 작업 중 일부는 최대한 효율적으로 사용 되 고 있는지 확인 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-110">Because physical qubits are a precious resource in a quantum computer, part of the compiler's job is to make sure they are being used as efficiently as possible.</span></span>
<span data-ttu-id="fb5e2-111">따라서 Q# 특정 문 블록 내에서 사용할 수 있도록이를 *할당* 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-111">As such, you need to tell Q# to *allocate* qubits for use within a particular statement block.</span></span>
<span data-ttu-id="fb5e2-112">이를 단일의 비트 또는 *레지스터* 라고 하는 원하는 비트 배열로 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-112">You can allocate qubits as a single qubit, or as an array of qubits, known as a *register* .</span></span> 

### <a name="clean-qubits"></a><span data-ttu-id="fb5e2-113">정리 비트</span><span class="sxs-lookup"><span data-stu-id="fb5e2-113">Clean qubits</span></span>

<span data-ttu-id="fb5e2-114">문을 사용 `using` 하 여 문 블록 중에 사용할 새 요소를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-114">Use the `using` statement to allocate new qubits for use during a statement block.</span></span>

<span data-ttu-id="fb5e2-115">문은 키워드로 구성 `using` 된 다음 괄호 안에 포함 된 바인딩과 함께 `( )` 사용할 수 있는 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-115">The statement consists of the keyword `using`, followed by a binding enclosed in parentheses `( )` and the statement block within which the qubits are available.</span></span>
<span data-ttu-id="fb5e2-116">바인딩은 문과 동일한 패턴을 따릅니다 `let` . 단일 기호 또는 기호 튜플, 등호 `=` , 단일 값 또는 *이니셜라이저의* 일치 하는 튜플 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-116">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers* .</span></span>

<span data-ttu-id="fb5e2-117">이니셜라이저는로 표시 된 단일의 비트 또는의 배열 ( `Qubit()` `Qubit[n]` 여기서 `n` 는 `Int` 식)으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-117">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="fb5e2-118">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-118">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="fb5e2-119">이 방법으로 할당 된 모든 모든 비트는 $ \ket {0} $ 상태에서 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-119">Any qubits allocated in this way start off in the $\ket{0}$ state.</span></span> <span data-ttu-id="fb5e2-120">따라서 앞의 예제에서 `auxiliary` 는 $ \ket $ 상태에 있는 단일 비트이 {0} 고, `register` 는 5 번째 비트 상태 $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cst\otimes \ket {0} $입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-120">Thus in the previous example, `auxiliary` is a single qubit in the state $\ket{0}$, and `register` is in the five-qubit state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="fb5e2-121">블록의 끝에서 `using` 해당 블록에 의해 할당 된 모든 요소는 즉시 할당 취소 되며 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-121">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="fb5e2-122">대상 컴퓨터는 할당 되지 않은 비트를 다시 사용 하 고 할당을 위해 다른 블록에 제공할 수 있습니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-122">Target machines can reuse deallocated qubits and offer them to other `using` blocks for allocation.</span></span> <span data-ttu-id="fb5e2-123">따라서 대상 컴퓨터는 할당 취소 직전에 해당 대상 컴퓨터가 $ \ket $ 상태에 있는 것으로 예상 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-123">As such, the target machine expects that qubits are in the $\ket{0}$ state immediately before deallocation.</span></span>
> <span data-ttu-id="fb5e2-124">가능 하면 항상 단일 작업을 사용 하 여 할당 된 모든 비트를 $ \ket $로 반환 {0} 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-124">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="fb5e2-125">가 필요한 경우 @"microsoft.quantum.intrinsic.reset" 작업을 사용 하 {0} 여 해당 값을 측정 하 고 결과에 따라 조건부로 작업을 수행 하 여 $ \ket $에 대 한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-125">If need be, you can use the @"microsoft.quantum.intrinsic.reset" operation, which returns the qubit to $\ket{0}$ by measuring it and conditionally performing an operation based on the result.</span></span> <span data-ttu-id="fb5e2-126">이러한 측정은 남은 비트를 포함 하는 모든 되거나 얽 히를 소멸 하므로 계산에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-126">Such a measurement destroys any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="fb5e2-127">빌려의 비트</span><span class="sxs-lookup"><span data-stu-id="fb5e2-127">Borrowed Qubits</span></span>

<span data-ttu-id="fb5e2-128">문을 사용 `borrowing` 하 여 특정 상태에 있을 필요가 없는 임시 사용에 대 한 비트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-128">Use the `borrowing` statement to allocate qubits for temporary use, which do not need to be in a specific state.</span></span>

<span data-ttu-id="fb5e2-129">계산을 수행 하는 동안에는를 사용 하 여 임시 공간으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-129">You can use borrowed qubits as scratch space during a computation.</span></span>
<span data-ttu-id="fb5e2-130">이러한 기능은 일반적으로 깨끗 한 상태가 아닙니다. 즉, $ \ket $와 같은 알려진 상태로 반드시 초기화 되는 것은 아닙니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-130">These qubits are generally not in a clean state, that is, they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="fb5e2-131">이러한 경우는 상태를 알 수 없으며 퀀텀 컴퓨터 메모리의 다른 부분과 함께 사용할 수 있기 때문에이를 "더티" 이상으로 지칭 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-131">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="fb5e2-132">바인딩은 문과 동일한 패턴 및 규칙을 따릅니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-132">The binding follows the same pattern and rules as the `using` statement.</span></span>
<span data-ttu-id="fb5e2-133">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-133">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="fb5e2-134">인 중 한 비트는 알 수 없는 상태 이며 문 블록의 끝에 있는 범위를 벗어났습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-134">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="fb5e2-135">대출자는이를 빌려 온 때와 동일한 상태로 유지 하는 커밋을 커밋합니다. 즉, 문 블록의 시작과 끝에 있는 상태는 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-135">The borrower commits to leaving the qubits in the same state they were in when they borrowed them; that is, their state at the beginning and the end of the statement block should be the same.</span></span>
<span data-ttu-id="fb5e2-136">이 상태는 반드시 클래식 상태가 아니어도 되며 대부분의 경우 borrowing 범위에는 측정값이 포함 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-136">Because this state is not necessarily a classical state, in most cases borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="fb5e2-137">Borrowing를 사용 하는 경우 시스템은 먼저 사용 중이지만 문의 본문 중에 액세스 하지 않는 작업에서 요청을 채우려고 시도 `borrowing` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-137">When borrowing qubits, the system first tries to fill the request from qubits that are in use but not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="fb5e2-138">이러한 것이 충분 하지 않은 경우 요청을 완료 하기 위해 새 비트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-138">If there aren't enough such qubits, then it allocates new qubits to complete the request.</span></span>

<span data-ttu-id="fb5e2-139">더티 비트의 알려진 사용 사례 중에는 incrementers의 구현이 매우 거의 필요 하지 않은 다중 제어 CNOT 게이트의 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-139">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="fb5e2-140">에서 사용 하는 예제는 Q# 이 문서의 [Borrowing robits 예제](#borrowing-qubits-example) 또는 Toffoli 기반 모듈식 곱하기 (Haner, Roet2n er 및 [*svore 2017)를 사용 하는 + 2를 사용 하*](https://arxiv.org/abs/1611.07995) 는 백서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-140">For an example of their use in Q#, see [Borrowing Qubits Example](#borrowing-qubits-example) in this article, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="fb5e2-141">내장 작업</span><span class="sxs-lookup"><span data-stu-id="fb5e2-141">Intrinsic Operations</span></span>

<span data-ttu-id="fb5e2-142">할당 된 후에는 함수 및 작업에 원하는 비트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-142">Once allocated, you can pass a qubit to functions and operations.</span></span>
<span data-ttu-id="fb5e2-143">어떤 경우에는 수행할 수 있는 작업은 Q# 모두 작업으로 정의 되므로 프로그램은 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-143">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>

<span data-ttu-id="fb5e2-144">이 문서에서는 사용자가 사용할 수 있는 몇 가지 유용한 작업을 설명 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-144">This article discusses a few useful Q# operations that you can use to interact with qubits.</span></span>
<span data-ttu-id="fb5e2-145">이러한 항목 및 기타에 대 한 자세한 내용은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-145">For more detail about these and others, see [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span> 

<span data-ttu-id="fb5e2-146">첫째, 단일 기능 비트 Pauli 연산자 $X $, $Y $ 및 $Z $는 내장 작업, 및로 표시 되며, Q# [`X`](xref:Microsoft.Quantum.Intrinsic.X) [`Y`](xref:Microsoft.Quantum.Intrinsic.Y) [`Z`](xref:Microsoft.Quantum.Intrinsic.Z) 각각 형식이 `(Qubit => Unit is Adj + Ctl)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-146">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations [`X`](xref:Microsoft.Quantum.Intrinsic.X), [`Y`](xref:Microsoft.Quantum.Intrinsic.Y), and [`Z`](xref:Microsoft.Quantum.Intrinsic.Z), each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="fb5e2-147">[내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에 설명 된 것 처럼, $X $ 등의 `X` 작업을 수행 하거나 게이트를 수행 하지 않는 것으로 간주 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-147">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="fb5e2-148">작업을 사용 하 여 `X` $ \ket{s_0 s_1 \dots .. s_n} $s $ 형식의 상태를 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-148">You can use the `X` operation to prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
        // Remember to reset the qubits before deallocation:
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="fb5e2-149">나중에이 작업을 작성 하는 보다 간단한 방법으로 수동 제어 흐름이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-149">Later, you will see more compact ways of writing this operation that do not require manual control flow.</span></span>

<span data-ttu-id="fb5e2-150">\Ket transform $H $를 사용 하 여 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left $ {2} 및 $ \ket {-} = \left (\ket Hadamard \left)/\left $와 같은 상태를 준비할 수도 있습니다 {0} {1} {2} .이는 Q# 내장 작업 ( [`H`](xref:Microsoft.Quantum.Intrinsic.H) => Unit is Adj + Ctl)에 의해 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-150">You can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation [`H`](xref:Microsoft.Quantum.Intrinsic.H) (also of type (Qubit => Unit is Adj + Ctl)\`):</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString in the earlier example.
    PrepareBitString(bitstring, register);
    // Next, use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the desired state.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="fb5e2-151">측정</span><span class="sxs-lookup"><span data-stu-id="fb5e2-151">Measurements</span></span>

<span data-ttu-id="fb5e2-152">개별 요소의 측정은 각각 [Bloch 구의](xref:microsoft.quantum.glossary#bloch-sphere)Pauli 축으로 표시 되는 다양 한 밑에서 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-152">Measurements of individual qubits can be performed in different bases, each represented by a Pauli axis on the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere).</span></span>
<span data-ttu-id="fb5e2-153">*계산 기준은* 기준을 나타내며 `PauliZ` 측정에 사용 되는 가장 일반적인 기준입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-153">The *computational basis* refers to the `PauliZ` basis, and is the most common basis used for measurement.</span></span>

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a><span data-ttu-id="fb5e2-154">단일 `PauliZ` 비트 단위 측정</span><span class="sxs-lookup"><span data-stu-id="fb5e2-154">Measure a single qubit in the `PauliZ` basis</span></span>

<span data-ttu-id="fb5e2-155">[`M`](xref:Microsoft.Quantum.Intrinsic.M)기본 제공 되는 기본이 아닌 작업 인 작업을 사용 하 여 단일 비트를 측정 하 `PauliZ` 고 결과에 기존 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-155">Use the [`M`](xref:Microsoft.Quantum.Intrinsic.M) operation, which is a built-in intrinsic non-unitary operation, to measure a single qubit in the `PauliZ` basis and assign a classical value to the result.</span></span>
<span data-ttu-id="fb5e2-156">`M` 에는 예약 된 반환 형식이 있습니다. 여기에는 `Result` 값을 사용 `Zero` 하거나 `One` 측정 된 상태 $ \ket {0} $ 또는 $ \ket {1} $-결과가 더 이상 퀀텀 상태가 아님을 나타내는 값만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-156">`M` has a reserved return type, `Result`, which can only take values `Zero` or `One` corresponding to the measured states $\ket{0}$ or $\ket{1}$ - indicating that the result is no longer a quantum state.</span></span>

<span data-ttu-id="fb5e2-157">간단한 예는 $ \ket $ 상태에서 1 개의 한 비트를 할당 하 {0} 고, Hadamard 작업을 적용 하 고, 결과를 측정 하는 다음 작업입니다 `H` `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-157">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // Apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, return the result of the measurement.
        return result;
    }
}
```

### <a name="measure-one-or-more-qubits-in-specific-bases"></a><span data-ttu-id="fb5e2-158">특정 베이스에서 하나 이상의 이상 비트 측정</span><span class="sxs-lookup"><span data-stu-id="fb5e2-158">Measure one or more qubits in specific bases</span></span>

<span data-ttu-id="fb5e2-159">특정 베이스에서 하나 이상의 고 비트 배열을 측정 하려면 작업을 사용할 수 있습니다 [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-159">To measure an array of one or more qubits in specific bases, you can use the [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) operation.</span></span>

<span data-ttu-id="fb5e2-160">에 대 한 입력은 `Measure` 형식의 배열 `Pauli` (예: `[PauliX, PauliZ, PauliZ]` ) 및의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-160">The inputs to `Measure` are an array of `Pauli` types (for example, `[PauliX, PauliZ, PauliZ]`) and an array of qubits.</span></span>

<span data-ttu-id="fb5e2-161">조금 더 복잡 한 예는 다음 연산에서 제공 됩니다 .이 경우에는 `true` 레지스터의 모든 모든 비트가 `Qubit[]` 지정 된 pai로 측정 될 때 0 상태에 있는 경우 부울 값을 반환 하 고, 그렇지 않으면를 반환 `false` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-161">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="fb5e2-162">이 예제는 계속 해 서 `Measure` 개별 작업을 한 번에 하나씩만 수행 하지만 작업을 여러 개의 성능으로 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-162">Note that this example still only performs `Measure` on individual qubits one at a time, but the operation can be extended to joint measurements on multiple qubits.</span></span>

## <a name="borrowing-qubits-example"></a><span data-ttu-id="fb5e2-163">Borrowing  Bits 예제</span><span class="sxs-lookup"><span data-stu-id="fb5e2-163">Borrowing Qubits Example</span></span>

<span data-ttu-id="fb5e2-164">`borrowing`다음 함수와 같이 키워드를 사용 하는 라고에는 예제가 있습니다 `MultiControlledXBorrow` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-164">There are examples in the canon that use the `borrowing` keyword, such as the following function `MultiControlledXBorrow`.</span></span> <span data-ttu-id="fb5e2-165">`controls`가 작업에 추가할 제어 비트를 나타내는 경우 `X` 이 구현에 의해 추가 된 더티 [ancillas](xref:microsoft.quantum.glossary#ancilla) 수는 `Length(controls)-2` 입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-165">If `controls` denotes the control qubits to add to an `X` operation, then the number of dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) added by this implementation is `Length(controls)-2`.</span></span>

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

<span data-ttu-id="fb5e2-166">이 예제에서는 `With` adjoint를 지 원하는 작업 (예:)에 적용할 수 있는 형식으로 조합 기의 광범위 한 사용을 사용 `WithA` 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-166">Note that this example used extensive use of the `With` combinator, in its form that is applicable for operations that support adjoint, for example, `WithA`.</span></span>
<span data-ttu-id="fb5e2-167">이는를 포함 하는 구조에 컨트롤을 추가 하 `With` 는 작업을 내부 작업에만 전파 하므로 좋은 프로그래밍 스타일입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5e2-167">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="fb5e2-168">또한 작업의 외에도 `body` 작업 본문의 구현은 문으로의 구현이 `controlled` 아니라 명시적으로 제공 되었습니다 `controlled auto` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-168">Also note that, in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="fb5e2-169">이에 대 한 이유는 회로 구조 때문에의 각 게이트에 컨트롤을 추가 하는 것과 비교 하 여 더 많은 컨트롤을 추가 하는 것이 쉽기 때문입니다 `body` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-169">The reason for this is that, because of the structure of the circuit, it is easy to add further controls, which is beneficial compared to adding control to each gate in the `body`.</span></span> 

<span data-ttu-id="fb5e2-170">그러나이 코드는 곱하기 제어 작업을 구현 하는 것과 동일한 목표를 달성 하는 다른 라고 함수와 비교 하는 것이 좋습니다 .이는 `MultiControlledXClean` `X` 메커니즘을 사용 하 여 여러 가지 깨끗 한 비트를 사용 합니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-170">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="fb5e2-171">다음 단계</span><span class="sxs-lookup"><span data-stu-id="fb5e2-171">Next steps</span></span>

<span data-ttu-id="fb5e2-172">의 [제어 흐름](xref:microsoft.quantum.guide.controlflow) 에 대해 알아봅니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="fb5e2-172">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>