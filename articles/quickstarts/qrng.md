---
title: 양자 난수 생성기 만들기
description: 양자 난수 생성기를 만들어서 중첩 같은 기본적인 양자 개념을 보여주는 Q# 프로젝트를 빌드합니다.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 8fafbccfe2a94a824353221b5e7eb8bac16c42f2
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327359"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="eb585-103">자습서: Q\#에서 양자 난수 생성기 구현</span><span class="sxs-lookup"><span data-stu-id="eb585-103">Tutorial: Implement a Quantum Random Number Generator in Q\#</span></span>

<span data-ttu-id="eb585-104">Q#으로 양자 난수 생성기를 작성하는 간단한 양자 알고리즘 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="eb585-105">이 알고리즘은 양자 메커니즘의 특성을 활용하여 난수를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eb585-106">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="eb585-106">Prerequisites</span></span>

- <span data-ttu-id="eb585-107">Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)</span><span class="sxs-lookup"><span data-stu-id="eb585-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="eb585-108">[명령줄에서 Q#을 사용](xref:microsoft.quantum.install.standalone)하거나 [Python 호스트 프로그램](xref:microsoft.quantum.install.python) 또는 [C# 호스트 프로그램](xref:microsoft.quantum.install.cs)을 사용하여 Q# 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-108">Create a Q# project for either [using Q# from the command line](xref:microsoft.quantum.install.standalone), or with a [Python host program](xref:microsoft.quantum.install.python) or [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="write-a-q-operation"></a><span data-ttu-id="eb585-109">Q# 연산 작성</span><span class="sxs-lookup"><span data-stu-id="eb585-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="eb585-110">Q# 연산 코드</span><span class="sxs-lookup"><span data-stu-id="eb585-110">Q# operation code</span></span>

1. <span data-ttu-id="eb585-111">Program.qs 파일의 내용을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-111">Replace the contents of the Program.qs file with the following code:</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

<span data-ttu-id="eb585-112">[양자 컴퓨팅 이해](xref:microsoft.quantum.overview.understanding) 문서에서 설명한 대로 큐비트는 중첩될 수 있는 양자 정보의 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-112">As mentioned in our [Understanding quantum computing](xref:microsoft.quantum.overview.understanding) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="eb585-113">측정된 큐비트는 0 또는 1 중 하나만 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="eb585-114">하지만 실행 중인 동안 큐비트 상태는 측정값이 0 또는 1일 수 있는 확률을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="eb585-115">이 확률적 상태를 중첩이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="eb585-116">이 확률을 사용하여 난수를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="eb585-117">Q# 연산에서는 Q#의 기본 형식인 `Qubit` 데이터 형식을 도입합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="eb585-118">`Qubit`는 `using` 문으로만 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="eb585-119">할당되는 경우 큐비트는 항상 `Zero` 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="eb585-120">`H` 연산을 사용하여 `Qubit`를 중첩 상태로 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="eb585-121">큐비트를 측정하고 값을 읽으려면 `M` 내장 연산을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="eb585-122">`Qubit`를 중첩 상태로 전환하고 측정하면 코드가 호출될 때마다 다른 값이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span>

<span data-ttu-id="eb585-123">`Qubit`를 할당 취소하면 큐비트가 명시적으로 다시 `Zero` 상태로 설정되어야 합니다. 그렇지 않으면 시뮬레이터가 런타임 오류를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="eb585-124">이렇게 하는 쉬운 방법은 `Reset`을 호출하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="eb585-125">블로흐 구를 사용하여 코드 시각화</span><span class="sxs-lookup"><span data-stu-id="eb585-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="eb585-126">Bloch 구의 북극은 클래식 **0** 값을 나타내고, 남극은 클래식 **1** 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="eb585-127">모든 중첩은 구의 점으로 표현할 수 있습니다(화살표로 표시).</span><span class="sxs-lookup"><span data-stu-id="eb585-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="eb585-128">화살표의 끝부분이 극에 가까울수록 측정 시 큐비트가 해당 극에 할당된 클래식 값으로 축소될 확률이 높아집니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="eb585-129">예를 들어 아래쪽 빨간색 화살표로 표현되는 큐비트 상태는 측정될 경우 **0** 값을 제공할 확률이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

