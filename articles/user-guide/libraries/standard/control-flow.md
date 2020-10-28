---
title: '표준 libararies 흐름 제어 :::no-loc(Q#):::'
description: 'Microsoft 표준 라이브러리의 흐름 제어 작업 및 함수에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: ad107f5c65a4bf368d12d30e4a72786f2076205c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690876"
---
# <a name="higher-order-control-flow"></a><span data-ttu-id="d4b0f-103">Higher-Order 제어 흐름</span><span class="sxs-lookup"><span data-stu-id="d4b0f-103">Higher-Order Control Flow</span></span> #

<span data-ttu-id="d4b0f-104">표준 라이브러리의 기본 역할 중 하나는 고급 알고리즘 아이디어를 [퀀텀 프로그램](https://en.wikipedia.org/wiki/Quantum_programming)으로 보다 쉽게 표현할 수 있도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-104">One of the primary roles of the standard library is to make it easier to express high-level algorithmic ideas as [quantum programs](https://en.wikipedia.org/wiki/Quantum_programming).</span></span>
<span data-ttu-id="d4b0f-105">따라서 :::no-loc(Q#)::: 라고은 함수 및 작업의 부분 응용 프로그램을 사용 하 여 구현 되는 다양 한 흐름 제어 구문을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-105">Thus, the :::no-loc(Q#)::: canon provides a variety of different flow control constructs, each implemented using partial application of functions and operations.</span></span>
<span data-ttu-id="d4b0f-106">한 예로 바로 이동 하 고, 등록에서 "CNOT 사다리"를 구성 하려는 경우를 고려해 보세요.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-106">Jumping immediately into an example, consider the case in which one wants to construct a "CNOT ladder" on a register:</span></span>

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

<span data-ttu-id="d4b0f-107">반복 및 루프를 사용 하 여이 패턴을 표현할 수 있습니다 `for` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-107">We can express this pattern by using iteration and `for` loops:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

<span data-ttu-id="d4b0f-108"><xref:Microsoft.Quantum.Canon.ApplyToEachCA>뿐만 아니라와 같은 배열 조작 함수를 사용 하 여 표현 <xref:Microsoft.Quantum.Arrays.Zipped> 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-108">Expressed in terms of <xref:Microsoft.Quantum.Canon.ApplyToEachCA> and array manipulation functions such as <xref:Microsoft.Quantum.Arrays.Zipped>, however, this is much shorter and easier to read:</span></span>

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

<span data-ttu-id="d4b0f-109">이 섹션의 나머지 부분에서는 조밀 express 퀀텀 프로그램에서 제공 하는 다양 한 흐름 제어 작업 및 함수를 사용 하는 방법에 대 한 몇 가지 예를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-109">In the rest of this section, we will provide a number of examples of how to use the various flow control operations and functions provided by the canon to compactly express quantum programs.</span></span>

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a><span data-ttu-id="d4b0f-110">배열 및 범위에 대 한 작업 및 함수 적용</span><span class="sxs-lookup"><span data-stu-id="d4b0f-110">Applying Operations and Functions over Arrays and Ranges</span></span> ##

<span data-ttu-id="d4b0f-111">라고에서 제공 하는 기본 추상화 중 하나가 반복입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-111">One of the primary abstractions provided by the canon is that of iteration.</span></span>
<span data-ttu-id="d4b0f-112">예를 들어 단일의 단일 기능 $U $에 대해 \otimes U \otimes \cst\otimes U $ $U 형태의 단일 형식을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-112">For instance, consider a unitary of the form $U \otimes U \otimes \cdots \otimes U$ for a single-qubit unitary $U$.</span></span>
<span data-ttu-id="d4b0f-113">에서는를 :::no-loc(Q#)::: 사용 하 여 <xref:Microsoft.Quantum.Arrays.IndexRange> 이를 레지스터에 대 한 루프로 나타낼 수 있습니다 `for` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-113">In :::no-loc(Q#):::, we might use <xref:Microsoft.Quantum.Arrays.IndexRange> to represent this as as a `for` loop over a register:</span></span>

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation ApplyHadamardToAll(
    register : Qubit[])
: Unit is Adj + Ctl {
    for (qubit in register) {
        H(qubit);
    }
}
```

<span data-ttu-id="d4b0f-114">그런 다음이 새로운 작업 `HAll(register)` 을 사용 하 여 h \otimes \cst\otimes h $에 $H을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-114">We can then use this new operation as `HAll(register)` to apply $H \otimes H \otimes \cdots \otimes H$.</span></span>

<span data-ttu-id="d4b0f-115">그러나이 방법은 특히 더 큰 알고리즘에서 수행 하는 것이 매우 복잡 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-115">This is cumbersome to do, however, especially in a larger algorithm.</span></span>
<span data-ttu-id="d4b0f-116">또한이 접근 방식은 각 작업에 적용 하려는 특정 작업에 특화 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-116">Moreover, this approach is specialized to the particular operation that we wish to apply to each qubit.</span></span>
<span data-ttu-id="d4b0f-117">이 알고리즘 개념을 보다 명시적으로 표현 하기 위해 작업이 최고 수준 이라는 사실을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-117">We can use the fact that operations are first-class to express this algorithmic concept more explicitly:</span></span>

```qsharp
ApplyToEachCA(H, register);
```

<span data-ttu-id="d4b0f-118">여기서 접미사는 `CA` 에 대 `ApplyToEach` 한 호출이 자체 adjointable 및 제어 가능 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-118">Here, the suffix `CA` indicates that the call to `ApplyToEach` is itself adjointable and controllable.</span></span>
<span data-ttu-id="d4b0f-119">따라서가 `U` 및를 지 원하는 경우 `Adjoint` `Controlled` 다음 줄은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-119">Thus, if `U` supports `Adjoint` and `Controlled`, the following lines are equivalent:</span></span>

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

<span data-ttu-id="d4b0f-120">특히이는에 대 `ApplyToEachCA` 한 호출이 adjoint 특수화가 자동 생성 되는 작업에 나타날 수 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-120">In particular, this means that calls to `ApplyToEachCA` can appear in operations for which an adjoint specialization is auto-generated.</span></span>
<span data-ttu-id="d4b0f-121">마찬가지로 <xref:Microsoft.Quantum.Canon.ApplyToEachIndex> 는 양식의 패턴을 표시 하는 데 유용 `U(0, targets[0]); U(1, targets[1]); ...` 하며 입력에서 지원 되는 함수의 각 조합에 대 한 버전을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-121">Similarly, <xref:Microsoft.Quantum.Canon.ApplyToEachIndex> is useful for representing patterns of the form `U(0, targets[0]); U(1, targets[1]); ...`, and offers versions for each combination of functors supported by its input.</span></span>

> [!TIP]
> <span data-ttu-id="d4b0f-122">`ApplyToEach` 는 이외의 입력을 취하는 작업과 함께 사용할 수 있도록 형식 매개 변수화 됩니다 `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-122">`ApplyToEach` is type-parameterized such that it can be used with operations that take inputs other than `Qubit`.</span></span>
> <span data-ttu-id="d4b0f-123">예를 들어, `codeBlocks` 가 복구 해야 하는 값의 배열 이라고 가정 합니다 <xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister> .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-123">For example, suppose that `codeBlocks` is an array of <xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister> values that need to be recovered.</span></span>
> <span data-ttu-id="d4b0f-124">그런 다음 `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` 는 `code` `recoveryFn` 각 블록에 독립적으로 오류 수정 코드 및 복구 기능을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-124">Then `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` will apply the error-correcting code `code` and recovery function `recoveryFn` to each block independently.</span></span>
> <span data-ttu-id="d4b0f-125">이는 기존 입력에 대해서도 유지 `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` 됩니다 .는 $ \pi/$2에 $Y $3 $pi $X 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-125">This holds even for classical inputs: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` will apply a rotation of $\pi / 2$ about $X$ followed by a rotation of $pi / 3$ about $Y$.</span></span>

<span data-ttu-id="d4b0f-126">:::no-loc(Q#):::또한 라고은 함수형 프로그래밍에 익숙한 클래식 열거형 패턴에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-126">The :::no-loc(Q#)::: canon also provides support for classical enumeration patterns familiar to functional programming.</span></span>
<span data-ttu-id="d4b0f-127">예를 들어은 <xref:Microsoft.Quantum.Arrays.Fold> 목록에 대 한 함수를 줄이기 위해 (f (f (s \_ {\text{initial}}, x \_ 0), x \_ 1), \도트) $ 패턴 $f을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-127">For instance, <xref:Microsoft.Quantum.Arrays.Fold> implements the pattern $f(f(f(s\_{\text{initial}}, x\_0), x\_1), \dots)$ for reducing a function over a list.</span></span>
<span data-ttu-id="d4b0f-128">이 패턴은 합계, 제품, 최소, 최대 및 기타 해당 함수를 구현 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-128">This pattern can be used to implement sums, products, minima, maxima and other such functions:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

<span data-ttu-id="d4b0f-129">마찬가지로 및와 같은 함수를 <xref:Microsoft.Quantum.Arrays.Mapped> <xref:Microsoft.Quantum.Arrays.MappedByIndex> 사용 하 여의 함수형 프로그래밍 개념을 표현할 수 있습니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-129">Similarly, functions like <xref:Microsoft.Quantum.Arrays.Mapped> and <xref:Microsoft.Quantum.Arrays.MappedByIndex> can be used to express functional programming concepts in :::no-loc(Q#):::.</span></span>

## <a name="composing-operations-and-functions"></a><span data-ttu-id="d4b0f-130">작업 및 함수 작성</span><span class="sxs-lookup"><span data-stu-id="d4b0f-130">Composing Operations and Functions</span></span> ##

<span data-ttu-id="d4b0f-131">라고 작업에서 제공 하는 제어 흐름 생성자는 입력으로 사용할 수 있습니다. 따라서 여러 작업이 나 함수를 단일 호출 가능으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-131">The control flow constructs offered by the canon take operations and functions as their inputs, such that it is helpful to be able to compose several operations or functions into a single callable.</span></span>
<span data-ttu-id="d4b0f-132">예를 들어, $UVU ^ {\dagger} $ 패턴은 퀀텀 프로그래밍에서 매우 일반적입니다 .이는 라고에서 작업을 <xref:Microsoft.Quantum.Canon.ApplyWith> 이 패턴의 추상화로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-132">For instance, the pattern $UVU^{\dagger}$ is extremely common in quantum programming, such that the canon provides the operation <xref:Microsoft.Quantum.Canon.ApplyWith> as an abstraction for this pattern.</span></span>
<span data-ttu-id="d4b0f-133">이 추상화를 사용 하면 `Controlled` 시퀀스에 대해 작업 `U(qubit); V(qubit); Adjoint U(qubit);` 을 수행할 필요가 없으므로 회로에 더 효율적으로 compliation 수 있습니다 `U` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-133">This abstraction also allows for more efficient compliation into circuits, as `Controlled` acting on the sequence `U(qubit); V(qubit); Adjoint U(qubit);` does not need to act on each `U`.</span></span>
<span data-ttu-id="d4b0f-134">이를 확인 하려면 $c (U) $를 단일 항목으로 `Controlled U([control], target)` 지정 하 고 $c (V) $를 동일한 방식으로 정의할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-134">To see this, let $c(U)$ be the unitary representing `Controlled U([control], target)` and let $c(V)$ be defined in the same way.</span></span>
<span data-ttu-id="d4b0f-135">그런 다음 임의의 상태 $ \ket{\psi} $, \begin{align} c (U) c (V) c (U) ^ \dagger \ket {1} \otimes \ket{\psi} & = \dagger} {1} \otime (uvu ^ {\ket{\psi} \boldone) \\ \\ & = (\Boldone \otimes u) (c (V)) (\Ket \otimes u ^ \dagger) {1} \otimes</span><span class="sxs-lookup"><span data-stu-id="d4b0f-135">Then for an arbitrary state $\ket{\psi}$, \begin{align} c(U) c(V) c(U)^\dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU^{\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{1} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="d4b0f-136">의 정의를 \end{align} `Controlled` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-136">\end{align} by the definition of `Controlled`.</span></span>
<span data-ttu-id="d4b0f-137">반면에 \begin{align} c (U) c (V) c (U) ^ {0} \dagger \ket \otimes \ket{\psi} & = {0} \otimes \ket{\psi} \\ \\ & = \ket {0} \otime (UU ^ \dagger \boldone) \\ \\ & = (\boldone \Otimes u) (c (V)) (\ket \otimes u ^ \dagger) {0} \otimes</span><span class="sxs-lookup"><span data-stu-id="d4b0f-137">On the other hand, \begin{align} c(U) c(V) c(U)^\dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \otimes (UU^\dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{0} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="d4b0f-138">\end{align}는이 방식으로 모든 입력 상태에 대해 $ out을 $U 수 있다는 결론을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-138">\end{align} By linearity, we can conclude that we can factor $U$ out in this way for all input states.</span></span>
<span data-ttu-id="d4b0f-139">즉, $c (UVU ^ \dagger) = U c (V) U ^ \ara$입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-139">That is, $c(UVU^\dagger) = U c(V) U^\dagger$.</span></span>
<span data-ttu-id="d4b0f-140">일반적으로 제어 작업은 비용이 많이 들 수 있으므로 및와 같은 제어 되는 변형을 사용 `WithC` `WithCA` 하면 적용 해야 하는 제어 함수 수를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-140">Since controlling operations can be expensive in general, using controlled variants such as `WithC` and `WithCA` can help reduce the number of control functors that need to be applied.</span></span>

> [!NOTE]
> <span data-ttu-id="d4b0f-141">$U $를 팩터링 하는 다른 한 가지 다른 결과는 함수를에 적용 하는 방법을 몰라도 됩니다 `Controlled` `U` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-141">One other consequence of factoring out $U$ is that we need not even know how to apply the `Controlled` functor to `U`.</span></span>
> <span data-ttu-id="d4b0f-142">`ApplyWithCA` 따라서 필요한 것 보다 더 약한 서명이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-142">`ApplyWithCA` therefore has a weaker signature than might be expected:</span></span>
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

<span data-ttu-id="d4b0f-143">마찬가지로는 <xref:Microsoft.Quantum.Canon.Bound> 다른 작업의 시퀀스를 차례로 적용 하는 작업을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-143">Similarly, <xref:Microsoft.Quantum.Canon.Bound> produces operations which apply a sequence of other operations in turn.</span></span>
<span data-ttu-id="d4b0f-144">예를 들어, 다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-144">For instance, the following are equivalent:</span></span>

```qsharp
H(qubit); X(qubit);
Bound([H, X], qubit);
```

<span data-ttu-id="d4b0f-145">반복 패턴과 결합 하면 특히 유용 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-145">Combining with iteration patterns can make this especially useful:</span></span>

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bound([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a><span data-ttu-id="d4b0f-146">Time-Ordered 컴퍼지션</span><span class="sxs-lookup"><span data-stu-id="d4b0f-146">Time-Ordered Composition</span></span> ###

<span data-ttu-id="d4b0f-147">부분 응용 프로그램 및 기존 함수 측면에서 흐름 제어를 고려 하 여 계속 진행할 수 있으며, 기존 흐름 제어 측면에서 매우 복잡 한 퀀텀 개념을 모델링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-147">We can go still further by thinking of flow control in terms of partial application and classical functions, and can model even fairly sophisticated quantum concepts in terms of classical flow control.</span></span>
<span data-ttu-id="d4b0f-148">이러한 비유는 단일 연산자를 사용 하 여 다른 단일 연산자의 측면에서 단일 연산자를 분해 하는 것과 같은 특정 단일 연산자의 역할을 하는 기존 서브루틴에 대 한 특정 호출 시퀀스를 생성 하는 것과 일치 한다는 것을 인식 하 여 정확 하 게 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-148">This analogy is made precise by the recognition that unitary operators correspond exactly to the side effects of calling operations, such that any decomposition of unitary operators in terms of other unitary operators corresponds to constructing a particular calling sequence for classical subroutines which emit instructions to act as particular unitary operators.</span></span>
<span data-ttu-id="d4b0f-149">이 뷰에서는가와 동일 하기 때문에 매트릭스 제품을 정확 하 게 표현 합니다 .이는 `Bound` `Bound([A, B])(target)` `A(target); B(target);` $BA $에 해당 하는 호출 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-149">Under this view, `Bound` is precisely the representation of the matrix product, since `Bound([A, B])(target)` is equivalent to `A(target); B(target);`, which in turn is the calling sequence corresponding to $BA$.</span></span>

<span data-ttu-id="d4b0f-150">보다 정교한 예는 [Trotter – Suzuki 확장](https://arxiv.org/abs/math-ph/0506007v1)입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-150">A more sophisticated example is the [Trotter–Suzuki expansion](https://arxiv.org/abs/math-ph/0506007v1).</span></span>
<span data-ttu-id="d4b0f-151">[데이터 구조의](xref:microsoft.quantum.libraries.data-structures)동적 생성기 표현 섹션에서 설명한 것 처럼 Trotter – Suzuki 확장은 행렬 지 수를 표현 하는 데 특히 유용한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-151">As discussed in the Dynamical Generator Representation section of [data structures](xref:microsoft.quantum.libraries.data-structures), the Trotter–Suzuki expansion provides a particularly useful way of expressing matrix exponentials.</span></span>
<span data-ttu-id="d4b0f-152">예를 들어, 가장 낮은 순서로 확장을 적용 하면 $ 및 $B $ $A 하는 모든 연산자 ($A = A ^ \aa$ 및 $B = B ^ \aate$)가 생성 됩니다. \begin{align} \tag{★} \label{eq: trotter-suzuki-0} \dagger (i [A + B] t) = \ lim_ {n\to\infty} \\sts (\dagger (i A t/n) \dagger (i B t/n) \dagger) ^ n.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-152">For instance, applying the expansion at its lowest order yields that for any operators $A$ and $B$ such that $A = A^\dagger$ and $B = B^\dagger$, \begin{align} \tag{★} \label{eq:trotter-suzuki-0} \exp(i [A + B] t) = \lim_{n\to\infty} \left(\exp(i A t / n) \exp(i B t / n)\right)^n.</span></span>
<span data-ttu-id="d4b0f-153">\end{align} 것 구어체 $A + B $에서 $A $ 및 $B $를 통해 지속적으로 변화 하는 상태를 대략적으로 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-153">\end{align} Colloquially, this says that we can approximately evolve a state under $A + B$ by alternately evolving under $A$ and $B$ alone.</span></span>
<span data-ttu-id="d4b0f-154">`A : (Double, Qubit[]) => Unit`^ {I} $ $e 적용 되는 작업을 통해 $A $에서 발전을 나타내는 경우 호출 시퀀스를 다시 정렬 하는 것과 관련 하 여 Trotter – Suzuki 확장의 표현이 명확 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-154">If we represent evolution under $A$ by an operation `A : (Double, Qubit[]) => Unit` that applies $e^{i t A}$, then the representation of the Trotter–Suzuki expansion in terms of rearranging calling sequences becomes clear.</span></span>
<span data-ttu-id="d4b0f-155">구체적으로와 같은 작업을 수행 하는 경우 `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` `A = U(0, _, _)` `B = U(1, _, _)` `U` 폼의 시퀀스를 생성 하 여 $t $의 정수 부분을 나타내는 새 작업을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-155">Concretely, given an operation `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` such that `A = U(0, _, _)` and `B = U(1, _, _)`, we can define a new operation representing the integral of `U` at time $t$ by generating sequences of the form</span></span>

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

<span data-ttu-id="d4b0f-156">이제는 *퀀텀 메커니즘을 참조 하지 않고* Trotter – Suzuki 확장에 대 한 이유를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-156">At this point, we can now reason about the Trotter–Suzuki expansion *without reference to quantum mechanics at all* .</span></span>
<span data-ttu-id="d4b0f-157">확장은 실제로 $ \eqref{eq: trotter-suzuki-0} $에서 지 주는 매우 구체적인 반복 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-157">The expansion is effectively a very particular iteration pattern motivated by $\eqref{eq:trotter-suzuki-0}$.</span></span>
<span data-ttu-id="d4b0f-158">이 반복 패턴은 다음을 통해 구현 됩니다 <xref:Microsoft.Quantum.Canon.DecomposedIntoTimestepsCA> .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-158">This iteration pattern is implemented by <xref:Microsoft.Quantum.Canon.DecomposedIntoTimestepsCA>:</span></span>

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

<span data-ttu-id="d4b0f-159">의 시그니처는 `DecomposeIntoTimeStepsCA` 의 일반적인 패턴을 따릅니다 :::no-loc(Q#)::: .이 패턴은 배열 또는 즉석에서 요소를 계산 하는 요소에 의해 지원 될 수 있는 컬렉션이 첫 번째 요소가 `Int` 해당 길이를 나타내는 값인 튜플로 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-159">The signature of `DecomposeIntoTimeStepsCA` follows a common pattern in :::no-loc(Q#):::, where collections that may be backed either by arrays or by something which compute elements on the fly are represented by tuples whose first elements are `Int` values indicating their lengths.</span></span>

## <a name="putting-it-together-controlling-operations"></a><span data-ttu-id="d4b0f-160">함께 배치: 작업 제어</span><span class="sxs-lookup"><span data-stu-id="d4b0f-160">Putting it Together: Controlling Operations</span></span> ##

<span data-ttu-id="d4b0f-161">마지막으로, 라고은 퀀텀 작업에 대 한 `Controlled` 추가 방법을 제공 하 여 함수를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-161">Finally, the canon builds on the `Controlled` functor by providing additional ways to condition quantum operations.</span></span>
<span data-ttu-id="d4b0f-162">특히 퀀텀 산술에서 $ \ket{0\cdots 0} $ 이외의 계산 기준 상태에 대 한 조건 작업에 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-162">It is common, especially in quantum arithmetic, to condition operations on computational basis states other than $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="d4b0f-163">위에서 소개한 제어 작업 및 함수를 사용 하 여 단일 문에서 더 일반적인 퀀텀 조건을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-163">Using the control operations and functions introduced above, we can more general quantum conditions in a single statement.</span></span>
<span data-ttu-id="d4b0f-164">이를 수행 하는 방법 <xref:Microsoft.Quantum.Canon.ControlledOnBitString> (예를 들어, 형식 매개 변수)으로 이동 하 여 피스를 하나씩 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-164">Let's jump in to how <xref:Microsoft.Quantum.Canon.ControlledOnBitString> does it (sans type parameters), then we'll break down the pieces one by one.</span></span>
<span data-ttu-id="d4b0f-165">가장 먼저 해야 할 일은 임의의 계산 기준 상태에서 컨트롤을 실제로 구현 하는 작업을 정의 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-165">The first thing we'll need to do is to define an operation which actually does the heavy lifting of implementing the control on arbitrary computational basis states.</span></span>
<span data-ttu-id="d4b0f-166">그러나이 작업을 직접 호출 하지 않으므로 `_` 이름의 시작 부분에를 추가 하 여 다른 구문의 구현 임을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-166">We won't call this operation directly, however, and so we add `_` to the beginning of the name to indicate that it's an implementation of another construct elsewhere.</span></span>

```qsharp
operation _ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl),
    controlRegister : Qubit[],
    targetRegister: Qubit[])
: Unit is Adj + Ctl
```

<span data-ttu-id="d4b0f-167">`Bool`지정 된 작업에 적용할 조절를 지정 하는 데 사용 하는, 배열로 표시 되는 비트 문자열을 사용 `oracle` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-167">Note that we take a string of bits, represented as a `Bool` array, that we use to specify the conditioning that we want to apply to the operation `oracle` that we are given.</span></span>
<span data-ttu-id="d4b0f-168">이 작업은 실제로 응용 프로그램을 직접 수행 하므로 컨트롤과 대상 레지스터를 모두로 표시 해야 `Qubit[]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-168">Since this operation actually does the application directly, we also need to take the control and target registers, both represented here as `Qubit[]`.</span></span>

<span data-ttu-id="d4b0f-169">다음으로, $ \_ \_ \_ \ket{\vec{s}} $를 $ \ket{0\cdots 0} $로 변환 하 여 비트 문자열 $ \vec{s} $에 대 한 계산 기준 상태 $ \ket{\vec{s}} = \ket{s 0 s 1 \dots .. s {n-1}} $를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-169">Next, we note that controlling on the computational basis state $\ket{\vec{s}} = \ket{s\_0 s\_1 \dots s\_{n - 1}}$ for a bit string $\vec{s}$ can be realized by transforming $\ket{\vec{s}}$ into $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="d4b0f-170">특히 $ \ket{\vec{s}} = X ^ {s \_ 0} \Otimes x ^ {s \_ 1} \otimes \Cst\otimes x ^ {s \_ {n-1}} \ket{0\cdots 0} $입니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-170">In particular, $\ket{\vec{s}} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{0\cdots 0}$.</span></span>
<span data-ttu-id="d4b0f-171">$X ^ {\dagger} = X $ 이므로 $ \ket{0\dots 0} = X ^ {s \_ 0} \otimes x ^ {s \_ 1} \otimes \cst\otimes x ^ {s \_ {n-1}} \ket{\vec{s}} $를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-171">Since $X^{\dagger} = X$, this implies that $\ket{0\dots 0} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{\vec{s}}$.</span></span>
<span data-ttu-id="d4b0f-172">따라서 $P = X ^ {s \_ 0} \Otimes x ^ {s \_ 1} \otimes \otimes \otimes x ^ {s \_ {n-1}} $, apply `Controlled oracle` 및 transform을 $ \vec{s} $로 다시 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-172">Thus, we can apply $P = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}}$, apply `Controlled oracle`, and transform back to $\vec{s}$.</span></span>
<span data-ttu-id="d4b0f-173">이 구성은 정확 `ApplyWith` 하므로 다음과 같이 새로운 작업의 본문을 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-173">This construction is precisely `ApplyWith`, so we write the body of our new operation accordingly:</span></span>

```qsharp
{
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

<span data-ttu-id="d4b0f-174">여기서는에 <xref:Microsoft.Quantum.Canon.ApplyPauliFromBitString> 사용할 수 있도록 해당 대상에 대해 부분적으로 적용 되는 $P $를 적용 하는 데 사용 되었습니다 `ApplyWith` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-174">Here, we have used <xref:Microsoft.Quantum.Canon.ApplyPauliFromBitString> to apply $P$, partially applying over its target for use with `ApplyWith`.</span></span>
<span data-ttu-id="d4b0f-175">그러나 *컨트롤* 레지스터를 원하는 형식으로 변환 해야 하므로 `(Controlled oracle)` *대상* 에서 내부 작업을 부분적으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-175">Note, however, that we need to transform the *control* register to our desired form, so we partially apply the inner operation `(Controlled oracle)` on the *target* .</span></span>
<span data-ttu-id="d4b0f-176">여기서 `ApplyWith` 는 원하는 대로 정확 하 게 $P $를 사용 하 여 컨트롤 레지스터를 대괄호로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-176">This leaves `ApplyWith` acting to bracket the control register with $P$, exactly as we desired.</span></span>

<span data-ttu-id="d4b0f-177">이 시점에서이 작업을 수행할 수는 있지만 새 작업에서 함수를 적용 하는 것 처럼 "느낌" 하지 않습니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-177">At this point, we could be done, but it is somehow unsatisfying that our new operation does not "feel" like applying the `Controlled` functor.</span></span>
<span data-ttu-id="d4b0f-178">따라서 oracle을 제어 하 고 새 작업을 반환 하는 함수를 작성 하 여 새로운 제어 흐름 개념의 정의를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4b0f-178">Thus, we finish defining our new control flow concept by writing a function that takes the oracle to be controlled and that returns a new operation.</span></span>
<span data-ttu-id="d4b0f-179">이러한 방식으로 새 함수는와 매우 유사 `Controlled` 합니다 .를 사용 하 여 강력한 새 제어 흐름 구문을 쉽게 정의 하 고 라고을 함께 사용할 수 있다는 것을 보여 주는 것입니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="d4b0f-179">In this way, our new function looks and feels very much like `Controlled`, illustrating that we can easily define powerful new control flow constructs using :::no-loc(Q#)::: and the canon together:</span></span>

```qsharp
function ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl))
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
