---
title: Q#에서 Grover의 검색 알고리즘 실행 - Quantum Development Kit
description: 정식 양자 알고리즘 중 하나인 Grover의 알고리즘을 보여 주는 Q# 프로젝트를 빌드합니다.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: c1fd578fdb3d56a7b48972e6ccc9b1605047fe36
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820354"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="a8d3f-103">빠른 시작: Q#에서 Grover의 검색 알고리즘 구현</span><span class="sxs-lookup"><span data-stu-id="a8d3f-103">Quickstart: Implement Grover's search algorithm in Q#</span></span>

<span data-ttu-id="a8d3f-104">이 빠른 시작에서는 Grover 검색을 빌드하고 실행하여 비정형 데이터의 검색 속도를 높이는 방법을 배울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-104">In this Quickstart, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="a8d3f-105">Grover 검색은 가장 인기 있는 양자 컴퓨팅 알고리즘의 하나이며, 비교적 소규모의 Q# 구현을 통해 양자 알고리즘을 표현하는 고급 Q# 양자 프로그래밍 언어를 사용하여 양자 솔루션 프로그래밍의 장점을 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="a8d3f-106">이 가이드를 마치면 클래식 컴퓨터에서 전체 목록을 검색하는 데 소요되는 시간보다 훨씬 짧은 시간에 시뮬레이션 출력이 특정 문자열과 함께 순서대로 정렬된 항목 목록을 찾는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of onordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="a8d3f-107">Grover의 알고리즘은 특정 항목에 대한 비정형 데이터의 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="a8d3f-108">예를 들어 다음과 같은 질문에 답할 수 있습니다. 한 벌의 카드에서 뽑은 이 카드는 하트 에이스인가요?</span><span class="sxs-lookup"><span data-stu-id="a8d3f-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="a8d3f-109">특정 항목의 레이블 지정은 _표시된 입력_이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="a8d3f-110">Grover의 검색 알고리즘을 사용하면 양자 컴퓨터에서 검색 중인 목록의 항목 수보다 더 적은 단계에서 이 검색을 실행할 수 있습니다. 즉 클래식 알고리즘에서 수행할 수 있는 작업이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="a8d3f-111">카드 한 벌의 경우 증가된 속도는 무시할 수 있지만, 수백만 또는 수십억 개의 항목이 포함된 목록에서는 상당한 시간이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="a8d3f-112">Grover의 검색 알고리즘은 몇 줄의 코드만으로 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a8d3f-113">사전 요구 사항</span><span class="sxs-lookup"><span data-stu-id="a8d3f-113">Prerequisites</span></span>

- <span data-ttu-id="a8d3f-114">Microsoft [Quantum Development Kit][install]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="a8d3f-115">Grover의 검색 알고리즘에서 수행하는 작업은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="a8d3f-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="a8d3f-116">Grover의 알고리즘은 목록의 항목이 검색 중인 항목인지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="a8d3f-117">이를 위해 각 계수 또는 확률 진폭을 사용하여 목록의 인덱스에 대한 양자 중첩을 생성하여 특정 인덱스가 찾고 있는 인덱스일 확률을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="a8d3f-118">알고리즘의 핵심에는 해당 계수의 확률 진폭이 1에 도달할 때까지 찾고 있는 인덱스의 계수를 점진적으로 증가시키는 두 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="a8d3f-119">증분 증폭의 수는 목록의 항목 수보다 작습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="a8d3f-120">이러한 이유로 Grover의 검색 알고리즘에서 클래식 알고리즘보다 적은 단계로 검색을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Grover의 검색 알고리즘에 대한 기능 다이어그램](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="a8d3f-122">코드 작성</span><span class="sxs-lookup"><span data-stu-id="a8d3f-122">Write the code</span></span>

