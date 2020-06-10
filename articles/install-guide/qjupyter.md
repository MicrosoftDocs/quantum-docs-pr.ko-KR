---
title: Q# Jupyter Notebook을 사용하여 개발
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630342"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="d5412-102">Q# Jupyter Notebook을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="d5412-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="d5412-103">Q # Jupyter 노트북에서 Q # 작업을 개발 하는 데 QDK를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="d5412-104">Jupyter 노트북은 지침, 메모 및 기타 콘텐츠와 함께 전체 코드 실행을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="d5412-105">이 환경은 포함 된 설명 또는 퀀텀 컴퓨팅 대화형 자습서를 통해 Q # 코드를 작성 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="d5412-106">사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="d5412-107">IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="d5412-108">Q # Jupyter 노트북에서 Q # 코드만 실행할 수 있으며, 외부 호스트 프로그램 (예: Python 또는 c # 파일)에서 작업을 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="d5412-109">외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합 하는 것이 목표 인 경우에는이 환경이 적절 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="d5412-110">전제 조건</span><span class="sxs-lookup"><span data-stu-id="d5412-110">Prerequisites</span></span>

    - <span data-ttu-id="d5412-111">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="d5412-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="d5412-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="d5412-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="d5412-113">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="d5412-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="d5412-114">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="d5412-115">단계 중에 오류가 발생 하면 `dotnet iqsharp install` 새 터미널 창을 열고 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="d5412-116">그래도 작동 하지 않으면 설치 된 `dotnet-iqsharp` 도구 (Windows)를 찾아 `dotnet-iqsharp.exe` 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="d5412-117">는 `/path/to/dotnet-iqsharp` 파일 시스템의 도구에 대 한 절대 경로로 바꾸어야 합니다 `dotnet-iqsharp` .</span><span class="sxs-lookup"><span data-stu-id="d5412-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="d5412-118">일반적으로이는 `.dotnet/tools` 사용자 프로필 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="d5412-119">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="d5412-120">다음 명령을 실행하여 Notebook 서버를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="d5412-121">Jupyter Notebook를 열려면 명령줄에서 제공 된 URL을 복사 하 여 브라우저에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="d5412-122">Q # 커널을 사용 하 여 Jupyter Notebook를 만들고 첫 번째 노트북 셀에 다음 코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="d5412-123">다음 Notebook 셀을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-123">Run this cell of the notebook:</span></span>

        ![Q # code를 사용 하 여 셀 Jupyter Notebook](~/media/install-guide-jupyter.png)

        <span data-ttu-id="d5412-125">셀의 출력에 `SayHello`가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="d5412-126">Jupyter Notebook에서 실행 되는 경우 Q # 코드가 컴파일되고, 노트북은 검색 된 작업의 이름을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="d5412-127">새 셀에서 명령을 사용 하 여 시뮬레이터에서 방금 만든 작업을 실행 합니다 `%simulate` .</span><span class="sxs-lookup"><span data-stu-id="d5412-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![% 시뮬레이트 마법을 사용 하 여 셀 Jupyter Notebook](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="d5412-129">호출 된 작업의 결과와 함께 화면에 메시지가 출력 되는 것을 볼 수 있습니다 ( `()` 작업에서 단순히 형식을 반환 하기 때문에 빈 튜플이 표시 됨 `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="d5412-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d5412-130">다음 단계</span><span class="sxs-lookup"><span data-stu-id="d5412-130">Next steps</span></span>

<span data-ttu-id="d5412-131">Q # Jupyter 노트북용 QDK를 설치 했으므로 Jupyter Notebook 환경 내에서 직접 Q # 코드를 작성 하 여 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng) 을 작성 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="d5412-132">Q # Jupyter 노트북으로 수행할 수 있는 작업에 대 한 자세한 예제는 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5412-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="d5412-133">[Q # 및 Jupyter Notebook를 소개](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/)합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="d5412-134">이 환경에서 Q #을 사용 하는 방법을 보여 주는 Q # Jupyter Notebook를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="d5412-135">[Katas](xref:microsoft.quantum.overview.katas)는 자체 학습 자습서의 오픈 소스 컬렉션인 Q # Jupyter 노트북 형태의 프로그래밍 연습 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="d5412-136">[퀀텀 Katas tutorial 노트북](https://github.com/microsoft/QuantumKatas#tutorial-topics) 은 좋은 출발점입니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="d5412-137">퀀텀 Katas는 퀀텀 컴퓨팅 및 Q # 프로그래밍의 요소를 동시에 학습 하는 것을 목표로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="d5412-138">Q # Jupyter 노트북을 사용 하 여 만들 수 있는 콘텐츠의 종류에 대 한 좋은 예입니다.</span><span class="sxs-lookup"><span data-stu-id="d5412-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
