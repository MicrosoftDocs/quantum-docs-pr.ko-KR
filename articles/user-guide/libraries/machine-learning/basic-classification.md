---
title: 퀀텀 Machine Learning 라이브러리를 사용 하는 기본 분류
description: Q#Microsoft QDK의 퀀텀 Machine Learning 라이브러리를 사용 하 여로 작성 된 퀀텀 순차 분류자를 실행 하는 방법에 대해 알아봅니다.
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5dc4614b9992e2c6b9f8ff4b839c0929ec8cab7c
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833716"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="919cf-103">기본 분류: QDK 데이터 분류</span><span class="sxs-lookup"><span data-stu-id="919cf-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="919cf-104">이 빠른 시작에서는 Q# QDK의 퀀텀 Machine Learning 라이브러리를 사용 하 여로 작성 된 퀀텀 순차 분류자를 실행 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-104">In this Quickstart, you will learn how to run a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="919cf-105">이 가이드에서는에 정의 된 분류자 구조를 사용 하 여 초승달 데이터 집합을 사용 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="919cf-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="919cf-106">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="919cf-106">Prerequisites</span></span>

- <span data-ttu-id="919cf-107">Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)</span><span class="sxs-lookup"><span data-stu-id="919cf-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="919cf-108">Q# [Python 호스트 프로그램](xref:microsoft.quantum.install.python) 또는 [c # 호스트 프로그램](xref:microsoft.quantum.install.cs)에 대 한 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-108">Create a Q# project for either a [Python host program](xref:microsoft.quantum.install.python) or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="host-program"></a><span data-ttu-id="919cf-109">호스트 프로그램</span><span class="sxs-lookup"><span data-stu-id="919cf-109">Host program</span></span>

<span data-ttu-id="919cf-110">호스트 프로그램은 다음 세 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="919cf-111">데이터 집합을 로드 하 고 모델의 시작 매개 변수 집합을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="919cf-112">학습을 실행 하 여 모델의 매개 변수 및 바이어스를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-112">Run training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="919cf-113">모델의 유효성을 검사 하 여 정확성 확인</span><span class="sxs-lookup"><span data-stu-id="919cf-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="919cf-114">Visual Studio 코드 또는 명령줄을 사용하는 Python</span><span class="sxs-lookup"><span data-stu-id="919cf-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="919cf-115">Q#Python의 분류자를 실행 하려면 다음 코드를로 저장 `host.py` 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="919cf-116">Q# `Training.qs` 이 자습서의 뒷부분에서 설명 하는 파일도 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="919cf-117">그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="919cf-118">Visual Studio 코드 또는 명령줄을 사용하는 C#</span><span class="sxs-lookup"><span data-stu-id="919cf-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="919cf-119">Q#C #의 분류자를 실행 하려면 다음 코드를로 저장 `Host.cs` 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="919cf-120">Q# `Training.qs` 이 자습서의 뒷부분에서 설명 하는 파일도 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="919cf-121">그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="919cf-122">Visual Studio 2019를 사용하는 C#</span><span class="sxs-lookup"><span data-stu-id="919cf-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="919cf-123">Q#Visual Studio의 c #에서 새 프로그램을 실행 하려면 `Host.cs` 다음 c # 코드를 포함 하도록을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="919cf-124">Q# `Training.qs` 이 자습서의 뒷부분에서 설명 하는 파일도 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="919cf-125">F5 키를 누르면 프로그램이 실행 되기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-125">Press F5, and the program will start to run.</span></span> <span data-ttu-id="919cf-126">새 창에 다음 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-126">A new window will display the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="919cf-127">Q \# 분류자 코드</span><span class="sxs-lookup"><span data-stu-id="919cf-127">Q\# classifier code</span></span>

<span data-ttu-id="919cf-128">이제 호스트 프로그램에서 호출 하는 작업이에서 정의 되는 방식을 살펴보겠습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="919cf-128">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="919cf-129">이라는 파일에 다음 코드를 저장 `Training.qs` 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-129">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="919cf-130">위의 코드에 정의 된 가장 중요 한 함수와 연산은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-130">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="919cf-131">`ClassifierStructure() : ControlledRotation[]` :이 함수에서 고려 하는 제어 되는 게이트의 계층을 추가 하 여 회로 모델 구조를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-131">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="919cf-132">이 단계는 순차적 심층 학습 모델에서 뉴런의 계층 선언과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-132">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="919cf-133">`TrainHalfMoonModel() : (Double[], Double)` :이 작업은 코드의 핵심 부분이 며 학습을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-133">`TrainHalfMoonModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="919cf-134">여기에서 라이브러리에 포함 된 데이터 집합의 샘플을 로드 하 고, 학습에 대 한 하이퍼 매개 변수 및 초기 매개 변수를 설정 하 고, 라이브러리에 포함 된 작업을 호출 하 여 학습을 시작 합니다 `TrainSequentialClassifier` .</span><span class="sxs-lookup"><span data-stu-id="919cf-134">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="919cf-135">분류자를 결정 하는 매개 변수 및 바이어스를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-135">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="919cf-136">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` :이 작업은 모델을 평가 하는 유효성 검사 프로세스를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-136">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="919cf-137">여기서는 유효성 검사에 대 한 샘플, 샘플 당 측정 수 및 허용 오차를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-137">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="919cf-138">유효성 검사를 위해 선택한 샘플 일괄 처리의 오 분류 수를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-138">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="919cf-139">다음 단계</span><span class="sxs-lookup"><span data-stu-id="919cf-139">Next steps</span></span>

<span data-ttu-id="919cf-140">첫째, 코드를 사용 하 여 재생 하 고 몇 가지 매개 변수를 변경 하 여 학습에 미치는 영향을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-140">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="919cf-141">그런 다음, 다음 자습서의 [고유한 분류자 디자인](xref:microsoft.quantum.libraries.machine-learning.design)에서 분류자의 구조를 정의 하는 방법을 배웁니다.</span><span class="sxs-lookup"><span data-stu-id="919cf-141">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
