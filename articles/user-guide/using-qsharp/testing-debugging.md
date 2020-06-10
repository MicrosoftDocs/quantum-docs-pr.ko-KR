---
title: 테스트 및 디버깅
description: 단위 테스트, 팩트 및 어설션을 사용 하는 방법 및 덤프 함수를 사용 하 여 퀀텀 프로그램을 테스트 하 고 디버그 하는 방법을 알아봅니다.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
ms.openlocfilehash: dd6c7ae8a016423f26c37f3eedf0ae9c1d126b78
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630023"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="96a3b-103">테스트 및 디버깅</span><span class="sxs-lookup"><span data-stu-id="96a3b-103">Testing and debugging</span></span>

<span data-ttu-id="96a3b-104">기존 프로그래밍과 마찬가지로 퀀텀 프로그램이 의도 한 대로 작동 하는지 확인 하 고 잘못 된 퀀텀 프로그램을 진단할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="96a3b-105">이 섹션에서는 퀀텀 프로그램 테스트 및 디버깅을 위해 Q #에서 제공 하는 도구를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="96a3b-106">단위 테스트</span><span class="sxs-lookup"><span data-stu-id="96a3b-106">Unit Tests</span></span>

<span data-ttu-id="96a3b-107">클래식 프로그램을 테스트 하는 일반적인 방법 중 하나는 라이브러리에서 코드를 실행 하 고 해당 출력을 예상 출력과 비교 하는 *단위 테스트* 라는 작은 프로그램을 작성 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="96a3b-108">예를 들어 `Square(2)` `4` $2 ^ 2 = $4 이라는 *apriori* 을 알고 있으므로가를 반환 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="96a3b-109">Q #은 퀀텀 프로그램에 대 한 단위 테스트 만들기를 지원 하 고 [Xunit](https://xunit.github.io/) 단위 테스트 프레임 워크 내에서 테스트로 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="96a3b-110">테스트 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="96a3b-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="96a3b-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="96a3b-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="96a3b-112">Visual Studio 2019를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="96a3b-113">메뉴로 이동 하 여를 `File` 선택 `New`  >  `Project...` 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="96a3b-114">오른쪽 위 모서리에서를 검색 하 `Q#` 고 `Q# Test Project` 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="96a3b-115">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="96a3b-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="96a3b-116">선호 하는 명령줄에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="96a3b-117">새 프로젝트에는 `Tests.qs` 새 Q # 단위 테스트를 정의 하는 데 편리한 장소를 제공 하는 단일 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="96a3b-118">처음에이 파일에는 `AllocateQubit` 새로 할당 된가 $ \ket $ 상태에 있는지 확인 하 {0} 고 메시지를 인쇄 하는 하나의 샘플 단위 테스트가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="96a3b-119">: new: 형식의 인수를 사용 하 고를 반환 하는 모든 Q # 작업 또는 함수는 `Unit` `Unit` 특성을 통해 단위 테스트로 표시 될 수 있습니다 `@Test("...")` .</span><span class="sxs-lookup"><span data-stu-id="96a3b-119">:new: Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="96a3b-120">위의 해당 특성에 대 한 인수는 `"QuantumSimulator"` 테스트가 실행 되는 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="96a3b-121">단일 테스트를 여러 대상에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="96a3b-122">예를 들어 위에 특성을 `@Test("ResourcesEstimator")` 추가 `AllocateQubit` 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="96a3b-123">파일을 저장 하 고 모든 테스트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-123">Save the file and execute all tests.</span></span> <span data-ttu-id="96a3b-124">이제 두 개의 단위 테스트가 있습니다. 여기에는 AllocateQuantumSimulator 비트가 실행 되 고 하나는 ResourceEstimator에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="96a3b-125">Q # 컴파일러는 기본 제공 대상 "QuantumSimulator", "ToffoliSimulator" 및 "ResourcesEstimator"를 단위 테스트에 대 한 올바른 실행 대상으로 인식 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="96a3b-126">또한 사용자 지정 실행 대상을 정의 하는 정규화 된 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="96a3b-127">Q # 단위 테스트 실행</span><span class="sxs-lookup"><span data-stu-id="96a3b-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="96a3b-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="96a3b-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="96a3b-129">솔루션 당 일회성 설치로 이동 하 여 메뉴로 이동 하 `Test` 고를 선택 `Test Settings`  >  `Default Processor Architecture`  >  `X64` 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="96a3b-130">Visual Studio의 기본 프로세서 아키텍처 설정은 `.suo` 각 솔루션에 대 한 솔루션 옵션 () 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="96a3b-131">이 파일을 삭제 하는 경우 `X64` 프로세서 아키텍처로 다시 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="96a3b-132">프로젝트를 빌드하고 메뉴로 이동 하 여를 `Test` 선택 `Windows`  >  `Test Explorer` 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="96a3b-133">`AllocateQubit`그룹의 테스트 목록에 표시 됩니다 `Not Run Tests` .</span><span class="sxs-lookup"><span data-stu-id="96a3b-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="96a3b-134">`Run All`이 개별 테스트를 선택 하거나 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="96a3b-135">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="96a3b-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="96a3b-136">테스트를 실행 하려면 프로젝트 폴더 (가 포함 된 폴더)로 이동 하 `Tests.csproj` 고 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="96a3b-137">다음과 유사한 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-137">You should get output similar to the following:</span></span>

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

