---
title: Q#에서 Grover의 검색 알고리즘 실행 - Quantum Development Kit
description: 정식 양자 알고리즘 중 하나인 Grover의 알고리즘을 보여 주는 Q# 프로젝트를 빌드합니다.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9e4c53b4d5159cf07f0654603c1d477ad09eb7c6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275270"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="a651f-103">자습서: Q\#에서 Grover의 검색 알고리즘 구현</span><span class="sxs-lookup"><span data-stu-id="a651f-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="a651f-104">이 자습서에서는 Grover 검색을 빌드하고 실행하여 비정형 데이터의 검색 속도를 높이는 방법을 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="a651f-105">Grover 검색은 가장 인기 있는 양자 컴퓨팅 알고리즘의 하나이며, 비교적 소규모의 Q# 구현을 통해 양자 알고리즘을 표현하는 고급 Q# 양자 프로그래밍 언어를 사용하여 양자 솔루션 프로그래밍의 장점을 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="a651f-106">가이드의 끝에서는 시뮬레이션 출력이 정렬되지 않은 항목 목록 중 특정 문자열을 찾는 데 걸리는 시간이 클래식 컴퓨터에서 전체 목록을 검색하는 데 걸리는 시간보다 짧다는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="a651f-107">Grover의 알고리즘은 특정 항목에 대한 비정형 데이터의 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="a651f-108">예를 들어 다음과 같은 질문에 답할 수 있습니다. 한 벌의 카드에서 뽑은 이 카드는 하트 에이스인가요?</span><span class="sxs-lookup"><span data-stu-id="a651f-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="a651f-109">특정 항목의 레이블 지정은 _표시된 입력_이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="a651f-110">Grover의 검색 알고리즘을 사용하면 양자 컴퓨터에서 검색 중인 목록의 항목 수보다 더 적은 단계에서 이 검색을 실행할 수 있습니다. 즉 클래식 알고리즘에서 수행할 수 있는 작업이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="a651f-111">카드 한 벌의 경우 증가된 속도는 무시할 수 있지만, 수백만 또는 수십억 개의 항목이 포함된 목록에서는 상당한 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="a651f-112">Grover의 검색 알고리즘은 몇 줄의 코드만으로 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a651f-113">사전 요구 사항</span><span class="sxs-lookup"><span data-stu-id="a651f-113">Prerequisites</span></span>

- <span data-ttu-id="a651f-114">Microsoft [Quantum Development Kit][install]</span><span class="sxs-lookup"><span data-stu-id="a651f-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="a651f-115">Grover의 검색 알고리즘에서 수행하는 작업은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="a651f-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="a651f-116">Grover의 알고리즘은 목록의 항목이 검색 중인 항목인지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="a651f-117">이를 위해 각 계수 또는 확률 진폭을 사용하여 목록의 인덱스에 대한 양자 중첩을 생성하여 특정 인덱스가 찾고 있는 인덱스일 확률을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="a651f-118">알고리즘의 핵심에는 해당 계수의 확률 진폭이 1에 도달할 때까지 찾고 있는 인덱스의 계수를 점진적으로 증가시키는 두 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="a651f-119">증분 증폭의 수는 목록의 항목 수보다 작습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="a651f-120">이러한 이유로 Grover의 검색 알고리즘에서 클래식 알고리즘보다 적은 단계로 검색을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Grover의 검색 알고리즘에 대한 기능 다이어그램](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="a651f-122">코드 작성</span><span class="sxs-lookup"><span data-stu-id="a651f-122">Write the code</span></span>

1. <span data-ttu-id="a651f-123">Quantum Development Kit를 사용하여 [명령줄 애플리케이션에 대한 새 Q# 프로젝트를 만듭니다](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="a651f-123">Using the Quantum Development Kit, [create a new Q# project for the command line application](xref:microsoft.quantum.install.standalone).</span></span> <span data-ttu-id="a651f-124">프로젝트 `Grover`의 제목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-124">Title the project `Grover`.</span></span>

1. <span data-ttu-id="a651f-125">다음 코드를 새 프로젝트의 `Program.qs` 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-125">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="a651f-126">검색하는 목록을 정의하려면 새 `Reflections.qs` 파일을 만들고, 다음 코드를 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-126">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="a651f-127">`ReflectAboutMarked` 연산은 검색 중인 표시된 입력, 즉 0과 1이 교대로 반복되는 문자열을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-127">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="a651f-128">이 샘플은 표시된 입력을 하드 코딩하며, 다른 입력을 검색하도록 확장하거나 모든 입력에 대해 일반화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-128">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="a651f-129">다음으로, 새 Q# 프로그램을 실행하여 `ReflectAboutMarked`로 표시된 항목을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-129">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="a651f-130">Visual Studio 또는 Visual Studio Code를 사용한 Q# 명령줄 애플리케이션</span><span class="sxs-lookup"><span data-stu-id="a651f-130">Q# command line applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="a651f-131">실행 파일은 프로젝트 구성 및 명령줄 옵션에 따라 시뮬레이터 또는 리소스 예측 도구에서 `@EntryPoint()` 특성으로 표시된 작업 또는 함수를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-131">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="a651f-132">Visual Studio에서 Ctrl + F5 키를 눌러 스크립트를 실행하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-132">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="a651f-133">VS Code에서 터미널에 아래를 입력하여 `Program.qs`를 처음으로 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-133">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="a651f-134">후속 실행 시, 다시 빌드할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-134">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="a651f-135">실행하려면 다음 명령을 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-135">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="a651f-136">터미널에 다음 메시지가 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-136">You should see the following message displayed in the terminal:</span></span>

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

<span data-ttu-id="a651f-137">이는 사용할 큐비트 수를 지정하지 않았기 때문에 터미널에서 실행 파일에 사용할 수 있는 명령을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-137">This is because you didn't specify the number of qubits you wanted to use, so the terminal tells you the commands available for the executable.</span></span> <span data-ttu-id="a651f-138">5개의 큐비트를 사용하려면 다음을 입력해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-138">If we want to use 5 qubits we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="a651f-139">Enter를 누르면 다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-139">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="a651f-140">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a651f-140">Next steps</span></span>

<span data-ttu-id="a651f-141">이 자습서를 사용한 경우 아래 리소스 중 일부를 확인하여 Q#에서 사용자 고유의 양자 애플리케이션을 작성하는 방법을 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="a651f-141">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="a651f-142">QDK 시작 가이드로 돌아가기</span><span class="sxs-lookup"><span data-stu-id="a651f-142">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="a651f-143">더 일반적인 Grover의 검색 알고리즘 [샘플](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)을 사용해 보기</span><span class="sxs-lookup"><span data-stu-id="a651f-143">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="a651f-144">Quantum Katas에서 Grover 검색에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="a651f-144">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="a651f-145">Grover 검색 알고리즘의 기반이 되는 양자 컴퓨팅 기술인 [진폭 증폭][amplitude-amplification]에 대해 자세히 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="a651f-145">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="a651f-146">양자 컴퓨팅 개념</span><span class="sxs-lookup"><span data-stu-id="a651f-146">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="a651f-147">Quantum Development Kit 샘플</span><span class="sxs-lookup"><span data-stu-id="a651f-147">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification