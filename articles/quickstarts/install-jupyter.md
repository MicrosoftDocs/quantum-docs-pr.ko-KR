---
title: Q# Jupyter Notebook을 사용하여 개발
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274092"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="12e3f-102">Q# Jupyter Notebook을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="12e3f-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="12e3f-103">Q# Jupyter Notebook에서 Q# 작업을 개발하기 위해 QDK를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="12e3f-104">Jupyter Notebook을 사용하면 지침, 메모 및 기타 콘텐츠와 함께 내부 코드를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="12e3f-105">이 환경은 설명 또는 퀀텀 컴퓨팅 대화형 자습서가 포함된 Q# 코드를 작성하는 데 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="12e3f-106">사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="12e3f-107">IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="12e3f-108">Q# Jupyter Notebook에서는 Q# 코드만 실행할 수 있고 외부 호스트 프로그램(예: Python 또는 C# 파일)에서 작업을 호출할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="12e3f-109">외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합하는 것이 목표라면 이 환경은 적합하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="12e3f-110">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="12e3f-110">Prerequisites</span></span>

    - <span data-ttu-id="12e3f-111">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="12e3f-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="12e3f-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="12e3f-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="12e3f-113">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="12e3f-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="12e3f-114">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="12e3f-115">`dotnet iqsharp install` 단계 중에 오류가 발생하면 새 터미널 창을 열고 다시 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="12e3f-116">그래도 해결되지 않으면 설치된 `dotnet-iqsharp` 도구(Windows의 경우 `dotnet-iqsharp.exe`)를 찾아서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="12e3f-117">여기서 `/path/to/dotnet-iqsharp`은 파일 시스템에서 `dotnet-iqsharp` 도구의 절대 경로로 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="12e3f-118">일반적으로 사용자 프로필 폴더의 `.dotnet/tools`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="12e3f-119">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="12e3f-120">다음 명령을 실행하여 Notebook 서버를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="12e3f-121">Jupyter Notebook을 열려면 명령줄에 제공된 URL을 복사하여 브라우저에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="12e3f-122">Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="12e3f-123">다음 Notebook 셀을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-123">Run this cell of the notebook:</span></span>

        ![Q# 코드가 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        <span data-ttu-id="12e3f-125">셀의 출력에 `SayHello`가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="12e3f-126">Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="12e3f-127">새 셀에서 `%simulate` 명령을 사용하여 방금 만든(시뮬레이터에서) 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![%simulate 매직이 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="12e3f-129">호출한 작업의 결과(여기서는 작업이 단순히 `Unit` 유형을 반환하기 때문에 빈 튜플 `()`이 표시됨)와 함께 메시지가 화면에 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="12e3f-130">다음 단계</span><span class="sxs-lookup"><span data-stu-id="12e3f-130">Next steps</span></span>

<span data-ttu-id="12e3f-131">Q# Jupyter Notebook용 QDK를 설치했으면, Jupyter Notebook 환경 내에서 직접 Q# 코드를 작성하여 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="12e3f-132">Q# Jupyter Notebook으로 수행할 수 있는 작업에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12e3f-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="12e3f-133">[Q# 및 Jupyter Notebook 소개](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="12e3f-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="12e3f-134">이 환경에서 Q#을 사용하는 방법을 보여주는 Q# Jupyter Notebook을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="12e3f-135">[Quantum Katas](xref:microsoft.quantum.overview.katas)는 Q# Jupyter Notebook 형태의 자기 주도적 자습서 및 프로그래밍 연습 세트를 포함하는 오픈 소스 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="12e3f-136">[Quantum Katas 자습서 Notebook](https://github.com/microsoft/QuantumKatas#tutorial-topics)은 좋은 시작점입니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="12e3f-137">Quantum Katas의 목표는 퀀텀 컴퓨팅과 Q# 프로그래밍 요소를 동시에 학습하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="12e3f-138">Q# Jupyter Notebook으로 만들 수 있는 콘텐츠의 종류를 보여주는 유용한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="12e3f-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
