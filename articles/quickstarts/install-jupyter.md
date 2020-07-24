---
title: Q# Jupyter Notebook을 사용하여 개발
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: bbd1f58ba7de205e452be7bac72b5fd78e7acd56
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871453"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="6e781-102">Q# Jupyter Notebook을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="6e781-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="6e781-103">Q# Jupyter Notebook에서 Q# 작업을 개발하기 위해 QDK를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="6e781-104">Jupyter Notebook을 사용하면 지침, 메모 및 기타 콘텐츠와 함께 내부 코드를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="6e781-105">이 환경은 설명 또는 퀀텀 컴퓨팅 대화형 자습서가 포함된 Q# 코드를 작성하는 데 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="6e781-106">사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

> [!NOTE]
> * <span data-ttu-id="6e781-107">Q# Jupyter Notebook에서는 Q# 코드만 실행할 수 있고 외부 호스트 프로그램(예: Python 또는 C# 파일)에서 작업을 호출할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-107">In Q# Jupyter Notebooks, you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="6e781-108">외부 클래식 호스트 프로그램과 퀀텀 프로그램을 결합하는 것이 목표라면 이 환경은 적합하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-108">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

## <a name="install-the-iq-jupyter-kernel"></a><span data-ttu-id="6e781-109">IQ# Jupyter 커널 설치</span><span class="sxs-lookup"><span data-stu-id="6e781-109">Install the IQ# Jupyter kernel</span></span>

