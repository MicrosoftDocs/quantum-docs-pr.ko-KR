---
title: '표준 라이브러리의 데이터 구조 :::no-loc(Q#):::'
description: 'Microsoft standard 라이브러리의 데이터 구조, oracles 및 동적 생성기에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: QuantumWriter
uid: microsoft.quantum.libraries.data-structures
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: c3ce5d531618c269d15be3e4eb58ecbb597a022c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692238"
---
# <a name="data-structures-and-modeling"></a><span data-ttu-id="f8e79-103">데이터 구조 및 모델링</span><span class="sxs-lookup"><span data-stu-id="f8e79-103">Data Structures and Modeling</span></span> #

## <a name="classical-data-structures"></a><span data-ttu-id="f8e79-104">기존 데이터 구조</span><span class="sxs-lookup"><span data-stu-id="f8e79-104">Classical Data Structures</span></span> ##

<span data-ttu-id="f8e79-105">또한 라고은 퀀텀 개념을 나타내는 데 사용 되는 사용자 정의 형식과 함께 퀀텀 시스템의 제어에 사용 되는 기존 데이터로 작업 하기 위한 작업, 함수 및 유형도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-105">Along with user-defined types for representing quantum concepts, the canon also provides operations, functions, and types for working with classical data used in the control of quantum systems.</span></span>
<span data-ttu-id="f8e79-106">예를 들어 <xref:Microsoft.Quantum.Arrays.Reversed> 함수는 배열을 입력으로 사용 하 고 동일한 배열을 역순으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-106">For instance, the <xref:Microsoft.Quantum.Arrays.Reversed> function takes an array as input and returns the same array in reverse order.</span></span>
<span data-ttu-id="f8e79-107">그러면 형식의 배열에서이를 사용 하 여 `Qubit[]` 양자의 퀀텀 표현 간에 변환 하는 동안 불필요 한 $ \operatorname{SWAP} $ 게이트를 적용할 필요가 없도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-107">This can then be used on an array of type `Qubit[]` to avoid having to apply unnecessary $\operatorname{SWAP}$ gates when converting between quantum representations of integers.</span></span>
<span data-ttu-id="f8e79-108">마찬가지로, 이전 섹션에서 형식의 형식이 `(Int, Int -> T)` 임의 액세스 컬렉션을 표시 하는 데 유용할 수 있으므로 <xref:Microsoft.Quantum.Arrays.LookupFunction> 함수는 배열 형식에서 이러한 형식을 생성 하는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-108">Similarly, we saw in the previous section that types of the form `(Int, Int -> T)` can be useful for representing random access collections, so the <xref:Microsoft.Quantum.Arrays.LookupFunction> function provides a convenient way of constructing such types from array types.</span></span>

### <a name="pairs"></a><span data-ttu-id="f8e79-109">문자짝</span><span class="sxs-lookup"><span data-stu-id="f8e79-109">Pairs</span></span> ###

<span data-ttu-id="f8e79-110">라고은 분해에의 한 튜플 액세스를 보완 하는 함수에 대 한 함수 스타일 표기법을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-110">The canon supports functional-style notation for pairs, complementing accessing tuples by deconstruction:</span></span>

```qsharp
let pair = (PauliZ, register); // type (Pauli, Qubit[])
ApplyToEach(H, Snd(pair)); // No need to deconstruct to access the register.
```

### <a name="arrays"></a><span data-ttu-id="f8e79-111">배열</span><span class="sxs-lookup"><span data-stu-id="f8e79-111">Arrays</span></span> ###

