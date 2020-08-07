---
title: 테스트 및 디버깅
description: 단위 테스트, 팩트 및 어설션을 사용 하는 방법 및 덤프 함수를 사용 하 여 퀀텀 프로그램을 테스트 하 고 디버그 하는 방법을 알아봅니다.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2b5276da594ba263177d435c1153f6d96e29c4e8
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867916"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="b7e58-103">테스트 및 디버깅</span><span class="sxs-lookup"><span data-stu-id="b7e58-103">Testing and debugging</span></span>

<span data-ttu-id="b7e58-104">기존 프로그래밍과 마찬가지로 퀀텀 프로그램이 의도 한 대로 작동 하는지 확인 하 고 잘못 된 동작을 진단할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose incorrect behavior.</span></span>
<span data-ttu-id="b7e58-105">이 섹션에서는에서 Q# 퀀텀 프로그램을 테스트 하 고 디버그 하는 데 제공 하는 도구를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="b7e58-106">단위 테스트</span><span class="sxs-lookup"><span data-stu-id="b7e58-106">Unit Tests</span></span>

<span data-ttu-id="b7e58-107">클래식 프로그램을 테스트 하는 일반적인 방법 중 하나는 라이브러리에서 코드를 실행 하 고 출력을 예상 출력과 비교 하는 *단위 테스트*라는 작은 프로그램을 작성 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-107">One common approach to testing classical programs is to write small programs called *unit tests*, which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="b7e58-108">예를 들어 `Square(2)` `4` $2 ^ 2 = $4 이라는 *apriori을* 알고 있으므로이 반환 되는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-108">For example, you can ensure that `Square(2)` returns `4` since you know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="b7e58-109">Q#는 퀀텀 프로그램에 대 한 단위 테스트 만들기를 지원 하 고 [Xunit](https://xunit.github.io/) 단위 테스트 프레임 워크 내에서 테스트로 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-109">Q# supports creating unit tests for quantum programs, and which can run as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="b7e58-110">테스트 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="b7e58-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="b7e58-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="b7e58-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="b7e58-112">Visual Studio 2019를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="b7e58-113">**파일** 메뉴로 이동 하 여 **새로 만들기 > 프로젝트**...를 선택 합니다. 오른쪽 위 모서리에서를 검색 하 `Q#` 고 \*\* Q# 테스트 프로젝트\*\* 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-113">Go to the **File** menu and select **New > Project...**. In the upper right corner, search for `Q#`, and select the **Q# Test Project** template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="b7e58-114">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b7e58-114">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="b7e58-115">선호 하는 명령줄에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-115">From your favorite command line, run the following command:</span></span>
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="b7e58-116">새 프로젝트에는 `Tests.qs` 새 단위 테스트를 정의 하는 데 편리한 장소를 제공 하는 단일 파일이 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="b7e58-116">Your new project has a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="b7e58-117">처음에이 파일에는 `AllocateQubit` 새로 할당 된가 $ \ket $ 상태에 있는지 확인 하 {0} 고 메시지를 인쇄 하는 하나의 샘플 단위 테스트가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-117">Initially, this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="b7e58-118">Q#형식의 인수를 사용 하 고를 반환 하는 모든 작업 또는 함수는 `Unit` `Unit` 특성을 통해 단위 테스트로 표시 될 수 있습니다 `@Test("...")` .</span><span class="sxs-lookup"><span data-stu-id="b7e58-118">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="b7e58-119">이전 예제에서 해당 특성에 대 한 인수는 `"QuantumSimulator"` 테스트가 실행 되는 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-119">In the previous example, the argument to that attribute, `"QuantumSimulator"`, specifies the target on which the test runs.</span></span> <span data-ttu-id="b7e58-120">단일 테스트를 여러 대상에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-120">A single test can run on multiple targets.</span></span> <span data-ttu-id="b7e58-121">예를 들어 앞에 특성을 추가 `@Test("ResourcesEstimator")` `AllocateQubit` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-121">For example, add an attribute `@Test("ResourcesEstimator")` before `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="b7e58-122">파일을 저장 하 고 모든 테스트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-122">Save the file and run all tests.</span></span> <span data-ttu-id="b7e58-123">이제 두 단위 테스트가 있습니다. 하나는에서 실행 되 고 다른 하나 `AllocateQubit` `QuantumSimulator` 는에서 실행 됩니다 `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="b7e58-123">There should now be two unit tests, one where `AllocateQubit` runs on the `QuantumSimulator`, and one where it runs in the `ResourcesEstimator`.</span></span> 

