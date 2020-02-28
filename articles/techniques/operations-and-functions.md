---
title: 'Q # 작업 및 함수'
description: 'Q # 작업 및 함수와 퀀텀 프로그램에 적용 되는 방법에 대해 알아봅니다.'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 43f0cf2da192a607e514d0c7de57a9bdd067faf7
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907667"
---
# <a name="q-operations-and-functions"></a><span data-ttu-id="3c211-103">Q # 작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="3c211-103">Q# Operations and Functions</span></span>

<span data-ttu-id="3c211-104">Q # 프로그램은 퀀텀 작업이 퀀텀 데이터에 대해 가질 수 있는 부작용을 설명 하는 하나 이상의 *작업* 으로 구성 되며, 기존 데이터를 수정할 수 있도록 하는 하나 이상의 *함수* 를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-104">Q# programs consist of one or more *operations* that describe side effects quantum operations can have on quantum data, and one or more *functions* that allow modifications to classical data.</span></span> <span data-ttu-id="3c211-105">연산과 달리 함수는 순수 하 게 모든 동작을 설명 하는 데 사용 되며 클래식 출력 값을 계산 하는 것 외에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-105">In contrast to operations, functions are used to describe purely classical behavior and do not have any effects besides computing classical output values.</span></span>

<span data-ttu-id="3c211-106">Q #에 정의 된 각 작업은 해당 언어로 정의 된 기본 제공 기본 작업을 포함 하 여 원하는 수의 다른 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-106">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="3c211-107">이러한 내장 작업이 정의 되는 특정 방법은 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-107">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span> <span data-ttu-id="3c211-108">컴파일되는 경우 각 작업은 대상 컴퓨터에 제공할 수 있는 .NET 클래스 형식으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-108">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="3c211-109">새 작업 정의</span><span class="sxs-lookup"><span data-stu-id="3c211-109">Defining New Operations</span></span>

<span data-ttu-id="3c211-110">위에서 설명한 것 처럼 Q #으로 작성 된 퀀텀 프로그램의 가장 기본적인 빌딩 블록은 작업입니다 .이는 기존 .NET 응용 프로그램에서 호출할 수 있는 *작업*입니다. 예를 들어 시뮬레이터를 사용 하거나 q # 내의 다른 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-110">As described above, the most basic building block of a quantum program written in Q# is an *operation*, which can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="3c211-111">각 작업은 입력을 가져오고, 출력을 생성 하 고, 하나 이상의 작업 특수화에 대해 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-111">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="3c211-112">예를 들어, 다음 작업은 기본 본문 특수화만 정의 하 고 단일 비트를 입력으로 사용 하 고 해당 입력에 대해 기본 제공 `X` 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-112">For instance, the following operation defines only a default body specialization and takes a single qubit as its input, then calls the built-in `X` operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="3c211-113">`operation` 키워드는 작업 정의를 시작 하 고 뒤에 이름이 옵니다. 여기에서 `BitFlip`합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-113">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="3c211-114">그런 다음 입력의 형식은 새 작업 내의 입력을 참조 하는 이름 `target`와 함께 `Qubit`로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-114">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="3c211-115">마찬가지로 `Unit`는 작업의 출력이 비어 있음을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-115">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="3c211-116">이는 및 기타 명령적 언어에서 C# `void` 하는 경우와 비슷하게 사용 되며 및 다른 기능 F# 언어의 `unit`와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-116">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

> [!NOTE]
> <span data-ttu-id="3c211-117">이 내용은 아래에 자세히 설명 되어 있지만, Q #의 각 작업은 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-117">We will explore this in more detail below, but each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="3c211-118">그런 다음 여러 개의 값을 단일 값으로 수집 하는 *튜플을*사용 하 여 여러 입력 및 출력을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-118">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="3c211-119">비공식적으로 Q #은 "튜플 인 튜플" 언어 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-119">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="3c211-120">이 개념에 따라 `()` `Unit`형식이 있는 "빈" 튜플로 읽어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-120">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

