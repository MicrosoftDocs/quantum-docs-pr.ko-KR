---
title: Q#을 사용한 얽힘 살펴보기
description: Q#에서 양자 프로그램을 작성하는 방법을 알아봅니다. QDK(Quantum Development Kit)를 사용하여 Bell State 애플리케이션을 개발합니다.
author: natke
ms.author: nakersha
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 989080e7d9979bb87d14b2580d28732bb1092eb1
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327376"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="91070-104">자습서: Q\#을 사용한 얽힘 살펴보기</span><span class="sxs-lookup"><span data-stu-id="91070-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="91070-105">이 자습서에서는 큐비트를 조작 및 측정하고 중첩과 얽힘의 효과를 시연하는 Q# 프로그램을 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91070-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>
<span data-ttu-id="91070-106">QDK를 설치하고, 프로그램을 빌드하여 양자 시뮬레이터에서 실행하는 방법을 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-106">This guides you on installing the QDK, building the program and executing that program on a quantum simulator.</span></span>  

<span data-ttu-id="91070-107">양자 얽힘을 보여주는 벨이라는 애플리케이션을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-107">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="91070-108">벨이라는 이름은 가장 간단한 중첩과 양자 얽힘의 예를 표현하는 데 사용되는 두 큐비트의 특정 양자 상태를 의미하는 벨 상태에서 따온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-108">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="91070-109">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="91070-109">Pre-requisites</span></span>

<span data-ttu-id="91070-110">코딩을 시작할 준비가 되면 계속하기 전에 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-110">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="91070-111">[Python](xref:microsoft.quantum.install.python) 또는 [.NET](xref:microsoft.quantum.install.cs)용 Quantum Development Kit를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-111">Install the Quantum Development Kit for [Python](xref:microsoft.quantum.install.python) or [.NET](xref:microsoft.quantum.install.cs).</span></span>
* <span data-ttu-id="91070-112">QDK가 이미 설치되어 있는 경우 최신 버전으로 [업데이트](xref:microsoft.quantum.update)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-112">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="91070-113">QDK를 설치하지 않고 설명에 따라 Q# 프로그래밍 언어와 양자 컴퓨팅의 첫 번째 개념을 검토할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-113">You can also follow along with the narrative without installing the QDK, reviewing the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="demonstrating-qubit-behavior-with-q"></a><span data-ttu-id="91070-114">Q#에서 큐비트 동작 시연</span><span class="sxs-lookup"><span data-stu-id="91070-114">Demonstrating qubit behavior with Q#</span></span>