<span data-ttu-id="6e781-110">IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-110">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="6e781-111">conda를 사용하여 설치(권장)</span><span class="sxs-lookup"><span data-stu-id="6e781-111">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="6e781-112">[Miniconda](https://docs.conda.io/en/latest/miniconda.html) 또는 [Anaconda](https://www.anaconda.com/products/individual#Downloads)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-112">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="6e781-113">**참고:** 64비트를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-113">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="6e781-114">Anaconda 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-114">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="6e781-115">또는 PowerShell이나 pwsh를 사용하려면 셸을 열고 `conda init powershell`을 실행한 다음, 셸을 닫았다가 다시 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-115">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="6e781-116">다음 명령을 실행하여 필요한 패키지(Jupyter Notebook 및 IQ# 포함)가 포함된 `qsharp-env`라는 새 conda 환경을 만들고 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-116">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="6e781-117">동일한 터미널에서 `python -c "import qsharp"`을 실행하여 설치를 확인하고, 로컬 패키지 캐시를 필요한 QDK 구성 요소로 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-117">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-advanced"></a>[<span data-ttu-id="6e781-118">.NET CLI를 사용하여 설치(고급)</span><span class="sxs-lookup"><span data-stu-id="6e781-118">Install using .NET CLI (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="6e781-119">필수 조건:</span><span class="sxs-lookup"><span data-stu-id="6e781-119">Prerequisites:</span></span>

    - <span data-ttu-id="6e781-120">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="6e781-120">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="6e781-121">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="6e781-121">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="6e781-122">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="6e781-122">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="6e781-123">`Microsoft.Quantum.IQSharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-123">Install the `Microsoft.Quantum.IQSharp` package.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="6e781-124">`dotnet iqsharp install` 단계 중에 오류가 발생하면 새 터미널 창을 열고 다시 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-124">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="6e781-125">그래도 해결되지 않으면 설치된 `dotnet-iqsharp` 도구(Windows의 경우 `dotnet-iqsharp.exe`)를 찾아서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-125">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="6e781-126">여기서 `/path/to/dotnet-iqsharp`은 파일 시스템에서 `dotnet-iqsharp` 도구의 절대 경로로 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-126">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="6e781-127">일반적으로 사용자 프로필 폴더의 `.dotnet/tools`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-127">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="6e781-128">이것으로 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-128">That's it!</span></span> <span data-ttu-id="6e781-129">이제 Q# Jupyter Notebook에서 Q# 작업을 컴파일 및 실행하기 위한 핵심 기능을 제공하는 Jupyter용 IQ# 커널이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-129">You now have the IQ# kernel for Jupyter, which provides the core functionality for compiling and executing Q# operations from Q# Jupyter Notebooks.</span></span>

## <a name="create-your-first-q-notebook"></a><span data-ttu-id="6e781-130">첫 번째 Q# Notebook 만들기</span><span class="sxs-lookup"><span data-stu-id="6e781-130">Create your first Q# notebook</span></span>

<span data-ttu-id="6e781-131">이제 간단한 Q# 작업을 작성하고 실행하여 Q# Jupyter Notebook 설치를 확인할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-131">Now you are ready to verify your Q# Jupyter Notebook installation by writing and executing a simple Q# operation.</span></span>

1. <span data-ttu-id="6e781-132">설치하는 동안 만든 환경(즉, 직접 만든 conda 환경 또는 Jupyter를 설치한 Python 환경)에서 다음 명령을 실행하여 Jupyter Notebook 서버를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-132">From the environment you created during installation (i.e., either the conda environment you created, or the Python environment where you installed Jupyter), run the following command to start the Jupyter Notebook server:</span></span>

    ```
    jupyter notebook
    ```

    - <span data-ttu-id="6e781-133">사용하는 브라우저에서 Jupyter Notebook이 자동으로 열리지 않으면 명령줄에 제공된 URL을 복사하여 브라우저에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-133">If the Jupyter Notebook doesn't open automatically in your browser, copy and paste the URL provided by the command line into your browser.</span></span>

1. <span data-ttu-id="6e781-134">"새로 만들기" → "Q#"을 선택하여 Q# 커널로 Jupyter Notebook을 만들고, 첫 번째 Notebook 셀에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-134">Choose "New" → "Q#" to create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. <span data-ttu-id="6e781-135">다음 Notebook 셀을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-135">Run this cell of the notebook:</span></span>

    ![Q# 코드가 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

    <span data-ttu-id="6e781-137">셀의 출력에 `SampleQuantumRandomNumberGenerator`가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-137">You should see `SampleQuantumRandomNumberGenerator` in the output of the cell.</span></span> <span data-ttu-id="6e781-138">Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고, 셀은 검색한 모든 작업의 이름을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-138">When running in Jupyter Notebook, the Q# code is compiled, and the cell outputs the name of any operations that it finds.</span></span>

1. <span data-ttu-id="6e781-139">새 셀에서 `%simulate` 명령을 사용하여 방금 만든(시뮬레이터에서) 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-139">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

    ![%simulate 매직이 포함된 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="6e781-141">호출한 작업의 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-141">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="6e781-142">이 예에서는 작업에서 임의의 결과를 생성하기 때문에 화면에 `Zero` 또는 `One`이 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-142">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="6e781-143">셀을 반복해서 실행하면 각 결과가 약 절반의 시간 동안 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-143">If you execute the cell repeatedly, you should see each result approximately half the time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6e781-144">다음 단계</span><span class="sxs-lookup"><span data-stu-id="6e781-144">Next steps</span></span>

<span data-ttu-id="6e781-145">Q# Jupyter Notebook용 QDK를 설치했으므로, Jupyter Notebook 환경 내에서 직접 Q# 코드를 작성하여 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-145">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="6e781-146">Q# Jupyter Notebook으로 수행할 수 있는 작업에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e781-146">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>

- <span data-ttu-id="6e781-147">[Q# 및 Jupyter Notebook 소개](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="6e781-147">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="6e781-148">Jupyter 환경에서 Q#을 사용하는 방법을 자세히 설명하는 Q# Jupyter Notebook을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-148">There you will find a Q# Jupyter Notebook that provides more details on how to use Q# in the Jupyter environment.</span></span>
- <span data-ttu-id="6e781-149">[Quantum Katas](xref:microsoft.quantum.overview.katas)는 Q# Jupyter Notebook 형태의 자기 주도적 자습서 및 프로그래밍 연습 세트를 포함하는 오픈 소스 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-149">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="6e781-150">[Quantum Katas 자습서 Notebook](https://github.com/microsoft/QuantumKatas#tutorial-topics)은 좋은 시작점입니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-150">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="6e781-151">Quantum Katas의 목표는 퀀텀 컴퓨팅과 Q# 프로그래밍 요소를 동시에 학습하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-151">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="6e781-152">Q# Jupyter Notebook으로 만들 수 있는 콘텐츠의 종류를 보여주는 유용한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="6e781-152">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