<span data-ttu-id="3c211-121">새 작업 내에서 기본 본문 특수화의 구현만 명시적으로 지정 해야 하는 경우 선언 내에서 직접 구현을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-121">Within the new operation, the implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to be specified explicitly.</span></span> <span data-ttu-id="3c211-122">또한 아래에서 구체화 된 하나 이상의 `functor` 작업 등의 구현을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-122">Additionally, it is possible to define the implementations of, for example, one or more `functor` operations, as elaborated below.</span></span> <span data-ttu-id="3c211-123">위의 예제에서 유일한 문은 <xref:microsoft.quantum.intrinsic.x>기본 제공 Q # 작업을 호출 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-123">In the example above, the only statement is to call the built-in Q# operation <xref:microsoft.quantum.intrinsic.x>.</span></span>

<span data-ttu-id="3c211-124">작업은 `Unit`보다 더 흥미로운 형식을 반환할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-124">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="3c211-125">예를 들어 <xref:microsoft.quantum.intrinsic.m> 작업은 측정을 수행 하는 것을 나타내는 `Result`형식의 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-125">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="3c211-126">작업의 출력을 다른 작업으로 전달 하거나 `let` 키워드와 함께 사용 하 여 새 변수를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-126">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>
<!-- Link to UID for superdense conceptual and example documentation. -->
<span data-ttu-id="3c211-127">이를 통해 슈퍼 조밀한 코딩의 경우와 같이 낮은 수준에서 퀀텀 작업과 상호 작용 하는 기존 계산을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-127">This allows for representing classical computation that interacts with quantum operations at a low level, such as in superdense coding:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a><span data-ttu-id="3c211-128">함수, adjoint 및 제어 됨</span><span class="sxs-lookup"><span data-stu-id="3c211-128">Functors, adjoint and controlled</span></span>
<span data-ttu-id="3c211-129">작업에서 단일 변환을 구현 하는 경우 *adjointed* 또는 *제어*될 때 작업이 작동 하는 방식을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-129">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="3c211-130">작업의 adjoint 특수화는 역방향으로 실행 될 때 작동 하는 방식을 지정 하는 반면, 제어 된 특수화는 퀀텀 레지스터의 상태에 조건 화 된 적용 될 때 작업이 작동 하는 방식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-130">An adjoint specialization of an operation specifies how it acts when run in reverse, while a controlled specialization specifies how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="3c211-131">이러한 특수화의 존재는 다음 예제에서 `is Adj + Ctl` 작업 시그니처의 일부로 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-131">The existence of these specializations can be declared as part of the operation signature: `is Adj + Ctl` in the following example.</span></span> <span data-ttu-id="3c211-132">이렇게 암시적으로 선언 된 각 특수화에 해당 하는 구현은 컴파일러에 의해 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-132">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> <span data-ttu-id="3c211-133">Q #의 많은 작업은 단일 게이트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-133">Many operations in Q# represent unitary gates.</span></span>
> <span data-ttu-id="3c211-134">$U $가 작업 `U`으로 표시 되는 단일 게이트가 면 `Adjoint U`는 단일 게이트 $U ^ \a와 $를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-134">If $U$ is the unitary gate represented by an operation `U`, then `Adjoint U` represents the unitary gate $U^\dagger$.</span></span>

