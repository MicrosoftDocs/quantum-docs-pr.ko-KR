---
title: Q# 프로그램 테스트 및 디버깅
description: 단위 테스트, 사실 및 어설션을 사용하고 함수를 덤프하여 양자 프로그램을 테스트하고 디버깅하는 방법을 알아봅니다.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030585"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="07649-103">테스트 및 디버깅</span><span class="sxs-lookup"><span data-stu-id="07649-103">Testing and Debugging</span></span>

<span data-ttu-id="07649-104">클래식 프로그래밍과 마찬가지로 양자 프로그램이 의도한 대로 작동하도록 하고 잘못된 양자 프로그램을 진단할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="07649-105">이 섹션에서는 양자 프로그램을 테스트하고 디버깅하기 위해 Q#에서 제공하는 도구를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="07649-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="07649-106">단위 테스트</span><span class="sxs-lookup"><span data-stu-id="07649-106">Unit Tests</span></span>

<span data-ttu-id="07649-107">클래식 프로그램을 테스트하는 한 가지 일반적인 방법은 라이브러리에서 코드를 실행하는 *단위 테스트라는* 작은 프로그램을 작성하고 출력을 일부 예상 출력과 비교하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="07649-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="07649-108">예를 들어$ 2 ^2 `Square(2)` `4`= 4 $라는 *선험을* 알고 있기 때문에 반환을 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="07649-109">Q#은 양자 프로그램에 대한 단위 테스트 생성을 지원하며 [xUnit](https://xunit.github.io/) 단위 테스트 프레임워크 내에서 테스트로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="07649-110">테스트 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="07649-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="07649-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="07649-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="07649-112">Visual Studio 2019를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="07649-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="07649-113">메뉴로 `File` 이동하여 `New`  >  `Project...`을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="07649-114">오른쪽 상단 모서리에서 `Q#`을 검색하고 `Q# Test Project` 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="07649-115">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="07649-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="07649-116">즐겨 찾는 명령줄에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="07649-117">새 프로젝트에는 새 Q# 단위 테스트를 정의할 수 있는 편리한 위치를 제공하는 단일 파일이 `Tests.qs`있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="07649-118">처음에이 파일에는 새로 `AllocateQubit` 할당 된 큐빗이 $\ket{0}$ 상태에 있는지 확인하고 메시지를 인쇄하는 하나의 샘플 단위 테스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:new: <span data-ttu-id="07649-119">형식 `Unit` 및 반환인수를 `Unit` 취하는 모든 Q# 작업 또는 함수는 `@Test("...")` 특성을 통해 단위 테스트로 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-119">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="07649-120">`"QuantumSimulator"` 위의 해당 특성에 대한 인수는 테스트가 실행되는 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="07649-121">단일 테스트는 여러 대상에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="07649-122">예를 들어 위의 `@Test("ResourcesEstimator")` 특성을 추가합니다. `AllocateQubit`</span><span class="sxs-lookup"><span data-stu-id="07649-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="07649-123">파일을 저장하고 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-123">Save the file and execute all tests.</span></span> <span data-ttu-id="07649-124">이제 두 개의 단위 테스트가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="07649-125">Q# 컴파일러는 기본 제공 대상인 "QuantumSimulator", "ToffoliSimulator"및 "ResourcesEstimator"를 단위 테스트의 유효한 실행 대상으로 인식합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="07649-126">사용자 지정 실행 대상을 정의하기 위해 정규화된 이름을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="07649-127">Q# 단위 테스트 실행</span><span class="sxs-lookup"><span data-stu-id="07649-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="07649-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="07649-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="07649-129">솔루션당 일회성 설정으로 메뉴로 이동하여 `Test` 을 `Test Settings`  >  `Default Processor Architecture`  >  `X64`선택합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="07649-130">Visual Studio의 기본 프로세서 아키텍처 설정은 각`.suo`솔루션에 대한 솔루션 옵션() 파일에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="07649-131">이 파일을 삭제하면 프로세서 아키텍처로 `X64` 다시 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="07649-132">프로젝트를 빌드하고 메뉴로 `Test` 이동하여 `Windows`  >  `Test Explorer`을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="07649-133">`AllocateQubit``Not Run Tests` 테스트 목록에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="07649-134">이 `Run All` 개별 테스트를 선택하거나 실행하면 통과해야 합니다!</span><span class="sxs-lookup"><span data-stu-id="07649-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="07649-135">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="07649-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="07649-136">테스트를 실행하려면 프로젝트 폴더(포함된 `Tests.csproj`폴더)로 이동하여 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="07649-137">다음과 유사한 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-137">You should get output similar to the following:</span></span>

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

