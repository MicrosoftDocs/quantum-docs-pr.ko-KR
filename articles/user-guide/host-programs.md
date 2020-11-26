---
title: 프로그램을 실행 하는 방법 Q#
description: 프로그램을 실행 하는 다양 한 방법에 대 한 개요입니다 Q# . 명령 프롬프트에서 Q# jupyter 노트북 및 Python 또는 .net 언어의 클래식 호스트 프로그램에서.
author: gillenhaalb
ms.author: a-gibec
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2c5bdebc826bb85f6d7e0ade6232e15e29e8fb19
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231692"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="90560-104">프로그램을 실행 하는 방법 Q#</span><span class="sxs-lookup"><span data-stu-id="90560-104">Ways to run a Q# program</span></span>

<span data-ttu-id="90560-105">퀀텀 개발 키트의 가장 큰 장점 중 하나는 플랫폼 및 개발 환경에서의 유연성입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="90560-106">그러나이는 새로운 Q# 사용자가 [설치 가이드](xref:microsoft.quantum.install)에 있는 다양 한 옵션을 사용 하 여 혼동 하거나 부담 하지 않을 수도 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="90560-107">이 페이지에서는 프로그램이 실행 될 때 발생 하는 상황을 설명 Q# 하 고 사용자가 수행할 수 있는 여러 가지 방법을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="90560-108">주요 차이점은 다음을 Q# 실행할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="90560-109">독립 실행형 응용 프로그램으로 서, Q# 가 관련 된 유일한 언어 이며 프로그램이 직접 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="90560-110">두 메서드는 실제로이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="90560-111">명령줄 인터페이스</span><span class="sxs-lookup"><span data-stu-id="90560-111">the command-line interface</span></span>
  - <span data-ttu-id="90560-112">Q# Jupyter 노트북</span><span class="sxs-lookup"><span data-stu-id="90560-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="90560-113">Python 또는 .NET 언어 (예: c # 또는 F #)로 작성 된 추가 *호스트 프로그램* 을 사용 하 여 프로그램을 호출 하 고 반환 된 결과를 추가로 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-113">with an additional *host program*, written in Python or a .NET language (for example, C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="90560-114">이러한 프로세스와 해당 차이점을 가장 잘 이해 하려면 간단한 프로그램을 고려 하 여 Q# 실행 하는 방법을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be run.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="90560-115">기본 Q# 프로그램</span><span class="sxs-lookup"><span data-stu-id="90560-115">Basic Q# program</span></span>