1. <span data-ttu-id="a8d3f-123">Quantum Development Kit를 사용하여 선택한 개발 환경에서 `Grover`라는 [새 Q# 프로젝트를 만듭니다](xref:microsoft.quantum.howto.createproject).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="a8d3f-124">다음 코드를 새 프로젝트의 `Operations.qs` 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-124">Add the following code to the `Operations.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-23" highlight="5,27":::

1. <span data-ttu-id="a8d3f-125">검색하는 목록을 정의하려면 새 `Reflections.qs` 파일을 만들고, 다음 코드를 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="a8d3f-126">`ReflectAboutMarked` 연산은 검색 중인 표시된 입력, 즉 0과 1이 교대로 반복되는 문자열을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="a8d3f-127">이 샘플은 표시된 입력을 하드 코딩하며, 다른 입력을 검색하도록 확장하거나 모든 입력에 대해 일반화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="a8d3f-128">다음으로, 새 Q# 프로그램을 실행하여 `ReflectAboutMarked`로 표시된 항목을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-linetabtabid-python"></a>[<span data-ttu-id="a8d3f-129">Visual Studio 코드 또는 명령줄을 사용하는 Python</span><span class="sxs-lookup"><span data-stu-id="a8d3f-129">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="a8d3f-130">Python에서 새 Q# 프로그램을 실행하려면 다음 코드를 `host.py`로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-130">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    <span data-ttu-id="a8d3f-131">그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-131">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-linetabtabid-csharp"></a>[<span data-ttu-id="a8d3f-132">Visual Studio 코드 또는 명령줄을 사용하는 C#</span><span class="sxs-lookup"><span data-stu-id="a8d3f-132">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="a8d3f-133">C#에서 새 Q# 프로그램을 실행하려면 다음 C# 코드를 포함하도록 `Driver.cs`를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-133">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    <span data-ttu-id="a8d3f-134">그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-134">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="a8d3f-135">Visual Studio 2019를 사용하는 C#</span><span class="sxs-lookup"><span data-stu-id="a8d3f-135">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="a8d3f-136">Visual Studio를 사용하여 C#에서 새 Q# 프로그램을 실행하려면 다음 C# 코드를 포함하도록 `Driver.cs`를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-136">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    <span data-ttu-id="a8d3f-137">그런 다음, F5 키를 누르면 프로그램이 실행되고 새 창에 다음 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-137">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    <span data-ttu-id="a8d3f-138">`ReflectAboutMarked` 연산은 4번만 호출되지만, Q# 프로그램이 2^{5} = 32$ 가능한 입력 중에서 "01010" 입력을 찾을 수 있었습니다!</span><span class="sxs-lookup"><span data-stu-id="a8d3f-138">The `ReflectAboutMarked` operation is called only four times, but your Q# program was able to find the "01010" input amongst $2^{5} = 32$ possible inputs!</span></span>

## <a name="next-steps"></a><span data-ttu-id="a8d3f-139">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a8d3f-139">Next steps</span></span>

<span data-ttu-id="a8d3f-140">이 빠른 시작을 사용한 경우 Q#을 사용하여 사용자 고유의 양자 애플리케이션을 작성하는 방법을 자세히 알아보기 위해 아래 리소스 중 일부를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-140">If you enjoyed this quickstart, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="a8d3f-141">QDK 시작 가이드로 돌아가기</span><span class="sxs-lookup"><span data-stu-id="a8d3f-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="a8d3f-142">더 일반적인 Grover의 검색 알고리즘 [샘플](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)을 사용해 보기</span><span class="sxs-lookup"><span data-stu-id="a8d3f-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="a8d3f-143">Quantum Katas에서 Grover 검색에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="a8d3f-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="a8d3f-144">Grover 검색 알고리즘의 기반이 되는 양자 컴퓨팅 기술인 [진폭 증폭](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification)에 대해 자세히 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-144">Read more about [Amplitude amplification](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="a8d3f-145">양자 컴퓨팅 개념</span><span class="sxs-lookup"><span data-stu-id="a8d3f-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="a8d3f-146">Quantum Development Kit 샘플</span><span class="sxs-lookup"><span data-stu-id="a8d3f-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