<span data-ttu-id="07649-138">단위 테스트는 이름 및/또는 실행 대상에 따라 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="07649-139">내장 함수에는 <xref:microsoft.quantum.intrinsic.message> 형식이 `(String -> Unit)` 있으며 진단 메시지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="07649-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="07649-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="07649-141">테스트 탐색기에서 테스트를 실행하고 테스트를 클릭하면 테스트 실행에 대한 정보(통과/실패 상태, 경과 시간 및 "출력" 링크)가 패널에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="07649-142">"출력" 링크를 클릭하면 테스트 출력이 새 창에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="07649-142">If you click the "Output" link, test output will open in a new window.</span></span>

![테스트 출력](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="07649-144">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="07649-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="07649-145">각 테스트의 합격/불합격 상태는 에 `dotnet test`의해 콘솔에 인쇄됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="07649-146">실패한 테스트의 경우 오류를 진단하는 데 도움이 되는 출력도 콘솔에 인쇄됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="07649-147">사실 및 어설션</span><span class="sxs-lookup"><span data-stu-id="07649-147">Facts and Assertions</span></span>

<span data-ttu-id="07649-148">Q#의 함수에는 _논리적_ 부작용이 없으므로 출력 유형이 빈 튜플인 `()` 함수를 실행하는 _다른 종류의_ 효과는 Q# 프로그램 내에서 관찰할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="07649-149">즉, 대상 컴퓨터는 이 누락이 다음 `()` Q# 코드의 동작을 수정하지 않는다는 보장과 함께 반환되는 함수를 실행하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="07649-150">이렇게 하면 함수 `()` 반환(즉, `Unit`즉)은 어설션을 포함하고 논리를 Q# 프로그램에 디버깅하는 데 유용한 도구가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="07649-151">간단한 예를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="07649-152">여기서 키워드는 `fail` 계산이 진행되지 않아야 한다는 것을 나타내며 Q# 프로그램을 실행하는 대상 컴퓨터에서 예외를 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="07649-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="07649-153">정의에 따르면 문에 도달한 후 더 이상 Q# 코드가 실행되지 않도록 `fail` Q#내에서 이러한 종류의 오류를 관찰할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="07649-154">따라서, 우리가 에 전화를 `PositivityFact`지나 가면 , 우리는 입력이 긍정적이었다는 것을 확신 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="07649-155">네임스페이스에서 `PositivityFact` [`Fact`](xref:microsoft.quantum.diagnostics.fact) 함수를 사용하는 것과 동일한 <xref:microsoft.quantum.diagnostics> 동작을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="07649-156">반면 *어설션은*사실과 유사하게 사용되지만 대상 컴퓨터의 상태에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="07649-157">이에 상응하여 작업으로 정의되는 반면 팩트는 함수(위와 같이)로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="07649-158">이러한 차이점을 이해하려면 어설션 내에서 팩트를 다음과 같은 용도로 사용하는 것을 고려하십시오.</span><span class="sxs-lookup"><span data-stu-id="07649-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="07649-159">여기서는 작업을 <xref:microsoft.quantum.environment.getqubitsavailabletouse> 사용하여 사용할 수 있는 큐빗 수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="07649-160">이는 프로그램의 전역 상태와 실행 환경에 따라 명확히 달라지므로 당사의 `AssertQubitsAreAvailable` 정의도 작업이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="07649-161">그러나 해당 전역 상태를 사용하여 `Bool` `Fact` 함수에 대한 입력으로 간단한 값을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="07649-162">이러한 아이디어를 [기반으로, 전주곡은](xref:microsoft.quantum.libraries.standard.prelude) 두 가지 특히 <xref:microsoft.quantum.intrinsic.assert> <xref:microsoft.quantum.intrinsic.assertprob> 유용한 어설션을 `()`제공하며, 둘 다 에 대한 작업으로 모델링됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="07649-163">이러한 주장은 각각 관심의 특정 측정을 설명하는 Pauli 연산자, 측정이 수행될 양자 레지스터 및 가상의 결과를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="07649-164">시뮬레이션에 의해 작동하는 대상 기계에서는 [복제 정리 없음에](https://en.wikipedia.org/wiki/No-cloning_theorem)구속되지 않으며 이러한 어설션에 전달된 레지스터를 방해하지 않고 이러한 측정을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="07649-165">그런 다음 시뮬레이터는 위의 `PositivityFact` 함수와 마찬가지로 가상의 결과가 실제로 관찰되지 않는 경우 계산을 중단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="07649-166">복제 가용되지 않는 정리가 양자 상태의 검사를 방지하는 물리적 양자 `Assert` 하드웨어에서는 다른 효과없이 작업과 `AssertProb` 작업이 반환됩니다. `()`</span><span class="sxs-lookup"><span data-stu-id="07649-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="07649-167">네임 스페이스는 <xref:microsoft.quantum.diagnostics> 우리가 더 `Assert` 고급 조건을 확인할 수 있도록 가족의 몇 가지 더 많은 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="07649-168">덤프 함수</span><span class="sxs-lookup"><span data-stu-id="07649-168">Dump Functions</span></span>

<span data-ttu-id="07649-169">양자 프로그램 문제 해결을 <xref:microsoft.quantum.diagnostics> 돕기 위해 네임스페이스는 대상 컴퓨터의 <xref:microsoft.quantum.diagnostics.dumpmachine> 현재 상태를 파일에 <xref:microsoft.quantum.diagnostics.dumpregister>덤프할 수 있는 두 가지 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="07649-170">각각의 생성된 출력은 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="07649-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="07649-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="07649-171">DumpMachine</span></span>

<span data-ttu-id="07649-172">양자 개발 키트의 일부로 배포 된 전체 상태 양자 시뮬레이터는 파일 전체에 전체 양자 시스템의 [웨이브 함수를](https://en.wikipedia.org/wiki/Wave_function) 기록, 복잡한 숫자의 1 차원 배열로, 각 요소는 계산 기준 상태를 측정 할 확률의 진폭을 나타내는 $\ket{n}, 여기서 $\ket{n} = {b_{b_{n-1}... b_1b_0$b_i 비트에\{대해\}$b_i.</span><span class="sxs-lookup"><span data-stu-id="07649-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="07649-173">예를 들어, 양자 상태에서 $${1}\begin{align} \ frac {\sqrt{2}} \\frac{{(1{00} + i)}{2} \ket{10}, \end{align} $$ 호출이 <xref:microsoft.quantum.diagnostics.dumpmachine> 할당된 컴퓨터에서 는 이 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="07649-174">첫 번째 행은 해당 큐빗의 해당 큐빗의 주요 순서로 주석을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="07649-175">나머지 행은 카르테시안 및 극성 형식 모두에서 기본 상태 벡터 $\ket{n}$를 측정하는 확률 진폭을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="07649-176">첫 번째 행에 대한 자세한 내용은 다음과 같은</span><span class="sxs-lookup"><span data-stu-id="07649-176">In detail for the first row:</span></span>

* <span data-ttu-id="07649-177">**`∣0❭:`** 이 행은 `0` 계산 기준 상태에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="07649-178">**`0.707107 +  0.000000 i`**: 카르테시안 형식의 확률 진폭입니다.</span><span class="sxs-lookup"><span data-stu-id="07649-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="07649-179">**` == `**: `equal` 부호는 두 동등한 표현을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-179">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="07649-180">**`**********  `**: 크기의 그래픽 표현, 개수는 `*` 이 상태 벡터를 측정할 확률에 비례한다.</span><span class="sxs-lookup"><span data-stu-id="07649-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="07649-181">**`[ 0.500000 ]`**: 크기의 숫자 값</span><span class="sxs-lookup"><span data-stu-id="07649-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="07649-182">**`    ---`**: 진폭의 위상에 대한 그래픽 표현입니다(아래 참조).</span><span class="sxs-lookup"><span data-stu-id="07649-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="07649-183">**`[ 0.0000 rad ]`**: 위상의 숫자 값(라디안)입니다.</span><span class="sxs-lookup"><span data-stu-id="07649-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="07649-184">크기와 위상모두 그래픽 표현으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="07649-185">크기 표현은 직선입니다: 막대가 `*`표시될 확률이 클수록 막대가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="07649-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="07649-186">위상에 대 한 범위에 따라 각도를 나타내는 다음 기호를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

<span data-ttu-id="07649-187">다음 예제는 `DumpMachine` 몇 가지 일반적인 상태에 대해 보여 준다.</span><span class="sxs-lookup"><span data-stu-id="07649-187">The following examples show `DumpMachine` for some common states:</span></span>

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > <span data-ttu-id="07649-188">큐빗의 ID는 런타임에 할당되며 큐빗이 할당된 순서 또는 큐빗 레지스터 내의 위치와 반드시 일치하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="07649-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="07649-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="07649-190">예를 들어 코드에 중단점을 배치하고 qubit 변수의 값을 검사하여 Visual Studio에서 qubit ID를 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![비주얼 스튜디오에서 큐비트 ID 표시](~/media/qubit_id.png)
  >
  > <span data-ttu-id="07649-192">`0` 인덱스가 `register2` 있는 큐빗에는`3`id=가 있으며 `1` 인덱스가`2`있는 큐빗에는 id=가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="07649-193">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="07649-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="07649-194">예를 들어 <xref:microsoft.quantum.intrinsic.message> 함수를 사용하고 메시지에서 qubit 변수를 전달하여 qubit ID를 알아낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="07649-195">이 출력을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="07649-196">즉, 인덱스가 `0` `register2` 있는 큐비트에`3`id=, 인덱스가 `1` 있는`2`큐비트에는 id=가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07649-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="07649-197"><xref:microsoft.quantum.diagnostics.dumpmachine><xref:microsoft.quantum.diagnostics> 네임스페이스의 일부이므로 사용하려면 `open` 문을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a><span data-ttu-id="07649-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="07649-198">DumpRegister</span></span>

<span data-ttu-id="07649-199"><xref:microsoft.quantum.diagnostics.dumpregister>정보 <xref:microsoft.quantum.diagnostics.dumpmachine>양을 해당 큐빗과 관련된 정보로만 제한하는 큐빗 배열을 제외하면 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="07649-200">와 <xref:microsoft.quantum.diagnostics.dumpmachine>마찬가지로, 생성 <xref:microsoft.quantum.diagnostics.dumpregister> 된 정보는 대상 컴퓨터에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="07649-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="07649-201">풀 스테이트 양자 시뮬레이터의 경우 제공된 양자 서브 시스템의 글로벌 단계까지 웨이브 함수를 파일에 기록하여 <xref:microsoft.quantum.diagnostics.dumpmachine>동일한 형식으로 제공된 큐빗에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="07649-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="07649-202">{1}예를 들어, 양자 상태에서 $$ \begin{align} = \frac {\sqrt{2}} \ket{00} - \frac{{(1 + i)}{2} \ket{10} = - e^{-i\pi/4에 할당된 두 개의{1}큐비트만 있는{2}기계를{0} 다시 가져가라. } (\frac{1} {\sqrt } \ket - \frac{{(1{2}+{0} i)} <xref:microsoft.quantum.diagnostics.dumpregister> {2} \otimes \frac{-(1 + i)}{\sqrt } \ket) \ end{align} $$ 이 출력을 생성하기 위해 `qubit[0]` 호출:</span><span class="sxs-lookup"><span data-stu-id="07649-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="07649-203"><xref:microsoft.quantum.diagnostics.dumpregister> 호출은 `qubit[1]` 이 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="07649-204">일반적으로 다른 레지스터와 얽혀 있는 레지스터의 상태는 순수 상태가 아닌 혼합 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="07649-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="07649-205">이 경우 <xref:microsoft.quantum.diagnostics.dumpregister> 다음 메시지를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="07649-206">다음 예제에서는 Q# 코드와 <xref:microsoft.quantum.diagnostics.dumpregister> <xref:microsoft.quantum.diagnostics.dumpmachine> 둘 다 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07649-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a><span data-ttu-id="07649-207">디버깅</span><span class="sxs-lookup"><span data-stu-id="07649-207">Debugging</span></span>

<span data-ttu-id="07649-208">`Dump` 기능 및 `Assert` 작업 외에도 Q#은 표준 Visual Studio 디버깅 기능의 하위 집합인 [줄 중단점 설정,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [F10을 사용한 코드 단계별 단계](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) 및 [클래식 변수의 값 검사는](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) 시뮬레이터에서 코드 실행 중에 모두 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="07649-209">Visual Studio 코드에서 디버깅은 OmniSharp에서 제공하는 Visual Studio 코드 확장용 C#에서 제공하는 디버깅 기능을 활용하며 [최신 버전을](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07649-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span> 