<span data-ttu-id="91070-115">간단한 [큐비트 정의](xref:microsoft.quantum.overview.understanding)를 떠올려 보세요.</span><span class="sxs-lookup"><span data-stu-id="91070-115">Recall our simple [definition of a qubit](xref:microsoft.quantum.overview.understanding).</span></span>  <span data-ttu-id="91070-116">클래식 비트는 0 또는 1 같은 단일 이진 값을 보유하는 반면, [큐비](xref:microsoft.quantum.glossary#qubit) 상태는 0과 1의 **중첩**에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-116">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="91070-117">개념적으로 큐비트는 공간의 방향(벡터라고도 함)이라고 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-117">Conceptually, a qubit can be thought of as a direction in space (also known as a vector).</span></span>  <span data-ttu-id="91070-118">가능한 모든 방향은 큐비트가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-118">A qubit can be in any of the possible directions.</span></span> <span data-ttu-id="91070-119">두 **클래식 상태**는 두 방향입니다. 즉, 0을 측정할 확률이 100%이고, 1을 측정할 확률이 100%입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-119">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>  <span data-ttu-id="91070-120">또한 이 표현은 [블로흐 구](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)를 통해 보다 형식적으로 시각화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-120">This representation is also more formally visualized by the [bloch sphere](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>

<span data-ttu-id="91070-121">측정 작업은 이진 결과를 생성하고 큐비트 상태를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-121">The act of measurement produces a binary result and changes a qubit state.</span></span> <span data-ttu-id="91070-122">측정은 이진 값(0 또는 1)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-122">Measurement produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="91070-123">큐비트는 중첩(모든 방향)에서 클래식 상태 중 하나로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-123">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="91070-124">그 후 개입 작업 없이 동일한 측정을 반복하여 동일한 이진 결과를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-124">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="91070-125">여러 큐비트가 서로 [**얽힐**](xref:microsoft.quantum.glossary#entanglement) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-125">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span> <span data-ttu-id="91070-126">얽힌 큐비트 하나를 측정하면 다른 큐비트의 상태 정보도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-126">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="91070-127">이제 Q#에서 이 동작을 어떻게 표현하는지 시연할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-127">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="91070-128">가능한 가장 간단한 프로그램으로 시작하여 양자 중첩 및 양자 얽힘을 보여주는 프로그램을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-128">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="setup"></a><span data-ttu-id="91070-129">설치 프로그램</span><span class="sxs-lookup"><span data-stu-id="91070-129">Setup</span></span>

<span data-ttu-id="91070-130">이 자습서에서는 호스트 프로그램을 사용하며 다음과 같은 두 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-130">This tutorial uses a host programs and consists of two parts:</span></span>

1. <span data-ttu-id="91070-131">Q# 양자 프로그래밍 언어를 사용하여 구현된 일련의 양자 알고리즘.</span><span class="sxs-lookup"><span data-stu-id="91070-131">A series of quantum algorithms, implemented using the Q# quantum programming language.</span></span>
1. <span data-ttu-id="91070-132">Python 또는 C#에서 구현되어 주 진입점 역할을 수행하고 Q# 연산을 호출하여 양자 알고리즘을 실행하는 호스트 프로그램.</span><span class="sxs-lookup"><span data-stu-id="91070-132">A host program, implemented in either Python or C#, that serves as the main entry point and invokes Q# operations to execute the quantum algorithms.</span></span>

#### <a name="python"></a>[<span data-ttu-id="91070-133">Python</span><span class="sxs-lookup"><span data-stu-id="91070-133">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="91070-134">애플리케이션의 위치 선택</span><span class="sxs-lookup"><span data-stu-id="91070-134">Choose a location for your application</span></span>

1. <span data-ttu-id="91070-135">`Bell.qs`라는 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91070-135">Create a file called `Bell.qs`.</span></span> <span data-ttu-id="91070-136">이 파일에는 Q# 코드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-136">This file will contain your Q# code.</span></span>

1. <span data-ttu-id="91070-137">`host.py`라는 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91070-137">Create a file called `host.py`.</span></span> <span data-ttu-id="91070-138">이 파일에는 Python 호스트 코드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-138">This file will contain your Python host code.</span></span>

#### <a name="c-command-line"></a>[<span data-ttu-id="91070-139">C# 명령줄</span><span class="sxs-lookup"><span data-stu-id="91070-139">C# Command Line</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="91070-140">새 Q# 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91070-140">Create a new Q# project:</span></span>

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    <span data-ttu-id="91070-141">`.csproj` 파일, Q# 파일(`Operations.qs`) 및 호스트 프로그램 파일(`Driver.cs`)이 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-141">You should see a `.csproj` file, a Q# file called `Operations.qs`, and a host program file called `Driver.cs`</span></span>

1. <span data-ttu-id="91070-142">Q# 파일 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="91070-142">Rename the Q# file</span></span>

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[<span data-ttu-id="91070-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="91070-143">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="91070-144">새 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="91070-144">Create a new project</span></span>

   * <span data-ttu-id="91070-145">Visual Studio 열기</span><span class="sxs-lookup"><span data-stu-id="91070-145">Open Visual Studio</span></span>
   * <span data-ttu-id="91070-146">**파일** 메뉴로 이동하여 **새로 만들기** -> **프로젝트...** 를 차례로 선택</span><span class="sxs-lookup"><span data-stu-id="91070-146">Go to the **File** menu and select **New** -> **Project...**</span></span>
   * <span data-ttu-id="91070-147">프로젝트 템플릿 탐색기에서 검색 필드에 `Q#`을 입력하고 `Q# Application` 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-147">In the project template explorer, type `Q#` into the search field and select the `Q# Application` template</span></span>
   * <span data-ttu-id="91070-148">프로젝트 이름을 `Bell`로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="91070-148">Give your project the name `Bell`</span></span>

1. <span data-ttu-id="91070-149">Q# 파일 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="91070-149">Rename the Q# file</span></span>

   * <span data-ttu-id="91070-150">**솔루션 탐색기**로 이동</span><span class="sxs-lookup"><span data-stu-id="91070-150">Navigate to the **Solution Explorer**</span></span>
   * <span data-ttu-id="91070-151">마우스 오른쪽 단추로 `Operations.qs` 파일 클릭</span><span class="sxs-lookup"><span data-stu-id="91070-151">Right click on the `Operations.qs` file</span></span>
   * <span data-ttu-id="91070-152">이름을 `Bell.qs`로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="91070-152">Rename it to `Bell.qs`</span></span>

* * *

## <a name="write-a-q-operation"></a><span data-ttu-id="91070-153">Q# 연산 작성</span><span class="sxs-lookup"><span data-stu-id="91070-153">Write a Q# operation</span></span>

<span data-ttu-id="91070-154">특정 양자 상태에 있는 두 큐비트를 준비하고, Q#에서 두 큐비트의 상태를 변경하는 작업을 수행하고 중첩 및 얽힘의 효과를 보여주는 것이 우리의 목표입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-154">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="91070-155">큐비트 상태, 작업 및 측정을 보여주는 연산을 하나씩 작성하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-155">We will build this up piece by piece to demonstrate qubit states, operations, and measurement.</span></span>

<span data-ttu-id="91070-156">**개요:**  아래의 첫 번째 코드에서는 Q#에서 큐비트를 작업하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="91070-156">**Overview:**  In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="91070-157">큐비트 상태를 변환하는 `M` 및 `X` 연산을 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-157">We’ll introduce two operations, `M` and `X` that transform the state of a qubit.</span></span> 

<span data-ttu-id="91070-158">이 코드 조각에서 `Set` 연산은 큐비트를 매개 변수로 사용하고 또 다른 매개 변수 `desired`를 사용하여 우리가 원하는 큐비트 상태를 나타내는 것으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-158">In this code snippet, an operation `Set` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="91070-159">`Set` 연산은 `M` 연산을 사용하여 큐비트를 측정합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-159">The operation `Set` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="91070-160">Q#에서 큐비트 측정은 항상 `Zero` 또는 `One`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-160">In Q#, a qubit measurement always returns either  `Zero` or `One`.</span></span>  <span data-ttu-id="91070-161">측정에서 반환된 값이 원하는 값과 일치하지 않으면 Set는 큐비트를 "대칭 이동"합니다. 즉, 큐비트 상태를 새로운 상태로 변경하는 `X` 연산을 실행합니다. 이 상태에서는 `Zero` 및 `One`을 반환하는 측정 확률이 반대입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-161">If the measurement returns a value not equal to a desired value, Set “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span>  <span data-ttu-id="91070-162">`Set` 연산의 효과를 보여주기 위해 `TestBellState` 연산이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-162">To demonstrate the effect of the `Set` operation, a `TestBellState` operation is then added.</span></span>  <span data-ttu-id="91070-163">이 연산은 `Zero` 또는 `One`을 입력으로 취하며, 이 입력을 사용하여 `Set` 연산을 몇 차례 호출하고, 큐비트 측정에서 `Zero`가 반환된 횟수와 `One`이 반환된 횟수를 집계합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-163">This operation takes as input a `Zero` or `One`, and calls the `Set` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="91070-164">물론 `TestBellState` 연산의 첫 번째 시뮬레이션 출력에서는 `Zero`를 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `Zero`를 반환하고, `One`을 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `One`을 반환할 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-164">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span>  <span data-ttu-id="91070-165">또한 중첩 및 얽힘을 보여주는 코드를 `TestBellState`에 추가할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-165">Further on, we’ll add code to `TestBellState` to demonstrating superposition and entanglement.</span></span>


### <a name="q-operation-code"></a><span data-ttu-id="91070-166">Q# 연산 코드</span><span class="sxs-lookup"><span data-stu-id="91070-166">Q# operation code</span></span>

1. <span data-ttu-id="91070-167">Bell.qs 파일의 내용을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="91070-167">Replace the contents of the Bell.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    <span data-ttu-id="91070-168">이제 이 연산을 호출하여 큐비트를 클래식 상태로 설정하면 항상 `Zero`를 반환하거나 항상 `One`을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-168">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>  <span data-ttu-id="91070-169">`Zero` 및 `One`은 큐비트 측정에서 가능한 두 가지 결과를 나타내는 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-169">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

    <span data-ttu-id="91070-170">`Set` 연산은 큐비트를 측정합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-170">The operation `Set` measures the qubit.</span></span>
    <span data-ttu-id="91070-171">큐비트가 현재 우리가 원하는 상태이면 `Set`는 큐비트를 그대로 둡니다. 그렇지 않으면 `X` 연산을 실행하여 큐비트를 원하는 상태로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-171">If the qubit is in the state we want, `Set` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

### <a name="about-q-operations"></a><span data-ttu-id="91070-172">Q# 연산 정보</span><span class="sxs-lookup"><span data-stu-id="91070-172">About Q# operations</span></span>

<span data-ttu-id="91070-173">Q# 연산은 양자 서브루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-173">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="91070-174">즉, 양자 연산을 포함하는 호출 가능 루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-174">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="91070-175">연산에 대한 인수는 괄호로 묶인 튜플로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-175">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="91070-176">연산의 반환 형식은 콜론 뒤에 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-176">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="91070-177">이 경우 `Set` 연산에는 반환이 없으므로 `Unit`를 반환하는 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-177">In this case, the `Set` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="91070-178">이는 F#의 `unit`와 동일한 Q#이며, C#의 `void` 및 Python의 빈 튜플(`Tuple[()]`)과 거의 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-178">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="91070-179">첫 번째 Q# 연산에서는 다음과 같은 두 개의 양자 연산을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-179">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="91070-180">[M](xref:microsoft.quantum.intrinsic.m) 연산 - 큐비트의 상태를 측정합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-180">The [M](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="91070-181">[X](xref:microsoft.quantum.intrinsic.x) 연산 - 큐비트의 상태를 대칭 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-181">The [X](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="91070-182">양자 연산은 큐비트의 상태를 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-182">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="91070-183">가끔 사람들은 클래식 논리 게이트와 비슷하게, 연산 대신 양자 게이트에 대해 이야기합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-183">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="91070-184">그 기원은 알고리즘이 이론적 아이디어에 불과했고 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되던 양자 컴퓨팅 초기 시대입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-184">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="add-q-test-code"></a><span data-ttu-id="91070-185">Q# 테스트 코드 추가</span><span class="sxs-lookup"><span data-stu-id="91070-185">Add Q# test code</span></span>

1. <span data-ttu-id="91070-186">`Set` 연산이 끝난 후 다음 연산을 네임스페이스 내의 `Bell.qs` 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-186">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `Set` operation:</span></span>

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    <span data-ttu-id="91070-187">이 연산(`TestBellState`)은 `count` 반복에 대해 루프를 실행하고, 큐비트에 지정된 `initial` 값을 설정한 다음, 결과를 측정합니다(`M`).</span><span class="sxs-lookup"><span data-stu-id="91070-187">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="91070-188">측정한 0과 1의 개수에 대한 통계를 수집하여 호출자에게 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-188">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="91070-189">다른 필요한 연산을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-189">It performs one other necessary operation.</span></span> <span data-ttu-id="91070-190">다른 사용자가 알려진 상태에서 이 큐비트를 할당할 수 있도록 반환하기 전에 해당 큐비트를 알려진 상태(`Zero`)로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-190">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="91070-191">이는 `using` 문에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-191">This is required by the `using` statement.</span></span>

### <a name="about-variables-in-q"></a><span data-ttu-id="91070-192">Q#의 변수 정보</span><span class="sxs-lookup"><span data-stu-id="91070-192">About variables in Q#</span></span>

<span data-ttu-id="91070-193">기본적으로 Q#의 변수는 변경할 수 없습니다. 바인딩된 후에는 해당 값이 변경되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-193">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="91070-194">`let` 키워드는 변경할 수 없는 변수의 바인딩을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-194">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="91070-195">연산 인수는 항상 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-195">Operation arguments are always immutable.</span></span>

<span data-ttu-id="91070-196">예제의 `numOnes`와 같이 값이 변경될 수 있는 변수가 필요한 경우 `mutable` 키워드를 사용하여 해당 변수를 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-196">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="91070-197">변경할 수 있는 변수의 값은 `set` 문을 사용하여 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-197">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="91070-198">두 경우 모두에서 변수 형식은 컴파일러를 통해 유추됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-198">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="91070-199">Q#에는 변수에 대한 형식 주석이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-199">Q# doesn't require any type annotations for variables.</span></span>

### <a name="about-using-statements-in-q"></a><span data-ttu-id="91070-200">Q#의 `using` 문 정보</span><span class="sxs-lookup"><span data-stu-id="91070-200">About `using` statements in Q#</span></span>

<span data-ttu-id="91070-201">`using` 문은 Q#에서도 특수합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-201">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="91070-202">코드 블록에서 사용할 큐비트를 할당하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-202">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="91070-203">Q#에서는 복잡한 알고리즘의 전체 수명 동안 유지되는 고정 리소스가 아니라 모든 큐비트가 동적으로 할당되고 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-203">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="91070-204">`using` 문은 시작 부분에서 큐비트 세트를 할당하고, 블록의 끝에서 해당 큐비트를 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-204">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="create-the-host-application-code"></a><span data-ttu-id="91070-205">호스트 애플리케이션 코드 만들기</span><span class="sxs-lookup"><span data-stu-id="91070-205">Create the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="91070-206">Python</span><span class="sxs-lookup"><span data-stu-id="91070-206">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="91070-207">`host.py` 파일을 열고 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-207">Open the `host.py` file and add the following code:</span></span>

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[<span data-ttu-id="91070-208">C#</span><span class="sxs-lookup"><span data-stu-id="91070-208">C#</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="91070-209">`Driver.cs` 파일의 내용을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="91070-209">Replace the contents of the `Driver.cs` file with the following code:</span></span>

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a><span data-ttu-id="91070-210">호스트 애플리케이션 코드 정보</span><span class="sxs-lookup"><span data-stu-id="91070-210">About the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="91070-211">Python</span><span class="sxs-lookup"><span data-stu-id="91070-211">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="91070-212">Python 호스트 애플리케이션은 다음 세 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-212">The Python host application has three parts:</span></span>

* <span data-ttu-id="91070-213">양자 알고리즘에 필요한 인수를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-213">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="91070-214">이 예제에서 `count`는 1,000으로 고정되고, `initial`은 큐비트의 초기 값입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-214">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="91070-215">가져온 Q# 연산의 `simulate()` 메서드를 호출하여 양자 알고리즘을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-215">Run the quantum algorithm by calling the `simulate()` method of the imported Q# operation.</span></span>
* <span data-ttu-id="91070-216">연산의 결과를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-216">Process the result of the operation.</span></span> <span data-ttu-id="91070-217">이 예제에서 `res`는 연산 결과를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-217">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="91070-218">여기서 결과는 시뮬레이터에서 측정한 0(`num_zeros`)의 수와 1(`num_ones`)의 수에 대한 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-218">Here the result is a tuple of the number of zeros (`num_zeros`) and number of ones (`num_ones`) measured by the simulator.</span></span> <span data-ttu-id="91070-219">튜플을 분해하여 두 개의 필드를 가져오고, 결과를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-219">We deconstruct the tuple to get the two fields, and print the results.</span></span>

#### <a name="c"></a>[<span data-ttu-id="91070-220">C#</span><span class="sxs-lookup"><span data-stu-id="91070-220">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="91070-221">C# 호스트 애플리케이션은 다음 네 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-221">The C# host application has four parts:</span></span>

* <span data-ttu-id="91070-222">양자 시뮬레이터를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-222">Construct a quantum simulator.</span></span> <span data-ttu-id="91070-223">이 예제에서 `qsim`은 시뮬레이터입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-223">In the example, `qsim` is the simulator.</span></span>
* <span data-ttu-id="91070-224">양자 알고리즘에 필요한 인수를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-224">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="91070-225">이 예제에서 `count`는 1,000으로 고정되고, `initial`은 큐비트의 초기 값입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-225">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="91070-226">양자 알고리즘을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-226">Run the quantum algorithm.</span></span> <span data-ttu-id="91070-227">각 Q# 연산은 동일한 이름의 C# 클래스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-227">Each Q# operation generates a C# class with the same name.</span></span> <span data-ttu-id="91070-228">이 클래스에는 **비동기적으로** 연산을 실행하는 `Run` 메서드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-228">This class has a `Run` method that **asynchronously** executes the operation.</span></span> <span data-ttu-id="91070-229">실제 하드웨어에서 비동기적으로 실행되므로 실행이 비동기적입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-229">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> <span data-ttu-id="91070-230">`Run` 메서드는 비동기적이므로 `Result` 속성을 가져옵니다. 이 속성은 작업이 완료될 때까지 실행을 차단하고 결과를 동기적으로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-230">Because the `Run` method is asynchronous, we fetch the `Result` property; this blocks execution until the task completes and returns the result synchronously.</span></span>
* <span data-ttu-id="91070-231">연산의 결과를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-231">Process the result of the operation.</span></span> <span data-ttu-id="91070-232">이 예제에서 `res`는 연산 결과를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-232">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="91070-233">여기서 결과는 시뮬레이터에서 측정한 0(`numZeros`)의 수와 1(`numOnes`)의 수에 대한 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-233">Here the result is a tuple of the number of zeros (`numZeros`) and number of ones (`numOnes`) measured by the simulator.</span></span> <span data-ttu-id="91070-234">이는 C#에서 ValueTuple로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-234">This is returned as a ValueTuple in C#.</span></span> <span data-ttu-id="91070-235">튜플을 분해하여 두 개의 필드를 가져오고, 결과를 출력하고, 키 누름을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="91070-235">We deconstruct the tuple to get the two fields, print the results, and wait for a keypress.</span></span>

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a><span data-ttu-id="91070-236">빌드 및 실행</span><span class="sxs-lookup"><span data-stu-id="91070-236">Build and run</span></span>

#### <a name="python"></a>[<span data-ttu-id="91070-237">Python</span><span class="sxs-lookup"><span data-stu-id="91070-237">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="91070-238">터미널에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-238">Run the following command at your terminal:</span></span>

    ```
    python host.py
    ```

    <span data-ttu-id="91070-239">이 명령은 Q# 연산을 시뮬레이션하는 호스트 애플리케이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-239">This command runs the host application, which simulates the Q# operation.</span></span>

<span data-ttu-id="91070-240">결과는 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-240">The results should be:</span></span>

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="91070-241">명령줄/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="91070-241">Command Line / Visual Studio Code</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="91070-242">터미널에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-242">Run the following at your terminal:</span></span>

    ```bash
    dotnet run
    ```

    <span data-ttu-id="91070-243">이 명령은 필요한 모든 패키지를 자동으로 다운로드하고, 애플리케이션을 빌드한 다음, 명령줄에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-243">This command will automatically download all required packages, build the application, then run it at the command line.</span></span>

1. <span data-ttu-id="91070-244">또는 **F1** 키를 눌러 명령 팔레트를 열고, **디버그: 디버깅하지 않고 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-244">Alternatively, press **F1** to open the Command Palette and select **Debug: Start Without Debugging.**</span></span>
<span data-ttu-id="91070-245">프로그램을 시작하는 방법을 설명하는 새 ``launch.json`` 파일을 만들라는 메시지가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-245">You may be prompted to create a new ``launch.json`` file describing how to start the program.</span></span>
<span data-ttu-id="91070-246">기본 ``launch.json``은 대부분의 애플리케이션에서 제대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-246">The default ``launch.json`` should work well for most applications.</span></span>

<span data-ttu-id="91070-247">결과는 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-247">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[<span data-ttu-id="91070-248">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="91070-248">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="91070-249">`F5` 키를 누르기만 하면 프로그램이 빌드되고 실행됩니다!</span><span class="sxs-lookup"><span data-stu-id="91070-249">Just hit `F5`, and your program should build and run!</span></span>

<span data-ttu-id="91070-250">결과는 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-250">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

<span data-ttu-id="91070-251">키를 누르면 프로그램이 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-251">The program will exit after you press a key.</span></span>

* * *

## <a name="prepare-superposition"></a><span data-ttu-id="91070-252">중첩 준비</span><span class="sxs-lookup"><span data-stu-id="91070-252">Prepare superposition</span></span>

<span data-ttu-id="91070-253">**개요** 이제 Q#에서 큐비트를 중첩된 것으로 표현하는 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-253">**Overview** Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="91070-254">앞에서 큐비트의 상태는 0과 1의 중첩일 수 있다고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-254">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="91070-255">`Hadamard` 연산을 사용하여 큐비트를 중첩하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-255">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="91070-256">큐비트가 두 클래식 상태 중 하나인 경우(즉, 측정에서 항상 `Zero`를 반환하거나 항상 `One`을 반환) `Hadamard` 또는 `H` 연산은 큐비트 측정 시 시간 중 50%는 `Zero`를 반환하고 시간 중 50%는 `One`을 반환하는 상태로 큐비트 상태를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-256">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="91070-257">개념적으로 큐비트는 `Zero`와 `One`의 중간으로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-257">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="91070-258">이제 `TestBellState` 연산을 시뮬레이션하면 측정 후 반환된 `Zero` 및 `One`의 수가 거의 동일한 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-258">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

<span data-ttu-id="91070-259">먼저 큐비트를 전환하겠습니다(큐비트가 `Zero` 상태이면 `One` 상태로 전환하고 그 반대의 경우도 마찬가지).</span><span class="sxs-lookup"><span data-stu-id="91070-259">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="91070-260">이 작업은 `X` 연산을 수행한 후 `TestBellState`에서 측정하는 순서로 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-260">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="91070-261">이제 `F5` 키를 누르면 결과가 되돌려집니다.</span><span class="sxs-lookup"><span data-stu-id="91070-261">Now the results (after pressing `F5`) are reversed:</span></span>

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

<span data-ttu-id="91070-262">그러나 지금까지 살펴본 모든 것은 클래식입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-262">However, everything we've seen so far is classical.</span></span> <span data-ttu-id="91070-263">양자 결과를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-263">Let's get a quantum result.</span></span> <span data-ttu-id="91070-264">이전 실행의 `X` 연산을 `H` 또는 Hadamard 연산으로 바꾸기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-264">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="91070-265">큐비트를 0에서 1까지 완전히 대칭 이동하는 대신, 절반만 대칭 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-265">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="91070-266">이제 `TestBellState`에서 대체된 줄은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-266">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="91070-267">이제 결과가 더 흥미로워집니다.</span><span class="sxs-lookup"><span data-stu-id="91070-267">Now the results get more interesting:</span></span>

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

<span data-ttu-id="91070-268">측정할 때마다 클래식 값을 요청하지만, 큐비트는 0에서 1 사이의 중간에 있으므로 통계적으로 0과 1을 절반씩 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91070-268">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span> <span data-ttu-id="91070-269">이를 __중첩__이라고 하며, 양자 상태에 대한 첫 번째 실제 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-269">This is known as __superposition__ and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="91070-270">얽힘 준비</span><span class="sxs-lookup"><span data-stu-id="91070-270">Prepare entanglement</span></span>

<span data-ttu-id="91070-271">**개요:**  이제 Q#에서 큐비트를 얽매는 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-271">**Overview:**  Now let’s look at how Q# expresses ways to entangle qubits.</span></span>  <span data-ttu-id="91070-272">먼저 첫 번째 큐비트를 초기 상태로 설정한 다음, `H` 연산을 사용하여 중첩 상태로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-272">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="91070-273">그리고 첫 번째 큐비트를 측정하기 전에, Controlled-Not을 나타내는 새로운 연산(`CNOT`)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-273">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-Not.</span></span>  <span data-ttu-id="91070-274">두 큐비트에 대해 이 연산을 실행하면 그 결과로 첫 번째 큐비트가 `One`인 경우 두 번째 큐비트가 대칭 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="91070-274">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="91070-275">이제 두 큐비트가 서로 얽혔습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-275">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="91070-276">첫 번째 큐비트에 대한 통계는 변경되지 않았지만(측정 후 `Zero` 또는 `One`일 확률이 50-50), 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-276">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="91070-277">`CNOT`는 두 큐비트를 얽어서 두 큐비트 중 한 큐비트에서 발생하는 모든 것이 다른 큐비트에서 발생하도록 했습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-277">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="91070-278">반대로 측정한 경우(먼저 두 번째 큐비트를 측정한 후에 첫 번째 큐비트를 측정함)에도 동일한 상황이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-278">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="91070-279">첫 번째 측정은 임의적이고, 두 번째 측정은 첫 번째 측정에서 발견된 모든 것과 함께 잠금 단계에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-279">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="91070-280">수행해야 할 첫 번째 작업은 `TestBellState`에서 1 대신 두 개의 큐비트를 할당하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-280">The first thing we'll need to do is allocate 2 qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="91070-281">이렇게 하면 `TestBellState`에서 측정(`M`)하기 전에 새 연산(`CNOT`)을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-281">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="91070-282">시작할 때 항상 `Zero` 상태에 있도록 첫 번째 큐비트를 초기화하는 다른 `Set` 연산을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-282">We've added another `Set` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="91070-283">또한 두 번째 큐비트를 해제하기 전에 다시 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-283">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

<span data-ttu-id="91070-284">이제 전체 루틴은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-284">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="91070-285">이 루틴을 실행하면 이전과 정확히 동일한 50-50의 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91070-285">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="91070-286">그러나 관심이 있는 것은 두 번째 큐비트가 측정되는 첫 번째 큐비트에 반응하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="91070-286">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="91070-287">새 버전의 `TestBellState` 연산을 사용하여 이 통계를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-287">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="91070-288">새 반환 값(`agree`)은 첫 번째 큐비트의 측정값이 두 번째 큐비트의 측정값과 일치할 때마다 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-288">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span> <span data-ttu-id="91070-289">또한 호스트 애플리케이션을 다음과 같이 적절히 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-289">We also have to update the host application accordingly:</span></span>

#### <a name="python"></a>[<span data-ttu-id="91070-290">Python</span><span class="sxs-lookup"><span data-stu-id="91070-290">Python</span></span>](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[<span data-ttu-id="91070-291">C#</span><span class="sxs-lookup"><span data-stu-id="91070-291">C#</span></span>](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

<span data-ttu-id="91070-292">이제 실행하는 경우 매우 놀라운 상황이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-292">Now when we run, we get something pretty amazing:</span></span>

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

<span data-ttu-id="91070-293">개요에서 설명했듯이, 첫 번째 큐비트에 대한 통계는 변경되지 않았지만(0 또는 1일 확률이 50-50), 이제 두 큐비트가 서로 얽혀 있으므로 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-293">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

<span data-ttu-id="91070-294">축하합니다. 첫 양자 프로그램을 작성했습니다!</span><span class="sxs-lookup"><span data-stu-id="91070-294">Congratulations, you've written your first quantum program!</span></span>

## <a name="next-steps"></a><span data-ttu-id="91070-295">다음 단계</span><span class="sxs-lookup"><span data-stu-id="91070-295">Next steps</span></span>

<span data-ttu-id="91070-296">[Grover의 검색](xref:microsoft.quantum.quickstarts.search) 자습서에서는 가장 인기 있는 양자 컴퓨팅 알고리즘 중 하나인 Grover 검색을 빌드하고 실행하는 방법을 보여 주고, 양자 컴퓨팅과 관련된 실제 문제를 해결하는 데 사용할 수 있는 Q# 프로그램의 좋은 예제를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="91070-296">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="91070-297">[Quantum Development Kit 시작](xref:microsoft.quantum.welcome)에서는 Q# 및 양자 프로그래밍을 배울 수 있는 더 많은 방법을 추천해줍니다.</span><span class="sxs-lookup"><span data-stu-id="91070-297">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