<span data-ttu-id="3c211-135">컴파일러가 구현을 생성할 수 없는 경우에는 명시적으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-135">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="3c211-136">이러한 명시적 특수화 선언은 적절 한 세대 지시문 또는 사용자 정의 구현으로 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-136">Such explicit specialization declarations can consist of a suitable generation directive or a user defined implementation.</span></span> <span data-ttu-id="3c211-137">위의 `PrepareEntangledPair` 코드는 다음 코드와 같이 명시적 특수화 선언이 포함 된 코드와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-137">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="3c211-138">키워드 `auto`은 컴파일러가 특수화 구현을 생성 하는 방법을 결정 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-138">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="3c211-139">컴파일러가 특정 특수화의 구현을 자동으로 생성할 수 없는 경우 또는 보다 효율적인 구현을 제공할 수 있는 경우에는 구현을 수동으로 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-139">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="3c211-140">위의 예제에서 `adjoint invert;`는 본문 구현을 반전 하 여 adjoint 특수화가 생성 되 고 `controlled adjoint invert;`는 제어 된 특수화의 지정 된 구현을 반전 하 여 제어 된 adjoint 특수화가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-140">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="3c211-141">이에 대 한 더 많은 예제는 [고차 제어 흐름](xref:microsoft.quantum.concepts.control-flow)에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-141">We will see more examples of this in [Higher-Order Control Flow](xref:microsoft.quantum.concepts.control-flow).</span></span>

<span data-ttu-id="3c211-142">작업의 특수화를 호출 하려면 `Adjoint` 또는 `Controlled` 키워드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-142">To call a specialization of an operation, use the `Adjoint` or `Controlled` keywords.</span></span>
<span data-ttu-id="3c211-143">예를 들어, 위의 슈퍼 조밀한 코딩 예는 조밀 `PrepareEntangledPair`의 adjoint를 사용 하 여 entangled 상태를 a비트의 unentangled 쌍으로 다시 변환 하 여 더 많은를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-143">For example, the superdense coding example above can be written more compactly by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="3c211-144">함수와 함께 사용 하기 위한 작업을 디자인할 때 고려해 야 할 몇 가지 중요 한 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-144">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="3c211-145">다른 작업의 출력 값을 사용 하는 작업에 대 한 특수화는 컴파일러에서 자동으로 생성할 수 없습니다. 이러한 작업에서 문을 다시 정렬 하 여 동일한 효과를 얻는 방법은 모호 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-145">Most critically, specializations for an operation that uses the output value of any other operation cannot be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>


## <a name="defining-new-functions"></a><span data-ttu-id="3c211-146">새 함수 정의</span><span class="sxs-lookup"><span data-stu-id="3c211-146">Defining New Functions</span></span>

<span data-ttu-id="3c211-147">Q #에서는 출력 값을 계산 하는 것 보다는 효과를 가질 수 없다는 점에서 작업과는 다른 *함수*를 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-147">Q# also allows for defining *functions*, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="3c211-148">특히 함수는 작업을 호출 하거나,이 함수를 호출할 수 없으며, 난수를 샘플링 하거나, 함수에 대 한 입력 값 이상으로 상태에 의존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-148">In particular, functions cannot call operations, act on qubits, sample random numbers, or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="3c211-149">결과적으로 Q # 함수는 항상 동일한 입력 값을 동일한 출력 값에 매핑하기 때문에 *순수*합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-149">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="3c211-150">이를 통해 Q # 컴파일러는 작업 특수화를 생성할 때 함수가 호출 되는 방법 및 시기를 안전 하 게 다시 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-150">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="3c211-151">함수 정의는 함수에 대해 adjoint 또는 제어 된 특수화를 정의할 수 없다는 점을 제외 하 고 작업을 정의 하는 것과 유사 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-151">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="3c211-152">예:</span><span class="sxs-lookup"><span data-stu-id="3c211-152">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
<span data-ttu-id="3c211-153">이러한 작업을 수행할 수 있는 경우 작업 내에서 보다 쉽게 사용할 수 있도록 작업 대신 함수를 기준으로 기존 논리를 작성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-153">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="3c211-154">예를 들어 `Square`를 작업으로 작성 한 경우 컴파일러는 동일한 입력을 사용 하 여 호출 하는 것이 일관 되 게 동일한 출력을 생성 하도록 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-154">If we had written `Square` as an operation, for example, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="3c211-155">함수 및 작업 간의 차이를 표시 하려면 Q # 작업 내에서 난수를 샘플링 하는 것과 관련 된 문제를 일반적으로.</span><span class="sxs-lookup"><span data-stu-id="3c211-155">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="3c211-156">`U`가 호출 될 때마다 `target`에서 다른 작업이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-156">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="3c211-157">특히 컴파일러는 `U(target); Adjoint U(target);` `U`에 `adjoint auto` 특수화 선언을 추가한 경우 id (즉, op)로 작동 하도록 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-157">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="3c211-158">이는 [벡터 및 매트릭스](xref:microsoft.quantum.concepts.vectors)에서 보았던 adjoint의 정의를 위반 하 여, 작업 <xref:microsoft.quantum.math.randomreal> 호출한 작업에서 adjoint 특수화를 자동으로 생성할 수 있도록 하 여 컴파일러에서 제공 하는 보증을 중단 합니다. <xref:microsoft.quantum.math.randomreal>는 adjoint 또는 제어 된 버전이 존재 하지 않는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-158">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="3c211-159">반면에 `Square`와 같은 함수 호출을 안전 하 게 사용할 수 있다는 것은 컴파일러가 출력을 안정적으로 유지 하기 위해 `Square` 입력을 유지 해야 한다는 것을 확신할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-159">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="3c211-160">따라서 함수에서 최대한 많은 고전 논리를 격리 하면 다른 함수와 작업에서 해당 논리를 쉽게 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-160">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>

