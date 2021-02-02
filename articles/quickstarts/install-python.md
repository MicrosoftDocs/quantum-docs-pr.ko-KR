---
title: Q# 및 Python을 사용하여 개발
description: Python을 사용하여 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1ec40b6f1b7a8d9144860e3b8cfd554eb51bae81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844263"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="ef836-103">Q# 및 Python을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="ef836-103">Develop with Q# and Python</span></span>

<span data-ttu-id="ef836-104">QDK를 설치하여 Q# 작업을 호출하는 Python 호스트 프로그램을 개발합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-104">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="ef836-105">`qsharp` Python 패키지 설치</span><span class="sxs-lookup"><span data-stu-id="ef836-105">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="ef836-106">conda를 사용하여 설치(권장)</span><span class="sxs-lookup"><span data-stu-id="ef836-106">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="ef836-107">[Miniconda](https://docs.conda.io/en/latest/miniconda.html) 또는 [Anaconda](https://www.anaconda.com/products/individual#Downloads)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-107">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="ef836-108">**참고:** 64비트를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-108">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="ef836-109">Anaconda 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-109">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="ef836-110">또는 PowerShell이나 pwsh를 사용하려면 셸을 열고 `conda init powershell`을 실행한 다음, 셸을 닫았다가 다시 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-110">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="ef836-111">다음 명령을 실행하여 필요한 패키지(Jupyter Notebook 및 IQ# 포함)가 포함된 `qsharp-env`라는 새 conda 환경을 만들고 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-111">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="ef836-112">동일한 터미널에서 `python -c "import qsharp"`을 실행하여 설치를 확인하고, 로컬 패키지 캐시를 필요한 QDK 구성 요소로 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-112">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="ef836-113">.NET CLI 및 pip를 사용하여 설치(고급)</span><span class="sxs-lookup"><span data-stu-id="ef836-113">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="ef836-114">필수 조건:</span><span class="sxs-lookup"><span data-stu-id="ef836-114">Prerequisites:</span></span>

    - <span data-ttu-id="ef836-115">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="ef836-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="ef836-116">[PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자</span><span class="sxs-lookup"><span data-stu-id="ef836-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="ef836-117">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="ef836-117">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="ef836-118">Q#과 Python 간에 interop를 사용할 수 있도록 하는 Python 패키지인 `qsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-118">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="ef836-119">IQ#을 설치합니다. Jupyter 및 Python에서 주로 사용되는 커널이며, Q# 작업을 컴파일하고 실행하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-119">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and running Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="ef836-120">`dotnet iqsharp install` 단계 중에 오류가 발생하면 새 터미널 창을 열고 다시 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-120">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="ef836-121">그래도 해결되지 않으면 설치된 `dotnet-iqsharp` 도구(Windows의 경우 `dotnet-iqsharp.exe`)를 찾아서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-121">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="ef836-122">여기서 `/path/to/dotnet-iqsharp`은 파일 시스템에서 `dotnet-iqsharp` 도구의 절대 경로로 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-122">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="ef836-123">일반적으로 사용자 프로필 폴더의 `.dotnet/tools`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-123">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
<span data-ttu-id="ef836-124">\*\*_</span><span class="sxs-lookup"><span data-stu-id="ef836-124">\*\*_</span></span>

<span data-ttu-id="ef836-125">이것으로 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-125">That's it!</span></span> <span data-ttu-id="ef836-126">이제 Python에서 Q# 작업을 컴파일 및 실행하기 위한 핵심 기능을 제공하고 Q# Jupyter Notebook을 사용할 수 있게 해주는 `qsharp` Python 패키지와 Jupyter용 IQ# 커널이 모두 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-126">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provide the core functionality for compiling and running Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="ef836-127">IDE 선택</span><span class="sxs-lookup"><span data-stu-id="ef836-127">Choose your IDE</span></span>

<span data-ttu-id="ef836-128">모든 IDE에서 Python과 함께 Q#을 사용할 수 있지만, Q# + Python 애플리케이션용 VS Code(Visual Studio Code) IDE를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-128">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="ef836-129">QDK Visual Studio Code 확장을 사용하여 경고, 구문 강조 표시, 프로젝트 템플릿 등과 같은 다양한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-129">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="ef836-130">VS Code를 사용하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-130">If you would like to use VS Code:</span></span>

- <span data-ttu-id="ef836-131">[VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-131">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="ef836-132">[VS Code용 QDK 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-132">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="ef836-133">그 외의 편집기는 위의 지침을 수행하면서 이미 설정이 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-133">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-q-program"></a><span data-ttu-id="ef836-134">첫 번째 Q# 프로그램 작성</span><span class="sxs-lookup"><span data-stu-id="ef836-134">Write your first Q# program</span></span>

<span data-ttu-id="ef836-135">이제 간단한 Q# 프로그램을 작성하고 실행하여 `qsharp` Python 패키지 설치를 확인할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-135">Now you are ready to verify your `qsharp` Python package installation by writing and running a simple Q# program.</span></span>

1. <span data-ttu-id="ef836-136">`Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-136">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="ef836-137">다음과 같이 `Operation.qs`와 동일한 폴더에 `host.py`라는 Python 프로그램을 만들어 Q# `SampleQuantumRandomNumberGenerator()` 작업을 시뮬레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-137">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. <span data-ttu-id="ef836-138">설치하는 동안 만든 환경(즉, `qsharp`을 설치한 conda 또는 Python 환경)에서 다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-138">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="ef836-139">호출한 작업의 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-139">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="ef836-140">이 예에서는 작업에서 임의의 결과를 생성하기 때문에 화면에 `0` 또는 `1`이 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-140">In this case, because your operation generates a random result, you will see either `0` or `1` printed on the screen.</span></span> <span data-ttu-id="ef836-141">프로그램을 반복해서 실행하면 각 결과가 약 절반의 시간 동안 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-141">If you run the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> <span data-ttu-id="ef836-142">_ Python 코드는 일반적인 Python 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-142">_ The Python code is just a normal Python program.</span></span> <span data-ttu-id="ef836-143">Python 기반 Jupyter Notebook을 비롯한 Python 환경을 사용하여 Python 프로그램을 작성하고 Q# 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-143">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="ef836-144">Python 프로그램은 Python 코드 자체와 동일한 폴더에 있는 모든 .qs 파일에서 Q# 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-144">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ef836-145">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ef836-145">Next steps</span></span>

<span data-ttu-id="ef836-146">기본 설정 환경에서 Quantum Development Kit를 테스트했으므로, 이제 이 자습서를 따라 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef836-146">Now that you have tested the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