<span data-ttu-id="90560-116">기본 퀀텀 프로그램은 $ \ket {0} $ 및 $ \ket $ 상태를 측정 하 고이를 측정 하 고 결과를 반환 하는 것으로 구성 되어 있을 수 있습니다 {1} .이는 확률이 동일한 두 상태 중 하나에 임의로 superposition.</span><span class="sxs-lookup"><span data-stu-id="90560-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="90560-117">실제로이 프로세스는 [퀀텀 난수 생성기](xref:microsoft.quantum.quickstarts.qrng) 빠른 시작의 핵심에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="90560-118">에서 Q# 이 작업은 다음 코드에 의해 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="90560-119">그러나이 코드는에서 실행할 수 없습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-119">However, this code alone can't be run by Q#.</span></span>
<span data-ttu-id="90560-120">이렇게 하려면 작업 본문을 구성 해야 합니다 .이 [작업](xref:microsoft.quantum.qsharp.operationsandfunctions)은 직접 또는 다른 작업을 통해---호출 될 때 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.qsharp.operationsandfunctions), which is then run when called---either directly or by another operation.</span></span> <span data-ttu-id="90560-121">따라서 다음 형식의 작업을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="90560-122">입력을 `MeasureSuperposition` 사용 하지 않고 [Result](xref:microsoft.quantum.qsharp.typesystem-index#available-types)형식의 값을 반환 하는 작업을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.qsharp.typesystem-index#available-types).</span></span>

<span data-ttu-id="90560-123">는 작업 외에 Q# 도 결정적 계산을 함수로 캡슐화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-123">In addition to operations, Q# also allows to encapsulate deterministic computations into functions.</span></span> <span data-ttu-id="90560-124">이를 의미 하는 것 외에,이는 중간 비트에 대해 수행 되는 계산을 함수 대신 작업으로 캡슐화 해야 한다는 의미입니다. 작업 및 함수 사이에는 약간의 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-124">Aside from the determinism guarantee that implies that computations that act on qubits need to be encapsulated into operations rather than functions, there is little difference between operations and function.</span></span> <span data-ttu-id="90560-125">이를 *callables* 이라고 통칭 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-125">We refer to them collectively as *callables*.</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="90560-126">파일에 정의 된 호출 가능 Q#</span><span class="sxs-lookup"><span data-stu-id="90560-126">Callable defined in a Q# file</span></span>

<span data-ttu-id="90560-127">호출 가능 하 고에서 실행 되는 것은 정확 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-127">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="90560-128">그러나 전체 파일을 구성 하기 위해 몇 가지 추가 항목이 필요 `*.qs` Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-128">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="90560-129">모든 Q# 형식 및 callables (정의 하는 모든 형식 및 해당 언어의 내장 함수)은 네임 스페이스 내에서 정의 됩니다 .이 *네임 스페이스* 는 각 이름에 대해 참조할 수 있는 전체 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-129">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="90560-130">예를 들어 [`H`](xref:Microsoft.Quantum.Intrinsic.H) 및 [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) 작업은 [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) 및 [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) 네임 스페이스 ( [ Q# 표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro)의 일부)에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-130">For example, the [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) and [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.libraries.standard.intro)).</span></span>
<span data-ttu-id="90560-131">따라서 항상 *전체* 이름 및를 통해 호출할 수 `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` 있지만 항상이 작업을 수행 하면 매우 복잡 한 코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-131">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="90560-132">대신 `open` 위의 작업 본문에서 수행한 것 처럼 문이 보다 간결한 줄임으로 참조 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-132">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="90560-133">Q#따라서 작업을 포함 하는 전체 파일은 고유한 네임 스페이스를 정의 하 고 작업에서 사용 하는 callables에 대 한 네임 스페이스를 연 다음 작업을 수행 하는 것으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-133">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="90560-134">열린 경우에도 네임 스페이스를 *별칭* 으로 지정할 수 있으며,이는 두 네임 스페이스의 호출 가능/형식 이름이 충돌할 경우 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-134">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="90560-135">예를 들어, 위의을 대신 사용 하 고를 통해를 호출할 수 있습니다 `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` `H` `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="90560-135">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="90560-136">이에 대 한 한 가지 예외는 [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) 항상 자동으로 열리는 네임 스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-136">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="90560-137">따라서와 같은 callables은 [`Length`](xref:Microsoft.Quantum.Core.Length) 항상 직접 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-137">Therefore, callables like [`Length`](xref:Microsoft.Quantum.Core.Length) can always be used directly.</span></span>

### <a name="running-on-target-machines"></a><span data-ttu-id="90560-138">대상 컴퓨터에서 실행</span><span class="sxs-lookup"><span data-stu-id="90560-138">Running on target machines</span></span>

<span data-ttu-id="90560-139">이제 프로그램의 일반 실행 모델이 명확 하 게 됩니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-139">Now the general run model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="90560-140">먼저 실행할 수 있는 특정 호출에는 동일한 네임 스페이스에 정의 된 다른 callables 및 형식에 대 한 액세스 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-140">Firstly, the specific callable to be run has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="90560-141">또한 [ Q# 라이브러리](xref:microsoft.quantum.libraries)에서 액세스 하는 것은 물론, 전체 이름을 통하거나 위에 설명 된 문을 사용 하 여 참조 해야 합니다 `open` .</span><span class="sxs-lookup"><span data-stu-id="90560-141">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="90560-142">그런 다음 호출 가능 자체는 *[대상 컴퓨터](xref:microsoft.quantum.machines)* 에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-142">The callable itself is then run on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="90560-143">이러한 대상 컴퓨터는 실제 퀀텀 하드웨어 이거나 QDK의 일부로 사용할 수 있는 여러 시뮬레이터 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-143">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="90560-144">여기에서 가장 유용 하 게 사용할 수 있는 대상 컴퓨터는 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)의 인스턴스이고,이는 `QuantumSimulator` 프로그램의 동작을 의미 없는 퀀텀 컴퓨터에서 실행 되는 것 처럼 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-144">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being run on a noise-free quantum computer.</span></span>

<span data-ttu-id="90560-145">지금까지 특정 Q# 호출 가능이 실행 중일 때 발생 하는 상황을 설명 했습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-145">So far, we've described what happens when a specific Q# callable is being run.</span></span>
<span data-ttu-id="90560-146">Q#는 독립 실행형 응용 프로그램에서 사용 되는지에 관계 없이 호스트 프로그램에서 사용 되는지에 관계 없이이 일반적인 프로세스는---하 여 QDK 유연성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-146">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="90560-147">따라서 퀀텀 개발 키트를 호출 하는 방법 간의 차이점으로 인해 해당 호출을 *how* Q# 실행 하기 위해 호출 하는 방법 및 결과가 반환 되는 방식에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-147">The differences between the ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be run, and in what manner any results are returned.</span></span>
<span data-ttu-id="90560-148">좀 더 구체적으로 말하자면 다음과 같이 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-148">More specifically, the differences revolve around:</span></span>

- <span data-ttu-id="90560-149">Q#실행할 호출 가능 여부 표시</span><span class="sxs-lookup"><span data-stu-id="90560-149">Indicating which Q# callable is to be run</span></span>
- <span data-ttu-id="90560-150">잠재적 호출 가능 인수가 제공 되는 방법</span><span class="sxs-lookup"><span data-stu-id="90560-150">How potential callable arguments are provided</span></span>
- <span data-ttu-id="90560-151">실행할 대상 컴퓨터 지정</span><span class="sxs-lookup"><span data-stu-id="90560-151">Specifying the target machine on which to run it</span></span>
- <span data-ttu-id="90560-152">결과가 반환 되는 방법</span><span class="sxs-lookup"><span data-stu-id="90560-152">How any results are returned</span></span>

<span data-ttu-id="90560-153">먼저 명령 프롬프트에서 독립 실행형 응용 프로그램을 사용 하 여이 작업을 수행한 Q# 다음 Python 및 c # 호스트 프로그램을 사용 하 여이 작업을 진행 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-153">First, we discuss how this is done with the Q# standalone application from the command prompt, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="90560-154">Q#처음 세 가지가 아닌 주 기능이 로컬 파일을 중심으로 하지 않기 때문에 처음에는 jupyter 노트북의 독립 실행형 응용 프로그램을 예약 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-154">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="90560-155">이러한 예에서 설명 하지는 않지만, 실행 메서드 간에는 프로그램 내에서 인쇄 되는 모든 메시지 Q# ( [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine) 예: 또는)가 항상 해당 콘솔에 인쇄 되는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-155">Although we don't illustrate it in these examples, one commonality between the run methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) or [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-prompt"></a><span data-ttu-id="90560-156">Q# 명령 프롬프트에서</span><span class="sxs-lookup"><span data-stu-id="90560-156">Q# from the command prompt</span></span>
<span data-ttu-id="90560-157">프로그램 작성을 시작 하는 가장 쉬운 방법 중 하나는 Q# 별도의 파일과 두 번째 언어를 함께 사용 하는 것을 걱정 하지 않는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-157">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="90560-158">QDK 확장과 함께 Visual Studio Code 또는 Visual Studio를 사용 하면 Q# 단일 파일 에서만 callables을 실행 하는 원활한 워크플로를 사용할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-158">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="90560-159">이를 위해 궁극적으로 다음을 입력 하 여 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-159">For this, we will ultimately run the program by entering</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="90560-160">명령 프롬프트에서</span><span class="sxs-lookup"><span data-stu-id="90560-160">at the command prompt.</span></span>
<span data-ttu-id="90560-161">가장 간단한 워크플로는 터미널의 디렉터리 위치가 파일과 동일 하 여 Q# Q# VS Code에서 통합 터미널을 사용 하 여 파일 편집과 함께 쉽게 처리할 수 있는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-161">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="90560-162">그러나이 [ `dotnet run` 명령은](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) 다양 한 옵션을 허용 하며, `--project <PATH>` 파일의 위치를 단순히 제공 하 여 다른 위치에서 프로그램을 실행할 수도 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-162">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="90560-163">파일에 진입점 추가 Q#</span><span class="sxs-lookup"><span data-stu-id="90560-163">Add entry point to Q# file</span></span>

<span data-ttu-id="90560-164">대부분의 Q# 파일에는 두 개 이상의 호출 가능이 포함 되므로, 기본적으로 컴파일러에서 *which* 명령을 제공할 때 실행할 호출 가능 항목을 알 수 있도록 해야 합니다 `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="90560-164">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to run when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="90560-165">이렇게 하려면 파일 자체에 대 한 간단한 변경 작업을 수행 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-165">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="90560-166">호출 가능 바로 앞에를 사용 하 여 줄을 추가 `@EntryPoint()` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-166">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="90560-167">따라서 위의 파일이 다음과 같은 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-167">Our file from above would therefore become</span></span>
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

<span data-ttu-id="90560-168">이제 `dotnet run` 명령 프롬프트에서를 호출 하면 `MeasureSuperposition` 실행 되 고 반환 된 값이 터미널에 직접 인쇄 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-168">Now, a call of `dotnet run` from the command prompt leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="90560-169">따라서 또는이 인쇄 된 것을 볼 수 있습니다 `One` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="90560-169">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="90560-170">아래에 더 많은 callables을 정의 하는 경우에는 문제가 되지 않습니다 `MeasureSuperposition` .</span><span class="sxs-lookup"><span data-stu-id="90560-170">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="90560-171">또한 선언 전에 호출 가능한 [문서 주석을](xref:microsoft.quantum.qsharp.comments#documentation-comments) 포함 하는 경우에는이 `@EntryPoint()` 특성을 위에 배치 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-171">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.qsharp.comments#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="90560-172">호출 가능 인수</span><span class="sxs-lookup"><span data-stu-id="90560-172">Callable arguments</span></span>

<span data-ttu-id="90560-173">지금까지 입력을 받지 않는 작업만 고려 했습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-173">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="90560-174">비슷한 작업을 수행 하려고 하지만 여러 가지 작업에서 인수로 제공 되는 수를---한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-174">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="90560-175">이러한 작업은 다음으로 작성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-175">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="90560-176">여기서 반환 된 값은 측정 결과의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-176">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="90560-177">및는 [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) 및 네임 스페이스에 있으므로 [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) `open` 각에 대 한 추가 문이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-177">Note that [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) and [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) are in the [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) and [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="90560-178">`@EntryPoint()`이 새 작업 앞에 특성을 이동 하는 경우 (참고: 파일에는 해당 줄이 하나만 있을 수 있음),이 작업을 실행 하려고 하면 `dotnet run` 추가 명령줄 옵션이 필요한 것을 나타내는 오류 메시지와이를 표현 하는 방법이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-178">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command-line options are required, and how to express them.</span></span>

<span data-ttu-id="90560-179">명령줄에 대 한 일반 형식은 실제로 이며 `dotnet run [options]` 호출 가능 인수가 여기에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-179">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="90560-180">이 경우 인수가 `n` 누락 되 고 옵션을 제공 해야 함을 보여 줍니다 `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="90560-180">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="90560-181">`MeasureSuperpositionArray`이제는를 사용 하 여를 실행 합니다. `n=4`</span><span class="sxs-lookup"><span data-stu-id="90560-181">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="90560-182">다음과 유사한 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-182">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="90560-183">이 과정에서 여러 인수를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-183">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="90560-184">에 정의 된 인수 이름은 `camelCase` 컴파일러에 의해 입력으로 허용 되도록 약간 변경 됩니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-184">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="90560-185">예를 들어, 대신 `n` 위의 이름을 사용한 경우 `numQubits` 이 입력은 대신를 통해 명령줄에서 제공 됩니다 `--num-qubits 4` `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="90560-185">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="90560-186">또한이 오류 메시지는 대상 컴퓨터를 변경 하는 방법을 포함 하 여 사용할 수 있는 다른 옵션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-186">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="90560-187">다른 대상 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="90560-187">Different target machines</span></span>

<span data-ttu-id="90560-188">지금까지 작업의 출력은 실제 환경에서 작업의 예상 결과를 가지 며, 명령줄의 기본 대상 컴퓨터가 전체 상태 퀀텀 시뮬레이터 인 것을 알 수 `QuantumSimulator` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-188">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quantum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="90560-189">그러나 옵션 `--simulator` (또는 약식)을 사용 하 여 특정 대상 컴퓨터에서 실행 되도록 callables에 지시할 수 있습니다 `-s` .</span><span class="sxs-lookup"><span data-stu-id="90560-189">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="90560-190">예를 들어, 다음에서 실행할 수 있습니다 [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) .</span><span class="sxs-lookup"><span data-stu-id="90560-190">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="90560-191">인쇄 된 출력은</span><span class="sxs-lookup"><span data-stu-id="90560-191">The printed output is then</span></span>

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

<span data-ttu-id="90560-192">이러한 메트릭에 표시 되는 내용에 대 한 자세한 내용은 [Resource 평가기: 보고 된 메트릭](xref:microsoft.quantum.machines.resources-estimator#metrics-reported)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90560-192">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-run-summary"></a><span data-ttu-id="90560-193">명령줄 실행 요약</span><span class="sxs-lookup"><span data-stu-id="90560-193">Command line run summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="90560-194">옵션이 아닌 Q# `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="90560-194">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="90560-195">위에서 언급 한 옵션을 사용 하 여 위에서 언급 한 것 처럼 `--project` 이 [ `dotnet run` 명령은](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) 호출 가능 인수와 관련이 없는 옵션도 허용 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-195">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="90560-196">두 종류의 옵션을 모두 제공 하는 경우 `dotnet` 관련 옵션을 먼저 제공 하 고 그 다음에 구분 기호가를 입력 한 다음 관련 옵션을 제공 해야 합니다 `--` Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-196">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="90560-197">예를 들어 위의 작업에 대해 숫자 값과 함께 경로를 지정 하는 것은를 통해 실행 됩니다 `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="90560-197">For example, specifying a path along with a number qubits for the operation above would be run via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="90560-198">Q# 호스트 프로그램 사용</span><span class="sxs-lookup"><span data-stu-id="90560-198">Q# with host programs</span></span>

<span data-ttu-id="90560-199">직접 파일을 사용 하는 경우 Q# 명령 프롬프트에서 직접 작업 또는 함수를 호출 하는 대신 다른 기존 언어로 *호스트 프로그램* 을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-199">With our Q# file in hand, an alternative to calling an operation or function directly from the command prompt is to use a *host program* in another classical language.</span></span> <span data-ttu-id="90560-200">특히 c # 또는 F # 등의 .NET 언어를 사용 하 여이 작업을 수행할 수 있습니다 .이를 위해 c # 또는 F #과 같은 .NET 언어를 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-200">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="90560-201">상호 운용성을 사용 하려면 약간의 설정이 필요 하지만 이러한 세부 정보는 [설치 가이드](xref:microsoft.quantum.install)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-201">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="90560-202">간단히 말해서, 이러한 상황에는 `*.py` `*.cs` 파일의 동일한 위치에 호스트 프로그램 파일 (예: 또는)이 포함 됩니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-202">In a nutshell, the situation now includes a host program file (for example, `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="90560-203">이제 실행 되는 *호스트* 프로그램이 실행 되는 동안 Q# 파일에서 특정 작업 및 함수를 호출할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-203">It's now the *host* program that gets run, and while it is running, it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="90560-204">상호 운용성의 핵심은 Q# Q# 호출 될 수 있도록 호스트 프로그램에서 파일의 콘텐츠를 액세스할 수 있도록 하는 컴파일러를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-204">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="90560-205">호스트 프로그램을 사용할 때의 주요 이점 중 하나는 프로그램에서 반환 된 기존 데이터가 Q# 호스트 언어로 추가로 처리 될 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="90560-205">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="90560-206">이는 일부 고급 데이터 처리 (예:에서 내부적으로 수행 될 수 없는 항목)로 구성 된 Q# 다음 Q# 해당 결과에 따라 추가 작업을 호출 하거나 결과를 그리는 것 처럼 간단 하 게 처리할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-206">This could consist of some advanced data processing (for example, something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="90560-207">일반적인 체계는 다음과 같습니다. 여기에서는 Python 및 c #에 대 한 특정 구현을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-207">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="90560-208">F # 호스트 프로그램을 사용 하는 샘플은 [.net 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-208">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="90560-209">`@EntryPoint()`응용 프로그램에 사용 되는 특성은 Q# 호스트 프로그램과 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-209">The `@EntryPoint()` attribute used for Q# applications cannot be used with host programs.</span></span>
> <span data-ttu-id="90560-210">호스트에서 호출 하는 파일에 있는 경우 오류가 발생 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-210">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="90560-211">다른 호스트 프로그램을 사용 하려면 파일에 필요한 변경 내용이 없습니다 `*.qs` Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-211">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="90560-212">다음 호스트 프로그램 구현은 모두 동일한 파일을 사용 하 여 작업 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-212">The following host program implementations all work with the same Q# file:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

<span data-ttu-id="90560-213">원하는 호스트 언어에 해당 하는 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-213">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="90560-214">Python</span><span class="sxs-lookup"><span data-stu-id="90560-214">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="90560-215">Python 호스트 프로그램은 다음과 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-215">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="90560-216">모듈 `qsharp` 을 가져옵니다 .이 모듈은 상호 운용성을 위해 모듈 로더를 등록 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-216">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="90560-217">이렇게 하면 Q# 네임 스페이스를 Python 모듈로 표시 하 여 "가져오기" 호출을 수행할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-217">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="90560-218">기술적으로는 가져올 수 있는 것이 아니라이를 Q# 호출할 수 있는 Python 스텁을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-218">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="90560-219">이러한 동작은 Python 클래스의 개체로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-219">These behave as objects of Python classes.</span></span> <span data-ttu-id="90560-220">이러한 개체의 메서드를 사용 하 여 프로그램을 실행할 때 작업을 보낼 대상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-220">We use methods on these objects to specify the target machines that we send the operation to when running the program.</span></span>

2. <span data-ttu-id="90560-221">Q#이 경우---를 직접 호출 하는 callables을 가져옵니다 `MeasureSuperposition` `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="90560-221">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="90560-222">모듈을 가져온 후에는 `qsharp` 라이브러리 네임 스페이스에서 직접 callables을 가져올 수도 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-222">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="90560-223">다른 Python 코드 중에서 이제 특정 대상 컴퓨터에서이 호출을 호출 하 고, 나중에 사용할 수 있도록 해당 반환을 변수에 할당 (값을 반환 하는 경우) 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-223">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="90560-224">대상 컴퓨터 지정</span><span class="sxs-lookup"><span data-stu-id="90560-224">Specifying target machines</span></span>
<span data-ttu-id="90560-225">특정 대상 컴퓨터에서 실행 되도록 작업을 호출 하는 것은 가져온 개체에 대 한 다른 Python 메서드를 통해 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-225">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="90560-226">예를 들어,는를 사용 하 여 작업을 실행 하는 반면,는를 사용 하 여 `.simulate(<args>)` 작업을 실행 합니다 `QuantumSimulator` `.estimate_resources(<args>)` `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="90560-226">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="90560-227">Q에 입력 전달\#</span><span class="sxs-lookup"><span data-stu-id="90560-227">Passing inputs to Q\#</span></span>
<span data-ttu-id="90560-228">호출 가능의 인수는 Q# 키워드 인수 형식으로 제공 해야 합니다. 여기서 키워드는 호출 가능 정의의 인수 이름입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-228">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="90560-229">즉,는 `MeasureSuperpositionArray.simulate(n=4)` 유효 하지만는 `MeasureSuperpositionArray.simulate(4)` 오류를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-229">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="90560-230">따라서 Python 호스트 프로그램</span><span class="sxs-lookup"><span data-stu-id="90560-230">Therefore, the Python host program</span></span> 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

<span data-ttu-id="90560-231">결과는 다음과 유사 하 게 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-231">results in an output like the following:</span></span>

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="90560-232">Q#다른 프로젝트 또는 패키지의 코드 사용</span><span class="sxs-lookup"><span data-stu-id="90560-232">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="90560-233">기본적으로이 `import qsharp` 명령은 현재 폴더의 모든 파일을 로드 `.qs` 하 고 Q# Python 스크립트 내에서 해당 작업 및 기능을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-233">By default, the `import qsharp` command loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the Python script.</span></span>

<span data-ttu-id="90560-234">Q#다른 폴더에서 코드를 로드 하기 위해 [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) 를 사용 하 여 `.csproj` 프로젝트에 대 한 파일 Q# (즉,를 참조 하는 프로젝트)에 대 한 참조를 추가할 수 있습니다 `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="90560-234">To load Q# code from another folder, the [`qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span>
<span data-ttu-id="90560-235">이 명령은 `.qs` 및 하위 폴더가 들어 있는 폴더의 모든 파일을 컴파일합니다 `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="90560-235">This command will compile any `.qs` files in the folder containing the `.csproj` and its subfolders.</span></span> <span data-ttu-id="90560-236">또한를 통해 참조 되 `PackageReference` Q# 는 패키지나 해당 파일의를 통해 참조 되는 프로젝트를 재귀적으로 로드 `ProjectReference` `.csproj` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-236">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span>

<span data-ttu-id="90560-237">예를 들어, 다음 Python 코드는 현재 폴더에 상대적인 경로를 참조 하 고 해당 작업 중 하나를 호출 하는 외부 프로젝트를 가져옵니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-237">As an example, the following Python code imports an external project, referencing its path relative to the current folder, and invokes one of its Q# operations:</span></span>

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

<span data-ttu-id="90560-238">그러면 다음과 같이 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-238">This results in output like the following:</span></span>

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

<span data-ttu-id="90560-239">코드를 포함 하는 외부 패키지를 로드 하려면 Q# [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-239">To load external packages containing Q# code, use the [`qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span></span>

<span data-ttu-id="90560-240">Q#현재 폴더의 코드가 외부 프로젝트 또는 패키지에 종속 `import qsharp` 된 경우 종속성이 아직 로드 되지 않았기 때문에 실행 시 오류가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-240">If the Q# code in the current folder depends on external projects or packages, you may see errors when running `import qsharp`, since the dependencies have not yet been loaded.</span></span>
<span data-ttu-id="90560-241">명령 중에 필요한 외부 패키지 또는 프로젝트를 로드 하려면 Python 스크립트를 포함 하는 Q# `import qsharp` 폴더에를 참조 하는 파일이 포함 되어 있는지 확인 `.csproj` `Microsoft.Quantum.Sdk` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-241">To load required external packages or Q# projects during the `import qsharp` command, ensure that the folder with the Python script contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="90560-242">그런 다음 `.csproj` 속성을에 추가 `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-242">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="90560-243">그러면 Q# `ProjectReference` `PackageReference` 명령 중에 찾은 항목이 나 항목을 재귀적으로 로드 `.csproj` `import qsharp` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-243">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` during the `import qsharp` command.</span></span>

<span data-ttu-id="90560-244">예를 들어 다음은 패키지를 `.csproj` Q# 자동으로 로드 하는 간단한 파일입니다 `Microsoft.Quantum.Chemistry` .</span><span class="sxs-lookup"><span data-stu-id="90560-244">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="90560-245">현재이 사용자 지정 `<IQSharpLoadAutomatically>` 속성은 python 호스트에 필요 하지만 나중에 `.csproj` python 스크립트와 동일한 폴더에 있는 파일에 대 한 기본 동작이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-245">Currently this custom `<IQSharpLoadAutomatically>` property is required by Python hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the Python script.</span></span>

> [!NOTE]
> <span data-ttu-id="90560-246">현재의 `<QsharpCompile>` 설정은 `.csproj` Python 호스트에서 무시 되 고 하위 폴더를 `.qs` 포함 하 여의 폴더에 있는 모든 파일이 `.csproj` 로드 되 고 컴파일됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-246">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Python hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="90560-247">나중에 설정에 대 한 지원이 `.csproj` 향상 됩니다 (자세한 내용은 [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) 참조).</span><span class="sxs-lookup"><span data-stu-id="90560-247">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>


### <a name="c"></a>[<span data-ttu-id="90560-248">C#</span><span class="sxs-lookup"><span data-stu-id="90560-248">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="90560-249">C # 호스트 프로그램에는 여러 구성 요소가 있으며, c #을 기반으로 하는 시뮬레이터와 같이 QDK 일부 구성 요소와 매우 긴밀 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-249">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="90560-250">Q#컴파일러는 Q# 파일의 네임 스페이스에서 동등 하 게 명명 된 c # 네임 스페이스를 생성 하 여 여기에서 작업 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-250">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="90560-251">여기에 정의 된 각 callables 또는 형식에 대해 동등 하 게 명명 된 c # 클래스를 생성 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-251">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="90560-252">먼저 `using` 파일의 문과 거의 analagous 하는 문을 사용 하 여 호스트 프로그램에서 사용 되는 모든 클래스를 사용 하도록 설정 합니다 `open` Q# .</span><span class="sxs-lookup"><span data-stu-id="90560-252">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (for example, QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="90560-253">다음으로 c # 네임 스페이스, 몇 가지 다른 비트 및 부분 (아래의 전체 코드 블록 참조)을 선언 하 고 원하는 모든 기존 프로그래밍 (예: callables의 인수 계산)을 선언 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-253">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (for example, computing arguments for the Q# callables).</span></span>
<span data-ttu-id="90560-254">후자의 경우에는 후자를 사용할 필요가 없지만 이러한 사용의 예는  [.net 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-254">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="90560-255">대상 머신</span><span class="sxs-lookup"><span data-stu-id="90560-255">Target machines</span></span>

<span data-ttu-id="90560-256">로 돌아가서 Q# 작업을 실행할 대상 컴퓨터의 인스턴스를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-256">Getting back to Q#, we must create an instance of whatever target machine we will run our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="90560-257">다른 대상 컴퓨터를 사용 하는 것은 다른 대상 컴퓨터를 인스턴스화하는 것 만큼 간단 합니다. 즉,이를 수행 하 고 반환을 처리 하는 방법은 약간 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-257">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="90560-258">간단 하 게 하기 위해 이제에는 [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [다음](#including-the-resources-estimator)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-258">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="90560-259">작업에서 생성 된 각 c # 클래스에는 Q# `Run` 메서드가 있습니다. 첫 번째 인수는 대상 컴퓨터 인스턴스여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-259">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="90560-260">따라서에서을 실행 하려면 `MeasureSuperposition` `QuantumSimulator` 를 사용 `MeasureSuperposition.Run(sim)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-260">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="90560-261">그러면 c #에서 반환 된 결과를 변수에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-261">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="90560-262">`Run`메서드는 실제 퀀텀 하드웨어의 경우에는 비동기적으로 실행 되므로 `await` 작업이 완료 될 때까지 키워드가 추가 처리를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-262">The `Run` method is run asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further processing until the task completes.</span></span>

<span data-ttu-id="90560-263">호출에 반환 형식이 있는 경우와 같이 반환 형식이 없는 경우에는 Q# `Unit` 변수에 할당 하지 않고 동일한 방법으로 실행을 계속 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-263">If the Q# callable does not have any returns (for example, it has return type `Unit`), then the run can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="90560-264">이 경우 전체 줄은 다음과 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-264">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="90560-265">인수</span><span class="sxs-lookup"><span data-stu-id="90560-265">Arguments</span></span>

<span data-ttu-id="90560-266">호출 가능한에 대 한 모든 인수 Q# 는 대상 컴퓨터 뒤에 추가 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-266">Any arguments to the Q# callable are simply passed as additional arguments after the target machine.</span></span>
<span data-ttu-id="90560-267">따라서에 대 한 결과는 다음을 `MeasureSuperpositionArray` `n=4` 통해 인출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-267">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="90560-268">따라서 전체 c # 호스트 프로그램은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-268">A full C# host program could thus look like</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

<span data-ttu-id="90560-269">C # 파일의 위치에서 다음을 입력 하 여 명령 프롬프트에서 호스트 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-269">At the location of the C# file, the host program can be run from the command prompt by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="90560-270">이 경우 콘솔에 기록 된 출력이 다음과 유사 하 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-270">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="90560-271">컴파일러는 네임 스페이스와의 상호 운용성 때문에 Q# 문 없이 callables을 사용할 수 있도록 설정 하 `using NamespaceName;` 고 c # 네임 스페이스 제목만 일치 시킬 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-271">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="90560-272">즉,를로 바꿉니다 `namespace host` `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="90560-272">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="90560-273">평가기 리소스 포함</span><span class="sxs-lookup"><span data-stu-id="90560-273">Including the resources estimator</span></span>

<span data-ttu-id="90560-274">에서 [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) 출력을 검색 하려면 약간 다른 구현이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-274">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="90560-275">첫째, 문을 사용 하 여 변수로 인스턴스화하는 대신 `using` (에서와 같이 `QuantumSimulator` ) 클래스의 개체를 직접 인스턴스화 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-275">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="90560-276">여러 작업에서 단일 대상 시뮬레이터를 사용 하는 대신 Q# 각각에 대해 하나씩 인스턴스화합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-276">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="90560-277">이는 대상 컴퓨터로 사용 되는 경우 개체 자체가 수정 되 고 그 결과를 나중에 클래스 메서드를 사용 하 여 검색할 수 있기 때문입니다 `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="90560-277">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="90560-278">리소스 추정에 대 한 작업을 실행 하려면 다음을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-278">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="90560-279">그런 다음 및를 사용 하 여 TSV (탭으로 구분 된 값)로 결과를 인출 합니다 `estimatorSingleQ.ToTSV()` `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="90560-279">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="90560-280">따라서 및를 모두 사용 하는 전체 c # 호스트 프로그램 `QuantumSimulator` 은 `ResourcesEstimator` 다음 형식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-280">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


<span data-ttu-id="90560-281">그러면 다음과 유사한 출력이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-281">which would yield output similar to</span></span>

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="90560-282">Q# Jupyter 노트북</span><span class="sxs-lookup"><span data-stu-id="90560-282">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="90560-283">Q# Jupyter 노트북은 Q# Q# 모든 지침, 메모 및 기타 콘텐츠와 함께---단일 노트북에서 callables을 정의, 컴파일 및 실행할 수 있는 I 커널을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-283">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="90560-284">즉, 파일의 내용을 가져오고 사용할 수는 있지만 `*.qs` Q# 실행 모델에는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-284">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the run model.</span></span>

<span data-ttu-id="90560-285">여기서는 위에 정의 된 작업을 실행 하는 방법에 대해 자세히 설명 Q# 하지만, jupyter 노트북을 사용 하는 방법에 대 한 더 광범위 한 소개는 Q# [ Q# 및 jupyter 노트북](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-285">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="90560-286">작업 정의</span><span class="sxs-lookup"><span data-stu-id="90560-286">Defining operations</span></span>

<span data-ttu-id="90560-287">Jupyter Notebook에서 Q# Q# 파일의 네임 스페이스 내에서와 같은 방식으로 코드를 입력 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-287">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="90560-288">따라서 해당 네임 스페이스에 대 한 문을 사용 하 여 [ Q# 표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro) 에서 callables에 액세스 하도록 설정할 수 있습니다 `open` .</span><span class="sxs-lookup"><span data-stu-id="90560-288">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.libraries.standard.intro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="90560-289">이러한 문을 사용 하 여 셀을 실행할 때 해당 네임 스페이스의 정의는 작업 영역 전체에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-289">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="90560-290">[Microsoft.](xref:Microsoft.Quantum.Intrinsic) m a s. a s. a s. a s. a s. a s. i [s.](xref:Microsoft.Quantum.Canon) [`H`](xref:Microsoft.Quantum.Intrinsic.H) [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) Q#</span><span class="sxs-lookup"><span data-stu-id="90560-290">Callables from [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic) and [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon) (for example, [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="90560-291">그러나 외부 소스 파일에서 가져온 코드 Q# ( [ Q# 및 Jupyter 노트북](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)에 표시 되는 프로세스)에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-291">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="90560-292">마찬가지로 작업을 정의 하려면 코드를 작성 Q# 하 고 셀을 실행 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-292">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

<span data-ttu-id="90560-293">그런 다음 출력에는 이후 셀에서 호출할 수 있는 해당 작업이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-293">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="90560-294">대상 머신</span><span class="sxs-lookup"><span data-stu-id="90560-294">Target machines</span></span>

<span data-ttu-id="90560-295">특정 대상 컴퓨터에서 작업을 실행 하는 기능은 [ Q# 매직 명령을](xref:microsoft.quantum.guide.quickref.iqsharp)통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-295">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="90560-296">예를 들어,를 `%simulate` 사용 하 `QuantumSimulator` 고는를 사용 `%estimate` 합니다 `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="90560-296">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="90560-297">함수 및 작업에 입력 전달</span><span class="sxs-lookup"><span data-stu-id="90560-297">Passing inputs to functions and operations</span></span>

<span data-ttu-id="90560-298">작업에 입력을 전달 하기 위해 Q# 인수는 `key=value` magic run 명령에 쌍으로 전달 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-298">To pass inputs to the Q# operations, the arguments can be passed as `key=value` pairs to the run magic command.</span></span>
<span data-ttu-id="90560-299">따라서 `MeasureSuperpositionArray` 4 개의 비트를 사용 하 여를 실행 하려면 다음을 실행할 수 있습니다 `%simulate MeasureSuperpositionArray n=4` .</span><span class="sxs-lookup"><span data-stu-id="90560-299">So, to run `MeasureSuperpositionArray` with four qubits, we can run `%simulate MeasureSuperpositionArray n=4`:</span></span>

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

<span data-ttu-id="90560-300">이 패턴은 `%estimate` 및 기타 실행 명령과 유사 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-300">This pattern can be used similarly with `%estimate` and other run commands.</span></span>

### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="90560-301">Q#다른 프로젝트 또는 패키지의 코드 사용</span><span class="sxs-lookup"><span data-stu-id="90560-301">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="90560-302">기본적으로 Jupyter Notebook는 Q# `.qs` 현재 폴더에 있는 모든 파일을 로드 하 고 해당 Q# 작업 및 기능을 노트북 내부에서 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-302">By default, a Q# Jupyter Notebook loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the notebook.</span></span> <span data-ttu-id="90560-303">[ `%who` 매직 명령은](xref:microsoft.quantum.iqsharp.magic-ref.who) 현재 사용할 수 있는 모든 Q# 작업 및 함수를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-303">The [`%who` magic command](xref:microsoft.quantum.iqsharp.magic-ref.who) lists all currently-available Q# operations and functions.</span></span>

<span data-ttu-id="90560-304">Q#다른 폴더에서 코드를 로드 하기 위해 [ `%project` 매직 명령은](xref:microsoft.quantum.iqsharp.magic-ref.project) `.csproj` 프로젝트에 대 한 파일 Q# (즉,를 참조 하는 프로젝트)에 대 한 참조를 추가 하는 데 사용할 수 있습니다 `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="90560-304">To load Q# code from another folder, the [`%project` magic command](xref:microsoft.quantum.iqsharp.magic-ref.project) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span> <span data-ttu-id="90560-305">이 명령은 `.qs` 및 하위 폴더를 포함 하는 폴더의 모든 파일을 컴파일합니다 `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="90560-305">This command will compile any `.qs` files in the folder containing the `.csproj` (and subfolders).</span></span> <span data-ttu-id="90560-306">또한를 통해 참조 되 `PackageReference` Q# 는 패키지나 해당 파일의를 통해 참조 되는 프로젝트를 재귀적으로 로드 `ProjectReference` `.csproj` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-306">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span> 

<span data-ttu-id="90560-307">예를 들어 다음 셀은 Q# 외부 프로젝트에서 작업을 시뮬레이션 합니다. 여기서 프로젝트 경로는 현재 폴더를 기준으로 참조 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-307">As an example, the following cells simulate a Q# operation from an external project, where the project path is referenced relative to the current folder:</span></span>

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

<span data-ttu-id="90560-308">코드를 포함 하는 외부 패키지를 로드 하려면 Q# [ `%package` 매직 명령을](xref:microsoft.quantum.iqsharp.magic-ref.package)사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-308">To load external packages containing Q# code, use the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="90560-309">패키지를 로드 하면 사용자 지정 매직 명령이 나 패키지의 일부인 모든 어셈블리에 포함 된 인코더 표시도 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-309">Loading a package will also make available any custom magic commands or display encoders that are contained in any assemblies that are part of the package.</span></span>

<span data-ttu-id="90560-310">노트북 초기화 시간에 외부 패키지 또는 프로젝트를 로드 하려면 노트북 폴더에를 참조 하는 Q# 파일이 포함 되어 있는지 확인 `.csproj` `Microsoft.Quantum.Sdk` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-310">To load external packages or Q# projects at notebook intialization time, ensure that the notebook folder contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="90560-311">그런 다음 `.csproj` 속성을에 추가 `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` 합니다.</span><span class="sxs-lookup"><span data-stu-id="90560-311">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="90560-312">이렇게 하면 Q# `ProjectReference` `PackageReference` 노트북 로드 시에 발견 된 항목 또는 항목을 재귀적으로 로드 하는 것을 알려 `.csproj` 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90560-312">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` at notebook load time.</span></span>

<span data-ttu-id="90560-313">예를 들어 다음은 패키지를 `.csproj` Q# 자동으로 로드 하는 간단한 파일입니다 `Microsoft.Quantum.Chemistry` .</span><span class="sxs-lookup"><span data-stu-id="90560-313">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="90560-314">현재이 사용자 지정 `<IQSharpLoadAutomatically>` 속성은 Q# Jupyter Notebook 호스트에 필요 하지만 나중에 `.csproj` 전자 필기장 파일과 동일한 폴더에 있는 파일에 대 한 기본 동작이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90560-314">Currently this custom `<IQSharpLoadAutomatically>` property is required by Q# Jupyter Notebook hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the notebook file.</span></span>

> [!NOTE]
> <span data-ttu-id="90560-315">현재의 `<QsharpCompile>` 설정은 `.csproj` Jupyter Notebook 호스트에서 무시 되 Q# 고 하위 폴더를 `.qs` 포함 하 여의 폴더에 있는 모든 파일이 `.csproj` 로드 되 고 컴파일됩니다.</span><span class="sxs-lookup"><span data-stu-id="90560-315">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Q# Jupyter Notebook hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="90560-316">나중에 설정에 대 한 지원이 `.csproj` 향상 됩니다 (자세한 내용은 [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) 참조).</span><span class="sxs-lookup"><span data-stu-id="90560-316">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>
