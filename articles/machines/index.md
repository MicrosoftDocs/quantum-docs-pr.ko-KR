---
title: 양자 시뮬레이터 및 클래식 드라이버 | Microsoft Docs
description: 클래식 컴퓨팅 .NET 언어(일반적으로 C# 또는 Q#)를 사용하여 양자 시뮬레이터을 구동하는 방법을 설명합니다.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 5ac79280669ae0acfe993a1c2ae1c069b0c01848
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035112"
---
# <a name="classical-drivers-and-machines"></a><span data-ttu-id="f2d6a-103">클래식 드라이버 및 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="f2d6a-103">Classical Drivers and Machines</span></span>

## <a name="what-youll-learn"></a><span data-ttu-id="f2d6a-104">학습할 내용</span><span class="sxs-lookup"><span data-stu-id="f2d6a-104">What You'll Learn</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="f2d6a-105">양자 알고리즘을 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="f2d6a-105">How quantum algorithms are executed</span></span>
> * <span data-ttu-id="f2d6a-106">이 릴리스에 포함된 양자 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="f2d6a-106">What quantum simulators are included in this release</span></span>
> * <span data-ttu-id="f2d6a-107">양자 알고리즘용 C# 드라이버를 작성하는 방법</span><span class="sxs-lookup"><span data-stu-id="f2d6a-107">How to write a C# driver for your quantum algorithm</span></span>

## <a name="the-quantum-development-kit-execution-model"></a><span data-ttu-id="f2d6a-108">Quantum Development Kit 실행 모델</span><span class="sxs-lookup"><span data-stu-id="f2d6a-108">The Quantum Development Kit Execution Model</span></span>

<span data-ttu-id="f2d6a-109">[양자 프로그램을 작성](xref:microsoft.quantum.write-program)할 때 `QuantumSimulator` 개체를 알고리즘 클래스의 `Run` 메서드에 전달하여 양자 알고리즘을 실행했습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-109">In [Writing a quantum program](xref:microsoft.quantum.write-program), we executed our quantum algorithm by passing a `QuantumSimulator` object to the algorithm class's `Run` method.</span></span>
<span data-ttu-id="f2d6a-110">`QuantumSimulator` 클래스는 `Teleport`를 실행하고 테스트하는 데 적합한 양자 상태 벡터를 완전히 시뮬레이션하여 양자 알고리즘을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-110">The `QuantumSimulator` class executes the quantum algorithm by fully simulating the quantum state vector, which is perfect for running and testing `Teleport`.</span></span>
<span data-ttu-id="f2d6a-111">양자 상태 벡터에 대한 자세한 내용은 [개념 가이드](xref:microsoft.quantum.concepts.intro)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-111">See the [Concepts guide](xref:microsoft.quantum.concepts.intro) for more on quantum state vectors.</span></span>

<span data-ttu-id="f2d6a-112">양자 알고리즘을 실행하는 데 다른 대상 컴퓨터를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-112">Other target machines may be used to run a quantum algorithm.</span></span>
<span data-ttu-id="f2d6a-113">컴퓨터는 이 알고리즘을 위한 양자 기본 형식을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-113">The machine is responsible for providing implementations of quantum primitives for the algorithm.</span></span>
<span data-ttu-id="f2d6a-114">여기에는 H, CNOT 및 측정과 같은 기본 작업 뿐만 아니라, 큐비트 관리와 추적도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-114">This includes primitive operations such as H, CNOT, and Measure, as well as qubit management and tracking.</span></span>
<span data-ttu-id="f2d6a-115">여러 다른 클래스의 양자 컴퓨터는 동일한 양자 알고리즘에 대해 서로 다른 실행 모델을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-115">Different classes of quantum machines represent different execution models for the same quantum algorithm.</span></span>

<span data-ttu-id="f2d6a-116">각 유형의 양자 컴퓨터는 이러한 기본 형식의 다른 구현을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-116">Each type of quantum machine may provide different implementations of these primitives.</span></span>
<span data-ttu-id="f2d6a-117">예를 들어, 개발 키트에 포함된 양자 컴퓨터 추적 시뮬레이터는 시뮬레이션을 전혀 수행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-117">For instance, the quantum computer trace simulator included in the development kit doesn't do any simulation at all.</span></span>
<span data-ttu-id="f2d6a-118">대신 알고리즘에 대한 게이트, 큐비트 및 기타 리소스 사용을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-118">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machines"></a><span data-ttu-id="f2d6a-119">양자 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="f2d6a-119">Quantum Machines</span></span>

<span data-ttu-id="f2d6a-120">향후, 다른 유형의 시뮬레이션을 지원하고 토폴로지 양자 컴퓨터에서 실행할 수 있도록 지원하는 추가 양자 컴퓨터 클래스를 정의할 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-120">In the future, we will define additional quantum machine classes to support other types of simulation and to support execution on topological quantum computers.</span></span>
<span data-ttu-id="f2d6a-121">기본 컴퓨터 구현을 변경하면서 알고리즘은 일정하게 유지하면 시뮬레이션에서 알고리즘을 쉽게 테스트하고 디버그한 다음, 알고리즘이 변경되지 않았다는 확신을 가지고 실제 하드웨어에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-121">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

### <a name="whats-included-in-this-release"></a><span data-ttu-id="f2d6a-122">이 릴리스에 포함된 내용</span><span class="sxs-lookup"><span data-stu-id="f2d6a-122">What's Included in this Release</span></span>

<span data-ttu-id="f2d6a-123">이 버전의 양자 개발자 키트에는 몇 가지 양자 컴퓨터 클래스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-123">This release of the quantum developer kit includes several quantum machine classes.</span></span>
<span data-ttu-id="f2d6a-124">이러한 모든 항목은 `Microsoft.Quantum.Simulation.Simulators` 네임스페이스에 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-124">All of them are defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

* <span data-ttu-id="f2d6a-125">[전체 상태 벡터 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` 클래스</span><span class="sxs-lookup"><span data-stu-id="f2d6a-125">A [full state vector simulator](xref:microsoft.quantum.machines.full-state-simulator), the `QuantumSimulator` class.</span></span>
* <span data-ttu-id="f2d6a-126">[단순 리소스 추정기](xref:microsoft.quantum.machines.resources-estimator), `ResourcesEstimator` 클래스. 양자 알고리즘을 실행하는 데 필요한 리소스를 최상위 수준에서 분석할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-126">A [simple resources estimator](xref:microsoft.quantum.machines.resources-estimator), the `ResourcesEstimator` class, it allows a top level analysis of the resources needed to run a quantum algorithm.</span></span>
* <span data-ttu-id="f2d6a-127">[추적 기반 리소스 추정기](xref:microsoft.quantum.machines.qc-trace-simulator.intro), `QCTraceSimulator` 클래스. 알고리즘의 전체 호출 그래프에 대해 리소스 사용량을 자세히 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-127">A [trace-based resource estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), the `QCTraceSimulator` class, it allows advanced analysis of resources consumptions for the algorithm's entire call-graph.</span></span>
* <span data-ttu-id="f2d6a-128">[Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator), `ToffoliSimulator` 클래스</span><span class="sxs-lookup"><span data-stu-id="f2d6a-128">A [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator), the `ToffoliSimulator` class.</span></span>

## <a name="writing-a-classical-driver-program"></a><span data-ttu-id="f2d6a-129">클래식 드라이버 프로그램 작성</span><span class="sxs-lookup"><span data-stu-id="f2d6a-129">Writing a Classical Driver Program</span></span>

<span data-ttu-id="f2d6a-130">[양자 프로그램을 작성](xref:microsoft.quantum.write-program)할 때 간단한 텔레포트 알고리즘용 C# 드라이버를 작성했습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-130">In [Writing a quantum program](xref:microsoft.quantum.write-program), we wrote a simple C# driver for our teleport algorithm.</span></span> <span data-ttu-id="f2d6a-131">C# 드라이버는 다음과 같은 4가지 주요 목적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-131">A C# driver has 4 main purposes:</span></span>

* <span data-ttu-id="f2d6a-132">대상 컴퓨터 생성</span><span class="sxs-lookup"><span data-stu-id="f2d6a-132">Constructing the target machine</span></span>
* <span data-ttu-id="f2d6a-133">양자 알고리즘에 필요한 인수 계산</span><span class="sxs-lookup"><span data-stu-id="f2d6a-133">Computing any arguments required for the quantum algorithm</span></span>
* <span data-ttu-id="f2d6a-134">시뮬레이터를 사용하여 양자 알고리즘 실행</span><span class="sxs-lookup"><span data-stu-id="f2d6a-134">Running the quantum algorithm using the simulator</span></span>
* <span data-ttu-id="f2d6a-135">연산 결과 처리</span><span class="sxs-lookup"><span data-stu-id="f2d6a-135">Processing the result of the operation</span></span>

<span data-ttu-id="f2d6a-136">여기서는 각 단계를 좀 더 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-136">Here we'll discuss each step in more detail.</span></span>

### <a name="constructing-the-target-machine"></a><span data-ttu-id="f2d6a-137">대상 컴퓨터 생성</span><span class="sxs-lookup"><span data-stu-id="f2d6a-137">Constructing the Target Machine</span></span>

<span data-ttu-id="f2d6a-138">양자 컴퓨터는 일반적인 .NET 클래스의 인스턴스로, .NET 클래스와 마찬가지로 해당 생성자를 호출하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-138">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span>
<span data-ttu-id="f2d6a-139">`QuantumSimulator`를 비롯한 일부 시뮬레이터는 .NET <xref:System.IDisposable?displayProperty=nameWithType> 인터페이스를 구현하므로 C# `using` 문에 래핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-139">Some simulators, including the `QuantumSimulator`, implement the .NET <xref:System.IDisposable?displayProperty=nameWithType> interface, and so should be wrapped in a C# `using` statement.</span></span>

### <a name="computing-arguments-for-the-algorithm"></a><span data-ttu-id="f2d6a-140">알고리즘의 인수 계산</span><span class="sxs-lookup"><span data-stu-id="f2d6a-140">Computing Arguments for the Algorithm</span></span>

<span data-ttu-id="f2d6a-141">`Teleport` 예제에서는 몇 가지 상대적인 인공 인수를 계산하여 양자 알고리즘에 전달했습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-141">In our `Teleport` example, we computed some relatively artificial arguments to pass to our quantum algorithm.</span></span>
<span data-ttu-id="f2d6a-142">그러나 일반적으로 양자 알고리즘에는 많은 데이터가 필요하며, 클래식 드라이버에서 이러한 데이터를 제공하는 것이 가장 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-142">More typically, however, there is significant data required by the quantum algorithm, and it is easiest to provide it from the classical driver.</span></span>

<span data-ttu-id="f2d6a-143">예를 들어, 화학 시뮬레이션을 수행할 때 양자 알고리즘에는 대규모 분자 궤도 상호 작용 적분 표가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-143">For instance, when doing chemical simulations, the quantum algorithm requires a large table of molecular orbital interaction integrals.</span></span>
<span data-ttu-id="f2d6a-144">일반적으로 이러한 데이터는 알고리즘을 실행할 때 제공되는 파일에서 읽어옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-144">Generally these are read in from a file that is provided when running the algorithm.</span></span>
<span data-ttu-id="f2d6a-145">Q#에는 파일 시스템에 액세스하는 메커니즘이 없으므로 이러한 종류의 데이터는 클래식 드라이버에서 가장 잘 수집되며, 수집된 이후 에 양자 알고리즘의 `Run` 메서드에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-145">Since Q# does not have a mechanism for accessing the file system, this sort of data is best collected by the classical driver and then passed to the quantum algorithm's `Run` method.</span></span>

<span data-ttu-id="f2d6a-146">클래식 드라이버가 주요 역할을 수행하는 또 다른 경우는 변분 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-146">Another case where the classical driver plays a key role is in variational methods.</span></span>
<span data-ttu-id="f2d6a-147">이 알고리즘 클래스에서 양자 상태는 일부 클래식 매개 변수를 기준으로 준비되며, 해당 상태를 사용하여 몇 가지 중요한 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-147">In this class of algorithms, a quantum state is prepared based on some classical parameters, and that state is used to compute some value of interest.</span></span>
<span data-ttu-id="f2d6a-148">이 매개 변수는 특정 유형의 언덕 오르기 또는 기계 학습 알고리즘에 따라 조정되며 양자 알고리즘이 다시 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-148">The parameters are adjusted based on some type of hill climbing or machine learning algorithm and the quantum algorithm run again.</span></span>
<span data-ttu-id="f2d6a-149">이러한 알고리즘의 경우 언덕 오르기 알고리즘 자체는 기존 드라이버에서 호출하는 순수한 클래식 함수로 구현하는 것이 가장 좋습니다. 그러면 언덕 오르기의 결과가 다음 번에 양자 알고리즘을 실행할 때 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-149">For such algorithms, the hill climbing algorithm itself is best implemented as a purely classical function that is called by the classical driver; the results of the hill climbing are then passed to the next execution of the quantum algorithm.</span></span>

### <a name="running-the-quantum-algorithm"></a><span data-ttu-id="f2d6a-150">양자 알고리즘 실행</span><span class="sxs-lookup"><span data-stu-id="f2d6a-150">Running the Quantum Algorithm</span></span>

<span data-ttu-id="f2d6a-151">이 부분은 일반적으로 매우 간단합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-151">This part is generally very straightforward.</span></span>
<span data-ttu-id="f2d6a-152">각 Q# 연산은 정적 `Run` 메서드를 제공하는 클래스로 컴파일됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-152">Each Q# operation is compiled into a class that provides a static `Run` method.</span></span>
<span data-ttu-id="f2d6a-153">이 메서드에 대한 인수는 연산 자체의 병합된 인수 튜플과, 실행할 시뮬레이터에 해당하는 첫 번째 추가 인수를 사용하여 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-153">The arguments to this method are given by the flattened argument tuple of the operation itself, plus an additional first argument which is the simulator to execute with.</span></span> <span data-ttu-id="f2d6a-154">명명된 `(a: String, (b: Double, c: Double))` 형식의 튜플을 예상하는 연산에서 병합된 상대 튜플의 형식은 `(String a, Double b, Double c)`입니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-154">For an operation that expects the named tuple of type `(a: String, (b: Double, c: Double))` its flattened counterpart is of type `(String a, Double b, Double c)`.</span></span>


<span data-ttu-id="f2d6a-155">`Run` 메서드에 인수를 전달할 때는 다음과 같은 미묘한 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-155">There are some subtleties when passing arguments to a `Run` method:</span></span>

* <span data-ttu-id="f2d6a-156">배열을 `Microsoft.Quantum.Simulation.Core.QArray<T>` 개체에 래핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-156">Arrays must be wrapped in a `Microsoft.Quantum.Simulation.Core.QArray<T>` object.</span></span>
    <span data-ttu-id="f2d6a-157">`QArray` 클래스에는 순서가 지정된 적절한 개체 컬렉션(`IEnumerable<T>`)을 사용할 수 있는 생성자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-157">A `QArray` class has a constructor that can take any ordered collection (`IEnumerable<T>`) of appropriate objects.</span></span>
* <span data-ttu-id="f2d6a-158">Q#에서 빈 튜플 `()`은 C#에서는 `QVoid.Instance`로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-158">The empty tuple, `()` in Q#, is represented by `QVoid.Instance` in C#.</span></span>
* <span data-ttu-id="f2d6a-159">비어 있지 않은 튜플은 .NET `ValueType` 인스턴스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-159">Non-empty tuples are represented as .NET `ValueType` instances.</span></span>
* <span data-ttu-id="f2d6a-160">Q# 사용자 정의 형식은 기본 형식으로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-160">Q# user-defined types are passed as their base type.</span></span>
* <span data-ttu-id="f2d6a-161">연산 또는 함수를 `Run` 메서드에 전달하려면 시뮬레이터의 `Get<>` 메서드를 사용하여 연산 또는 함수의 클래스 인스턴스를 가져와기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-161">To pass an operation or a function to a `Run` method, you have to obtain an   instance of the operation's or function's class, using the simulator's `Get<>` method.</span></span>

### <a name="processing-the-results"></a><span data-ttu-id="f2d6a-162">결과 처리</span><span class="sxs-lookup"><span data-stu-id="f2d6a-162">Processing the Results</span></span>

<span data-ttu-id="f2d6a-163">양자 알고리즘의 결과는 `Run` 메서드에서 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-163">The results of the quantum algorithm are returned from the `Run` method.</span></span>
<span data-ttu-id="f2d6a-164">`Run` 메서드는 비동기적으로 실행되므로 <xref:System.Threading.Tasks.Task`1>의 인스턴스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-164">The `Run` method executes asynchronously thus it returns an instance of <xref:System.Threading.Tasks.Task`1>.</span></span>
<span data-ttu-id="f2d6a-165">실제 연산의 결과를 가져오는 방법에는 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-165">There are multiple ways to get the actual operation's results.</span></span> <span data-ttu-id="f2d6a-166">가장 간단한 방법은 `Task`의 [`Result` 속성](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result)을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-166">The simplest is by using the `Task`'s [`Result` property](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):</span></span>

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
<span data-ttu-id="f2d6a-167">그러나  [`Wait` 메서드](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) 또는 C# [`await` 키워드](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await)를 사용하는 것과 같은 다른 기법도 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-167">but other techniques, like using the [`Wait` method](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) or C# [`await` keyword](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) will also work.</span></span>

<span data-ttu-id="f2d6a-168">인수를 사용할 때와 마찬가지로 Q# 튜플은 `ValueTuple` 인스턴스로 표시되고 Q# 배열은 `QArray` 인스턴스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-168">As with arguments, Q# tuples are represented as `ValueTuple` instances and Q# arrays are represented as `QArray` instances.</span></span>
<span data-ttu-id="f2d6a-169">사용자 정의 형식은 기본 형식으로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-169">User-defined types are returned as their base types.</span></span>
<span data-ttu-id="f2d6a-170">빈 튜플 `()`는 `QVoid` 클래스의 인스턴스로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-170">The empty tuple, `()`, is returned as an instance of the `QVoid` class.</span></span>

<span data-ttu-id="f2d6a-171">많은 양자 알고리즘은 유용한 답변을 파생하기 위해 상당한 사후 처리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-171">Many quantum algorithms require substantial post-processing to derive useful answers.</span></span>
<span data-ttu-id="f2d6a-172">예를 들어 Shor 알고리즘의 양자 부분은 한 숫자의 인수를 찾아내는 계산의 시작에 불과합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-172">For instance, the quantum part of Shor's algorithm is just the beginning of a computation that finds the factors of a number.</span></span>

<span data-ttu-id="f2d6a-173">대부분의 경우 클래식 드라이버에서 이러한 종류의 사후 처리를 수행하는 것이 가장 간단하고 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-173">In most cases, it is simplest and easiest to do this sort of post-processing in the classical driver.</span></span>
<span data-ttu-id="f2d6a-174">클래식 드라이버만 사용자에게 결과를 보고하거나 디스크에 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-174">Only the classical driver can report results to the user or write them to disk.</span></span>
<span data-ttu-id="f2d6a-175">클래식 드라이버는 Q#에 표시되지 않는 분석 라이브러리 및 기타 수학 함수에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-175">The classical driver will have access to analytical libraries and other mathematical functions that are not exposed in Q#.</span></span>


## <a name="failures"></a><span data-ttu-id="f2d6a-176">오류</span><span class="sxs-lookup"><span data-stu-id="f2d6a-176">Failures</span></span>

<span data-ttu-id="f2d6a-177">연산을 실행하는 동안 Q# `fail` 문에 도달하면 `ExecutionFailException`이 throw됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-177">When the Q# `fail` statement is reached during the execution of an operation, an `ExecutionFailException` is thrown.</span></span>

<span data-ttu-id="f2d6a-178">`Run` 메서드에서 `System.Task`를 사용하기 때문에 `fail` 문의 결과로 throw되는 예외는 `System.AggregateException`에 래핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-178">Due to the use of `System.Task` in the `Run` method, the exception thrown as a result of a `fail` statement will be wrapped into a `System.AggregateException`.</span></span>
<span data-ttu-id="f2d6a-179">오류의 실제 원인을 찾으려면 `AggregateException` 
`InnerExceptions`를 반복해야 합니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-179">To find the actual reason for the failure, you need to iterate into the `AggregateException` 
`InnerExceptions`, for example:</span></span>

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a><span data-ttu-id="f2d6a-180">기타 클래식 언어</span><span class="sxs-lookup"><span data-stu-id="f2d6a-180">Other Classical Languages</span></span>

<span data-ttu-id="f2d6a-181">제공된 샘플은 C#, F# 및 Python으로 작성된 것이지만, Quantum Development Kit는 다른 언어로 작성된 클래식 호스트 프로그램 작성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d6a-181">While the samples we have provided are in C#, F#, and Python, the Quantum Development Kit also supports writing classical host programs in other languages.</span></span>
<span data-ttu-id="f2d6a-182">예를 들어, Visual Basic에서 호스트 프로그램을 작성하려는 경우에는 [문제가 없이 잘 작동합니다](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span><span class="sxs-lookup"><span data-stu-id="f2d6a-182">For example, if you want to write a host program in Visual Basic, [it should work just fine](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span></span>
