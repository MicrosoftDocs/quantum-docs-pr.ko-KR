---
title: 퀀텀 개발 기술 소개 | Microsoft Docs
description: 퀀텀 개발 기술 소개
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 702d23293a1c340ddd3d7032d0e05294345469b2
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442555"
---
# <a name="q-program-overview"></a><span data-ttu-id="929cc-103">Q # 프로그램 개요</span><span class="sxs-lookup"><span data-stu-id="929cc-103">Q# program overview</span></span>

<span data-ttu-id="929cc-104">Q #은 퀀텀 컴퓨팅을 위한 확장 가능한 다중 패러다임의 도메인별 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-104">Q# is a scalable, multi-paradigm, domain-specific programming language for quantum computing.</span></span> <span data-ttu-id="929cc-105">Q #은 퀀텀 컴퓨터에서 명령이 실행 되는 방식을 설명 하는 데 사용할 수 있는 퀀텀 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-105">Q# is a quantum programming language in that it can be used to describe how instructions are executed on quantum machines.</span></span> <span data-ttu-id="929cc-106">대상으로 지정할 수 있는 컴퓨터가 시뮬레이터에서 실제 퀀텀 하드웨어로의 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-106">The machines that can be targeted range from simulators to actual quantum hardware.</span></span> <span data-ttu-id="929cc-107">Q #은 확장 가능 합니다. 몇 가지 방법으로 실행 되는 텔레포트와 같은 간단한 데모 프로그램을 작성 하는 데 사용할 수 있습니다. 또한 수백만 억 비트를 포함 하는 큰 컴퓨터를 필요로 하는 복잡 한 molecules의 시뮬레이션 등의 복잡 한 프로그램을 작성 하는 것도 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-107">Q# is scalable: it can be used to write simple demonstration programs like teleport that run on a few qubits, but also supports writing large, sophisticated programs such as simulations of complex molecules that will require large machines with millions of qubits.</span></span> <span data-ttu-id="929cc-108">실제 컴퓨터의 규모가 미래에도 불구 하 고 Q #을 사용 하면 프로그래머가 복잡 한 퀀텀 알고리즘을 프로그래밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-108">Even though large physical machines are still in the future, Q# allows a programmer to program complex quantum algorithms now.</span></span> <span data-ttu-id="929cc-109">무엇 보다도 Q #은 디버깅, 프로 파일링, 리소스 예측 및 특정 용도의 특정 용도의 시뮬레이션 등의 다양 한 작업을 확장 가능한 방식으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-109">What is more, Q# supports various tasks such as debugging, profiling, resource estimation, and certain special-purpose simulations in a scalable way.</span></span> 

