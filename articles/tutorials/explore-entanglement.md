---
title: 되거나 얽 히를 사용 하 여 탐색Q#
description: 에서 퀀텀 프로그램을 작성 하는 방법에 대해 알아봅니다 Q# . QDK(Quantum Development Kit)를 사용하여 Bell State 애플리케이션을 개발합니다.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- Q#
- $$v
ms.openlocfilehash: c66d26b5ea253d6fc2633fbe52fa35ba703d185d
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869701"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="1b122-104">자습서: Q\#을 사용한 얽힘 살펴보기</span><span class="sxs-lookup"><span data-stu-id="1b122-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="1b122-105">이 자습서에서는 Q# 다양 한 비트를 조작 하 고 측정 하는 프로그램을 작성 하 고 superposition 및 되거나 얽 히의 효과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>

<span data-ttu-id="1b122-106">양자 얽힘을 보여주는 벨이라는 애플리케이션을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-106">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="1b122-107">벨이라는 이름은 가장 간단한 중첩과 양자 얽힘의 예를 표현하는 데 사용되는 두 큐비트의 특정 양자 상태를 의미하는 벨 상태에서 따온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-107">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="1b122-108">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="1b122-108">Pre-requisites</span></span>

<span data-ttu-id="1b122-109">코딩을 시작할 준비가 되면 계속하기 전에 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-109">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="1b122-110">원하는 언어 및 개발 환경을 사용 하 여 퀀텀 개발 키트를 [설치](xref:microsoft.quantum.install) 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-110">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your  preferred language and development environment.</span></span>
* <span data-ttu-id="1b122-111">QDK가 이미 설치되어 있는 경우 최신 버전으로 [업데이트](xref:microsoft.quantum.update)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-111">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="1b122-112">QDK를 설치 하지 않고도 설명을 따라 수행 하 고, Q# 프로그래밍 언어의 개요와 퀀텀 컴퓨팅의 첫 번째 개념을 검토할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-112">You can also follow along with the narrative without installing the QDK, reviewing  the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="1b122-113">이 자습서에서는 다음 작업을 수행하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-113">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="1b122-114">Q에서 작업 만들기 및 결합\#</span><span class="sxs-lookup"><span data-stu-id="1b122-114">Create and combine operations in Q\#</span></span>
> * <span data-ttu-id="1b122-115">Superposition, entangle에 원하는 비트를 배치 하 고 측정 하는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-115">Create operations to put qubits in superposition, entangle and measure them.</span></span>
> * <span data-ttu-id="1b122-116">시뮬레이터에서 프로그램이 실행 되는 퀀텀 되거나 얽 히을 보여 줍니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="1b122-116">Demonstrate quantum entanglement with a Q# program run in a simulator.</span></span> 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a><span data-ttu-id="1b122-117">QDK 동작 시연</span><span class="sxs-lookup"><span data-stu-id="1b122-117">Demonstrating qubit behavior with the QDK</span></span>