## <a name="control-flow"></a><span data-ttu-id="3c211-161">제어 흐름</span><span class="sxs-lookup"><span data-stu-id="3c211-161">Control Flow</span></span>

<span data-ttu-id="3c211-162">작업 또는 함수 내에서 각 문은 순서 대로 실행 되며 가장 일반적인 명령적 언어와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-162">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="3c211-163">그러나이 제어 흐름은 다음과 같은 세 가지 방법으로 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-163">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="3c211-164">`if` 문</span><span class="sxs-lookup"><span data-stu-id="3c211-164">`if` Statements</span></span>
- <span data-ttu-id="3c211-165">`for` 루프</span><span class="sxs-lookup"><span data-stu-id="3c211-165">`for` Loops</span></span>
- <span data-ttu-id="3c211-166">`repeat`-`until` 루프</span><span class="sxs-lookup"><span data-stu-id="3c211-166">`repeat`-`until` Loops</span></span>

<span data-ttu-id="3c211-167">[성공 (RUS) 회로까지 반복](xref:microsoft.quantum.techniques.qubits#measurements) 에 대해 논의할 때까지 후자의 토론을 연기 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-167">We defer discussion of the latter until we discuss [Repeat Until Success (RUS)](xref:microsoft.quantum.techniques.qubits#measurements) circuits.</span></span>
<span data-ttu-id="3c211-168">그러나 `if` 및 `for` 제어 흐름 구문은 대부분의 일반적인 프로그래밍 언어에 대해 잘 알고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-168">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>
<span data-ttu-id="3c211-169">특히 `if` 문은 조건을 사용할 수 있으며 그 뒤에 하나 이상의 `elif` 문이 올 수 있으며 `else`으로 끝날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-169">In particular, an `if` statement can take a condition, may be followed by one or more `elif` statements, and may end with an `else`:</span></span>

```qsharp
if (pauli == PauliX) {
    X(qubit);
} elif (pauli == PauliY) {
    Y(qubit);
} elif (pauli == PauliZ) {
    Z(qubit);
} else {
    fail "Cannot use PauliI here.";
}
```

<span data-ttu-id="3c211-170">마찬가지로 `for` 루프는 정수 범위 또는 배열의 요소에 대 한 반복을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-170">Similarly, `for` loops indicate iteration over a range of integers or over the elements of an array:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

<span data-ttu-id="3c211-171">중요 한 것은 특수화가 자동 생성 되는 작업에도 `for` 루프 및 `if` 문을 사용할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-171">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="3c211-172">이 경우 `for` 루프의 adjoint는 방향을 바꾸고 각 반복의 adjoint를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-172">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="3c211-173">이는 "신발 및 socks" 원칙을 따릅니다. 즉, socks에 배치를 취소 한 다음 신발로 전환 하려면 축구 전환에 대 한 실행을 취소 하 고 socks에 배치를 실행 취소 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-173">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="3c211-174">계속 해 서 신발를 decidedly 하는 동안 시도 하 고 socks를 사용 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-174">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="operations-and-functions-as-first-class-values"></a><span data-ttu-id="3c211-175">작업 및 함수를 첫 번째 클래스 값으로</span><span class="sxs-lookup"><span data-stu-id="3c211-175">Operations and Functions as First-Class Values</span></span>

<span data-ttu-id="3c211-176">작업 대신 함수를 사용 하는 제어 흐름과 기존 논리를 추론 하는 한 가지 중요 한 기술은 Q #의 해당 작업 및 함수를 *첫 번째 클래스*에 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-176">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="3c211-177">즉, 해당 언어의 각 값은 고유한 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-177">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="3c211-178">예를 들어, 약간 간접적인 경우 다음은 완벽 하 게 유효한 Q # 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-178">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="3c211-179">위의 코드 조각에서 `ourH` 된 변수 값은 다른 작업 처럼 해당 값을 호출할 수 있도록 하는 작업이 <xref:microsoft.quantum.intrinsic.h>됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-179">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="3c211-180">이렇게 하면 작업을 입력의 일부로 사용 하 여 고차 제어 흐름 개념을 형성 하는 작업을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-180">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="3c211-181">예를 들어 동일한 대상의 동일한 대상에 두 번 적용 하 여 작업을 "제곱" 하는 것을 생각해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-181">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="3c211-182">이 예제에서 `(Qubit => Unit)` 형식에 표시 되는 `=>` 화살표는 입력 `op` 필드가 `Qubit` 형식의 입력으로 사용 하 고 빈 튜플을 출력으로 생성 하는 작업 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-182">In this example, the `=>` arrow that appears in the type `(Qubit => Unit)` denotes that the input field `op` is an operation which takes as its input the type `Qubit` and produces an empty tuple as its output.</span></span>
<span data-ttu-id="3c211-183">또한 지원 되는 함수에 대 한 정보를 포함 하는 해당 작업 유형의 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-183">Additionally we specify the characteristics of that operation type, which contain the information about which functors are supported.</span></span>
<span data-ttu-id="3c211-184">`(Qubit => Unit)` 형식의 연산은 `Adjoint` 및 `Controlled` 함수를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-184">An operation of type `(Qubit => Unit)` supports neither the `Adjoint` nor the `Controlled` functor.</span></span> <span data-ttu-id="3c211-185">`Adjoint` 함수와 같이 해당 형식의 작업에서를 지원 해야 함을 나타내려면 adjointable로 선언 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-185">If we want to indicate that an operation of that type has to support e.g. the `Adjoint` functor, we have to declare it as being adjointable.</span></span> <span data-ttu-id="3c211-186">이 작업은 주석 `is Adj`를 형식에 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-186">This is done by using the annotation `is Adj` to the type.</span></span> <span data-ttu-id="3c211-187">마찬가지로 `(Qubit => Unit is Ctl)`는 해당 형식의 작업이 `Controlled` 함수를 지원함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-187">Similarly, `(Qubit => Unit is Ctl)` denotes that an operation of that type supports the `Controlled` functor.</span></span> <span data-ttu-id="3c211-188">[Q #](xref:microsoft.quantum.language.type-model) 보다 일반적으로이에 대해 설명 하는 경우이에 대해 자세히 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-188">We will explore this further when we discuss [types in Q#](xref:microsoft.quantum.language.type-model) more generally.</span></span>

<span data-ttu-id="3c211-189">지금은 작업의 형태로 퀀텀 프로그램에 대 한 설명을 반환 하는 클래식 함수로 일부 종류의 클래식 조건부 논리를 격리할 수 있도록 작업을 출력의 일부로 반환할 수도 있음을 강조 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-189">For now, we emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="3c211-190">간단한 예로, 2 비트 클래식 메시지를 수신 하는 파티가 메시지를 사용 하 여 해당 teleportation를 적절 한 teleported 상태로 디코딩하는 경우를 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-190">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="3c211-191">이러한 두 개의 기존 비트를 사용 하 고 적절 한 디코딩 작업을 반환 하는 함수를 기준으로이를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-191">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

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

<span data-ttu-id="3c211-192">이 새 함수는 실제로는 함수 이며 `hereBit` 및 `thereBit`값이 같은 값을 사용 하 여 호출 하는 경우 항상 동일한 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-192">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="3c211-193">따라서 디코딩 논리가 다른 작업 특수화의 정의와 상호 작용 하는 방법에 대해 설명 하지 않고도 작업 내에서 디코더를 안전 하 게 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-193">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="3c211-194">즉, 함수 내에서 기존 논리를 격리 하 여 입력이 유지 되는 한 함수 호출이  unity를 사용 하 여 다시 정렬할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-194">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>

<span data-ttu-id="3c211-195">함수를 고급 값으로 취급할 수도 있습니다 .이는 [작업 및 함수 형식](#operations-and-functions-as-first-class-values)에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-195">We can also treat functions as first-class values, as we will see in more detail when we discuss [operations and function types](#operations-and-functions-as-first-class-values).</span></span>

## <a name="partially-applying-operations-and-functions"></a><span data-ttu-id="3c211-196">작업 및 함수를 부분적으로 적용</span><span class="sxs-lookup"><span data-stu-id="3c211-196">Partially Applying Operations and Functions</span></span>

<span data-ttu-id="3c211-197">*부분 응용 프로그램*을 사용 하 여 작업을 반환 하는 함수를 사용 하 여 작업을 반환 하는 함수를 사용 하 여 훨씬 더 많은 작업을 수행할 수 있습니다. 이러한 함수는 실제로 호출 하지 않고도 함수 또는 작업에 입력 부분</span><span class="sxs-lookup"><span data-stu-id="3c211-197">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="3c211-198">예를 들어 위의 `ApplyTwice` 예제를 회수할 때 입력 작업을 적용 해야 하는 것을 즉시 지정 하지 않을 것을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-198">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="3c211-199">이 경우 지역 변수 `twiceOp` `ApplyTwice(op, _)`부분적으로 적용 된 작업을 보관 합니다. 여기서 아직 지정 하지 않은 입력 부분은 `_`표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-199">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="3c211-200">실제로 다음 줄에서 `twiceOp`를 호출 하는 경우 입력의 나머지 부분을 모두 원래 작업에 대 한 입력으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-200">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="3c211-201">따라서 위의 코드 조각은 실제로 `ApplyTwice(op, target)`를 직접 호출 하는 것과 동일 합니다. 즉, 입력의 일부를 제공 하는 동안 호출을 지연할 수 있는 새 지역 변수를 도입 했습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-201">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="3c211-202">부분적으로 적용 된 작업은 전체 입력이 제공 될 때까지 실제로 호출 되지 않으므로 함수 내 에서도 작업을 부분적으로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-202">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="3c211-203">원칙적으로 `SquareOperation` 내의 기존 논리는 훨씬 더 많은 작업을 수행 했을 수 있지만 컴파일러에서 함수에 대해 제공할 수 있도록 보장을 통해 작업의 나머지 부분과 여전히 격리 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-203">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="3c211-204">이 접근 방식은 퀀텀 프로그램 내에서 쉽게 사용할 수 있는 방식으로 클래식 제어 흐름을 표현 하기 위해 Q # 표준 라이브러리 전체에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c211-204">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>