<span data-ttu-id="929cc-110">기술적 측면에서 볼 때 퀀텀 프로그램은 호출 시 부작용으로 퀀텀 회로를 생성 하는 특정 클래식 함수 집합으로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-110">From a technical perspective, a quantum program can be seen as a particular set of classical functions which, when called, generate quantum circuits as their side effects.</span></span> <span data-ttu-id="929cc-111">이 보기의 중요 한 결과는 Q #으로 작성 된 프로그램이 직접 직접 모델을 모델링 하는 것이 아니라 클래식 제어 컴퓨터가 해당 하는 비트와 상호 작용 하는 방식을 설명 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-111">An important consequence of that view is that a program written in Q# does not directly model qubits themselves, but rather describes how a classical control computer interacts with those qubits.</span></span>
<span data-ttu-id="929cc-112">기본적으로 Q #은 퀀텀 상태 또는 퀀텀 메커니즘의 다른 속성을 직접 정의 하지 않고 언어에 정의 된 다양 한 서브루틴의 작업을 간접적으로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-112">By design, Q# thus does not define quantum states or other properties of quantum mechanics directly, but rather does so indirectly through the action of the various subroutines defined in the language.</span></span>
<span data-ttu-id="929cc-113">예를 들어 [퀀텀 컴퓨팅 개념](xref:microsoft.quantum.concepts.intro) 가이드에 설명 된 $ \ket{+} = \left (\ket{0} + \ket{1}\left)/\left{2}$ 상태를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-113">For instance, consider the state $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ discussed in the [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) guide.</span></span>
<span data-ttu-id="929cc-114">Q #에서이 상태를 준비 하기 위해 $ \ket{0}$ 상태에서이를 초기화 하는 팩트와 $ \ket{+} = H\ket{0}$를 사용 합니다. 여기서 $H $은 Hadamard transform입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-114">To prepare this state in Q#, we use the facts that the qubits are initialized in the $\ket{0}$ state, and that $\ket{+} = H\ket{0}$, where $H$ is the Hadamard transform:</span></span>

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0〉.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0〉 = |+〉, as we wanted.
}
```
## <a name="q-tranformations-of-quantum-states"></a><span data-ttu-id="929cc-115">Q # 변환은 퀀텀 상태</span><span class="sxs-lookup"><span data-stu-id="929cc-115">Q# tranformations of quantum states</span></span>

<span data-ttu-id="929cc-116">중요 한 점은 위의 프로그램을 작성할 때 Q # 내에서 상태를 명시적으로 참조 하지 않고 프로그램에서 상태를 *변환* 하는 방법을 설명 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-116">Importantly, in writing the above program, we did not explicitly refer to the state within Q#, but rather described how the state was *transformed* by our program.</span></span>
<span data-ttu-id="929cc-117">따라서 그래픽 셰이더 프로그램에서 각 꼭 짓 점에 대 한 변환 설명을 누적 하는 방법과 마찬가지로 Q #의 퀀텀 프로그램은 퀀텀 상태에 대 한 변환을 누적 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-117">Thus, similar to how a graphics shader program accumulates a description of transformations to each vertex, a quantum program in Q# accumulates transformations to quantum states.</span></span>
<span data-ttu-id="929cc-118">이를 통해 각 대상 컴퓨터 *에도 있는 퀀텀 상태를 완전히* 제어할 수 있으며,이는 컴퓨터에 따라 서로 다르게 해석 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-118">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="929cc-119">Q # 프로그램의 관점에서 보면, 목표는 대상 컴퓨터의 내부 구조에 대 한 완전히 불투명 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-119">From the perspective of a Q# program, a qubit is an entirely opaque reference to the internal structure of a target machine.</span></span>
<span data-ttu-id="929cc-120">Q # 프로그램에는 대상 컴퓨터에 대 한 introspect의 상태 또는 프로그램에서 사용할 수 있는 다른 모든 기능에 해당 하는 것과 같은 것이 든 상관 없이 상태를 확인할 수 있는 기능이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-120">A Q# program has no ability to introspect into the state of a qubit, its representation on a target machine, or even whether it is the same qubit as any other qubit available to the program.</span></span>
<span data-ttu-id="929cc-121">대신 프로그램은 `Measure` 등의 작업을 호출 하 여 해당 정보를 파악 하 고 `X` 및 `H`와 같은 작업을 호출 하 여 해당 상태에 대 한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-121">Rather, a program can call operations such as `Measure` to learn information from a qubit, and call operations such as `X` and `H` to act on the state of a qubit.</span></span>
<span data-ttu-id="929cc-122">이러한 작업에는 언어 내에 내장 된 정의가 없으며 특정 Q # 프로그램을 실행 하는 데 사용 되는 대상 컴퓨터에 의해서만 구체적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-122">These operations have no intrinsic definition within the language, and are made concrete only by the target machine used to run a particular Q# program.</span></span>
<span data-ttu-id="929cc-123">Q # 프로그램은 대상 컴퓨터에서 정의한 대로 이러한 작업을 다시 결합 하 여 퀀텀 계산을 표현할 수 있는 새로운 수준의 새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-123">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="929cc-124">이러한 방식으로 Q #를 사용 하면 대상 컴퓨터 또는 시뮬레이터의 구조와 관련 하 여 일반적으로 사용 되는 논리 퀀텀 및 하이브리드 퀀텀-기존 알고리즘을 쉽게 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-124">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum-classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

## <a name="q-operations-and-functions"></a><span data-ttu-id="929cc-125">Q # 작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="929cc-125">Q# operations and functions</span></span>

<span data-ttu-id="929cc-126">구체적으로 Q # 프로그램은 하나 이상의 *작업*, 하나 이상의 *함수*및 사용자 정의 형식으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-126">Concretely, a Q# program is comprised of one or more *operations*, one or more *functions*, and user defined types.</span></span> <span data-ttu-id="929cc-127">작업은 퀀텀 컴퓨터의 상태에 대 한 변환을 설명 하는 데 사용 되며 Q # 프로그램의 가장 기본적인 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-127">Operations are used to describe the transformations of the state of a quantum machine and are the most basic building block of Q# programs.</span></span> <span data-ttu-id="929cc-128">Q #에 정의 된 각 작업은 대상 컴퓨터에서 구현 하는 기본 제공 *기본 작업을* 포함 하 여 많은 수의 다른 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-128">Each operation defined in Q# may then call any number of other operations, including the built-in *intrinsic* operations implemented by a target machine.</span></span>
<span data-ttu-id="929cc-129">컴파일되는 경우 각 작업은 대상 컴퓨터에 제공할 수 있는 .NET 클래스 형식으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-129">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="929cc-130">연산과 달리 함수는 순수 하 게 모든 동작을 설명 하는 데 사용 되며 클래식 출력 값을 계산 하는 것 외에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-130">In contrast to operations, functions are used to describe purely classical behavior and do not have any effects besides computing classical output values.</span></span> <span data-ttu-id="929cc-131">Q #은 강력한 형식의 언어 이며 사용자 정의 형식에 대 한 지원 뿐만 아니라 기본 제공 기본 형식 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-131">Q# is a strongly typed language and comes with a set of built-in primitive types as well as support for user defined types.</span></span> 

<span data-ttu-id="929cc-132">이 가이드의 나머지 부분에서는 작업, 함수 및 형식의 기본 구성 요소를 통해 복잡 한 퀀텀 프로그램을 정의 하는 데 도움이 되는 다양 한 언어 개념 및 구문을 사용 하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-132">Throughout the rest of this guide, we will see how to use different language concepts and constructs to help us define complex quantum programs through the basic building blocks of operations, functions, and types.</span></span> 

## <a name="structure-of-q-source-files"></a><span data-ttu-id="929cc-133">Q # 소스 파일의 구조</span><span class="sxs-lookup"><span data-stu-id="929cc-133">Structure of Q# Source Files</span></span>

<span data-ttu-id="929cc-134">최소한 Q # 소스 파일은 *네임 스페이스 선언*으로 구성 됩니다 .이 선언에서는 소스 파일의 정의가 포함 될 .net 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-134">Minimally, a Q# source file consists of a *namespace declaration*, which specifies a .NET namespace which will contain the definitions in the source file.</span></span>
<span data-ttu-id="929cc-135">`open` 문을 사용 하 여 다른 Q # 소스 파일 및 라이브러리의 정의를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-135">Definitions from other Q# source files and libraries can be included using the `open` statement.</span></span>
<span data-ttu-id="929cc-136">예를 들어 기본 게이트를 정의 하는 대부분의 작업은 <xref:microsoft.quantum.intrinsic> 네임 스페이스에 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-136">For instance, most of the operations defining fundamental gates are defined in the <xref:microsoft.quantum.intrinsic> namespace.</span></span>
<span data-ttu-id="929cc-137">이를 코드에 사용할 수 있도록 하려면 각 파일의 맨 위에 해당 네임 스페이스를 `open` 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-137">To make this available to our code, we simply `open` that namespace at the top of each file:</span></span>

```qsharp
namespace Example {
    open Microsoft.Quantum.Intrinsic;

    // ...
}
```

<span data-ttu-id="929cc-138">네임 스페이스 내에서 각 Q # 소스 파일은 *작업*, *함수*및 *사용자 정의 형식의*조합을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-138">Within a namespace, each Q# source file can define any combination of *operations*, *functions*, and *user-defined types*.</span></span>
<span data-ttu-id="929cc-139">이 섹션의 나머지 부분에서는 각각에 대해 설명 하 고, 유용한 퀀텀 프로그램을 만드는 데 사용 하는 방법에 대 한 예제를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="929cc-139">In the rest of this section, we will describe each in turn and provide examples of how they can be used in practice to make useful quantum programs.</span></span>