<span data-ttu-id="b7e58-124">Q#컴파일러는 기본 제공 대상 `"QuantumSimulator"` , 및를 `"ToffoliSimulator"` `"ResourcesEstimator"` 단위 테스트의 유효한 실행 대상으로 인식 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-124">The Q# compiler recognizes the built-in targets `"QuantumSimulator"`, `"ToffoliSimulator"`, and `"ResourcesEstimator"` as valid execution targets for unit tests.</span></span> <span data-ttu-id="b7e58-125">또한 사용자 지정 실행 대상을 정의 하는 정규화 된 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-125">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-no-locq-unit-tests"></a><span data-ttu-id="b7e58-126">Q#단위 테스트 실행</span><span class="sxs-lookup"><span data-stu-id="b7e58-126">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="b7e58-127">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="b7e58-127">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="b7e58-128">솔루션 당 일회성 설치로 **테스트** 메뉴로 이동 하 여 **테스트 설정 > 기본 프로세서 아키텍처 > X64**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-128">As a one-time per-solution setup, go to the **Test** menu and select **Test Settings > Default Processor Architecture > X64**.</span></span>

> [!TIP]
> <span data-ttu-id="b7e58-129">Visual Studio의 기본 프로세서 아키텍처 설정은 `.suo` 각 솔루션에 대 한 솔루션 옵션 () 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-129">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="b7e58-130">이 파일을 삭제 하는 경우 프로세서 아키텍처로 **X64** 를 다시 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-130">If you delete this file, then you need to select **X64** as your processor architecture again.</span></span>

<span data-ttu-id="b7e58-131">프로젝트를 빌드하고 **테스트** 메뉴를 열고 **Windows > 테스트 탐색기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-131">Build the project, open the **Test** menu, and select **Windows > Test Explorer**.</span></span> <span data-ttu-id="b7e58-132">**Allocate bit** 는 테스트 **실행 안 함** 그룹의 테스트 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-132">**AllocateQubit** displays in the list of tests in the **Not Run Tests** group.</span></span> <span data-ttu-id="b7e58-133">**모두 실행** 을 선택 하거나이 개별 테스트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-133">Select **Run All** or run this individual test.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="b7e58-134">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b7e58-134">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="b7e58-135">테스트를 실행 하려면 프로젝트 폴더 (가 포함 된 폴더)로 이동 하 `Tests.csproj` 고 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-135">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and run the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="b7e58-136">다음과 유사한 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-136">You should get output similar to the following:</span></span>

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

<span data-ttu-id="b7e58-137">단위 테스트는 이름 또는 실행 대상에 따라 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-137">Unit tests can be filtered according to their name or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="b7e58-138">내장 함수에는 <xref:microsoft.quantum.intrinsic.message> 형식이 `(String -> Unit)` 있으며 진단 메시지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-138">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="b7e58-139">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="b7e58-139">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="b7e58-140">테스트 탐색기에서 테스트를 실행 하 고 테스트를 클릭 하면 테스트 실행에 대 한 정보 (통과/실패 상태, 경과 시간 및 출력에 대 한 링크)가 패널에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-140">After you run a test in Test Explorer and click on the test, a panel displays with information about test execution: Pass/fail status, elapsed time, and a link to the output.</span></span> <span data-ttu-id="b7e58-141">**출력** 을 클릭 하 여 새 창에서 테스트 출력을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-141">Click **Output** to open the test output in a new window.</span></span>

