---
title: 'Q # Introdution'
description: 'Q에서 퀀텀 프로그램에 대 한 간략 한 소개 #'
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233976"
---
# <a name="q-quantum-programming-language"></a><span data-ttu-id="8059e-103">Q # 퀀텀 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="8059e-103">Q# Quantum Programming Language</span></span>

<span data-ttu-id="8059e-104">Q # 프로그래밍 언어에 대해 알고 있어야 하는 모든 항목은 [q # 언어 가이드](xref:microsoft.quantum.qsharp.index)에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-104">Everything you need to know about the Q# programming language is detailed in the [Q# language guide](xref:microsoft.quantum.qsharp.index).</span></span> <span data-ttu-id="8059e-105">다른 것과 마찬가지로, [언어 디자인 프로세스](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) 는 오픈 소스 이며 기여를 환영 합니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-105">Like anything else, our [language design process](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) is open source and we welcome contributions.</span></span>
<span data-ttu-id="8059e-106">Q #의 기초 및 동기에 대 한 자세한 배경 정보는 [q #?가 필요한 이유](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8059e-106">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>  
<span data-ttu-id="8059e-107">Q #은 QDK (퀀텀 개발 키트)의 일부로 제공 되며, 간략 한 개요를 보려면 [qdk?](xref:microsoft.quantum.overview.q-sharp)를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="8059e-107">Q# is shipped as part of the Quantum Development Kit (QDK) For a quick overview, check out [What is the QDK?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="8059e-108">퀀텀 프로그램 이란?</span><span class="sxs-lookup"><span data-stu-id="8059e-108">What is a quantum program?</span></span>

<span data-ttu-id="8059e-109">퀀텀 프로그램은 호출 시 퀀텀 시스템과 상호 작용 하 여 계산을 수행 하는 특정 한 기존 서브루틴 집합으로 볼 수 있습니다. Q #으로 작성 된 프로그램은 퀀텀 상태를 직접 모델링 하는 것이 아니라 클래식 제어 컴퓨터가 이러한 컴퓨터와 어떻게 상호 작용 하는지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-109">A quantum program can be seen as a particular set of classical subroutines which, when called, perform a computation by interacting with a quantum system; a program written in Q# does not directly model the quantum state, but rather describes how a classical control computer interacts with qubits.</span></span>
<span data-ttu-id="8059e-110">이를 통해 각 대상 컴퓨터 *에도 있는 퀀텀 상태를 완전히* 제어할 수 있으며,이는 컴퓨터에 따라 서로 다르게 해석 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-110">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="8059e-111">그 이유는 Q #에서 퀀텀 메커니즘의 introspect 또는 기타 속성의 상태에 직접 연결할 수 있는 기능이 없다는 것입니다 .이는 Q # 프로그램이 양자 컴퓨터에서 실제로 실행 될 수 있도록 보장 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-111">An important consequence of that is that Q# has no ability to introspect into the state of a qubit or other properties of quantum mechanics directly, which guarantees that a Q# program can be physically executed on a quantum computer.</span></span>
<span data-ttu-id="8059e-112">대신 프로그램은 등의 작업을 호출 하 여 해당 작업 [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) 에서 기존 정보를 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-112">Instead, a program can call operations such as [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) to extract classical information from a qubit.</span></span>

<span data-ttu-id="8059e-113">할당 된 후에는 인수를 *callables* 이 라고도 하는 작업 및 함수에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-113">Once allocated, a qubit can be passed to operations and functions, also referred to as *callables*.</span></span> <span data-ttu-id="8059e-114">어떤 의미에서 Q # 프로그램은 이러한 모든 작업을 수행할 수 있습니다. 원하는 비트의 상태에 대 한 모든 직접적인 작업은 *intrinsic* [`X`](xref:Microsoft.Quantum.Intrinsic.X) 및 [`H`](xref:Microsoft.Quantum.Intrinsic.H) -즉, 구현이 Q # 내에서 정의 되지 않았지만 대상 컴퓨터에서 정의 되는 callables과 같은 내장 callables에 의해 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-114">In some sense, this is all that a Q# program can do with a qubit; Any direct actions on state of a qubit are all defined by *intrinsic* callables such as [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) - i.e. callables whose implementations are not defined within Q# but are instead defined by the target machine.</span></span> <span data-ttu-id="8059e-115">이러한 작업은 실제로 *수행* 하는 작업은 특정 Q # 프로그램을 실행 하는 데 사용 하는 대상 컴퓨터에만 구체적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-115">What these operations actually *do* is only made concrete by the target machine we use to run the particular Q# program.</span></span>

<span data-ttu-id="8059e-116">예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)에서 프로그램을 실행 하는 경우 시뮬레이터는 시뮬레이션 된 퀀텀 시스템에 해당 하는 수치 연산을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-116">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="8059e-117">하지만 향후에는 대상 컴퓨터가 실제 퀀텀 컴퓨터인 경우 Q #에서 이러한 작업을 호출 하면 *실제* 퀀텀 시스템에서 해당 하는 *실제* 작업을 수행 하도록 퀀텀 컴퓨터가 지시 합니다 (예: 정확히 시간이 지정 된 레이저 펄스).</span><span class="sxs-lookup"><span data-stu-id="8059e-117">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# will direct the quantum computer to perform the corresponding *real* operations on the *real* quantum system (e.g. precisely timed laser pulses).</span></span>

<span data-ttu-id="8059e-118">Q # 프로그램은 대상 컴퓨터에서 정의한 대로 이러한 작업을 다시 결합 하 여 퀀텀 계산을 표현할 수 있는 새로운 수준의 새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-118">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="8059e-119">이러한 방식으로 Q #를 사용 하면 대상 컴퓨터 또는 시뮬레이터의 구조와 관련 하 여 일반적으로 사용 되는 논리 퀀텀 및 하이브리드 퀀텀 – 기존 알고리즘을 쉽게 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-119">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

<span data-ttu-id="8059e-120">간단한 예는 $ \ket $ 상태에서 한 가지 비트를 할당 하 {0} 고, Hadamard 작업을 적용 하 고, 결과를 측정 하는 다음 프로그램입니다 `H` `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="8059e-120">A simple example is the following program, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
@EntryPoint()
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

<span data-ttu-id="8059e-121">[퀀텀 Katas](https://github.com/microsoft/QuantumKatas#introduction) 은 일반적인 퀀텀 작업과 같은 [퀀텀 컴퓨팅 개념](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) 을 소개 하 고,이를 조작 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-121">Our [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) give a good introduction on [Quantum Computing Concepts](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) such as common quantum operations and how to manipulate qubits.</span></span> <span data-ttu-id="8059e-122">기타 예제는 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude)에서도 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8059e-122">More examples can also be found in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span>