<span data-ttu-id="96a3b-138">단위 테스트는 이름 및/또는 실행 대상에 따라 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="96a3b-139">내장 함수에는 <xref:microsoft.quantum.intrinsic.message> 형식이 `(String -> Unit)` 있으며 진단 메시지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="96a3b-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="96a3b-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="96a3b-141">테스트 탐색기에서 테스트를 실행 하 고 테스트를 클릭 하면 테스트 실행: 성공/실패 상태, 경과 시간 및 "출력" 링크에 대 한 정보가 포함 된 패널이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="96a3b-142">"출력" 링크를 클릭 하면 테스트 출력이 새 창에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-142">If you click the "Output" link, test output will open in a new window.</span></span>

![테스트 출력](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="96a3b-144">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="96a3b-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="96a3b-145">각 테스트에 대 한 통과/실패 상태는에 의해 콘솔에 출력 됩니다 `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="96a3b-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="96a3b-146">실패 한 테스트의 경우 출력은 오류를 진단 하는 데 도움이 되도록 콘솔에도 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="96a3b-147">팩트 및 어설션</span><span class="sxs-lookup"><span data-stu-id="96a3b-147">Facts and Assertions</span></span>

<span data-ttu-id="96a3b-148">Q #의 함수에는 _논리적인_ 부작용이 없으므로 출력 형식이 빈 튜플 인 함수를 실행 하는 _다른 종류_ 의 효과는 `()` Q # 프로그램 내에서 관찰할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="96a3b-149">즉, 대상 컴퓨터에서 반환 하는 함수를 실행 하지 않도록 선택할 수 있습니다 `()` .이를 생략 하면 다음 Q # 코드의 동작이 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="96a3b-150">이를 통해 함수 `()` `Unit` 는 어설션 및 디버깅 논리를 Q # 프로그램에 포함 하는 데 유용한 도구를 반환 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="96a3b-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="96a3b-151">간단한 예제를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="96a3b-152">여기서 키워드는 `fail` 계산이 진행 되지 않고 Q # 프로그램을 실행 하는 대상 컴퓨터에서 예외가 발생 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="96a3b-153">정의에 따라 문이 도달한 후 추가 Q # 코드가 실행 되지 않으므로 Q # 내에서 이러한 종류의 오류를 확인할 수 없습니다 `fail` .</span><span class="sxs-lookup"><span data-stu-id="96a3b-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="96a3b-154">따라서에 대 한 호출을 계속 진행 하는 경우 `PositivityFact` 해당 입력이 긍정적 임을 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="96a3b-155">`PositivityFact` [`Fact`](xref:microsoft.quantum.diagnostics.fact) 네임 스페이스에서 함수를 사용 하는 것과 동일한 동작을 구현할 수 있습니다 <xref:microsoft.quantum.diagnostics> .</span><span class="sxs-lookup"><span data-stu-id="96a3b-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

<span data-ttu-id="96a3b-156">반면에 *어설션은*팩트와 유사 하 게 사용 되지만 대상 컴퓨터의 상태에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="96a3b-157">이와 마찬가지로 팩트는 작업으로 정의 되는 반면 팩트는 위에 나와 있는 함수로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="96a3b-158">구분을 이해 하려면 어설션 내에서 다음과 같은 팩트를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="96a3b-159">여기에서 작업을 사용 하 여 <xref:microsoft.quantum.environment.getqubitsavailabletouse> 사용할 수 있는 값 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="96a3b-160">이는 프로그램의 전역 상태와 해당 실행 환경에 따라 달라 지기 때문에의 정의 `AssertQubitsAreAvailable` 도 작업 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="96a3b-161">그러나이 전역 상태를 사용 하 여 간단한 `Bool` 값을 함수에 대 한 입력으로 생성할 수 있습니다 `Fact` .</span><span class="sxs-lookup"><span data-stu-id="96a3b-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="96a3b-162">이러한 아이디어를 기반으로 하 [는 prelude는](xref:microsoft.quantum.libraries.standard.prelude) 두 가지 특히 유용한 어설션을 제공 <xref:microsoft.quantum.intrinsic.assert> 하며 <xref:microsoft.quantum.intrinsic.assertprob> 둘 다 작업으로 모델링 `()` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="96a3b-163">이러한 어설션은 각각 특정 측정값을 설명 하는 Pauli 연산자, 측정을 수행 해야 하는 퀀텀 레지스터 및 가상 결과를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="96a3b-164">시뮬레이션을 통해 작동 하는 대상 컴퓨터에서는 [복제 안 함 정리](https://en.wikipedia.org/wiki/No-cloning_theorem)바인딩되지 않으며 이러한 어설션에 전달 된 레지스터를 방해 하지 않고 이러한 측정을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="96a3b-165">그러면 시뮬레이터는 `PositivityFact` 위의 함수와 비슷하며 가상 결과가 실제로 관찰 되지 않는 경우 계산을 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="96a3b-166">복제 안 함 정리에서 퀀텀 상태 검사를 방지 하는 실제 퀀텀 하드웨어에서 `Assert` 및 작업은 `AssertProb` `()` 다른 영향 없이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="96a3b-167"><xref:microsoft.quantum.diagnostics>네임 스페이스는 `Assert` 더 많은 고급 조건을 확인할 수 있도록 하는 패밀리의 여러 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="96a3b-168">덤프 함수</span><span class="sxs-lookup"><span data-stu-id="96a3b-168">Dump Functions</span></span>

<span data-ttu-id="96a3b-169">퀀텀 프로그램의 문제를 해결 하기 위해 <xref:microsoft.quantum.diagnostics> 네임 스페이스는 대상 컴퓨터의 현재 상태 (및)를 파일에 덤프할 수 있는 두 가지 함수를 제공 합니다 <xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics.dumpregister> .</span><span class="sxs-lookup"><span data-stu-id="96a3b-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="96a3b-170">각각의 생성 된 출력은 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="96a3b-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="96a3b-171">DumpMachine</span></span>

<span data-ttu-id="96a3b-172">퀀텀 개발 키트의 일부분으로 배포 되는 전체 상태 퀀텀 시뮬레이터는 전체 퀀텀 시스템의 [wave 함수](https://en.wikipedia.org/wiki/Wave_function) 를 파일에 기록 하 고, 각 요소가 계산 기준 상태 $ \ket{n} $를 측정할 확률의 진폭을 나타냅니다. 여기서 $ \ket{n} = \ket{b_ {n-1} ... bits $ b_i $의 b_1b_0} $ \{ \} 입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="96a3b-173">예를 들어 두 개의 om비트가 할당 되 고 퀀텀 상태 $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} \ket 인 컴퓨터에서 {2} {10} \end{align} $ $ 호출은 <xref:microsoft.quantum.diagnostics.dumpmachine> 다음 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="96a3b-174">첫 번째 행은 중요 한 순서 대로 해당 하는의 Id를 사용 하 여 주석을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="96a3b-175">나머지 행은 데카르트 및 극좌표 형식의 기본 상태 vector $ \ket{n} $를 측정 하는 확률 진폭을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="96a3b-176">첫 번째 행에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-176">In detail for the first row:</span></span>

* <span data-ttu-id="96a3b-177">**`∣0❭:`** 이 행은 `0` 계산 기준 상태에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="96a3b-178">**`0.707107 +  0.000000 i`**: 데카르트 형식의 확률 진폭입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="96a3b-179">**` == `**: `equal` 부호는 두 동등한 표현을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-179">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="96a3b-180">**`**********  `**: 크기의 그래픽 표현으로,의 수는 `*` 이 상태 벡터를 측정할 확률에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="96a3b-181">**`[ 0.500000 ]`**: 크기의 숫자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="96a3b-182">**`    ---`**: 진폭의 단계를 그래픽으로 표현한 것입니다 (아래 참조).</span><span class="sxs-lookup"><span data-stu-id="96a3b-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="96a3b-183">**`[ 0.0000 rad ]`**: 단계의 숫자 값 (라디안 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="96a3b-184">크기와 단계가 모두 그래픽 표현으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="96a3b-185">크기 표현은 간단 하 게 표시 됩니다. 막대를 표시 하 고 막대의 클수록 표시 되는 `*` 확률이 커집니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="96a3b-186">단계에서는 범위에 따라 각도를 나타내기 위해 다음 기호를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="96a3b-187">다음 예에서는 `DumpMachine` 몇 가지 일반적인 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-187">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="96a3b-188">의 id는 런타임에 할당 되며,이는 해당 비트를 할당 하는 순서 또는이를 사용 하는 순서에 따라 결정 되는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="96a3b-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="96a3b-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="96a3b-190">코드에 중단점을 배치 하 고 다음과 같이 다음과 같이 Visual Studio에서 사용자 비트 id를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Visual Studio에서 이상 비트 id 표시](~/media/qubit_id.png)
  >
  > <span data-ttu-id="96a3b-192">인덱스에 있는 이상 비트의 id는 id =이 고 인덱스의는 `0` `register2` `3` `1` id = `2` 입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="96a3b-193">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="96a3b-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="96a3b-194">함수를 사용 하 <xref:microsoft.quantum.intrinsic.message> 고 다음과 같이 메시지에 다음과 같은 기능을 사용 하 여 원하는 비트 id를 알아낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="96a3b-195">다음 출력이 생성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="96a3b-196">즉, 인덱스가 있는 이상 비트의 id는 id =이 고 인덱스의는 `0` `register2` `3` `1` id = `2` 입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="96a3b-197"><xref:microsoft.quantum.diagnostics.dumpmachine>는 네임 스페이스의 일부 이므로 <xref:microsoft.quantum.diagnostics> 사용 하기 위해 문을 추가 해야 합니다 `open` .</span><span class="sxs-lookup"><span data-stu-id="96a3b-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="96a3b-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="96a3b-198">DumpRegister</span></span>

<span data-ttu-id="96a3b-199"><xref:microsoft.quantum.diagnostics.dumpregister>는와 유사 하 게 작동 합니다. 단,이 경우에는 해당 하는 이상 <xref:microsoft.quantum.diagnostics.dumpmachine> 비트와 관련 된 정보만으로 정보의 양을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="96a3b-200">와 마찬가지로 <xref:microsoft.quantum.diagnostics.dumpmachine> 에서 생성 되는 정보는 <xref:microsoft.quantum.diagnostics.dumpregister> 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="96a3b-201">전체 상태 퀀텀 시뮬레이터에 대해 wave 함수를 파일에 기록 합니다 .이 함수는와 동일한 형식으로 제공 된 해당 하는 것으로 생성 된 퀀텀 하위 시스템의 전역 단계까지 파일에 기록 합니다 <xref:microsoft.quantum.diagnostics.dumpmachine> .</span><span class="sxs-lookup"><span data-stu-id="96a3b-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="96a3b-202">예를 들어 두 개의 기능을 할당 하 고 퀀텀 상태 $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} \ket =-e ^ {로 컴퓨터를 다시 사용 합니다. {2} {10} -i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \frac \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ 호출은 <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[0]` 다음 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="96a3b-203">및를 호출 하면 <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[1]` 다음 출력이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="96a3b-204">일반적으로 다른 레지스터와 함께 사용 되는 레지스터의 상태는 순수 상태가 아닌 혼합 된 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="96a3b-205">이 경우는 <xref:microsoft.quantum.diagnostics.dumpregister> 다음 메시지를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="96a3b-206">다음 예제에서는 <xref:microsoft.quantum.diagnostics.dumpregister> <xref:microsoft.quantum.diagnostics.dumpmachine> Q # 코드에서 및를 모두 사용할 수 있는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="96a3b-207">디버깅</span><span class="sxs-lookup"><span data-stu-id="96a3b-207">Debugging</span></span>

<span data-ttu-id="96a3b-208">`Assert`및 `Dump` 함수 및 작업의 위쪽에서 Q #은 표준 Visual Studio 디버깅 기능의 하위 집합을 지원 합니다. [줄 중단점 설정](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), F10 키를 [사용 하 여 코드 단계별](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) 실행 및 [클래식 변수의 값 검사](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) 는 모두 시뮬레이터에서 코드를 실행 하는 동안 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="96a3b-209">Visual Studio Code 디버깅은 c #에서 제공 하는 c # For Visual Studio Code 확장에서 제공 하는 디버깅 기능을 활용 하 고 [최신 버전](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96a3b-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
