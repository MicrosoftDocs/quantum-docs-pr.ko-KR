---
title: 'Q에서 해당 하는 비트 수준 프로그램 작성 및 시뮬레이트 #'
description: 개별 기능 비트 수준에서 작동 하는 퀀텀 프로그램 작성 및 시뮬레이션에 대 한 단계별 자습서
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
ms.openlocfilehash: 05d3292e1c6e3c8c1163c460f2aaa51c591aa1d5
ms.sourcegitcommit: 8d9d392bf5e114ae223e6f689ba80d25866ff586
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2020
ms.locfileid: "84422243"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a><span data-ttu-id="7a1b7-103">자습서: Q:에서의 비트 수준 프로그램 작성 및 시뮬레이트\#</span><span class="sxs-lookup"><span data-stu-id="7a1b7-103">Tutorial: Write and simulate qubit-level programs in Q\#</span></span>

<span data-ttu-id="7a1b7-104">개별 ombits에서 작동 하는 기본 퀀텀 프로그램 작성 및 시뮬레이션에 대 한 퀀텀 Development Kit 자습서를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-104">Welcome to the Quantum Development Kit tutorial on writing and simulating a basic quantum program that operates on individual qubits.</span></span> 

<span data-ttu-id="7a1b7-105">Q #은 대규모 퀀텀 프로그램에 대 한 높은 수준의 프로그래밍 언어로 작성 되었지만, 더 낮은 수준의 퀀텀 프로그램을 탐색 하는 데 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-105">Although Q# was primarily created as a high-level programming language for large-scale quantum programs, it can just as easily be used to explore the lower level of quantum programs: directly addressing specific qubits.</span></span>
<span data-ttu-id="7a1b7-106">Q #의 유연성을 통해 사용자는 이러한 추상화 수준에서 퀀텀 시스템에 접근 하는 데 사용할 수 있으며,이 자습서에서는 원하는 비트 단위를 자세히 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-106">The flexibility of Q# allows users to approach quantum systems from any such level of abstraction, and in this tutorial we dive into the qubits themselves.</span></span>
<span data-ttu-id="7a1b7-107">특히, 많은 수의 큰 퀀텀 알고리즘에 필수적인 서브루틴 인 [퀀텀 푸리에 변환](https://en.wikipedia.org/wiki/Quantum_Fourier_transform)의 후드를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-107">Specifically, we take a look under the hood of the [quantum Fourier transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), a subroutine that is integral to many larger quantum algorithms.</span></span>

<span data-ttu-id="7a1b7-108">퀀텀 정보 처리에 대 한이 하위 수준 보기는 시스템의 특정 비트에 대 한 게이트의 순차적 적용을 나타내는 "[퀀텀 회로](xref:microsoft.quantum.concepts.circuits)" 측면에서 설명 하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-108">Note that this low-level view of quantum information processing is often described in terms of "[quantum circuits](xref:microsoft.quantum.concepts.circuits)," which represent the sequential application of gates to specific qubits of a system.</span></span>

<span data-ttu-id="7a1b7-109">따라서 순차적으로 적용 한 단일 및 다중 작업 비트 작업을 "회로 다이어그램"으로 쉽게 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-109">Thus, the single- and multi-qubit operations we sequentially apply can be readily represented in a "circuit diagram."</span></span>
<span data-ttu-id="7a1b7-110">여기서는 회로로 표시 되는 다음 표현이 포함 된 전체 3-비트 퀀텀 푸리에 변환을 수행 하는 Q # 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-110">In our case, we will define a Q# operation to perform the full three-qubit quantum Fourier transform, which has the following representation as a circuit:</span></span>

<br/>
<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a><span data-ttu-id="7a1b7-111">사전 요구 사항</span><span class="sxs-lookup"><span data-stu-id="7a1b7-111">Prerequisites</span></span>

* <span data-ttu-id="7a1b7-112">원하는 언어 및 개발 환경을 사용 하 여 퀀텀 개발 키트를 [설치](xref:microsoft.quantum.install) 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-112">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment.</span></span>
* <span data-ttu-id="7a1b7-113">QDK가 이미 설치되어 있는 경우 최신 버전으로 [업데이트](xref:microsoft.quantum.update)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-113">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>


## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="7a1b7-114">이 자습서에서 학습할 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-114">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="7a1b7-115">Q에서 퀀텀 작업 정의 #</span><span class="sxs-lookup"><span data-stu-id="7a1b7-115">Define quantum operations in Q#</span></span>
> * <span data-ttu-id="7a1b7-116">명령줄에서 또는 기존 호스트 프로그램을 사용 하 여 Q # 작업을 직접 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-116">Call Q# operations directly from the command line or using a classical host program</span></span>
> * <span data-ttu-id="7a1b7-117">측정 출력에 대 한 정량 비트 할당에서 퀀텀 작업 시뮬레이트</span><span class="sxs-lookup"><span data-stu-id="7a1b7-117">Simulate a quantum operation from qubit allocation to measurement output</span></span>
> * <span data-ttu-id="7a1b7-118">작업 전체에서 퀀텀 시스템의 시뮬레이션 된 wavefunction 진화 하는 방식 관찰</span><span class="sxs-lookup"><span data-stu-id="7a1b7-118">Observe how the quantum system's simulated wavefunction evolves throughout the operation</span></span>

<span data-ttu-id="7a1b7-119">Microsoft의 퀀텀 개발 키트를 사용 하 여 퀀텀 프로그램을 실행 하는 작업은 일반적으로</span><span class="sxs-lookup"><span data-stu-id="7a1b7-119">Running a quantum program with Microsoft's Quantum Development Kit typically consists of two parts:</span></span>
1. <span data-ttu-id="7a1b7-120">프로그램 자체는 Q # 퀀텀 프로그래밍 언어를 사용 하 여 구현 된 다음 퀀텀 컴퓨터 또는 퀀텀 시뮬레이터에서 실행 되도록 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-120">The program itself, which is implemented using the Q# quantum programming language, and then invoked to run on a quantum computer or quantum simulator.</span></span> <span data-ttu-id="7a1b7-121">다음으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-121">These consist of</span></span> 
    - <span data-ttu-id="7a1b7-122">Q # 작업: 퀀텀 레지스터에서 동작 하는 서브루틴</span><span class="sxs-lookup"><span data-stu-id="7a1b7-122">Q# operations: subroutines acting on quantum registers, and</span></span> 
    - <span data-ttu-id="7a1b7-123">Q # 함수: 퀀텀 알고리즘 내에서 사용 되는 기존 서브루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-123">Q# functions: classical subroutines used within the quantum algorithm.</span></span>
2. <span data-ttu-id="7a1b7-124">퀀텀 프로그램을 호출 하 고 실행 해야 하는 대상 컴퓨터를 지정 하는 데 사용 되는 진입점입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-124">The entry point used to call the quantum program and specify the target machine on which it should be run.</span></span>
    <span data-ttu-id="7a1b7-125">이 작업은 명령줄에서 직접 수행 하거나 Python 또는 c #과 같은 클래식 프로그래밍 언어로 작성 된 호스트 프로그램을 통해 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-125">This can be done directly from the command line, or through a host program written in a classical programming language like Python or C#.</span></span>
    <span data-ttu-id="7a1b7-126">이 자습서에는 원하는 방법에 대 한 지침이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-126">This tutorial includes instructions for whichever method you prefer.</span></span>

## <a name="allocate-qubits-and-define-quantum-operations"></a><span data-ttu-id="7a1b7-127">이상 비트 할당 및 퀀텀 작업 정의</span><span class="sxs-lookup"><span data-stu-id="7a1b7-127">Allocate qubits and define quantum operations</span></span>

<span data-ttu-id="7a1b7-128">이 자습서의 첫 번째 부분은 `Perform3qubitQFT` 3 개의 성능에서 퀀텀 푸리에 변환을 수행 하는 Q # 작업을 정의 하는 것으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-128">The first part of this tutorial consists of defining the Q# operation `Perform3qubitQFT`, which performs the quantum Fourier transform on three qubits.</span></span> 

<span data-ttu-id="7a1b7-129">또한 함수를 사용 [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) 하 여 세 가지 wavefunction의 시뮬레이션 된 작업이 작업 전체에서 어떻게 진화 하는지 관찰 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-129">In addition, we will use the [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) function to observe how the simulated wavefunction of our three qubit system evolves across the operation.</span></span>

<span data-ttu-id="7a1b7-130">첫 번째 단계는 Q # 프로젝트 및 파일을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-130">The first step is creating your Q# project and file.</span></span>
<span data-ttu-id="7a1b7-131">이에 대 한 단계는 프로그램을 호출 하는 데 사용 하는 환경에 따라 다르며, 각 [설치 가이드](xref:microsoft.quantum.install)에서 세부 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-131">The steps for this depend on the environment you will use to call the program, and you can find the details in the respective [installation guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="7a1b7-132">파일의 구성 요소를 단계별로 안내 하지만 아래의 전체 블록으로도 코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-132">We will walk you through the components of the file step-by-step, but the code is also available as a full block below.</span></span>

### <a name="namespaces-to-access-other-q-operations"></a><span data-ttu-id="7a1b7-133">다른 Q # 작업에 액세스 하기 위한 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="7a1b7-133">Namespaces to access other Q# operations</span></span>
<span data-ttu-id="7a1b7-134">이 파일 내에서 먼저 컴파일러에서 액세스할 네임 스페이스를 정의 합니다 `NamespaceQFT` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-134">Inside the file, we first define the namespace `NamespaceQFT` which will be accessed by the compiler.</span></span>
<span data-ttu-id="7a1b7-135">기존 Q # 작업을 사용 하기 위해 작업을 수행 하려면 관련 `Microsoft.Quantum.<>` 네임 스페이스를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-135">For our operation to make use of existing Q# operations, we open the relevant `Microsoft.Quantum.<>` namespaces.</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a><span data-ttu-id="7a1b7-136">인수를 사용 하 여 작업 정의 및 반환</span><span class="sxs-lookup"><span data-stu-id="7a1b7-136">Define operations with arguments and returns</span></span>
<span data-ttu-id="7a1b7-137">다음으로 작업을 정의 합니다 `Perform3qubitQFT` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-137">Next, we define the `Perform3qubitQFT` operation:</span></span>

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

<span data-ttu-id="7a1b7-138">지금은 작업에서 인수를 사용 하지 않고 아무 것---도 반환 하지 않습니다 .이 경우 `Unit` c #에서와 같은 개체를 반환 하 고 `void` Python에서 빈 튜플을 반환 한다는 것을 작성 합니다 `Tuple[()]` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-138">For now, the operation takes no arguments and does not return anything---in this case we write that it returns a `Unit` object, which is akin to `void` in C# or an empty tuple, `Tuple[()]`, in Python.</span></span>
<span data-ttu-id="7a1b7-139">나중에이를 수정 하 여 측정 결과의 배열을 반환 하도록 지정 합니다. 여기서 point는 `Unit` 로 대체 됩니다 `Result[]` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-139">Later, we will modify it to return an array of measurement results, at which point `Unit` will be replaced by `Result[]`.</span></span> 

### <a name="allocate-qubits-with-using"></a><span data-ttu-id="7a1b7-140">에서의 비트 할당`using`</span><span class="sxs-lookup"><span data-stu-id="7a1b7-140">Allocate qubits with `using`</span></span>
<span data-ttu-id="7a1b7-141">Q # 작업 내에서 먼저 다음 문을 사용 하 여 세 가지의 레지스터를 할당 합니다 `using` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-141">Within our Q# operation, we first allocate a register of three qubits with the `using` statement:</span></span>

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

<span data-ttu-id="7a1b7-142">을 사용 하는 경우에는 `using` $ \ket $ 상태에서 해당 비트가 자동으로 할당 됩니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-142">With `using`, the qubits are automatically allocated in the $\ket{0}$ state.</span></span> <span data-ttu-id="7a1b7-143">및를 사용 하 여이를 확인할 수 있습니다 [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) .이는 문자열과 시스템의 현재 상태를 콘솔에 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-143">We can verify this by using [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) and [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine), which print a string and the system's current state to the console.</span></span>

> [!NOTE]
> <span data-ttu-id="7a1b7-144">및 `Message(<string>)` `DumpMachine()` 함수 ( [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) 각각 및)는 콘솔에 직접 인쇄 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-144">The `Message(<string>)` and `DumpMachine()` functions (from [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics), respectively) both print directly to the console.</span></span> <span data-ttu-id="7a1b7-145">실제 퀀텀 계산과 마찬가지로 Q #은이에 대 한 직접 액세스를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-145">Just like a real quantum computation, Q# does not allow us to directly access qubit states.</span></span>
> <span data-ttu-id="7a1b7-146">그러나는 `DumpMachine` 대상 컴퓨터의 현재 상태를 인쇄 하므로 전체 상태 시뮬레이터와 함께 사용 될 때 디버깅 및 학습에 대 한 중요 한 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-146">However, as `DumpMachine` prints the target machine's current state, it can provide valuable insight for debugging and learning when used in conjunction with the full state simulator.</span></span>


### <a name="applying-single-qubit-and-controlled-gates"></a><span data-ttu-id="7a1b7-147">단일 및 제어 되는 게이트 적용</span><span class="sxs-lookup"><span data-stu-id="7a1b7-147">Applying single-qubit and controlled gates</span></span>

<span data-ttu-id="7a1b7-148">다음으로 작업 자체를 구성 하는 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-148">Next, we apply the gates which comprise the operation itself.</span></span>
<span data-ttu-id="7a1b7-149">Q #에는 네임 스페이스의 작업으로 이미 많은 기본 퀀텀 문이 포함 되어 [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) 있으며, 이러한 작업은 예외가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-149">Q# already contains many basic quantum gates as operations in the [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, and these are no exception.</span></span> 

<span data-ttu-id="7a1b7-150">Q # 작업 내에서 callables을 호출 하는 문은 물론 순차적으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-150">Within a Q# operation, the statements invoking callables will of course be executed in sequential order.</span></span>
<span data-ttu-id="7a1b7-151">따라서 첫 번째는 적용 되는 첫 번째 게이트가 [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard)입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-151">Hence, the first gate to apply is the [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) to the first qubit:</span></span>

<br/>
<img src="./qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

<span data-ttu-id="7a1b7-152">레지스터 (예: 배열의 단일)에 작업을 적용 하려면 `Qubit` `Qubit[]` 표준 인덱스 표기법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-152">To apply an operation to a specific qubit from a register (i.e. a single `Qubit` from an array `Qubit[]`) we use standard index notation.</span></span>
<span data-ttu-id="7a1b7-153">따라서를 [`H`](xref:microsoft.quantum.intrinsic.h) 등록의 첫 번째 비트에 적용 하면 `qs` 다음 형식이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-153">So, applying the [`H`](xref:microsoft.quantum.intrinsic.h) to the first qubit of our register `qs` takes the form:</span></span>

```qsharp
            H(qs[0]);
```

<span data-ttu-id="7a1b7-154">(Hadamard) 게이트를 개별의 개별 비트에 적용 하는 것 외에도 `H` QFT 회로는 주로 제어 되는 회전으로 구성 됩니다 [`R1`](xref:microsoft.quantum.intrinsic.r1) .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-154">Besides applying the `H` (Hadamard) gate to individual qubits, the QFT circuit consists primarily of controlled [`R1`](xref:microsoft.quantum.intrinsic.r1) rotations.</span></span>
<span data-ttu-id="7a1b7-155">`R1(θ, <qubit>)`일반적으로 작업은 {0} $e ^ {i\theta} $의 회전을 $ \ket $ 구성 요소에 적용 하는 동안의 $ \ket $ 구성 요소를 변경 하지 않고 그대로 유지 합니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-155">An `R1(θ, <qubit>)` operation in general leaves the $\ket{0}$ component of the qubit unchanged, while applying a rotation of $e^{i\theta}$ to the $\ket{1}$ component.</span></span>

#### <a name="controlled-operations"></a><span data-ttu-id="7a1b7-156">제어 된 작업</span><span class="sxs-lookup"><span data-stu-id="7a1b7-156">Controlled operations</span></span>

<span data-ttu-id="7a1b7-157">Q #을 사용 하면 하나 또는 여러 컨트롤의 작업을 매우 쉽게 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-157">Q# makes it extremely easy to condition the execution of an operation upon one or multiple control qubits.</span></span>
<span data-ttu-id="7a1b7-158">일반적으로 호출을로 호출 하 `Controlled` 고 작업 인수가 다음과 같이 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-158">In general, we merely preface the call with `Controlled`, and the operation arguments change as:</span></span>

 <span data-ttu-id="7a1b7-159">`Op(<normal args>)`$ \to $ `Controlled Op([<control qubits>], (<normal args>))` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-159">`Op(<normal args>)` $\to$ `Controlled Op([<control qubits>], (<normal args>))`.</span></span>

<span data-ttu-id="7a1b7-160">컨트롤은 단일 비트 인 경우에도 배열로 제공 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-160">Note that the control qubits must be provided as an array, even if it is a single qubit.</span></span>

<span data-ttu-id="7a1b7-161">이후에는 `H` 다음 게이트가 `R1` 첫 번째의 작업을 수행 하 고 두 번째/셋째로 제어 되는 게이트 임을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-161">After the `H`, we see that the next gates are the `R1` gates acting on the first qubit (and controlled by the second/third):</span></span>

<br/>
<img src="./qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

<span data-ttu-id="7a1b7-162">다음을 사용 하 여이를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-162">We call these with</span></span>

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

<span data-ttu-id="7a1b7-163">네임 스페이스의 함수를 사용 하 여 [`PI()`](xref:microsoft.quantum.math.pi) [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) pi 라디안 측면에서 회전을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-163">Note that we use the [`PI()`](xref:microsoft.quantum.math.pi) function from the [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace to define the rotations in terms of pi radians.</span></span>
<span data-ttu-id="7a1b7-164">또한 정수로 나누기는 `Double` `2.0` `2` 형식 오류를 throw 하기 때문에 (예:)로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-164">Additionally, we divide by a `Double` (e.g. `2.0`) because dividing by an integer `2` would throw a type error.</span></span> 

> [!TIP]
> <span data-ttu-id="7a1b7-165">`R1(π/2)`및 `R1(π/4)` 는 `S` 및 `T` 작업과 동일 합니다 (에도 해당 `Microsoft.Quantum.Intrinsic` ).</span><span class="sxs-lookup"><span data-stu-id="7a1b7-165">`R1(π/2)` and `R1(π/4)` are equivalent to the `S` and `T` operations (also in `Microsoft.Quantum.Intrinsic`).</span></span>


<span data-ttu-id="7a1b7-166">관련 `H` 작업 및 제어 된 회전을 두 번째 및 세 번째 비트에 적용 한 후:</span><span class="sxs-lookup"><span data-stu-id="7a1b7-166">After applying the relevant `H` operations and controlled rotations to the second and third qubits:</span></span>

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

<span data-ttu-id="7a1b7-167">회로를 완료 하려면 게이트를 적용 하기만 하면 됩니다 [`SWAP`](xref:microsoft.quantum.intrinsic.swap) .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-167">we need only apply a [`SWAP`](xref:microsoft.quantum.intrinsic.swap) gate to complete the circuit:</span></span>

```qsharp
            SWAP(qs[2], qs[0]);
```

<span data-ttu-id="7a1b7-168">이는 양자를 사용 하는 경우에 필요 합니다. 즉, 양자를 사용 하 여 서브루틴을 더 큰 알고리즘으로 원활 하 게 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-168">This is necessary because the nature of the quantum Fourier transform outputs the qubits in reverse order, so the swaps allow for seamless integration of the subroutine into larger algorithms.</span></span>

<span data-ttu-id="7a1b7-169">따라서 Q # 작업에 퀀텀 푸리에 변환의 엔터프라이즈급 비트 작업을 작성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-169">Hence we have finished writing the qubit-level operations of the quantum Fourier transform into our Q# operation:</span></span>

<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

<span data-ttu-id="7a1b7-170">그러나 아직 하루에는 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-170">However, we can't call it a day just yet.</span></span>
<span data-ttu-id="7a1b7-171">Microsoft는이 기능을 {0} 할당 했을 때 $ \ket $ 상태 였습니다. Q #에서는이를 검색 하는 것과 같은 방식으로 그대로 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-171">Our qubits were in state $\ket{0}$ when we allocated them, and much like in life, in Q# we should leave things the same way we found them (or better!).</span></span>

### <a name="deallocate-qubits"></a><span data-ttu-id="7a1b7-172">비트 할당 취소</span><span class="sxs-lookup"><span data-stu-id="7a1b7-172">Deallocate qubits</span></span>

<span data-ttu-id="7a1b7-173">다시 호출 [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) 하 여 사후 작업 상태를 확인 하 고, 마지막으로를 호출 하 여 작업을 완료 하기 전에 다음과 같이를 다시 호출 하 여 작업을 [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) 완료 하기 전에이를 $ \ket $로 다시 설정 합니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-173">We call [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) again to see the post-operation state, and finally apply [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) to the qubit register to reset our qubits to $\ket{0}$ before completing the operation:</span></span>

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

<span data-ttu-id="7a1b7-174">할당 되지 않은 모든 작업을 명시적으로 $ \ket $로 설정 해야 하는 것 {0} 은 다른 작업에서 동일한 기능을 사용 하기 시작할 때 해당 상태를 정확 하 게 알 수 있기 때문에 Q #의 기본 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-174">Requiring that all deallocated qubits be explicitly set to $\ket{0}$ is a basic feature of Q#, as it allows other operations to know their state precisely when they begin using those same qubits (a scarce resource).</span></span>
<span data-ttu-id="7a1b7-175">또한 시스템의 다른 모든 비트를 사용 하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-175">Additionally, this assures that they not be entangled with any other qubits in the system.</span></span>
<span data-ttu-id="7a1b7-176">할당 블록의 끝에서 reset을 수행 하지 않으면 `using` 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-176">If the reset is not performed at the end of a `using` allocation block, a runtime error will be thrown.</span></span>

<span data-ttu-id="7a1b7-177">이제 전체 Q # 파일이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-177">Your full Q# file should now look like this:</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


<span data-ttu-id="7a1b7-178">Q # 파일 및 작업이 완료 되 면 퀀텀 프로그램을 호출 하 고 시뮬레이션할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-178">With the Q# file and operation complete, our quantum program is ready to be called and simulated.</span></span>

## <a name="execute-the-program"></a><span data-ttu-id="7a1b7-179">프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="7a1b7-179">Execute the program</span></span>

<span data-ttu-id="7a1b7-180">파일에 Q # 작업을 정의 했으므로 `.qs` 이제 해당 작업을 호출 하 고 반환 된 모든 기존 데이터를 관찰 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-180">Having defined our Q# operation in a `.qs` file, we now need to call that operation and observe any returned classical data.</span></span>
<span data-ttu-id="7a1b7-181">지금은 반환 된 내용이 없지만 (위에서 정의한 작업이 반환 됨 `Unit` ) 나중에 Q # 작업을 수정 하 여 측정 결과 ()의 배열을 반환 하는 경우에는 `Result[]` 이를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-181">For now, there isn't anything returned (recall that our operation defined above returns `Unit`), but when we later modify the Q# operation to return an array of measurement results (`Result[]`), we will address this.</span></span>

<span data-ttu-id="7a1b7-182">Q # 프로그램은이를 호출 하는 데 사용 되는 환경에서의 작업을 수행 하는 반면,이 작업을 수행 하는 방법은 다양 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-182">While the Q# program is ubiquitous across the environments used to call it, the manner of doing so will of course vary.</span></span> <span data-ttu-id="7a1b7-183">따라서 설정에 해당 하는 탭의 지침을 따르면 됩니다. Q # 명령줄 응용 프로그램에서 작업 하거나 Python 또는 c #에서 호스트 프로그램을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-183">As such, simply follow the instructions in the tab corresponding to your setup: working from the Q# command line application or using a host program in Python or C#.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="7a1b7-184">명령 줄</span><span class="sxs-lookup"><span data-stu-id="7a1b7-184">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="7a1b7-185">명령줄에서 Q # 프로그램을 실행 하려면 Q # 파일을 약간만 변경 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-185">Running the Q# program from the command line requires only a small change to the Q# file.</span></span>

<span data-ttu-id="7a1b7-186">`@EntryPoint()`작업 정의 앞의 줄에를 추가 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-186">Simply add `@EntryPoint()` to a line preceding the operation definition:</span></span>

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

<span data-ttu-id="7a1b7-187">프로그램을 실행 하려면 프로젝트의 폴더에서 터미널을 열고 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-187">To run the program, open the terminal in the folder of your project and enter</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="7a1b7-188">실행 시 `Message` `DumpMachine` 콘솔에 아래 출력 및 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-188">Upon execution, you should see the `Message` and `DumpMachine` outputs below printed in your console.</span></span>


#### <a name="python"></a>[<span data-ttu-id="7a1b7-189">Python</span><span class="sxs-lookup"><span data-stu-id="7a1b7-189">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="7a1b7-190">Python 호스트 파일을 만듭니다 `host.py` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-190">Create a Python host file: `host.py`.</span></span>

<span data-ttu-id="7a1b7-191">호스트 파일은 다음과 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-191">The host file is constructed as follows:</span></span> 
1. <span data-ttu-id="7a1b7-192">먼저, `qsharp` Q # 상호 운용성에 대 한 모듈 로더를 등록 하는 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-192">First, we import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="7a1b7-193">이를 통해 q # 작업을 가져올 수 있는 Python 모듈로 표시 되는 Q # 네임 스페이스 (예: `NamespaceQFT` q # 파일에 정의 된)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-193">This allows Q# namespaces (e.g. the `NamespaceQFT` we defined in our Q# file) to appear as Python modules, from which we can import Q# operations.</span></span>
2. <span data-ttu-id="7a1b7-194">그런 다음이 경우---직접 호출 하는 Q # 작업을 가져옵니다 `Perform3qubitQFT` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-194">Then, import the Q# operations which we will directly invoke---in this case, `Perform3qubitQFT`.</span></span>
    <span data-ttu-id="7a1b7-195">진입점을 Q # 프로그램 으로만 가져와야 합니다. 즉 _not_ `H` `R1` , 다른 q # 작업에서 호출 하지만 기존 호스트에서는 호출 하지 않는와 같은 작업은 수행 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-195">We need only import the entry point into a Q# program (i.e. _not_ operations like `H` and `R1`, which are called by other Q# operations but never by the classical host).</span></span>
3. <span data-ttu-id="7a1b7-196">Q # 작업 또는 함수를 시뮬레이션 하는 경우 폼을 사용 `<Q#callable>.simulate(<args>)` 하 여 `QuantumSimulator()` 대상 컴퓨터에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-196">In simulating Q# operations or functions, use the form `<Q#callable>.simulate(<args>)` to run them on the `QuantumSimulator()` target machine.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a1b7-197">예를 들어와 같이 다른 컴퓨터에서 작업을 호출 하려는 경우를 `ResourceEstimator()` 사용 `<Q#callable>.estimate_resources(<args>)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-197">If we wanted to call the operation on a different machine, for example the `ResourceEstimator()`, we would simply use `<Q#callable>.estimate_resources(<args>)`.</span></span>
> <span data-ttu-id="7a1b7-198">일반적으로 Q # 작업은 실행 되는 컴퓨터와는 독립적 이지만와 같은 일부 기능은 `DumpMachine` 다르게 동작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-198">In general, Q# operations are agnostic to the machines on which they're run, but some features such as `DumpMachine` may behave differently.</span></span>

4. <span data-ttu-id="7a1b7-199">시뮬레이션을 수행할 때 작업 호출은 Q # 파일에 정의 된 대로 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-199">Upon performing the simulation, the operation call will return values as defined in the Q# file.</span></span>
    <span data-ttu-id="7a1b7-200">지금은 아무 것도 반환 되지 않지만 나중에 이러한 값을 할당 하 고 처리 하는 예제를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-200">For now there is nothing returned, but later on we will see an example of assigning and processing these values.</span></span>
    <span data-ttu-id="7a1b7-201">실습 및 완전히 고전의 결과 데이터를 사용 하 여 원하는 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-201">With the resultant data in our hands and totally classical, we can do whatever we'd like with it.</span></span>

<span data-ttu-id="7a1b7-202">전체 `host.py` 파일은 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-202">Your full `host.py` file should be this:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

<span data-ttu-id="7a1b7-203">Python 파일을 실행 하 고 콘솔에 인쇄 하 여 `Message` 아래와 출력을 확인 해야 합니다 `DumpMachine` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-203">Run the Python file, and printed in your console you should see the `Message` and `DumpMachine` outputs below.</span></span> 


#### <a name="c"></a>[<span data-ttu-id="7a1b7-204">C#</span><span class="sxs-lookup"><span data-stu-id="7a1b7-204">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="7a1b7-205">[설치 가이드](xref:microsoft.quantum.install.cs)에 나와 있는 것과 동일한 지침에 따라 c # 호스트 파일을 만들고 이름을로 바꿉니다 `host.cs` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-205">Following the same instructions as in the [install guide](xref:microsoft.quantum.install.cs), create a C# host file, and rename it to `host.cs`.</span></span>

<span data-ttu-id="7a1b7-206">C # 호스트는 네 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-206">The C# host has four parts:</span></span>
1. <span data-ttu-id="7a1b7-207">양자 시뮬레이터를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-207">Construct a quantum simulator.</span></span>
    <span data-ttu-id="7a1b7-208">아래 코드에서 변수입니다 `qsim` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-208">In the code below, this is the variable `qsim`.</span></span>
2. <span data-ttu-id="7a1b7-209">양자 알고리즘에 필요한 인수를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-209">Compute any arguments required for the quantum algorithm.</span></span>
    <span data-ttu-id="7a1b7-210">이 예제에는 없음이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-210">There are none in this example.</span></span>
3. <span data-ttu-id="7a1b7-211">양자 알고리즘을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-211">Run the quantum algorithm.</span></span> 
    <span data-ttu-id="7a1b7-212">각 Q# 연산은 동일한 이름의 C# 클래스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-212">Each Q# operation generates a C# class with the same name.</span></span> 
    <span data-ttu-id="7a1b7-213">이 클래스에는 **비동기적으로** 연산을 실행하는 `Run` 메서드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-213">This class has a `Run` method that **asynchronously** executes the operation.</span></span>
    <span data-ttu-id="7a1b7-214">실제 하드웨어에서 비동기적으로 실행되므로 실행이 비동기적입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-214">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> 
    <span data-ttu-id="7a1b7-215">메서드가 비동기 이기 때문에 `Run` 메서드를 호출 합니다 `Wait()` .이 메서드는 작업이 완료 될 때까지 실행을 차단 하 고 결과를 동기적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-215">Because the `Run` method is asynchronous, we call the `Wait()` method; this blocks execution until the task completes and returns the result synchronously.</span></span> 
4. <span data-ttu-id="7a1b7-216">작업의 반환 된 결과를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-216">Process the returned result of the operation.</span></span>
    <span data-ttu-id="7a1b7-217">지금은 작업에서 아무 것도 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-217">For now, the operation returns nothing.</span></span>


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
<span data-ttu-id="7a1b7-218">응용 프로그램을 실행 하면 출력이 아래와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-218">Run the application, and your output should match that below.</span></span>
<span data-ttu-id="7a1b7-219">키를 누르면 프로그램이 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-219">The program will exit after you press a key.</span></span>
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

<span data-ttu-id="7a1b7-220">전체 상태 시뮬레이터에서 호출 될 때는 `DumpMachine()` 퀀텀 상태 wavefunction의 다양 한 표현을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-220">When called on the full-state simulator, `DumpMachine()` provides these mutliple representations of the quantum state's wavefunction.</span></span> <span data-ttu-id="7a1b7-221">$N $-hbit 시스템의 가능한 상태는 $2 ^ n $ 계산 기준 상태로 표시 될 수 있으며 각각은 해당 하는 복잡 한 계수 (진폭 및 단계)를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-221">The possible states of an $n$-qubit system can be represented by $2^n$ computational basis states, each with a corresponding complex coefficient (simply an amplitude and a phase).</span></span>
<span data-ttu-id="7a1b7-222">계산 기준 상태는 가능한 모든 이진 문자열 길이 $n $---즉, \ket $ 및 $ \ket $ 및 $ $의 가능한 모든 조합에 해당 합니다 {0} {1} . 여기서 각 이진 숫자는 개별 비트에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-222">The computational basis states correspond to all the possible binary strings of length $n$---that is, all the possible combinations of qubit states $\ket{0}$ and $\ket{1}$, where each binary digit corresponds to an individual qubit.</span></span>

<span data-ttu-id="7a1b7-223">첫 번째 행은 중요 한 순서 대로 해당 하는의 Id를 사용 하 여 주석을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-223">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="7a1b7-224">`2`"가장 중요 한" 것은 단지 기본 상태 vector $ \ket{i} $의 이진 표현에서, 고 비트의 상태는 `2` 맨 왼쪽 숫자에 해당 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-224">Qubit `2` being the "most significant" simply means that in the binary representation of basis state vector $\ket{i}$, the state of qubit `2` corresponds to the left-most digit.</span></span> <span data-ttu-id="7a1b7-225">예를 들어 $ \ket {6} = \ket {110} $은 $ `2` `1` \ket $의 $ \ket $ 및의 두 가지로 구성 {1} `0` {0} 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-225">For example, $\ket{6} = \ket{110}$ comprises qubits `2` and `1` both in $\ket{1}$ and qubit `0` in $\ket{0}$.</span></span>


<span data-ttu-id="7a1b7-226">나머지 행은 데카르트 및 극좌표 형식의 기본 상태 vector $ \ket{i} $를 측정 하는 확률 진폭을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-226">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{i}$ in both Cartesian and polar formats.</span></span>
<span data-ttu-id="7a1b7-227">입력 상태 $ \ket $의 첫 번째 행에 대해 자세히 설명 합니다 {000} .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-227">In detail for the first row of our input state $\ket{000}$:</span></span>
* <span data-ttu-id="7a1b7-228">**`|0>:`** 이 행은 `0` 계산 기준 상태에 해당 합니다 (초기 상태 사후 할당이 $ \ket $로 지정 된 {000} 경우이 시점에서 확률 진폭의 유일한 상태가 됨).</span><span class="sxs-lookup"><span data-stu-id="7a1b7-228">**`|0>:`** this row corresponds to the `0` computational basis state (given that our initial state post-allocation was $\ket{000}$, we would expect this to be the only state with probability amplitude at this point).</span></span>
* <span data-ttu-id="7a1b7-229">**`1.000000 +  0.000000 i`**: 데카르트 형식의 확률 진폭입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-229">**`1.000000 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="7a1b7-230">**` == `**: `equal` 부호는 두 동등한 표현을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-230">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="7a1b7-231">**`********************`**: 크기의 그래픽 표현으로,의 수는 `*` 이 상태 벡터를 측정할 확률에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-231">**`********************`**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span> 
* <span data-ttu-id="7a1b7-232">**`[ 1.000000 ]`**: 크기의 숫자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-232">**`[ 1.000000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="7a1b7-233">**`    ---`**: 진폭의 단계를 그래픽으로 표현한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-233">**`    ---`**: A graphical representation of the amplitude's phase.</span></span>
* <span data-ttu-id="7a1b7-234">**`[ 0.0000 rad ]`**: 단계의 숫자 값 (라디안 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-234">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="7a1b7-235">크기와 단계가 모두 그래픽 표현으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-235">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="7a1b7-236">크기 표현은 간단 합니다. 즉, 막대를 표시 하 `*` 고 확률이 높을수록 막대가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-236">The magnitude representation is straightforward: it shows a bar of `*`, and the higher the probability, the larger the bar will be.</span></span> <span data-ttu-id="7a1b7-237">단계는 [테스트 및 디버깅:](xref:microsoft.quantum.guide.testingdebugging#dump-functions) 각도 범위를 기준으로 가능한 기호 표현의 덤프 함수를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-237">For the phase, see [Testing and debugging: dump functions](xref:microsoft.quantum.guide.testingdebugging#dump-functions) for the possible symbol representations based on angle ranges.</span></span>


<span data-ttu-id="7a1b7-238">따라서 인쇄 된 출력은 프로그래밍 된 게이트가</span><span class="sxs-lookup"><span data-stu-id="7a1b7-238">So, the printed output is illustrating that our programmed gates transformed our state from</span></span>

<span data-ttu-id="7a1b7-239">$ $ \ket{\psi} \_ {초기} = \ket {000} $ $</span><span class="sxs-lookup"><span data-stu-id="7a1b7-239">$$ \ket{\psi}\_{initial} = \ket{000} $$</span></span>

<span data-ttu-id="7a1b7-240">다음으로 변경:</span><span class="sxs-lookup"><span data-stu-id="7a1b7-240">to</span></span> 

<span data-ttu-id="7a1b7-241">$ $ \begin{align} \ket{\psi} \_ {final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="7a1b7-241">$$ \begin{align} \ket{\psi}\_{final} &= \frac{1}{\sqrt{8}} \left( \ket{000} + \ket{001} + \ket{010} + \ket{011} + \ket{100} + \ket{101} + \ket{110} + \ket{111}  \right) \\\\ &= \frac{1}{\sqrt{2^n}}\sum\_{j=0}^{2^n-1} \ket{j}, \end{align} $$</span></span>

<span data-ttu-id="7a1b7-242">이는 3-이상 비트 푸리에 변환의 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-242">which is precisely the behavior of the 3-qubit Fourier transform.</span></span> 

<span data-ttu-id="7a1b7-243">다른 입력 상태가 영향을 받는 방법에 대 한 자세한 내용을 보려면 변형 전에 원하는 비트 작업을 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-243">If you are curious about how other input states are affected, we encourage you to play around with applying qubit operations before the transform.</span></span>

## <a name="adding-measurements"></a><span data-ttu-id="7a1b7-244">측정값 추가</span><span class="sxs-lookup"><span data-stu-id="7a1b7-244">Adding measurements</span></span>

<span data-ttu-id="7a1b7-245">불행 하 게도 퀀텀 메커니즘을 cornerstone 실제 퀀텀 시스템은 이러한 기능을 가질 수 없다는 것을 알 수 `DumpMachine` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-245">Unfortunately, a cornerstone of quantum mechanics tells us that a real quantum system cannot have such a `DumpMachine` function.</span></span> <span data-ttu-id="7a1b7-246">대신 일반적으로 전체 퀀텀 상태를 제공 하는 데 실패할 뿐만 아니라 시스템 자체를 크게 변경할 수 있는 측정을 통해 정보를 추출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-246">Instead, we're forced to extract information through measurements, which in general not only fail to provide us the full quantum state, but can also drastically alter the system itself.</span></span>
<span data-ttu-id="7a1b7-247">다양 한 종류의 퀀텀 측정이 있지만 가장 기본적인: projective 측정에 중점을 두고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-247">There are many sorts of quantum measurements, but we will focus on the most basic: projective measurements on single qubits.</span></span>
<span data-ttu-id="7a1b7-248">지정 된 기준 (예: 계산 기준 $ \{ \ket {0} , \ket $)을 기준으로 하는 경우에는 {1} \} 두 값 사이에 있는 모든 superposition를 소멸---측정 된 기준에 따른 비트 상태를 예측 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-248">Upon measurement in a given basis (e.g. the computational basis $ \{ \ket{0}, \ket{1} \} $), the qubit state is projected onto whichever basis state was measured---hence destroying any superposition between the two.</span></span>

<span data-ttu-id="7a1b7-249">Q # 프로그램 내에서 측정값을 구현 하기 위해 `M` 형식을 반환 하는 작업 (의 경우)을 사용 합니다 `Microsoft.Quantum.Intrinsic` `Result` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-249">To implement measurements within a Q# program, we use the `M` operation (from `Microsoft.Quantum.Intrinsic`), which returns a `Result` type.</span></span>

<span data-ttu-id="7a1b7-250">첫째, `Perform3QubitQFT` 대신 측정 결과 배열을 반환 하도록 작업을 수정 `Result[]` `Unit` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-250">First, we modify our `Perform3QubitQFT` operation to return an array of measurement results, `Result[]`, instead of `Unit`.</span></span>

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a><span data-ttu-id="7a1b7-251">배열 정의 및 초기화 `Result[]`</span><span class="sxs-lookup"><span data-stu-id="7a1b7-251">Define and initialize `Result[]` array</span></span>

<span data-ttu-id="7a1b7-252">이 경우에는 (즉, 문 앞에 있는 `using` ),이 세 번째 길이의 배열을 선언 하 고 바인딩합니다. `Result`</span><span class="sxs-lookup"><span data-stu-id="7a1b7-252">Before even allocating qubits (i.e. before the `using` statement), we declare and bind this length-3 array (one `Result` for each qubit):</span></span> 

```qsharp
        mutable resultArray = new Result[3];
```

<span data-ttu-id="7a1b7-253">`mutable`앞 키워드를 `resultArray` 사용 하면---코드에서 나중에 (예: 측정 결과를 추가할 때) 변수를 다시 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-253">The `mutable` keyword prefacing `resultArray` allows the variable to be rebound later in the code---for example, when adding our measurement results.</span></span>

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a><span data-ttu-id="7a1b7-254">루프에서 측정값을 수행 `for` 하 고 배열에 결과를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-254">Perform measurements in a `for` loop and add results to array</span></span>

<span data-ttu-id="7a1b7-255">블록 내의 푸리에 변환 작업 후에 `using` 다음 코드를 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-255">After the Fourier transform operations inside the `using` block, insert the following code:</span></span>

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
<span data-ttu-id="7a1b7-256">[`IndexRange`](xref:microsoft.quantum.arrays.indexrange)배열에 대해 호출 되는 함수 (예: 값의 배열)는 `qs` 배열의 인덱스에 대해 범위를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-256">The [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) function called on an array (e.g. our array of qubits, `qs`) returns a range over the indices of the array.</span></span> <span data-ttu-id="7a1b7-257">여기서 `for` 는 문을 사용 하 여 각 비트를 순차적으로 측정 하기 위해 루프에서 사용 `M(qs[i])` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-257">Here, we use it in our `for` loop to sequentially measure each qubit using the `M(qs[i])` statement.</span></span>
<span data-ttu-id="7a1b7-258">그러면 각 측정 된 `Result` 형식 ( `Zero` 또는 `One` )이 `resultArray` 업데이트 및 재할당 문으로의 해당 인덱스 위치에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-258">Each measured `Result` type (either `Zero` or `One`) is then added to the corresponding index position in `resultArray` with an update-and-reassign statement.</span></span>

> [!NOTE]
> <span data-ttu-id="7a1b7-259">이 문의 구문은 Q #에서 고유 하지만 `resultArray[i] <- M(qs[i])` F # 및 R과 같은 다른 언어에서 보이는 유사한 변수 재할당에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-259">The syntax of this statement is unique to Q#, but corresponds to the similar variable reassignment `resultArray[i] <- M(qs[i])` seen in other languages such as F# and R.</span></span>

<span data-ttu-id="7a1b7-260">키워드는를 `set` 사용 하 여 바인딩된 변수를 다시 할당 하는 데 항상 사용 됩니다 `mutable` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-260">The keyword `set` is always used to reassign variables bound using `mutable`.</span></span>

#### <a name="return-resultarray"></a><span data-ttu-id="7a1b7-261">돌려`resultArray`</span><span class="sxs-lookup"><span data-stu-id="7a1b7-261">Return `resultArray`</span></span>

<span data-ttu-id="7a1b7-262">3 개의 모든 비트를 측정 하 고 결과를에 추가 하 여 `resultArray` 이전 처럼 이제는이를 다시 설정 하 고 할당을 취소 해도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-262">With all three qubits measured and the results added to `resultArray`, we are safe to reset and deallocate the qubits as before.</span></span>
<span data-ttu-id="7a1b7-263">`using`블록을 닫은 후 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-263">After the `using` block's close, insert</span></span>

```qsharp
        return resultArray;
```
<span data-ttu-id="7a1b7-264">궁극적으로 작업의 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-264">to ultimately return the output of our operation.</span></span> 

### <a name="understanding-the-effects-of-measurement"></a><span data-ttu-id="7a1b7-265">측정 효과 이해</span><span class="sxs-lookup"><span data-stu-id="7a1b7-265">Understanding the effects of measurement</span></span>

<span data-ttu-id="7a1b7-266">`DumpMachine`측정 전후에 상태를 출력 하도록 함수의 배치를 변경해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-266">Let's change the placement of our `DumpMachine` functions to output the state before and after the measurements.</span></span>
<span data-ttu-id="7a1b7-267">최종 작업 코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-267">The final operation code should look like:</span></span> 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

<span data-ttu-id="7a1b7-268">명령줄에서 작업 하는 경우 반환 된 배열은 단순히 실행이 끝날 때 콘솔에 직접 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-268">If you are working from the command line, the returned array will simply be printed directly to the console at the end of the execution.</span></span>
<span data-ttu-id="7a1b7-269">그렇지 않으면 반환 된 배열을 처리 하도록 호스트 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-269">Otherwise, update your host program to process the returned array.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="7a1b7-270">명령 줄</span><span class="sxs-lookup"><span data-stu-id="7a1b7-270">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="7a1b7-271">콘솔에 출력 되는 반환 된 배열을 보다 잘 이해 하기 위해 `Message` 문 바로 앞에 있는 Q # 파일에 다른 배열을 추가할 수 있습니다 `return` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-271">To have more understanding of the returned array which will be printed in the console, we can add another `Message` in the Q# file just before the `return` statement:</span></span>

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

<span data-ttu-id="7a1b7-272">프로젝트를 실행 하면 출력이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-272">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[<span data-ttu-id="7a1b7-273">Python</span><span class="sxs-lookup"><span data-stu-id="7a1b7-273">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="7a1b7-274">Python 프로그램을 다음으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-274">Update your Python program to the following:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

<span data-ttu-id="7a1b7-275">파일을 실행 하면 출력이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-275">Run the file, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[<span data-ttu-id="7a1b7-276">C#</span><span class="sxs-lookup"><span data-stu-id="7a1b7-276">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="7a1b7-277">이제 작업에서 결과를 반환 했으므로 메서드 호출을 `Wait()` 속성 인출으로 바꿉니다 `Result` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-277">Now that our operation is returning a result, replace the method call `Wait()` with fetching the `Result` property.</span></span> <span data-ttu-id="7a1b7-278">이는 앞에서 설명한 것과 동일한 synchronicity을 계속 수행 하 고이 값을 변수에 직접 바인딩할 수 있습니다 `measurementResult` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-278">This still accomplishes the same synchronicity discussed earlier, and we can directly bind this value to the variable `measurementResult`.</span></span>

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="7a1b7-279">프로젝트를 실행 하면 출력이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-279">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

<span data-ttu-id="7a1b7-280">이 출력은 몇 가지 다른 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-280">This output illustrates a few different things:</span></span>
1. <span data-ttu-id="7a1b7-281">반환 된 결과를 사전 측정 결과와 비교 하는 `DumpMachine` 것은 기준 상태에 대해 QFT superposition를 명확 하 게 설명 _하지_ 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-281">Comparing the returned result to the pre-measurement `DumpMachine`, it clearly does _not_ illustrate the post-QFT superposition over basis states.</span></span>
    <span data-ttu-id="7a1b7-282">측정은 시스템의 wavefunction에서 해당 상태의 진폭에 의해 결정 되는 확률을 사용 하 여 단일 기준 상태만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-282">A measurement only returns a single basis state, with a probability determined by the amplitude of that state in the system's wavefunction.</span></span>
2. <span data-ttu-id="7a1b7-283">사후 측정에서 측정값은 `DumpMachine` 상태 자체를 _변경_ 하 여 초기 superposition 기준 상태를 측정 된 값에 해당 하는 단일 기준 상태로 프로젝션 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-283">From the post-measurement `DumpMachine`, we see that measurement _changes_ the state itself, projecting it from the initial superposition over basis states to the single basis state that corresponds to the measured value.</span></span>

<span data-ttu-id="7a1b7-284">이 작업을 여러 번 반복 하는 경우 결과 통계는 각 샷의 무작위 결과를 제공 하는 QFT 상태의 동일 하 게 가중치가 적용 된 superposition을 보여 주기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-284">If we were to repeat this operation many times, we would see the result statistics begin to illustrate the equally weighted superposition of the post-QFT state that gives rise to a random result on each shot.</span></span>
<span data-ttu-id="7a1b7-285">_그러나_비효율적이 고 여전히 아직까지 완벽 하는 것 외에도,이 경우에는 그 사이에 상대적인 단계가 아니라 전용 상태의 상대적 amplitudes 재현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-285">_However_, besides being inefficient and still imperfect, this would nevertheless only reproduce the relative amplitudes of the basis states, not the relative phases between them.</span></span>
<span data-ttu-id="7a1b7-286">후자는이 예에서는 문제가 되지 않지만 $ \ket $ 보다 QFT에 더 복잡 한 입력이 지정 된 경우에는 상대 단계가 표시 됩니다 {000} .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-286">The latter is not an issue in this example, but we would see relative phases appear if given a more complex input to the QFT than $\ket{000}$.</span></span>

#### <a name="partial-measurements"></a><span data-ttu-id="7a1b7-287">부분 측정</span><span class="sxs-lookup"><span data-stu-id="7a1b7-287">Partial measurements</span></span> 
<span data-ttu-id="7a1b7-288">레지스터의 일부를 측정 하 여 시스템의 상태에 영향을 줄 수 있는 방법을 살펴보려면 다음을 루프 내부에 추가 해 보세요 `for` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-288">To explore how measuring only some qubits of the register can affect the system's state, try adding the following inside the `for` loop, after the measurement line:</span></span>
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

<span data-ttu-id="7a1b7-289">이 함수에 액세스 하려면 다음을 추가 해야 합니다. `IntAsString`</span><span class="sxs-lookup"><span data-stu-id="7a1b7-289">Note that to access the `IntAsString` function you will have to add</span></span> 
```qsharp
    open Microsoft.Quantum.Convert;
```
<span data-ttu-id="7a1b7-290">나머지 네임 스페이스 `open` 문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-290">with the rest of the namespace `open` statements.</span></span>

<span data-ttu-id="7a1b7-291">결과 출력에서 각 고가 측정 될 때 하위 공간에 대 한 점진적 프로젝션을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-291">In the resulting output, you will see the gradual projection into subspaces as each qubit is measured.</span></span>


## <a name="use-the-q-libraries"></a><span data-ttu-id="7a1b7-292">Q # 라이브러리 사용</span><span class="sxs-lookup"><span data-stu-id="7a1b7-292">Use the Q# libraries</span></span>
<span data-ttu-id="7a1b7-293">소개 부분에서 언급 했 듯이, Q #의 많은 힘은 개별 신경 쓰지를 처리 하는 것이 가능 하다는 사실에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-293">As we mentioned in the introduction, much of Q#'s power rests in the fact that it allows you to abstract-away the worries of dealing with individual qubits.</span></span>
<span data-ttu-id="7a1b7-294">실제로, 적용 가능한 모든 퀀텀 프로그램을 개발 하려는 경우 특정 순환의 전후에 작업이 발생 하는지 걱정 해도 `H` 속도가 저하 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-294">Indeed, if you want to develop full-scale, applicable quantum programs, worrying about whether an `H` operation goes before or after a particular rotation would only slow you down.</span></span> 

<span data-ttu-id="7a1b7-295">Q # 라이브러리에는 [Qft](xref:microsoft.quantum.canon.qft) 연산이 포함 되어 있으며,이 작업은 원하는 수의 다양 한 비트에 대해 간단 하 게 적용 하 고 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-295">The Q# libraries contain the [QFT](xref:microsoft.quantum.canon.qft) operation, which you can simply take and apply for any number of qubits.</span></span>
<span data-ttu-id="7a1b7-296">이 작업을 수행 하려면의 내용이 동일한 Q # 파일에 새 작업을 정의 합니다 .이 작업은 `Perform3QubitQFT` 첫 번째에서로 대체 되는 모든 항목을 `H` `SWAP` 두 개의 간단한 줄로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-296">To give it a try, define a new operation in your Q# file which has the same contents of `Perform3QubitQFT`, but with everything from the first `H` to the `SWAP` replaced by two easy lines:</span></span>
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
<span data-ttu-id="7a1b7-297">첫 번째 줄에서는 [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) `qs` [qft](xref:microsoft.quantum.canon.qft) 작업에서 인수로 사용 되는,의 할당 된 배열의 식을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-297">The first line simply creates a [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expression of the allocated array of qubits, `qs`, which is what the [QFT](xref:microsoft.quantum.canon.qft) operation takes as an argument.</span></span>
<span data-ttu-id="7a1b7-298">이는 레지스터의 고 비트의 인덱스 순서에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-298">This corresponds to index ordering of the qubits in the register.</span></span>

<span data-ttu-id="7a1b7-299">이러한 작업에 액세스 하려면 `open` Q # 파일의 시작 부분에 해당 네임 스페이스에 대 한 문을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-299">To have access to these operations, add `open` statements for their respective namespaces at the beginning of the Q# file:</span></span>
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

<span data-ttu-id="7a1b7-300">이제 호스트 프로그램을 조정 하 여 새 작업의 이름 (예:)을 호출 하 `PerformIntrinsicQFT` 고 그럼를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-300">Now, adjust your host program to call the name of your new operation (e.g. `PerformIntrinsicQFT`), and give it a whirl.</span></span>

<span data-ttu-id="7a1b7-301">Q # 라이브러리 작업을 사용 하는 실제 혜택을 확인 하려면 다음과 같은 방법으로 값을 변경 합니다 `3` .</span><span class="sxs-lookup"><span data-stu-id="7a1b7-301">To see the real benefit of using the Q# library operations, change the number of qubits to something other than `3`:</span></span>
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
<span data-ttu-id="7a1b7-302">따라서 `H` 각 이상에서 새로운 작업 및 회전에 대해 걱정할 필요 없이 지정 된 수의 수 만큼 적절 한 QFT를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-302">You can thus apply the proper QFT for any given number of qubits, without having to worry about the mess of new `H` operations and rotations on each qubit.</span></span>

<span data-ttu-id="7a1b7-303">실제 퀀텀 하드웨어로 전환 하는 이유를 정확 하 게---하는 것 처럼, 퀀텀 시뮬레이터를 실행 하는 데 많은 시간이 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1b7-303">Note that the quantum simulator takes exponentially more time to run as you increase the number of qubits---precisely why we look forward to real quantum hardware!</span></span>