<span data-ttu-id="1b122-118">클래식 비트는 0 또는 1 같은 단일 이진 값을 보유하는 반면, [큐비](xref:microsoft.quantum.glossary#qubit) 상태는 0과 1의 **중첩**에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-118">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="1b122-119">개념적으로,의 상태는 추상 공간 (벡터가 라고도 함)의 방향으로 간주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-119">Conceptually, the state of a qubit can be thought of as a direction in an abstract space (also known as a vector).</span></span>  <span data-ttu-id="1b122-120">이 경우 가능한 모든 방향이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-120">A qubit state can be in any of the possible directions.</span></span> <span data-ttu-id="1b122-121">두 **클래식 상태**는 두 방향입니다. 즉, 0을 측정할 확률이 100%이고, 1을 측정할 확률이 100%입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-121">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>

<span data-ttu-id="1b122-122">측정 작업은 이진 결과를 생성하고 큐비트 상태를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-122">The act of measurement produces a binary result and changes a qubit state.</span></span>
<span data-ttu-id="1b122-123">측정은 0 또는 1의 이진 값을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-123">Measurement  produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="1b122-124">큐비트는 중첩(모든 방향)에서 클래식 상태 중 하나로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-124">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="1b122-125">그 후 개입 작업 없이 동일한 측정을 반복하여 동일한 이진 결과를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-125">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="1b122-126">여러 큐비트가 서로 [**얽힐**](xref:microsoft.quantum.glossary#entanglement) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-126">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span>  <span data-ttu-id="1b122-127">얽힌 큐비트 하나를 측정하면 다른 큐비트의 상태 정보도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-127">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="1b122-128">이제에서이 동작을 표현 하는 방법을 보여 드릴 준비가 되었습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="1b122-128">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="1b122-129">가능한 가장 간단한 프로그램으로 시작하여 양자 중첩 및 양자 얽힘을 보여주는 프로그램을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-129">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="creating-a-no-locq-project"></a><span data-ttu-id="1b122-130">프로젝트 만들기 Q#</span><span class="sxs-lookup"><span data-stu-id="1b122-130">Creating a Q# project</span></span>

<span data-ttu-id="1b122-131">가장 먼저 해야 할 일은 새 프로젝트를 만드는 것입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="1b122-131">The first thing we have to do is to create a new Q# project.</span></span> <span data-ttu-id="1b122-132">이 자습서에서는 [VS Code를 사용 하 여 명령줄 응용 프로그램](xref:microsoft.quantum.install.standalone)을 기반으로 환경을 사용할 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-132">In this tutorial we are going to use the environment based on [command line applications with VS Code](xref:microsoft.quantum.install.standalone).</span></span>

<span data-ttu-id="1b122-133">새 프로젝트를 만들려면 VS Code에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-133">To create a new project, in VS Code:</span></span> 

1. <span data-ttu-id="1b122-134">**보기**  ->  **명령 팔레트** 를 클릭 하 고 다음을 선택 하 여 \*\* Q# 새 프로젝트 만들기\*\*를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-134">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="1b122-135">**Standalone console application**(독립 실행형 콘솔 애플리케이션)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-135">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="1b122-136">프로젝트를 저장할 위치로 이동하여 **프로젝트 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-136">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="1b122-137">프로젝트가 만들어지면 오른쪽 아래에서 **Open new project...** (새 프로젝트 열기)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-137">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="1b122-138">이 경우 프로젝트를 호출 했습니다 `Bell` .</span><span class="sxs-lookup"><span data-stu-id="1b122-138">In this case we called the project `Bell`.</span></span> <span data-ttu-id="1b122-139">그러면 `Bell.csproj` `Program.qs` 응용 프로그램을 작성 하는 데 사용할 응용 프로그램의 템플릿인, 프로젝트 파일 및 라는 두 개의 파일이 생성 Q# 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-139">This generates two files: `Bell.csproj`, the project file and `Program.qs`, a template of a Q# application that we will use to write our application.</span></span> <span data-ttu-id="1b122-140">의 내용은 `Program.qs` 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-140">The content of `Program.qs` should be:</span></span>

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a><span data-ttu-id="1b122-141">Q \# 응용 프로그램 작성</span><span class="sxs-lookup"><span data-stu-id="1b122-141">Write the Q\# application</span></span>
 
<span data-ttu-id="1b122-142">Microsoft의 목표는 특정 퀀텀 상태에서 두 개의 작업을 준비 하는 것입니다 .를 사용 하 여이 작업을 수행 하 여 Q# 상태를 변경 하 고 superposition 및 되거나 얽 히의 효과를 보여 주는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-142">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="1b122-143">여기서는이를 구성 하 여 몇 비트 상태, 작업 및 측정을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-143">We will build this up piece by piece to introduce qubit states, operations, and measurement.</span></span>

### <a name="initialize-qubit-using-measurement"></a><span data-ttu-id="1b122-144">측정을 사용 하 여 비트를 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-144">Initialize qubit using measurement</span></span>

<span data-ttu-id="1b122-145">아래의 첫 번째 코드에서는에서 원하는 비트를 사용 하는 방법을 보여 줍니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="1b122-145">In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="1b122-146">여기서는 두 가지 작업을 소개 하 고,이를 통해 [`M`](xref:microsoft.quantum.intrinsic.m) [`X`](xref:microsoft.quantum.intrinsic.x) 원하는 비트의 상태를 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-146">We’ll introduce two operations, [`M`](xref:microsoft.quantum.intrinsic.m) and [`X`](xref:microsoft.quantum.intrinsic.x) that transform the state of a qubit.</span></span> <span data-ttu-id="1b122-147">이 코드 조각에서 `SetQubitState` 연산은 큐비트를 매개 변수로 사용하고 또 다른 매개 변수 `desired`를 사용하여 우리가 원하는 큐비트 상태를 나타내는 것으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-147">In this code snippet, an operation `SetQubitState` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="1b122-148">`SetQubitState` 연산은 `M` 연산을 사용하여 큐비트를 측정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-148">The operation `SetQubitState` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="1b122-149">에서 Q# ,의 비트 측정은 항상 또는를 반환 합니다 `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="1b122-149">In Q#, a qubit measurement always returns either `Zero` or `One`.</span></span>  <span data-ttu-id="1b122-150">측정값이 원하는 값과 일치 하지 않는 값을 반환 하는 경우에는 해당 값을 `SetQubitState` "대칭 이동" 합니다. 즉, 작업을 실행 합니다 .이 작업은 해당 값을 `X` 반환 하는 측정값의 확률을 반환 하는 새 상태로의 값을 변경 합니다 `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="1b122-150">If the measurement returns a value not equal to the desired value, `SetQubitState` “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span> <span data-ttu-id="1b122-151">이러한 방식으로 `SetQubitState` 는 항상 대상의를 원하는 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-151">This way, `SetQubitState` always puts the target qubit in the desired state.</span></span>

<span data-ttu-id="1b122-152">의 내용을 `Program.qs` 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-152">Replace the contents of `Program.qs` with the following code:</span></span>


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

<span data-ttu-id="1b122-153">이제 이 연산을 호출하여 큐비트를 클래식 상태로 설정하면 항상 `Zero`를 반환하거나 항상 `One`을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-153">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>
<span data-ttu-id="1b122-154">`Zero` 및 `One`은 큐비트 측정에서 가능한 두 가지 결과를 나타내는 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-154">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

<span data-ttu-id="1b122-155">`SetQubitState` 연산은 큐비트를 측정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-155">The operation `SetQubitState` measures the qubit.</span></span> <span data-ttu-id="1b122-156">큐비트가 현재 우리가 원하는 상태이면 `SetQubitState`는 큐비트를 그대로 둡니다. 그렇지 않으면 `X` 연산을 실행하여 큐비트를 원하는 상태로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-156">If the qubit is in the state we want, `SetQubitState` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

#### <a name="about-no-locq-operations"></a><span data-ttu-id="1b122-157">Q#작업 정보</span><span class="sxs-lookup"><span data-stu-id="1b122-157">About Q# operations</span></span>

<span data-ttu-id="1b122-158">Q#작업은 퀀텀 서브루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-158">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="1b122-159">즉, 다른 퀀텀 작업에 대 한 호출을 포함 하는 호출 가능 루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-159">That is, it is a callable routine that contains calls to other quantum operations.</span></span>

<span data-ttu-id="1b122-160">연산에 대한 인수는 괄호로 묶인 튜플로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-160">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="1b122-161">연산의 반환 형식은 콜론 뒤에 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-161">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="1b122-162">이 경우 `SetQubitState` 연산에는 반환이 없으므로 `Unit`를 반환하는 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-162">In this case, the `SetQubitState` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="1b122-163">이는 Q# `unit` c #의와 거의 유사한 F #의에 해당 `void` 하며 Python의 빈 튜플 ( `Tuple[()]` )입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-163">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="1b122-164">첫 번째 작업에서 두 개의 퀀텀 작업을 사용 했습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="1b122-164">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="1b122-165">[`M`](xref:microsoft.quantum.intrinsic.m)작업으로,이 작업은의 상태를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-165">The [`M`](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="1b122-166">[`X`](xref:microsoft.quantum.intrinsic.x)작업은이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-166">The [`X`](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="1b122-167">양자 연산은 큐비트의 상태를 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-167">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="1b122-168">가끔 사람들은 클래식 논리 게이트와 비슷하게, 연산 대신 양자 게이트에 대해 이야기합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-168">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="1b122-169">그 기원은 알고리즘이 이론적 아이디어에 불과했고 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되던 양자 컴퓨팅 초기 시대입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-169">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="counting-measurement-outcomes"></a><span data-ttu-id="1b122-170">측정 결과 계산</span><span class="sxs-lookup"><span data-stu-id="1b122-170">Counting measurement outcomes</span></span>

<span data-ttu-id="1b122-171">`SetQubitState` 연산의 효과를 보여주기 위해 `TestBellState` 연산이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-171">To demonstrate the effect of the `SetQubitState` operation, a `TestBellState` operation is then added.</span></span> <span data-ttu-id="1b122-172">이 연산은 `Zero` 또는 `One`을 입력으로 취하며, 이 입력을 사용하여 `SetQubitState` 연산을 몇 차례 호출하고, 큐비트 측정에서 `Zero`가 반환된 횟수와 `One`이 반환된 횟수를 집계합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-172">This operation takes as input a `Zero` or `One`, and calls the `SetQubitState` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="1b122-173">물론 `TestBellState` 연산의 첫 번째 시뮬레이션 출력에서는 `Zero`를 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `Zero`를 반환하고, `One`을 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `One`을 반환할 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-173">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span> <span data-ttu-id="1b122-174">또한에 코드를 추가 하 여 `TestBellState` superposition 및 되거나 얽 히를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-174">Further on, we’ll add code to `TestBellState` to demonstrate superposition and entanglement.</span></span>

<span data-ttu-id="1b122-175">`SetQubitState` 연산이 끝난 후 다음 연산을 네임스페이스 내의 `Bell.qs` 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-175">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `SetQubitState` operation:</span></span>

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
<span data-ttu-id="1b122-176">`return`() 함수 ()를 사용 하 여 콘솔에 설명 메시지를 인쇄 하기 위해 앞에 줄을 추가 했습니다 ( `Message` ).</span><span class="sxs-lookup"><span data-stu-id="1b122-176">Note that we added a line before the `return` to print an explanatory message in the console with the function (`Message`)[microsoft.quantum.intrinsic.message]</span></span>

<span data-ttu-id="1b122-177">이 연산(`TestBellState`)은 `count` 반복에 대해 루프를 실행하고, 큐비트에 지정된 `initial` 값을 설정한 다음, 결과를 측정합니다(`M`).</span><span class="sxs-lookup"><span data-stu-id="1b122-177">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="1b122-178">측정한 0과 1의 개수에 대한 통계를 수집하여 호출자에게 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-178">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="1b122-179">다른 필요한 연산을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-179">It performs one other necessary operation.</span></span> <span data-ttu-id="1b122-180">다른 사용자가 알려진 상태에서 이 큐비트를 할당할 수 있도록 반환하기 전에 해당 큐비트를 알려진 상태(`Zero`)로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-180">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="1b122-181">이는 `using` 문에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-181">This is required by the `using` statement.</span></span>

#### <a name="about-variables-in-q"></a><span data-ttu-id="1b122-182">Q의 변수 정보\#</span><span class="sxs-lookup"><span data-stu-id="1b122-182">About variables in Q\#</span></span>

<span data-ttu-id="1b122-183">기본적으로의 변수 Q# 는 변경할 수 없으며, 바인딩된 후에는 해당 값이 변경 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-183">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="1b122-184">`let` 키워드는 변경할 수 없는 변수의 바인딩을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-184">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="1b122-185">연산 인수는 항상 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-185">Operation arguments are always immutable.</span></span>

<span data-ttu-id="1b122-186">예제의 `numOnes`와 같이 값이 변경될 수 있는 변수가 필요한 경우 `mutable` 키워드를 사용하여 해당 변수를 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-186">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="1b122-187">변경할 수 있는 변수의 값은 `setQubitState` 문을 사용하여 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-187">A mutable variable's value may be changed using a `setQubitState` statement.</span></span>

<span data-ttu-id="1b122-188">두 경우 모두에서 변수 형식은 컴파일러를 통해 유추됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-188">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="1b122-189">Q#변수에는 형식 주석이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-189">Q# doesn't require any type annotations for variables.</span></span>

#### <a name="about-using-statements-in-q"></a><span data-ttu-id="1b122-190">`using`Q의 문 정보\#</span><span class="sxs-lookup"><span data-stu-id="1b122-190">About `using` statements in Q\#</span></span>

<span data-ttu-id="1b122-191">`using`문은에도 특수 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-191">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="1b122-192">코드 블록에서 사용할 큐비트를 할당하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-192">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="1b122-193">에서는 Q# 복잡 한 알고리즘의 전체 수명 동안 유지 되는 고정 리소스 대신 모든 모든 비트를 동적으로 할당 하 고 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-193">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="1b122-194">`using` 문은 시작 부분에서 큐비트 세트를 할당하고, 블록의 끝에서 해당 큐비트를 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-194">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="execute-the-code-from-the-command-line"></a><span data-ttu-id="1b122-195">명령줄에서 코드를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-195">Execute the code from the command line</span></span>

<span data-ttu-id="1b122-196">코드를 실행 하기 위해 명령을 제공할 때 실행할 수 *있는* 컴파일러를 지정 해야 합니다 `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="1b122-196">In order to run the code we need to specify the compiler *which* callable to run when we provide the `dotnet run` command.</span></span> <span data-ttu-id="1b122-197">이 Q# 작업은 호출 가능한 바로 앞에를 사용 하 여 줄을 추가 하 여 파일을 간단히 변경 하는 방식으로 수행 됩니다 `@EntryPoint()` `TestBellState` .이 경우에는 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-197">This is done with a simple change in the Q# file by adding a line with `@EntryPoint()` directly preceding the callable: the `TestBellState` operation in this case.</span></span> <span data-ttu-id="1b122-198">전체 코드는 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-198">The full code should be:</span></span>

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

<span data-ttu-id="1b122-199">프로그램을 실행 하려면 `count` 명령줄에서 및 인수를 지정 해야 `initial` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-199">To run the program we need to specify `count` and `initial` arguments from the command line.</span></span> <span data-ttu-id="1b122-200">예를 들어 및을 선택 하겠습니다 `count = 1000` `initial = One` .</span><span class="sxs-lookup"><span data-stu-id="1b122-200">Let's choose for example `count = 1000` and `initial = One`.</span></span> <span data-ttu-id="1b122-201">다음 명령을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-201">Enter the following command:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

<span data-ttu-id="1b122-202">다음 출력을 관찰 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-202">And you should observe the following output:</span></span>

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="1b122-203">로 시도 하 `initial = Zero` 는 경우 다음 사항을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-203">If you try with `initial = Zero` you should observe:</span></span>

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a><span data-ttu-id="1b122-204">중첩 준비</span><span class="sxs-lookup"><span data-stu-id="1b122-204">Prepare superposition</span></span>

<span data-ttu-id="1b122-205">이제를 사용 하 Q# 여 superposition에를 배치 하는 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-205">Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="1b122-206">앞에서 큐비트의 상태는 0과 1의 중첩일 수 있다고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-206">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="1b122-207">`Hadamard` 연산을 사용하여 큐비트를 중첩하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-207">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="1b122-208">큐비트가 두 클래식 상태 중 하나인 경우(즉, 측정에서 항상 `Zero`를 반환하거나 항상 `One`을 반환) `Hadamard` 또는 `H` 연산은 큐비트 측정 시 시간 중 50%는 `Zero`를 반환하고 시간 중 50%는 `One`을 반환하는 상태로 큐비트 상태를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-208">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="1b122-209">개념적으로 큐비트는 `Zero`와 `One`의 중간으로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-209">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="1b122-210">이제 `TestBellState` 연산을 시뮬레이션하면 측정 후 반환된 `Zero` 및 `One`의 수가 거의 동일한 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-210">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

### <a name="x-flips-qubit-state"></a><span data-ttu-id="1b122-211">`X`가는 비트 상태를 대칭 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-211">`X` flips qubit state</span></span>

<span data-ttu-id="1b122-212">먼저 큐비트를 전환하겠습니다(큐비트가 `Zero` 상태이면 `One` 상태로 전환하고 그 반대의 경우도 마찬가지).</span><span class="sxs-lookup"><span data-stu-id="1b122-212">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="1b122-213">이 작업은 `X` 연산을 수행한 후 `TestBellState`에서 측정하는 순서로 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-213">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="1b122-214">이제 결과가 반전 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-214">Now the results are reversed:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="1b122-215">이제는 이상 비트의 퀀텀 속성을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-215">Now let's explore the quantum properties of the qubits.</span></span>

### <a name="h-prepares-superposition"></a><span data-ttu-id="1b122-216">`H`superposition 준비</span><span class="sxs-lookup"><span data-stu-id="1b122-216">`H` prepares superposition</span></span>

<span data-ttu-id="1b122-217">이전 실행의 `X` 연산을 `H` 또는 Hadamard 연산으로 바꾸기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-217">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="1b122-218">큐비트를 0에서 1까지 완전히 대칭 이동하는 대신, 절반만 대칭 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-218">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="1b122-219">이제 `TestBellState`에서 대체된 줄은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-219">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="1b122-220">이제 결과가 더 흥미로워집니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-220">Now the results get more interesting:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

<span data-ttu-id="1b122-221">측정할 때마다 클래식 값을 요청하지만, 큐비트는 0에서 1 사이의 중간에 있으므로 통계적으로 0과 1을 절반씩 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-221">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span>
<span data-ttu-id="1b122-222">이를 **중첩**이라고 하며, 양자 상태에 대한 첫 번째 실제 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-222">This is known as **superposition** and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="1b122-223">얽힘 준비</span><span class="sxs-lookup"><span data-stu-id="1b122-223">Prepare entanglement</span></span>

<span data-ttu-id="1b122-224">이제를 entangle로 표시 하는 방법을 살펴보겠습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="1b122-224">Now let’s look at how Q# expresses ways to entangle qubits.</span></span>
<span data-ttu-id="1b122-225">먼저 첫 번째 큐비트를 초기 상태로 설정한 다음, `H` 연산을 사용하여 중첩 상태로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-225">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="1b122-226">그런 다음, 첫 번째 비트를 측정 하기 전에 제어 되지 않음을 나타내는 새 작업 ()을 사용 `CNOT` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-226">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-NOT.</span></span>  <span data-ttu-id="1b122-227">두 큐비트에 대해 이 연산을 실행하면 그 결과로 첫 번째 큐비트가 `One`인 경우 두 번째 큐비트가 대칭 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-227">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="1b122-228">이제 두 큐비트가 서로 얽혔습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-228">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="1b122-229">첫 번째 큐비트에 대한 통계는 변경되지 않았지만(측정 후 `Zero` 또는 `One`일 확률이 50-50), 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-229">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="1b122-230">`CNOT`는 두 큐비트를 얽어서 두 큐비트 중 한 큐비트에서 발생하는 모든 것이 다른 큐비트에서 발생하도록 했습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-230">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="1b122-231">반대로 측정한 경우(먼저 두 번째 큐비트를 측정한 후에 첫 번째 큐비트를 측정함)에도 동일한 상황이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-231">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="1b122-232">첫 번째 측정은 임의적이고, 두 번째 측정은 첫 번째 측정에서 발견된 모든 것과 함께 잠금 단계에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-232">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="1b122-233">가장 먼저 해야 할 일은에서 하나 대신 두 개의 두 비트를 할당 하는 것입니다 `TestBellState` .</span><span class="sxs-lookup"><span data-stu-id="1b122-233">The first thing we'll need to do is allocate two qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="1b122-234">이렇게 하면 `TestBellState`에서 측정(`M`)하기 전에 새 연산(`CNOT`)을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-234">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="1b122-235">시작할 때 항상 `Zero` 상태에 있도록 첫 번째 큐비트를 초기화하는 다른 `SetQubitState` 연산을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-235">We've added another `SetQubitState` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="1b122-236">또한 두 번째 큐비트를 해제하기 전에 다시 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-236">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

<span data-ttu-id="1b122-237">이제 전체 루틴은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-237">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="1b122-238">이 루틴을 실행하면 이전과 정확히 동일한 50-50의 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-238">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="1b122-239">그러나 관심이 있는 것은 두 번째 큐비트가 측정되는 첫 번째 큐비트에 반응하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-239">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="1b122-240">새 버전의 `TestBellState` 연산을 사용하여 이 통계를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-240">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="1b122-241">새 반환 값(`agree`)은 첫 번째 큐비트의 측정값이 두 번째 큐비트의 측정값과 일치할 때마다 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-241">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span>

<span data-ttu-id="1b122-242">가져오는 코드를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-242">Running the code we obtain:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

<span data-ttu-id="1b122-243">개요에서 설명했듯이, 첫 번째 큐비트에 대한 통계는 변경되지 않았지만(0 또는 1일 확률이 50-50), 이제 두 큐비트가 서로 얽혀 있으므로 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-243">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

## <a name="next-steps"></a><span data-ttu-id="1b122-244">다음 단계</span><span class="sxs-lookup"><span data-stu-id="1b122-244">Next steps</span></span>

<span data-ttu-id="1b122-245">자습서 [Grover의 검색](xref:microsoft.quantum.quickstarts.search) 에서는 가장 인기 있는 퀀텀 컴퓨팅 알고리즘 중 하나인 Grover 검색을 빌드 및 실행 하는 방법을 보여 주고, Q# 퀀텀 컴퓨팅의 실제 문제를 해결 하는 데 사용할 수 있는 프로그램의 좋은 예를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-245">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="1b122-246">[퀀텀 개발 키트를 시작](xref:microsoft.quantum.welcome) 하 여 배우 프로그래밍에 대 한 추가 방법을 권장 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b122-246">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