<span data-ttu-id="eb585-130">이 표현을 사용하여 코드가 하는 일을 시각화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="eb585-131">먼저 **0** 상태에서 시작된 큐비트로 시작하고, `H`를 적용하여 **0**과 **1**의 확률이 동일한 중첩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-131">First we start with a qubit initialized in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* <span data-ttu-id="eb585-132">그런 다음, 큐비트를 측정하고 출력을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

<span data-ttu-id="eb585-133">측정 결과는 완전히 임의적이므로 임의의 비트를 얻었습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="eb585-134">이 연산을 여러 번 호출하여 정수를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="eb585-135">예를 들어 이 연산을 세 번 호출하여 세 개의 임의 비트를 얻으면 임의의 3비트 숫자(즉, 0~7 사이의 임의 숫자)를 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>


## <a name="creating-a-complete-random-number-generator"></a><span data-ttu-id="eb585-136">완전한 난수 생성기 만들기</span><span class="sxs-lookup"><span data-stu-id="eb585-136">Creating a complete random number generator</span></span>

<span data-ttu-id="eb585-137">이제 임의 비트를 생성하는 Q# 연산 기능이 있으므로 이를 사용하여 완전한 양자 난수 생성기를 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator.</span></span> <span data-ttu-id="eb585-138">Q# 명령줄 애플리케이션을 사용하거나 호스트 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-138">We can use the Q# command line applications or use a host program.</span></span>



### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[<span data-ttu-id="eb585-139">Visual Studio 또는 Visual Studio Code를 사용한 Q# 명령줄 애플리케이션</span><span class="sxs-lookup"><span data-stu-id="eb585-139">Q# command line applications with Visual Studio or Visual Studio Code</span></span>](#tab/tabid-qsharp)

<span data-ttu-id="eb585-140">전체 Q# 명령줄 애플리케이션을 만들려면 다음 진입점을 Q# 프로그램에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-140">To create the full Q# command line application, add the following entry point to your Q# program:</span></span> 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

<span data-ttu-id="eb585-141">실행 파일은 프로젝트 구성 및 명령줄 옵션에 따라 시뮬레이터 또는 리소스 예측 도구에서 `@EntryPoint()` 특성으로 표시된 작업 또는 함수를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-141">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

<span data-ttu-id="eb585-142">Visual Studio에서 Ctrl + F5 키를 눌러 스크립트를 실행하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-142">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="eb585-143">VS Code에서 터미널에 아래를 입력하여 Program.qs를 처음으로 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-143">In VS Code, build the Program.qs the first time by typing the below in the terminal:</span></span>

```dotnetcli
dotnet build
```

<span data-ttu-id="eb585-144">후속 실행 시, 다시 빌드할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-144">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="eb585-145">실행하려면 다음 명령을 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-145">To run it, type the following command and press enter:</span></span>

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="eb585-146">Visual Studio 코드 또는 명령줄을 사용하는 Python</span><span class="sxs-lookup"><span data-stu-id="eb585-146">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

<span data-ttu-id="eb585-147">Python에서 새 Q# 프로그램을 실행하려면 다음 코드를 `host.py`로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-147">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

<span data-ttu-id="eb585-148">그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-148">You can then run your Python host program from the command line:</span></span>

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[<span data-ttu-id="eb585-149">Visual Studio Code 또는 Visual Studio를 사용한 C#</span><span class="sxs-lookup"><span data-stu-id="eb585-149">C# with Visual Studio Code or Visual Studio</span></span>](#tab/tabid-csharp)

<span data-ttu-id="eb585-150">C#에서 새 Q# 프로그램을 실행하려면 다음 C# 코드를 포함하도록 `Driver.cs`를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eb585-150">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

<span data-ttu-id="eb585-151">그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다(Visual Studio에서는 F5를 눌러야 함).</span><span class="sxs-lookup"><span data-stu-id="eb585-151">You can then run your C# host program from the command line (in Visual Studio you should press F5):</span></span>

```bash
$ dotnet run
The random number generated is 42
```

***