![테스트 출력](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="b7e58-143">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b7e58-143">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="b7e58-144">각 테스트에 대 한 통과/실패 상태는에 의해 콘솔에 출력 됩니다 `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="b7e58-144">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="b7e58-145">실패 한 테스트의 경우 출력은 오류를 진단 하는 데 도움이 되도록 콘솔에도 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-145">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="b7e58-146">팩트 및 어설션</span><span class="sxs-lookup"><span data-stu-id="b7e58-146">Facts and Assertions</span></span>

<span data-ttu-id="b7e58-147">의 함수에는 Q# _논리적인_ 부작용이 없기 때문에 프로그램 내에서 다른 종류의 영향을 볼 수 없습니다 Q# . 출력 형식이 빈 튜플이 있는 함수를 실행 하는 것 `()` 입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-147">Because functions in Q# have no _logical_ side effects, you can never observe, from within a Q# program, any other kinds of effects from running a function whose output type is the empty tuple `()`.</span></span>
<span data-ttu-id="b7e58-148">즉, 대상 컴퓨터에서 반환 하는 함수를 실행 하지 않도록 선택할 수 있습니다 `()` .이를 생략 하면 다음 코드의 동작이 수정 되지 않습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="b7e58-148">That is, a target machine can choose not to run any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="b7e58-149">이 동작은 `()` `Unit` 어설션 및 디버깅 논리를 프로그램에 포함 하는 데 유용한 도구인 (예:)를 반환 하는 함수를 만듭니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="b7e58-149">This behavior makes functions returning `()` (such as `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="b7e58-150">간단한 예제를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-150">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="b7e58-151">여기서 키워드는 `fail` 계산이 진행 되지 않아야 함을 나타내며 프로그램을 실행 하는 대상 컴퓨터에서 예외를 발생 시킵니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="b7e58-151">Here, the keyword `fail` indicates that the computation should not proceed, and raises an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="b7e58-152">정의에 따라 Q# 대상 컴퓨터에서 문을 실행 한 후 더 이상 코드를 실행 하지 않으므로에서 이러한 종류의 오류를 관찰할 수 없습니다 Q# `fail` .</span><span class="sxs-lookup"><span data-stu-id="b7e58-152">By definition, a failure of this kind cannot be observed from within Q#, as the target machine no longer runs the Q# code after reaching a `fail` statement.</span></span>
<span data-ttu-id="b7e58-153">따라서에 대 한 호출을 계속 진행 하는 경우 `PositivityFact` 해당 입력이 긍정적 임을 확신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-153">Thus, if we proceed past a call to `PositivityFact`, we can be assured that its input was positive.</span></span>

<span data-ttu-id="b7e58-154">`PositivityFact` [`Fact`](xref:microsoft.quantum.diagnostics.fact) 네임 스페이스에서 함수를 사용 하는 것과 동일한 동작을 구현할 수 있습니다 <xref:microsoft.quantum.diagnostics> .</span><span class="sxs-lookup"><span data-stu-id="b7e58-154">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="b7e58-155">반면에 *어설션은*팩트와 유사 하 게 사용 되지만 대상 컴퓨터의 상태에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-155">*Assertions*, on the other hand, are used similarly to facts but may depend on the state of the target machine.</span></span> <span data-ttu-id="b7e58-156">마찬가지로, 팩트는 작업으로 정의 되는 반면 팩트는 이전 예제와 같이 함수로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-156">Correspondingly, they are defined as operations, whereas facts are defined as functions (as in the previous example).</span></span>
<span data-ttu-id="b7e58-157">구분을 이해 하려면 어설션 내에서 다음과 같은 팩트를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-157">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="b7e58-158">여기에서 작업을 사용 하 여 <xref:microsoft.quantum.environment.getqubitsavailabletouse> 사용할 수 있는 값 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-158">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="b7e58-159">이는 프로그램의 전역 상태와 해당 실행 환경에 따라 달라 지므로의 정의 `AssertQubitsAreAvailable` 도 작업 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-159">As this depends on the global state of the program and its execution environment, our definition of `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="b7e58-160">그러나이 전역 상태를 사용 하 여 간단한 `Bool` 값을 함수에 대 한 입력으로 생성할 수 있습니다 `Fact` .</span><span class="sxs-lookup"><span data-stu-id="b7e58-160">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="b7e58-161">이러한 아이디어를 기반으로 하 [는 Prelude는](xref:microsoft.quantum.libraries.standard.prelude)두 가지 특히 유용한 어설션을 제공 <xref:microsoft.quantum.diagnostics.assertmeasurement> 하며 <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> 둘 다 작업으로 모델링 `()` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-161">[The prelude](xref:microsoft.quantum.libraries.standard.prelude), building on these ideas, offers two especially useful assertions, <xref:microsoft.quantum.diagnostics.assertmeasurement> and <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> both modeled as operations onto `()`.</span></span> <span data-ttu-id="b7e58-162">이러한 어설션은 각각 특정 측정값을 설명 하는 Pauli 연산자, 측정을 수행 하는 퀀텀 레지스터 및 가상 결과를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-162">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="b7e58-163">시뮬레이션에서 작업 하는 대상 컴퓨터는 [복제 안 함 정리](https://en.wikipedia.org/wiki/No-cloning_theorem)에 바인딩되지 않으며 이러한 어설션에 전달 되는 레지스터를 방해 하지 않고 이러한 측정값을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-163">Target machines which work by simulation are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register that passes to such assertions.</span></span>
<span data-ttu-id="b7e58-164">그러면 시뮬레이터는 `PositivityFact` 앞서 설명한 함수와 비슷하며 가상 결과가 실제로 관찰 되지 않는 경우 계산을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-164">A simulator can then, similar to the `PositivityFact` function previous, stop computation if the hypothetical outcome is not observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    AssertMeasurement([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="b7e58-165">복제 안 함 정리에서 퀀텀 상태를 검사 하지 못하게 하는 실제 퀀텀 하드웨어에서 `AssertMeasurement` 및 작업은 `AssertMeasurementProbability` `()` 다른 영향 없이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-165">On physical quantum hardware, where the no-cloning theorem prevents examination of a quantum state, the `AssertMeasurement` and `AssertMeasurementProbability` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="b7e58-166"><xref:microsoft.quantum.diagnostics>네임 스페이스는 `Assert` 더 많은 고급 조건을 확인할 수 있는 패밀리의 여러 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-166">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family, with which you can check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="b7e58-167">덤프 함수</span><span class="sxs-lookup"><span data-stu-id="b7e58-167">Dump Functions</span></span>

<span data-ttu-id="b7e58-168">퀀텀 프로그램의 문제를 해결 하기 위해 <xref:microsoft.quantum.diagnostics> 네임 스페이스는 대상 컴퓨터의 현재 상태 (및)를 파일에 덤프할 수 있는 두 가지 함수를 제공 합니다 <xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics.dumpregister> .</span><span class="sxs-lookup"><span data-stu-id="b7e58-168">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="b7e58-169">각각의 생성 된 출력은 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-169">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="b7e58-170">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="b7e58-170">DumpMachine</span></span>

<span data-ttu-id="b7e58-171">퀀텀 개발 키트의 일부분으로 배포 되는 전체 상태 퀀텀 시뮬레이터는 전체 퀀텀 시스템의 [wave 함수](https://en.wikipedia.org/wiki/Wave_function) 를 파일에 기록 하 고, 각 요소가 계산 기준 상태 $ \ket{n} $를 측정할 확률의 진폭을 나타냅니다. 여기서 $ \ket{n} = \ket{b_ {n-1} ... bits $ b_i $의 b_1b_0} $ \{ \} 입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-171">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="b7e58-172">예를 들어 두 개의 om비트가 할당 되 고 퀀텀 상태 $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} \ket 인 컴퓨터에서 {2} {10} \end{align} $ $ 호출은 <xref:microsoft.quantum.diagnostics.dumpmachine> 다음 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-172">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="b7e58-173">첫 번째 행은 중요 한 순서 대로 해당 하는의 id를 사용 하 여 주석을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-173">The first row provides a comment with the ids of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="b7e58-174">나머지 행은 데카르트 및 극좌표 형식의 기본 상태 vector $ \ket{n} $를 측정 하는 확률 진폭을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-174">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="b7e58-175">첫 번째 행에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-175">In detail for the first row:</span></span>

* <span data-ttu-id="b7e58-176">**`∣0❭:`** 이 행은 `0` 계산 기준 상태에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-176">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="b7e58-177">**`0.707107 +  0.000000 i`**: 데카르트 형식의 확률 진폭입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-177">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="b7e58-178">**` == `**: `equal` 부호는 두 동등한 표현을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-178">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="b7e58-179">**`**********  `**: 크기의 그래픽 표현으로,의 수는 `*` 이 상태 벡터를 측정할 확률에 비례 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-179">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="b7e58-180">**`[ 0.500000 ]`**: 크기의 숫자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-180">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="b7e58-181">**`    ---`**: 진폭의 단계를 그래픽으로 표현한 것입니다 (다음 출력 참조).</span><span class="sxs-lookup"><span data-stu-id="b7e58-181">**`    ---`**: A graphical representation of the amplitude's phase (see the following output).</span></span>
* <span data-ttu-id="b7e58-182">**`[ 0.0000 rad ]`**: 단계의 숫자 값 (라디안 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-182">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="b7e58-183">크기와 단계가 모두 그래픽 표현으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-183">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="b7e58-184">크기 표현은 간단 하 게 표시 됩니다. 막대를 표시 하 고 막대의 클수록 표시 되는 `*` 확률이 커집니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-184">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="b7e58-185">단계에서는 범위에 따라 각도를 나타내기 위해 다음 기호를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-185">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="b7e58-186">다음 예에서는 `DumpMachine` 몇 가지 일반적인 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-186">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="b7e58-187">이 경우의 id는 런타임에 할당 되며,이는 해당 비트를 할당 한 순서 또는 해당 위치에서의 위치에 따라 정렬 되지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-187">The id of a qubit is assigned at runtime and is not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="b7e58-188">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="b7e58-188">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="b7e58-189">코드에 중단점을 배치 하 고 다음과 같은 방법으로 Visual Studio에서 사용자 비트 id를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-189">You can locate a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Visual Studio에서 이상 비트 id 표시](~/media/qubit_id.png)
  >
  > <span data-ttu-id="b7e58-191">인덱스에 있는 이상 비트의 id는 id =이 고 인덱스의는 `0` `register2` `3` `1` id = `2` 입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-191">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="b7e58-192">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b7e58-192">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="b7e58-193">함수를 사용 하 여 <xref:microsoft.quantum.intrinsic.message> 다음과 같이 메시지에 다음과 같은 기능을 사용 하 여 원하는 비트 id를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-193">You can locate a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="b7e58-194">다음 출력이 생성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-194">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="b7e58-195">즉, 인덱스가 있는 이상 비트의 id는 id =이 고 인덱스의는 `0` `register2` `3` `1` id = `2` 입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-195">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="b7e58-196"><xref:microsoft.quantum.diagnostics.dumpmachine>는 네임 스페이스의 일부 이므로 <xref:microsoft.quantum.diagnostics> `open` 액세스 하려면 문을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-196">Since <xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, you must add an `open` statement to access it:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="b7e58-197">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="b7e58-197">DumpRegister</span></span>

<span data-ttu-id="b7e58-198"><xref:microsoft.quantum.diagnostics.dumpregister>는 해당 하는 것과 <xref:microsoft.quantum.diagnostics.dumpmachine> 관련 된 정보만으로 정보량의 배열을 사용 한다는 점을 제외 하 고와 유사 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-198"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except that it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="b7e58-199">와 마찬가지로 <xref:microsoft.quantum.diagnostics.dumpmachine> 에서 생성 되는 정보는 <xref:microsoft.quantum.diagnostics.dumpregister> 대상 컴퓨터에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-199">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="b7e58-200">전체 상태 퀀텀 시뮬레이터에 대해 wave 함수를 파일에 기록 합니다 .이 함수는와 동일한 형식으로 제공 된 해당 하는 것으로 생성 된 퀀텀 하위 시스템의 전역 단계까지 파일에 기록 합니다 <xref:microsoft.quantum.diagnostics.dumpmachine> .</span><span class="sxs-lookup"><span data-stu-id="b7e58-200">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="b7e58-201">예를 들어 두 개의 기능을 할당 하 고 퀀텀 상태 $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} \ket =-e ^ {로 컴퓨터를 다시 사용 합니다. {2} {10} -i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \frac \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ 호출은 <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[0]` 다음 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-201">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="b7e58-202">및를 호출 하면 <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[1]` 다음 출력이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-202">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="b7e58-203">일반적으로 다른 레지스터와 함께 사용 되는 레지스터의 상태는 순수 상태가 아닌 혼합 된 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-203">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="b7e58-204">이 경우는 <xref:microsoft.quantum.diagnostics.dumpregister> 다음 메시지를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-204">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="b7e58-205">다음 예제에서는 <xref:microsoft.quantum.diagnostics.dumpregister> 코드에서 및를 모두 사용할 수 있는 방법을 보여 줍니다 <xref:microsoft.quantum.diagnostics.dumpmachine> Q# .</span><span class="sxs-lookup"><span data-stu-id="b7e58-205">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="b7e58-206">디버깅</span><span class="sxs-lookup"><span data-stu-id="b7e58-206">Debugging</span></span>

<span data-ttu-id="b7e58-207">`Assert`및 `Dump` 함수 및 작업을 기반으로 하는는 Q# 표준 Visual Studio 디버깅 기능의 하위 집합을 지원 합니다. [줄 중단점 설정](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), F10 키를 [사용 하 여 코드 단계별](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)실행 및 [클래식 변수의 값 검사](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) 는 모두 시뮬레이터에서 코드를 실행 하는 동안 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-207">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger), and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="b7e58-208">Visual Studio Code 디버깅은 c #에서 제공 하는 c # For Visual Studio Code 확장에서 제공 하는 디버깅 기능을 활용 하 고 [최신 버전](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e58-208">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