<span data-ttu-id="f8e79-112">라고에서는 배열을 조작 하기 위한 여러 함수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-112">The canon provides several functions for manipulating arrays.</span></span>
<span data-ttu-id="f8e79-113">이러한 함수는 형식 매개 변수화 되므로 모든 형식의 배열과 함께 사용할 수 있습니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="f8e79-113">These functions are type-parameterized, and thus can be used with arrays of any :::no-loc(Q#)::: type.</span></span>
<span data-ttu-id="f8e79-114">예를 들어, <xref:Microsoft.Quantum.Arrays.Reversed> 함수는 요소가 입력에서 역순으로 포함 된 새 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-114">For instance, the <xref:Microsoft.Quantum.Arrays.Reversed> function returns a new array whose elements are in reverse order from its input.</span></span>
<span data-ttu-id="f8e79-115">이를 사용 하 여 작업을 호출할 때 퀀텀 레지스터가 표시 되는 방식을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-115">This can be used to change how a quantum register is represented when calling operations:</span></span>

```qsharp
let leRegister = LittleEndian(register);
// QFT expects a BigEndian, so we can reverse before calling.
QFT(BigEndian(Reversed(leRegister!)));
// This is how the LittleEndianAsBigEndian function is implemented:
QFT(LittleEndianAsBigEndian(leRegister));
```

<span data-ttu-id="f8e79-116">마찬가지로 함수를 <xref:Microsoft.Quantum.Arrays.Subarray> 사용 하 여 배열 요소의 순서를 변경 하거나 하위 집합을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-116">Similarly, the <xref:Microsoft.Quantum.Arrays.Subarray> function can be used to reorder or take subsets of the elements of an array:</span></span>

```qsharp
// Applies H to qubits 2 and 5.
ApplyToEach(H, Subarray([2, 5], register));
```

<span data-ttu-id="f8e79-117">흐름 제어와 함께 사용 하는 경우와 같은 배열 조작 함수는 <xref:Microsoft.Quantum.Arrays.Zipped> 퀀텀 프로그램을 표현할 수 있는 강력한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-117">When combined with flow control, array manipulation functions such as <xref:Microsoft.Quantum.Arrays.Zipped> can provide a powerful way to express quantum programs:</span></span>

```qsharp
// Applies X₃ Y₁ Z₇ to a register of any size.
ApplyToEach(
    ApplyPauli(_, register),
    Map(
        EmbedPauli(_, _, Length(register)),
        Zipped([PauliX, PauliY, PauliZ], [3, 1, 7])
    )
);
```

## <a name="oracles"></a><span data-ttu-id="f8e79-118">Oracles</span><span class="sxs-lookup"><span data-stu-id="f8e79-118">Oracles</span></span> ##

<span data-ttu-id="f8e79-119">[단계 예측](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm) 및 [진폭 증폭](https://en.wikipedia.org/wiki/Amplitude_amplification) 홍보 자료에서 oracle의 개념은 자주 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-119">In the [phase estimation](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm) and [amplitude amplification](https://en.wikipedia.org/wiki/Amplitude_amplification) literature the concept of an oracle appears frequently.</span></span>
<span data-ttu-id="f8e79-120">여기서 oracle 이라는 용어는 다양 한 비트 집합에 적용 되는 블랙 박스 퀀텀 서브루틴을 나타내며 단계로 서 답변을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-120">Here the term oracle refers to a blackbox quantum subroutine that acts upon a set of qubits and returns the answer as a phase.</span></span>
<span data-ttu-id="f8e79-121">이 서브루틴은 다른 몇 가지 매개 변수와 함께 oracle을 허용 하는 퀀텀 알고리즘에 대 한 입력으로, 일련의 퀀텀 작업을 적용 하 고이 퀀텀 서브루틴에 대 한 호출을 기본 게이트 처럼 처리 하는 것으로 간주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-121">This subroutine often can be thought of as an input to a quantum algorithm that accepts the oracle, in addition to some other parameters, and applies a series of quantum operations and treating a call to this quantum subroutine as if it were a fundamental gate.</span></span>
<span data-ttu-id="f8e79-122">분명히 큰 알고리즘을 실제로 구현 하기 위해 oracle을 기본 게이트로 구체적으로 분해 해야 하지만 oracle을 호출 하는 알고리즘을 이해 하기 위해 이러한 분해는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-122">Obviously, in order to actually implement the larger algorithm a concrete decomposition of the oracle into fundamental gates must be provided but such a decomposition is not needed in order to understand the algorithm that calls the oracle.</span></span>
<span data-ttu-id="f8e79-123">에서 :::no-loc(Q#)::: 이 추상화는 작업을 첫 번째 클래스 값으로 사용 하 여 표현 됩니다. 이러한 작업은 블랙 박스 방식으로 퀀텀 알고리즘의 구현에 전달 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-123">In :::no-loc(Q#):::, this abstraction is represented by using that operations are first-class values, such that operations can be passed to implementations of quantum algorithms in a black-box manner.</span></span>
<span data-ttu-id="f8e79-124">또한 사용자 정의 형식은 형식이 안전한 방식으로 다양 한 oracle 표현의 레이블을 지정 하는 데 사용 되므로 실수로 다른 종류의 블랙 박스 작업을 conflate 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-124">Moreover, user-defined types are used to label the different oracle representations in a type-safe way, making it difficult to accidentally conflate different kinds of black box operations.</span></span>

<span data-ttu-id="f8e79-125">이러한 oracles는 [Grover의 검색](https://en.wikipedia.org/wiki/Grover%27s_algorithm) 및 퀀텀 시뮬레이션 알고리즘과 같은 유명한 예를 포함 하 여 다양 한 컨텍스트에서 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-125">Such oracles appear in a number of different contexts, including famous examples such as [Grover's search](https://en.wikipedia.org/wiki/Grover%27s_algorithm) and quantum simulation algorithms.</span></span>
<span data-ttu-id="f8e79-126">여기서는 두 가지 응용 프로그램 (진폭 증폭 및 단계 예측)에 필요한 oracles에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-126">Here we focus on the oracles needed for just two applications: amplitude amplification and phase estimation.</span></span>
<span data-ttu-id="f8e79-127">단계 예측을 진행 하기 전에 먼저 진폭 증폭 oracles에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-127">We will first discuss amplitude amplification oracles before proceeding to phase estimation.</span></span>

### <a name="amplitude-amplification-oracles"></a><span data-ttu-id="f8e79-128">진폭 증폭 Oracles</span><span class="sxs-lookup"><span data-stu-id="f8e79-128">Amplitude Amplification Oracles</span></span> ###

<span data-ttu-id="f8e79-129">진폭 증폭 알고리즘은 상태의 반사 시퀀스를 적용 하 여 초기 상태와 최종 상태 간의 회전을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-129">The amplitude amplification algorithm aims to perform a rotation between an initial state and a final state by applying a sequence of reflections of the state.</span></span>
<span data-ttu-id="f8e79-130">알고리즘이 작동 하려면 이러한 두 상태를 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-130">In order for the algorithm to function, it needs a specification of both of these states.</span></span>
<span data-ttu-id="f8e79-131">이러한 사양은 두 oracles에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-131">These specifications are given by two oracles.</span></span>
<span data-ttu-id="f8e79-132">이러한 oracles는 입력을 두 개의 공백, "대상" 하위 공간 및 "초기" 하위 공간으로 분리 하 여 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-132">These oracles work by breaking the inputs into two spaces, a "target" subspace and an "initial" subspace.</span></span>
<span data-ttu-id="f8e79-133">Oracles는 이러한 공간에 $ \pm $1 단계를 적용 하 여 Pauli 연산자가 두 공간을 식별 하는 방식과 유사 하 게 이러한 하위 공간을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-133">The oracles identify such subspaces, similar to how Pauli operators identify two spaces, by applying a $\pm 1$ phase to these spaces.</span></span>
<span data-ttu-id="f8e79-134">주요 차이점은이 응용 프로그램에서 이러한 공간을 절반으로 사용할 필요가 없다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-134">The main difference is that these spaces need not be half-spaces in this application.</span></span>
<span data-ttu-id="f8e79-135">또한 이러한 두 개의 하위 공간은 일반적으로 함께 사용할 수 없습니다. 두 공간의 멤버인 벡터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-135">Also note that these two subspaces are not usually mutually exclusive: there will be vectors that are members of both spaces.</span></span>
<span data-ttu-id="f8e79-136">이 값이 true가 아니면 진폭 증폭은 아무런 영향도 주지 않으므로 초기 하위 공간에서 0이 아닌 대상 하위 공간에 겹치지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-136">If this were not true then amplitude amplification would have no effect so we need the initial subspace to have non-zero overlap with the target subspace.</span></span>

<span data-ttu-id="f8e79-137">\_다음 작업을 수행 하도록 정의 된 진폭 증폭에 필요한 첫 번째 oracle이 $0을 $P 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-137">We will denote the first oracle that we need for amplitude amplification to be $P\_0$, defined to have the following action.</span></span>  <span data-ttu-id="f8e79-138">모든 상태 $ \ket{x} $의 "초기" 하위 공간 $P \_ 0 \ket{x} =-\ket{x} $ 이며이 하위 공간에 없는 모든 상태 $ \ket{y} $에 대해 \_ 0 \ket{y} = \ket{y} $ $P 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-138">For all states $\ket{x}$ in the "initial" subspace $P\_0 \ket{x} = -\ket{x}$ and for all states $\ket{y}$ that are not in this subspace we have $P\_0 \ket{y} = \ket{y}$.</span></span>
<span data-ttu-id="f8e79-139">대상 하위 공간 $P _1 $을 표시 하는 oracle은 정확히 동일한 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-139">The oracle that marks the target subspace, $P_1$, takes exactly the same form.</span></span>
<span data-ttu-id="f8e79-140">대상 하위 공간의 모든 상태 $ \ket{x} $에 대해 (즉, 출력 하는 알고리즘에 대 한 모든 상태) _1 \ k {x} =-\ket{x} $를 $P 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-140">For all states $\ket{x}$ in the target subspace (i.e., for all states that you'd like the algorithm to output), $P_1\ket{x} = -\ket{x}$.</span></span>
<span data-ttu-id="f8e79-141">마찬가지로 대상 하위 공간에 없는 모든 상태 $ \ket{y} $에 대해 _1 \ k {y} = \ket{y} $를 $P 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-141">Similarly, for all states $\ket{y}$ that are not in the target subspace $P_1\ket{y} = \ket{y}$.</span></span>
<span data-ttu-id="f8e79-142">그런 다음이 두 반사를 결합 하 여 진폭 시행의 단일 단계를 구성 하는 연산자를 형성 합니다. $Q = P_0 P_1 $. 여기서 전체 빼기 기호는 제어 되는 응용 프로그램에서 고려 하는 경우에만 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-142">These two reflections are then combined to form an operator that enacts a single step of amplitude amplification, $Q = -P_0 P_1$, where the overall minus sign is only important to consider in controlled applications.</span></span>
<span data-ttu-id="f8e79-143">그런 다음 초기 하위 공간에 있는 $ \ket{\psi} $ 초기 상태를 수행 하 고 $ \ket{\psi} \mapsq ^ m \ket{\psi} $를 수행 하 여 진폭 증폭을 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-143">Amplitude amplification then proceeds by taking an initial state, $\ket{\psi}$ that is in the initial subspace and then performs $\ket{\psi} \mapsto Q^m \ket{\psi}$.</span></span>
<span data-ttu-id="f8e79-144">이러한 반복을 수행 하는 경우에는 표시 된 공간을 사용 하 여 $ \sin ^ 2 (\sin) $ 겹치는 초기 상태로 시작 하는 경우 $2m 다음 $m에이 겹치는 항목은 $ \sin ^ 2 ([+ 1] \sin) $가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-144">Performing such an iteration guarantees that if one starts with an initial state that has overlap $\sin^2(\theta)$ with the marked space then after $m$ iterations this overlap becomes $\sin^2([2m + 1] \theta)$.</span></span>
<span data-ttu-id="f8e79-145">따라서 일반적 $m으로 $ [2m + 1] \theta = \ pi/2 $;를 사용 하 여 $ [ 그러나 이러한 고정 선택은 고정 소수점 진폭 증폭과 같은 일부 형태의 진폭 증폭에는 중요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-145">We therefore typically wish to choose $m$ to be a free parameter such that $[2m+1]\theta = \pi/2$; however, such rigid choices are not as important for some forms of amplitude amplification such as fixed point amplitude amplification.</span></span>
<span data-ttu-id="f8e79-146">이 프로세스를 통해 표시 함수에 대 한 쿼리 수를 quadratically를 사용 하 여 표시 된 하위 공간에서 상태를 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-146">This process allows us to prepare a state in the marked subspace using quadratically fewer queries to the marking function and the state preparation function than would be possible on a strictly classical device.</span></span>
<span data-ttu-id="f8e79-147">이러한 이유로, 진폭 증폭은 많은 퀀텀 컴퓨팅 응용 프로그램에 대 한 중요 한 빌딩 블록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-147">This is why amplitude amplification is a significant building block for many applications of quantum computing.</span></span>

<span data-ttu-id="f8e79-148">알고리즘을 사용 하는 방법을 이해 하려면 oracles 생성을 제공 하는 예제를 제공 하는 것이 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-148">In order to understand how to use the algorithm, it is useful to provide an example that gives a construction of the oracles.</span></span>  <span data-ttu-id="f8e79-149">이 설정에서 데이터베이스 검색에 대 한 Grover 알고리즘을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-149">Consider performing Grover's algorithm for database searches in this setting.</span></span>
<span data-ttu-id="f8e79-150">Grover의 목표 검색에서 목표는 상태 $ \ket{+} ^ {\otimes n} = H ^ {\otimes n} \ket {0} $를 표시 된 많은 상태 중 하나로 변환 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-150">In Grover's search the goal is to transform the state $\ket{+}^{\otimes n} = H^{\otimes n} \ket{0}$ into one of (potentially) many marked states.</span></span>
<span data-ttu-id="f8e79-151">보다 간소화 하기 위해 표시 된 상태만 $ \ket $ 인 경우만 살펴보겠습니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="f8e79-151">To further simplify, let's just look at the case where the only marked state is $\ket{0}$.</span></span>
<span data-ttu-id="f8e79-152">그런 다음 두 개의 oracles를 디자인 했습니다. 첫 번째 상태 $ \ket{+} ^ {\otimes n} $만 빼기 기호로 표시 하 고 다른 하나는 표시 된 상태 $ \ket {0} $를 빼기 기호로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-152">Then we have design two oracles: one that only marks the initial state $\ket{+}^{\otimes n}$ with a minus sign and another that marks the marked state $\ket{0}$ with a minus sign.</span></span>
<span data-ttu-id="f8e79-153">다음 처리 작업을 사용 하 여 canon의 제어 흐름 작업을 사용 하 여 두 번째 게이트를 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-153">The latter gate can be implemented using the following process operation, by using the control flow operations in the canon:</span></span>

```qsharp
operation ReflectAboutAllZeros(register : Qubit[]) : Unit 
is Adj + Ctl {

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);

    // Apply an $n-1$ controlled $Z$-gate to the $n^{\text{th}}$ qubit.
    // This gate will lead to a sign flip if and only if every qubit is
    // $1$, which happens only if each of the qubits were $0$ before step 1.
    Controlled Z(Most(register), Tail(register));

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);
}
```

<span data-ttu-id="f8e79-154">이 oracle은 작업의 특별 한 경우입니다 <xref:Microsoft.Quantum.Canon.RAll1> .이 경우 리플렉션 사례 $ \a= \phi $ 대신 임의의 단계로 회전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-154">This oracle is then a special case of the <xref:Microsoft.Quantum.Canon.RAll1> operation, which allows for rotating by an arbitrary phase instead of the reflection case $\phi = \pi$.</span></span>
<span data-ttu-id="f8e79-155">이 경우 `RAll1` 는 prelude 작업과 유사 하며,이 <xref:Microsoft.Quantum.Intrinsic.R1> 는 단일가 나 비트 상태 $ \ket $ 대신 $ \ket{11\cdots1} $를 회전 {1} 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-155">In this case, `RAll1` is similar to the <xref:Microsoft.Quantum.Intrinsic.R1> prelude operation, in that it rotates about $\ket{11\cdots1}$ instead of the single-qubit state $\ket{1}$.</span></span>

<span data-ttu-id="f8e79-156">초기 하위 공간을 표시 하는 oracle을 유사 하 게 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-156">The oracle that marks the initial subspace can be constructed similarly.</span></span>
<span data-ttu-id="f8e79-157">의사 코드:</span><span class="sxs-lookup"><span data-stu-id="f8e79-157">In pseudocode:</span></span>

1. <span data-ttu-id="f8e79-158">모든 고 비트에 $H $ 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-158">Apply $H$ gates to every qubit.</span></span>
2. <span data-ttu-id="f8e79-159">모든 고 비트에 $X $ 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-159">Apply $X$ gates to every qubit.</span></span>
3. <span data-ttu-id="f8e79-160">$N ^ {\text{th}} $ stbit에 $n-$1 제어 $Z $ gate를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-160">Apply an $n-1$ controlled $Z$-gate to the $n^{\text{th}}$ qubit.</span></span>
4. <span data-ttu-id="f8e79-161">모든 고 비트에 $X $ 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-161">Apply $X$ gates to every qubit.</span></span>
5. <span data-ttu-id="f8e79-162">모든 고 비트에 $H $ 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-162">Apply $H$ gates to every qubit.</span></span>

<span data-ttu-id="f8e79-163">이번에는 <xref:Microsoft.Quantum.Canon.ApplyWith> 위에서 설명한 작업과 함께를 사용 하는 방법도 보여 줍니다 <xref:Microsoft.Quantum.Canon.RAll1> .</span><span class="sxs-lookup"><span data-stu-id="f8e79-163">This time, we also demonstrate using <xref:Microsoft.Quantum.Canon.ApplyWith> together with the <xref:Microsoft.Quantum.Canon.RAll1> operation discussed above:</span></span>

```qsharp
operation ReflectAboutInitial(register : Qubit[]) : Unit
is Adj + Ctl {
    ApplyWithCA(ApplyToEach(H, _), ApplyWith(ApplyToEach(X, _), RAll1(_, PI()), _), register);
}
```

<span data-ttu-id="f8e79-164">그런 다음 이러한 두 oracles를 결합 하 여 두 상태 사이를 회전 하 고 $ \ket{+} ^ {\otimes n} $를 $ \ket $로 변형 하 여 $ {0} \sqrt{2 ^ n}에 비례 하는 Hadamard 게이트의 여러 계층을 사용할 수 있습니다. (ie $m \otimes \sqrt{2 ^ n} $) 및 {0} 결과 $0 $가 관찰 될 때까지 초기 상태를 준비 하 고 측정 하 여 $ \ket $ 상태를 명확 하 게 준비 하는 데 필요한 약 $2 ^ n $ 계층에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-164">We can then combine these two oracles together to rotate between the two states and deterministically transform $\ket{+}^{\otimes n}$ to $\ket{0}$ using a number of layers of Hadamard gates that is proportional to $\sqrt{2^n}$ (ie $m\propto \sqrt{2^n}$) versus the roughly $2^n$ layers that would be needed to non-deterministically prepare the $\ket{0}$ state by preparing and measuring the initial state until the outcome $0$ is observed.</span></span>

### <a name="phase-estimation-oracles"></a><span data-ttu-id="f8e79-165">단계 추정 Oracles</span><span class="sxs-lookup"><span data-stu-id="f8e79-165">Phase Estimation Oracles</span></span> ###

<span data-ttu-id="f8e79-166">단계 예측의 경우 oracles는 다소 자연스럽 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-166">For phase estimation the oracles are somewhat more natural.</span></span>
<span data-ttu-id="f8e79-167">단계 추정의 목표는 단일 행렬의 고유 값에서 샘플링할 수 있는 서브루틴을 디자인 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-167">The aim in phase estimation is to design a subroutine that is capable of sampling from the eigenvalues of a unitary matrix.</span></span>
<span data-ttu-id="f8e79-168">이 메서드는 화학 및 자재 과학의 많은 물리적 문제를 발생 시키기 때문에 퀀텀 시뮬레이션의 필수적인 기능입니다. 이러한 고유 값은 주력할의 단계 다이어그램에 대 한 중요 한 정보를 제공 하는 퀀텀 시스템의 그라운드 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-168">This method is indispensable in quantum simulation because for many physical problems in chemistry and material science these eigenvalues give the ground-state energies of quantum systems which provides us valuable information about the phase diagrams of materials and reaction dynamics for molecules.</span></span>
<span data-ttu-id="f8e79-169">단계 추정의 모든 버전에는 입력이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-169">Every flavor of phase estimation needs an input unitary.</span></span>
<span data-ttu-id="f8e79-170">이는 두 가지 유형의 oracles 중 하나로 설명 되는 일반적으로입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-170">This unitary is customarily described by one of two types of oracles.</span></span>

> [!TIP]
> <span data-ttu-id="f8e79-171">아래에 설명 된 두 oracle 형식은 모두 샘플에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-171">Both of the oracle types described below are covered in the samples.</span></span>
> <span data-ttu-id="f8e79-172">연속 쿼리 oracles 대해 자세히 알아보려면 [ **PhaseEstimation** 샘플](https://github.com/microsoft/Quantum/tree/main/samples/characterization/phase-estimation)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8e79-172">To learn more about continuous query oracles, please see the [**PhaseEstimation** sample](https://github.com/microsoft/Quantum/tree/main/samples/characterization/phase-estimation).</span></span>
> <span data-ttu-id="f8e79-173">불연속 쿼리 oracles에 대해 자세히 알아보려면 [ **IsingPhaseEstimation** 샘플](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/phase-estimation)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8e79-173">To learn more about discrete query oracles, please see the [**IsingPhaseEstimation** sample](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/phase-estimation).</span></span>

<span data-ttu-id="f8e79-174">Oracle의 첫 번째 유형은 개별 쿼리를 호출 하 고 사용자 정의 유형을 사용 하 여 표시 하는 oracle은 <xref:Microsoft.Quantum.Oracles.DiscreteOracle> 단일 행렬을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-174">The first type of oracle, which we call a discrete query oracle and represent with the user-defined type <xref:Microsoft.Quantum.Oracles.DiscreteOracle>, simply involves a unitary matrix.</span></span>
<span data-ttu-id="f8e79-175">$U $가 예측 하려는 고유 값의 단일 인 경우 $U $에 대 한 oracle은 단순히 $U $를 구현 하는 서브루틴에 대 한 독립 실행형입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-175">If $U$ is the unitary whose eigenvalues we wish to estimate then the oracle for $U$ is simply a stand-in for a subroutine that implements $U$.</span></span>
<span data-ttu-id="f8e79-176">예를 들어, $ $U를 사용 하 여 진폭에 대해 앞에서 정의한 oracle $Q $를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-176">For example, one could take $U$ to be the oracle $Q$ defined above for amplitude estimation.</span></span>
<span data-ttu-id="f8e79-177">이 행렬의 고유 값를 사용 하 여 초기 및 대상 상태 $ \sin ^ 2 (\sin) $ 사이에서 겹치는 항목을 추정 하는 데 사용할 수 있습니다. 그 외에도 quadratically를 사용 하는 경우 보다 작은 샘플을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-177">The eigenvalues of this matrix can be used to estimate the overlap between the initial and target states, $\sin^2(\theta)$, using quadratically fewer samples than one would need otherwise.</span></span>
<span data-ttu-id="f8e79-178">이는 Grover oracle $Q $를 사용 하 여 진폭 추정의 모니커를 입력으로 적용 하는 단계 예측의 적용을 획득 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-178">This earns the application of phase estimation using the Grover oracle $Q$ as input the moniker of amplitude estimation.</span></span>
<span data-ttu-id="f8e79-179">퀀텀 metrology에서 널리 사용 되는 또 다른 일반적인 응용 프로그램에는 작은 회전 각도를 계산 하는 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-179">Another common application, widely used in quantum metrology, involves estimating a small rotation angle.</span></span>
<span data-ttu-id="f8e79-180">즉, \theta ($R _z) $ 형식의 알 수 없는 회전 게이트를 위해 $ \theta $를 추정 하고자 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-180">In other words, we wish to estimate $\theta$ for an unknown rotation gate of the form $R_z(\theta)$.</span></span>
<span data-ttu-id="f8e79-181">이러한 경우, 게이트에서 $ \theta $의이 고정 된 값을 학습 하기 위해 상호 작용 하는 서브루틴이 $ $ \begin{align} U & = R_z (\theta) \\ \\ & = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {a\ 테타/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="f8e79-181">In such cases, the subroutine that we would interact with in order to learn this fixed value of $\theta$ for the gate is $$ \begin{align} U & = R_z(\theta) \\\\ & = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i\theta/2} \end{bmatrix}.</span></span>
<span data-ttu-id="f8e79-182">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="f8e79-182">\end{align} $$</span></span>

<span data-ttu-id="f8e79-183">단계 예측에 사용 되는 oracle의 두 번째 유형은 형식으로 표현 되는 연속 쿼리 oracle입니다 <xref:Microsoft.Quantum.Oracles.ContinuousOracle> .</span><span class="sxs-lookup"><span data-stu-id="f8e79-183">The second type of oracle used in phase estimation is the continuous query oracle, represented by the <xref:Microsoft.Quantum.Oracles.ContinuousOracle> type.</span></span>
<span data-ttu-id="f8e79-184">단계 예측을 위한 연속 쿼리 oracle은 $U (t) $를 사용 합니다. 여기서 $t $은 알려진 일반적으로입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-184">A continuous query oracle for phase estimation takes the form $U(t)$ where $t$ is a classically known real number.</span></span>
<span data-ttu-id="f8e79-185">$를 고정 된 단일 형식으로 $U 수 있는 경우 연속 쿼리 oracle은 $U (t) = U ^ t $ 형식으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-185">If we let $U$ be a fixed unitary then the continuous query oracle takes the form $U(t) = U^t$.</span></span>
<span data-ttu-id="f8e79-186">이렇게 하면 불연속 쿼리 모델에서 직접 구현할 수 없는 $ \sqrt{U} $와 같은 행렬을 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-186">This allows us to query matrices such as $\sqrt{U}$, which could not be implemented directly in the discrete query model.</span></span>

<span data-ttu-id="f8e79-187">이 유형의 oracle은 특정 단일 사용자를 검색 하지 않고 단일의 생성기 속성을 배우는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-187">This type of oracle is valuable when you're not probing a particular unitary, but rather wish to learn the properties of the generator of the unitary.</span></span>
<span data-ttu-id="f8e79-188">예를 들어 동적 퀀텀 시뮬레이션에서 목표는 Hermitian 행렬 $H $ 및 진화 시간 $t $에 대해 $U (t) = e ^ {-i H t} $와 긴밀 하 게 근접 한 퀀텀 회로를 고안 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-188">For example, in dynamical quantum simulation the goal is to devise quantum circuits that closely approximate $U(t)=e^{-i H t}$ for a Hermitian matrix $H$ and evolution time $t$.</span></span>
<span data-ttu-id="f8e79-189">$U (t) $의 고유 값는 $H $의 고유 값와 직접 관련 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-189">The eigenvalues of $U(t)$ are directly related to the eigenvalues of $H$.</span></span>
<span data-ttu-id="f8e79-190">이를 확인 하려면 $H $: $H \ket{E} = E\ket {E} $ 인 것으로 간주 합니다. 그러면 $U (t) \ket{E} = e ^ {i\eml\ k {E} = e ^ {-iEt} \ket{E} $와 같은 매트릭스 지 수의 전원 계열 정의에서 쉽게 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-190">To see this, consider an eigenvector of $H$: $H \ket{E} = E\ket{E}$ then it is easy to see from the power-series definition of the matrix exponential that $U(t) \ket{E} = e^{i\phi}\ket{E}= e^{-iEt}\ket{E}$.</span></span>
<span data-ttu-id="f8e79-191">따라서 $U (t) $의 eigenphase를 예측 하면 eigenvector $ \ket{E} $가 단계 추정 알고리즘에 입력 된 것으로 가정 하 고 eigenphase $E $가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-191">Thus estimating the eigenphase of $U(t)$ gives the eigenvalue $E$ assuming the eigenvector $\ket{E}$ is input into the phase estimation algorithm.</span></span>
<span data-ttu-id="f8e79-192">그러나이 경우에는 $t $ 값을 사용자의 판단에 따라 선택할 수 있습니다 .이 값은 $t의 충분 한 작은 값이 있으므로 eigenvalue $E $는 $E =-\ o s o/t $를 통해 고유 하 게 반전 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-192">However, in this case the value $t$ can be chosen at the user's discretion since for any sufficiently small value of $t$ the eigenvalue $E$ can be uniquely inverted through $E=-\phi/t$.</span></span>
<span data-ttu-id="f8e79-193">퀀텀 시뮬레이션 메서드는 소수 부분 진화를 수행 하는 기능을 제공 하기 때문에, 특히 불연속 쿼리 모델이 정수 $j에 적용 되는 $U ^ j $ 형식의 unitaries만 허용 하는 반면 연속 쿼리 oracle을 사용 하면 실제 값 $t $에 대해 $U ^ t $ 형식의 근사치를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-193">Since quantum simulation methods provide the ability to perform a fractional evolution, this grants phase estimation algorithms an additional freedom when querying the unitary, specifically while the discrete query model allows only unitaries of the form $U^j$ to applied for integer $j$ the continuous query oracle allows us to approximate unitaries of the form $U^t$ for any real valued $t$.</span></span>
<span data-ttu-id="f8e79-194">이는 $E $;에 대 한 대부분의 정보를 제공 하는 실험을 정확 하 게 선택할 수 있기 때문에, 효율성의 마지막 온스를 모두 단계 예측 알고리즘에서 잡은 것이 중요 합니다. 반면 불연속 쿼리를 기반으로 하는 메서드는 알고리즘에서 가장 적합 한 정수 수의 쿼리를 선택 하 여 해당 메서드를 손상 된 상태로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-194">This is important to squeeze every last ounce of efficiency out of phase estimation algorithms because it allows us to choose precisely the experiment that would provide the most information about $E$; whereas methods based on discrete queries must make do with compromising by choosing the best integer number of queries in the algorithm.</span></span>

<span data-ttu-id="f8e79-195">이에 대 한 구체적인 예로, 출입문의 회전 각도는 아니지만 회전 퀀텀 시스템의 procession 빈도를 추정 하는 문제를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-195">As a concrete example of this, consider the problem of estimating not the rotation angle of a gate but the procession frequency of a rotating quantum system.</span></span>
<span data-ttu-id="f8e79-196">이러한 퀀텀 dynamics를 설명 하는 단일는 진화 $t 시간에 대 한 $U (t) = R_z (2 \ 오메가 t) $이 고 알 수 없는 frequency $ \000s $입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-196">The unitary that describes such quantum dynamics is $U(t)=R_z(2\omega t)$ for evolution time $t$ and unknown frequency $\omega$.</span></span>
<span data-ttu-id="f8e79-197">이 컨텍스트에서는 단일 $R _z $ gate를 사용 하 여 모든 $t $에 대 한 $U (t) $를 시뮬레이션할 수 있으며,이 경우에는 불연속 쿼리로만 제한 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-197">In this context, we can simulate $U(t)$ for any $t$ using a single $R_z$ gate and as such do not need to restrict ourselves to only discrete queries to the unitary.</span></span>
<span data-ttu-id="f8e79-198">이러한 연속 모델에는 또한 로그 함수의 분기 컷에 의해 마스킹 될 수 있는 단계 정보는 $t $의 비 비례하여 값에서 수행 되는 실험 결과에서 표시 될 수 있기 때문에 연속 쿼리를 사용 하는 단계 예측 프로세스에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-198">Such a continuous model also has the property that frequencies greater than $2\pi$ can be learned from phase estimation processes that use continuous queries because phase information that would otherwise be masked by the branch-cuts of the logarithm function can be revealed from the results of experiments performed on non-commensurate values of $t$.</span></span>
<span data-ttu-id="f8e79-199">따라서 단계 예측 oracle의 이러한 연속 쿼리 모델과 같은 문제의 경우에는 적합 하지 않지만 불연속 쿼리 모델에도 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-199">Thus for problems such as this continuous query models for the phase estimation oracle are not only appropriate but are also preferable to the discrete query model.</span></span>
<span data-ttu-id="f8e79-200">이러한 이유로 :::no-loc(Q#)::: 두 쿼리 형태 모두에 대 한 기능을 제공 하 고 사용자에 게 제공 하 여 요구 사항 및 사용 가능한 oracle 유형에 맞는 단계 추정 알고리즘을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-200">For this reason :::no-loc(Q#)::: has functionality for both forms of queries and leave it to the user to decide upon a phase estimation algorithm to fit their needs and the type of oracle that is available.</span></span>

## <a name="dynamical-generator-modeling"></a><span data-ttu-id="f8e79-201">동적 생성기 모델링</span><span class="sxs-lookup"><span data-stu-id="f8e79-201">Dynamical Generator Modeling</span></span> ##

<span data-ttu-id="f8e79-202">시간 이동의 생성기는 시간에 따라 상태가 어떻게 향상 됨을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-202">Generators of time-evolution describe how states evolve through time.</span></span> <span data-ttu-id="f8e79-203">예를 들어 퀀텀 상태의 dynamics $ \ket{\psi} $은 Schrödinger 수식 $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = H \ket{\psi (t)}, \end{align} $ $ $H (Hermitian)를 동작의 생성기로 사용 하 여 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-203">For instance, the dynamics of a quantum state $\ket{\psi}$ is governed by the Schrödinger equation $$ \begin{align} i\frac{d \ket{\psi(t)}}{d t} & = H \ket{\psi(t)}, \end{align} $$ with a Hermitian matrix $H$, known as the Hamiltonian, as the generator of motion.</span></span> <span data-ttu-id="f8e79-204">지정 된 초기 상태 $ \ket{\psi (0)} $ at time $t = $0,이 수식에 대 한 공식 솔루션 ($t $)은 원칙적으로 $ $ \begin{align} \ket{\psi (t)} = U (t) \ket{\psi (0)}, \end{align} $ $로 작성 될 수 있습니다. 여기서 행렬 지 수 $U (t) = e ^ {-i H t} $는 단일 시간 진화 연산자 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-204">Given an initial state $\ket{\psi(0)}$ at time $t=0$, the formal solution to this equation at time $t$ may be, in principle, written $$ \begin{align} \ket{\psi(t)} = U(t)\ket{\psi(0)}, \end{align} $$ where the matrix exponential $U(t)=e^{-i H t}$ is known as the unitary time-evolution operator.</span></span> <span data-ttu-id="f8e79-205">다음에서이 폼의 생성기에 중점을 두고 있기는 하지만,이 개념은 개방형 퀀텀 시스템의 시뮬레이션 또는 보다 복잡 한 차등 방정식과 같이 더 광범위 하 게 적용 된다는 것을 강조 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-205">Though we focus on generators of this form in the following, we emphasize that the concept applies more broadly, such as to the simulation of open quantum systems, or to more abstract differential equations.</span></span>

<span data-ttu-id="f8e79-206">동적 시뮬레이션의 기본 목표는 퀀텀 컴퓨터의 비트 단위에서 인코딩된 일부 퀀텀 상태에서 시간 진화 연산자를 구현 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-206">A primary goal of dynamical simulation is to implement the time-evolution operator on some quantum state encoded in qubits of a quantum computer.</span></span>  <span data-ttu-id="f8e79-207">대부분의 경우 Hamiltonian를 몇 $d $ 보다 더 간단한 용어로 나눌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-207">In many cases, the Hamiltonian may be broken into a sum of some $d$ simpler terms</span></span>

<span data-ttu-id="f8e79-208">$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} H_j, \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="f8e79-208">$$ \begin{align} H & = \sum^{d-1}_{j=0} H_j, \end{align} $$</span></span>

<span data-ttu-id="f8e79-209">각 용어에의 한 시간-진화는 퀀텀 컴퓨터에서 쉽게 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-209">where time-evolution by each term alone is easy to implement on a quantum computer.</span></span> <span data-ttu-id="f8e79-210">예를 들어 $H _j $가 valbit 레지스터의 첫 번째 및 두 번째 요소에 대해 작동 하는 _1X_2 $ 연산자 $X 하는 경우 `qubits` 언제 든 지 시간을 기준으로 시간을 증가 시킬 수 있습니다. $t $는 서명을 포함 하는 작업을 호출 하 여 간단히 구현할 수 있습니다 `Exp([PauliX,PauliX], t, qubits[1..2])` `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="f8e79-210">For instance, if $H_j$ is a Pauli $X_1X_2$ operator acting on the 1st and 2nd elements of the qubit register `qubits`, time-evolution by it for any time $t$ may be implemented simply by calling the operation `Exp([PauliX,PauliX], t, qubits[1..2])`, which has signature `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="f8e79-211">Hamiltonian 시뮬레이션의 뒷부분에서 설명 했 듯이, 한 가지 해결 방법은 $H $에서 간단한 작업의 시퀀스로 대략적인 시간 진화를 수행 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-211">As discussed later in Hamiltonian Simulation, one solution then is to approximate time-evolution by $H$ with a sequence of simpler operations</span></span>

<span data-ttu-id="f8e79-212">$ $ \begin{align} U (t) & = \left (e ^ {-iH \_ 0 t/r} e ^ {-ih \_ 1 t/r} \c도트 e ^ {-ih \_ {d-1} t/r} \left) ^ {r} + \mathcal{O} (d ^ 2 \ max_j \\ | H \_ j \\ | ^ 2 t ^ 2/r), \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="f8e79-212">$$ \begin{align} U(t) & = \left( e^{-iH\_0 t / r} e^{-iH\_1 t / r} \cdots e^{-iH\_{d-1} t / r} \right)^{r} + \mathcal{O}(d^2 \max_j \\|H\_j\\|^2 t^2/r), \end{align} $$</span></span>

<span data-ttu-id="f8e79-213">여기서 정수 $r > $0는 근사값 오류를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-213">where the integer $r > 0$ controls the approximation error.</span></span>

<span data-ttu-id="f8e79-214">동적 생성기 모델링 라이브러리는 간단한 생성기를 기준으로 복잡 한 생성기를 위한 프레임 워크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-214">The dynamical generator modeling library provides a framework for systematically encoding complicated generators in terms of simpler generators.</span></span> <span data-ttu-id="f8e79-215">이러한 설명은 시뮬레이션 라이브러리를 사용 하 여 선택의 시뮬레이션 알고리즘에의 한 시간 진화를 구현 하는 것과 같은 여러 세부 정보가 자동으로 처리 되는 것을 말합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-215">Such a description may then be passed to, say, the simulation library to implement time-evolution by a simulation algorithm of choice, with many details automatically taken care of.</span></span>

> [!TIP]
> <span data-ttu-id="f8e79-216">아래에 설명 된 동적 생성기 라이브러리는 샘플에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-216">The dynamical generator library described below is covered in the samples.</span></span> <span data-ttu-id="f8e79-217">Ising 모델을 기반으로 하는 예제는 [ **Isinggenerators** 샘플](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/generators)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8e79-217">For an example based on the Ising model, please see the [**IsingGenerators** sample](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/generators).</span></span>
> <span data-ttu-id="f8e79-218">분자 Hydrogen를 기반으로 하는 예제는 [**H2SimulationCmdLine**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/command-line) 및 [**H2SimulationGUI**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/gui) 샘플을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8e79-218">For an example based on molecular Hydrogen, please see the [**H2SimulationCmdLine**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/command-line) and [**H2SimulationGUI**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/gui) samples.</span></span>

### <a name="complete-description-of-a-generator"></a><span data-ttu-id="f8e79-219">생성기의 전체 설명</span><span class="sxs-lookup"><span data-stu-id="f8e79-219">Complete Description of a Generator</span></span> ###

<span data-ttu-id="f8e79-220">최상위 수준에서 Hamiltonian에 대 한 전체 설명은 `EvolutionGenerator` 두 개의 구성 요소가 포함 된 사용자 정의 형식에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-220">At the top level, a complete description of a Hamiltonian is contained in the `EvolutionGenerator` user-defined type which has two components.:</span></span>

```qsharp
newtype EvolutionGenerator = (EvolutionSet, GeneratorSystem);
```

<span data-ttu-id="f8e79-221">`GeneratorSystem`사용자 정의 형식은 Hamiltonian에 대 한 기존 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-221">The `GeneratorSystem` user-defined type is a classical description of the Hamiltonian.</span></span>

```qsharp
newtype GeneratorSystem = (Int, (Int -> GeneratorIndex));
```

<span data-ttu-id="f8e79-222">튜플의 첫 번째 요소는 `Int` Hamiltonian의 용어 $d $ 수를 저장 하 고, 두 번째 요소는 `(Int -> GeneratorIndex)` \{ \} `GeneratorIndex` Hamiltonian의 각 기본 용어를 고유 하 게 식별 하는 사용자 정의 형식에 $0, 1,..., d-1 $의 정수 인덱스를 매핑하는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-222">The first element `Int` of the tuple stores the number of terms $d$ in the Hamiltonian, and the second element `(Int -> GeneratorIndex)` is a function that maps an integer index in $\{0,1,...,d-1\}$ to a `GeneratorIndex` user-defined type which uniquely identifies each primitive term in the Hamiltonian.</span></span> <span data-ttu-id="f8e79-223">Hamiltonian의 용어 컬렉션을 배열이 아니라 함수로 표현 하 여의 `GeneratorIndex[]` 즉시 계산을 수행할 수 있습니다 .이는 `GeneratorIndex` 많은 수의 용어로 Hamiltonians를 설명할 때 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-223">Note that by expressing the collection of terms in the Hamiltonian as a function rather than as an array `GeneratorIndex[]`, this allows for on-the-fly computation of the `GeneratorIndex` which is especially useful when describing Hamiltonians with a large number of terms.</span></span>

<span data-ttu-id="f8e79-224">매우에 의해 식별 되는 기본 용어에 대 한 규칙을 적용 하는 것 `GeneratorIndex` 은 쉽지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-224">Crucially, we do not impose a convention on what primitive terms identified by the `GeneratorIndex` are easy-to-simulate.</span></span> <span data-ttu-id="f8e79-225">예를 들어, 기본 용어는 위에서 설명한 대로 Pauli 연산자 일 수 있지만, 일반적으로 퀀텀 화학 시뮬레이션에서 사용 되는 Fermionic annihilation 및 만들기 연산자 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-225">For instance, primitive terms could be Pauli operators as discussed above, but they could also be Fermionic annihilation and creation operators commonly used in quantum chemistry simulation.</span></span> <span data-ttu-id="f8e79-226">즉,가 `GeneratorIndex` 가리키는 용어의 시간 혁신을 퀀텀 회로로 구현할 수 있으므로는 의미가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-226">By itself, a `GeneratorIndex` is meaningless as it does not describe how time-evolution by the term it points to may be implemented as a quantum circuit.</span></span>

<span data-ttu-id="f8e79-227">`EvolutionSet` `GeneratorIndex` 일부 정식 집합에서 가져온 임의의를 퀀텀 회로로 표현 된 단일 연산자 ()로 매핑하는 사용자 정의 형식을 지정 하 여이를 확인 합니다 `EvolutionUnitary` .</span><span class="sxs-lookup"><span data-stu-id="f8e79-227">This is resolved by specifying an `EvolutionSet` user-defined type that maps any `GeneratorIndex`, drawn from some canonical set, to a unitary operator, the `EvolutionUnitary`, expressed as a quantum circuit.</span></span> <span data-ttu-id="f8e79-228">는 `EvolutionSet` 이 구성 되는 방식에 대 한 규칙을 정의 하 `GeneratorIndex` 고 가능한 집합을 정의 합니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="f8e79-228">The `EvolutionSet` defines the convention of how a `GeneratorIndex` is structured, and also defines the set of possible `GeneratorIndex`.</span></span>

```qsharp
newtype EvolutionSet = (GeneratorIndex -> EvolutionUnitary);
```

### <a name="pauli-operator-generators"></a><span data-ttu-id="f8e79-229">Pauli 연산자 생성기</span><span class="sxs-lookup"><span data-stu-id="f8e79-229">Pauli Operator Generators</span></span> ###

<span data-ttu-id="f8e79-230">구체적이 고 유용한 생성기 예제는 각각 다른 계수를 사용 하 여 Pauli 연산자의 합계인 Hamiltonians입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-230">A concrete and useful example of generators are Hamiltonians that are a sum of Pauli operators, each possibly with a different coefficient.</span></span>
<span data-ttu-id="f8e79-231">$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} a_j H_j, \end{align} $ $ 여기서 각 $ \sum H_j $는 이제 Pauli 그룹에서 그려집니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-231">$$ \begin{align} H & = \sum^{d-1}_{j=0} a_j H_j, \end{align} $$ where each $\hat H_j$ is now drawn from the Pauli group.</span></span> <span data-ttu-id="f8e79-232">이러한 시스템의 경우 `PauliEvolutionSet()` `EvolutionSet` Pauli 그룹의 요소와 계수를에 의해 식별 되는 방법에 대 한 규칙을 정의 하는 형식의를 제공 합니다. 여기에는 `GeneratorIndex` 다음과 같은 시그니처가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-232">For such systems, we provide the `PauliEvolutionSet()` of type `EvolutionSet` that defines a convention for how an element of the Pauli group and a coefficient may be identified by a `GeneratorIndex`, which has the following signature.</span></span>

```qsharp
newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```

<span data-ttu-id="f8e79-233">이 인코딩에서 첫 번째 매개 변수는 `Int[]` Pauli 문자열을 지정 합니다. 여기서 $ \Hat I\rightarrow $0, $ \Hat X\rightarrow $1, $ \Hat Y\rightarrow $2 및 $ \Hat Z\rightarrow $3입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-233">In our encoding, the first parameter `Int[]` specifies a Pauli string, where $\hat I\rightarrow 0$, $\hat X\rightarrow 1$, $\hat Y\rightarrow 2$, and $\hat Z\rightarrow 3$.</span></span> <span data-ttu-id="f8e79-234">두 번째 매개 변수는 `Double[]` Hamiltonian에서 Pauli 문자열의 계수를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-234">The second parameter `Double[]` stores the coefficient of the Pauli string in the Hamiltonian.</span></span> <span data-ttu-id="f8e79-235">이 배열의 첫 번째 요소만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-235">Note that only the first element of this array is used.</span></span> <span data-ttu-id="f8e79-236">세 번째 매개 변수는 `Int[]` 이 Pauli 문자열이 작동 하는 요소를 인덱싱하고 중복 된 요소가 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-236">The third parameter `Int[]` indexes the qubits that this Pauli string acts on, and must have no duplicate elements.</span></span> <span data-ttu-id="f8e79-237">따라서 Hamiltonian term $0.4 \hat X_0 \hat Y_8 \hat I_2 \hat Z_1 $는로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-237">Thus the Hamiltonian term $0.4 \hat X_0 \hat Y_8\hat I_2\hat Z_1$ may be represented as</span></span>

```qsharp
let generatorIndexExample = GeneratorIndex(([1,2,0,3], [0.4]]), [0,8,2,1]);
```

<span data-ttu-id="f8e79-238">는 `PauliEvolutionSet()` 다음 서명을 사용 하 여이 폼을에 매핑하는 함수입니다 `GeneratorIndex` `EvolutionUnitary` .</span><span class="sxs-lookup"><span data-stu-id="f8e79-238">The `PauliEvolutionSet()` is a function that maps any `GeneratorIndex` of this form to an `EvolutionUnitary` with the following signature.</span></span>

```qsharp
newtype EvolutionUnitary = ((Double, Qubit[]) => Unit is Adj + Ctl);
```

<span data-ttu-id="f8e79-239">첫 번째 매개 변수는 단일 진화의 계수를 곱하여 하는 시간 기간을 나타냅니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="f8e79-239">The first parameter represents a time-duration, that will be multiplied by the coefficient in the `GeneratorIndex`, of unitary evolution.</span></span> <span data-ttu-id="f8e79-240">두 번째 매개 변수는 단일 역할을 수행 하는 고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-240">The second parameter is the qubit register the unitary acts on.</span></span> 

### <a name="time-dependent-generators"></a><span data-ttu-id="f8e79-241">Time-Dependent 생성기</span><span class="sxs-lookup"><span data-stu-id="f8e79-241">Time-Dependent Generators</span></span> ###

<span data-ttu-id="f8e79-242">대부분의 경우에는 Schrödinger 수식 $ $ \begin{align} i\frac {d \ket{\psi (t)} {d t} & = \hat H (t) \ket{\psi (t)}, \end{align} $ $에서 발생 하는 것 처럼 시간 종속 생성기에도 관심이 있습니다. $ \hat H (t) $는 이제 시간에 따라 다릅니다</span><span class="sxs-lookup"><span data-stu-id="f8e79-242">In many cases, we are also interested in modelling time-dependent generators, as might occur in the Schrödinger equation $$ \begin{align} i\frac{d \ket{\psi(t)}}{d t} & = \hat H(t) \ket{\psi(t)}, \end{align} $$ where the generator $\hat H(t)$ is now time-dependent.</span></span> <span data-ttu-id="f8e79-243">위의 시간 독립적 생성기에서이 경우의 확장은 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-243">The extension from the time-independent generators above to this case is straightforward.</span></span> <span data-ttu-id="f8e79-244">$T $에 대해 Hamiltonian를 설명 하는 고정을 사용 하는 대신 `GeneratorSystem` `GeneratorSystemTimeDependent` 사용자 정의 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-244">Rather than having a fixed `GeneratorSystem` describing the Hamiltonian for all times $t$, we instead have the `GeneratorSystemTimeDependent` user-defined type.</span></span>

```qsharp
newtype GeneratorSystemTimeDependent = (Double -> GeneratorSystem);
```

<span data-ttu-id="f8e79-245">첫 번째 매개 변수는 [0, 1] $ 인 $s 연속 일정 매개 변수이 고이 형식의 함수는 `GeneratorSystem` 해당 일정에 대해를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-245">The first parameter is a continuous schedule parameter $s\in [0,1]$, and functions of this type return a `GeneratorSystem` for that schedule.</span></span> <span data-ttu-id="f8e79-246">일정 매개 변수는 실제 시간 매개 변수 (예: $s = t/T $)와 선형으로 관련 될 수 있습니다. 예를 들어 총 시뮬레이션 시간은 $T $입니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-246">Note that the schedule parameter may be linearly related to the physical time parameter e.g. $s = t / T$, for some total time of simulation $T$.</span></span> <span data-ttu-id="f8e79-247">그러나이 경우에는 일반적이 지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-247">In general however, this need not be the case.</span></span>

<span data-ttu-id="f8e79-248">마찬가지로이 생성기의 전체 설명에는가 필요 `EvolutionSet` 하므로 `EvolutionSchedule` 사용자 정의 형식을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8e79-248">Similarly, a complete description of this generator requires an `EvolutionSet`, and so we define an `EvolutionSchedule` user-defined type.</span></span>

```qsharp
newtype EvolutionSchedule = (EvolutionSet, GeneratorSystemTimeDependent);
```
