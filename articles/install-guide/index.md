---
title: Microsoft QDK(Quantum Development Kit) 설치 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 580ac14f2e839d723884a96e9c5fd336ebcb5da0
ms.sourcegitcommit: 30fcb35986b43388ad65dfb876eb3ad8ad0533ce
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2019
ms.locfileid: "73799158"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="dd4d4-102">Microsoft QDK(Quantum Development Kit) 설치</span><span class="sxs-lookup"><span data-stu-id="dd4d4-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="dd4d4-103">양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="dd4d4-104">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-104">The QDK consists of:</span></span>

- <span data-ttu-id="dd4d4-105">Go 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="dd4d4-105">the Q# programming language</span></span>
- <span data-ttu-id="dd4d4-106">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="dd4d4-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="dd4d4-107">Q#으로 작성된 양자 연산을 실행하는 호스트 애플리케이션(Python 또는 .NET 언어로 작성)</span><span class="sxs-lookup"><span data-stu-id="dd4d4-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="dd4d4-108">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="dd4d4-108">tools to facilitate your development</span></span>

<span data-ttu-id="dd4d4-109">선택한 개발 환경에 따라 여러 가지 설치 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="dd4d4-110">아래 섹션에서 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="dd4d4-111">Python으로 개발</span><span class="sxs-lookup"><span data-stu-id="dd4d4-111">Develop with Python</span></span>

<span data-ttu-id="dd4d4-112">Python용 qsharp 패키지를 사용하면 Python 내에서 Q# 작업 및 함수를 쉽게 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-112">The qsharp package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="dd4d4-113">IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-113">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python that provides the core functionality for compiling and simulating Q# operations.</span></span>

1. <span data-ttu-id="dd4d4-114">필수 조건</span><span class="sxs-lookup"><span data-stu-id="dd4d4-114">Pre-requisites</span></span>

    - <span data-ttu-id="dd4d4-115">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="dd4d4-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="dd4d4-116">[PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자</span><span class="sxs-lookup"><span data-stu-id="dd4d4-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="dd4d4-117">.NET Core SDK 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="dd4d4-117">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="dd4d4-118">`qsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-118">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="dd4d4-119">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-119">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="dd4d4-120">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-120">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="dd4d4-121">`Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-121">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - <span data-ttu-id="dd4d4-122">`hello_world.py`이라는 Python 프로그램을 만들어 Q# `SayHello()` 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-122">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="dd4d4-123">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-123">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="dd4d4-124">출력을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-124">Verify the output.</span></span> <span data-ttu-id="dd4d4-125">프로그램은 다음 줄을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-125">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="dd4d4-126">Jupyter Notebook을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="dd4d4-126">Develop with Jupyter notebooks</span></span>

<span data-ttu-id="dd4d4-127">교육 기관 설정, 과학 랩 및 온라인 기반 협업 프로그래밍에 자주 사용되는 Jupyter Notebook은 이제 Q#를 포함한 바로 코드 실행을 제공하며 지침, 메모 및 기타 콘텐츠도 함께 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-127">A favorite of academic settings, scientific labs, and online-based collaborative programming, Jupyter Notebooks offer in-place code execution—now including Q# code—along with instructions, notes, and other content.</span></span>  <span data-ttu-id="dd4d4-128">사용자 고유의 Q# Notebook 만들기를 시작하려면 다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-128">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="dd4d4-129">IQ#(i-q-sharp로 발음)은 Jupyter 및 Python에서 .NET Core SDK에 주로 사용되며, Q# 작업을 컴파일하고 시뮬레이션하는 핵심 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-129">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>


1. <span data-ttu-id="dd4d4-130">필수 조건</span><span class="sxs-lookup"><span data-stu-id="dd4d4-130">Pre-requisites</span></span>

    - <span data-ttu-id="dd4d4-131">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="dd4d4-131">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="dd4d4-132">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="dd4d4-132">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="dd4d4-133">.NET Core SDK 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="dd4d4-133">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="dd4d4-134">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-134">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="dd4d4-135">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-135">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="dd4d4-136">다음 명령을 실행하여 Notebook 서버를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-136">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="dd4d4-137">명령줄에 표시된 URL로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-137">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="dd4d4-138">예: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="dd4d4-138">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="dd4d4-139">Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-139">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="dd4d4-140">다음 Notebook 셀을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-140">Run this cell of the notebook:</span></span>

        ![Q# 코드를 사용하는 Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        <span data-ttu-id="dd4d4-142">셀의 출력에 `SayHello`가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-142">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="dd4d4-143">Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-143">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="dd4d4-144">새 셀에서 `%simulate` 매직을 사용하여 방금 만든 작업의 양자 컴퓨터에서 실행을 시뮬레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-144">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

        ![%simulate 매직을 사용하는 Jupyter Notebook 셀](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="dd4d4-146">호출한 작업의 결과(여기서는 비어 있음)와 함께 메시지가 화면에 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-146">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>


## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="dd4d4-147">Windows C#에서 Visual Studio를 사용하여 C#으로 개발</span><span class="sxs-lookup"><span data-stu-id="dd4d4-147">Develop with C# on Windows, using Visual Studio</span></span>

<span data-ttu-id="dd4d4-148">Visual Studio는 Q# 프로그램을 개발할 수 있는 풍부한 환경을 제공하며, 개발자에게 애플리케이션 빌드 방법을 안내하는 코드 완성 및 구문 강조 표시 같은 유용한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-148">Visual Studio offers a rich environment for developing Q# programs, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="dd4d4-149">Q# Visual Studio 확장에는 구문 강조 표시 및 IntelliSense 지원뿐 아니라 Q# 파일 및 프로젝트용 템플릿이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-149">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting and IntelliSense support.</span></span>


1. <span data-ttu-id="dd4d4-150">필수 조건</span><span class="sxs-lookup"><span data-stu-id="dd4d4-150">Pre-requisites</span></span>

    - <span data-ttu-id="dd4d4-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정</span><span class="sxs-lookup"><span data-stu-id="dd4d4-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="dd4d4-152">Q# Visual Studio 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-152">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="dd4d4-153">[Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-153">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="dd4d4-154">Visual Studio에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-154">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="dd4d4-155">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-155">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="dd4d4-156">새 Q# 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="dd4d4-156">Create a new Q# application</span></span>

        - <span data-ttu-id="dd4d4-157">**파일** -> **새로 만들기** -> **프로젝트**로 이동</span><span class="sxs-lookup"><span data-stu-id="dd4d4-157">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="dd4d4-158">검색 상자에 `Q#` 입력</span><span class="sxs-lookup"><span data-stu-id="dd4d4-158">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="dd4d4-159">**Q# 애플리케이션**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-159">Select **Q# Application**</span></span>
        - <span data-ttu-id="dd4d4-160">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-160">Select **Next**</span></span>
        - <span data-ttu-id="dd4d4-161">애플리케이션의 이름 및 위치를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-161">Choose a name and location for your application</span></span>
        - <span data-ttu-id="dd4d4-162">**만들기**</span><span class="sxs-lookup"><span data-stu-id="dd4d4-162">Select **Create**</span></span>

    - <span data-ttu-id="dd4d4-163">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-163">Inspect the project</span></span>

        <span data-ttu-id="dd4d4-164">C# 호스트 애플리케이션에 해당하는 `Driver.cs`와 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램에 해당하는 `Operation.qs`의 두 파일이 생성된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-164">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="dd4d4-165">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="dd4d4-165">Run the application</span></span>

        - <span data-ttu-id="dd4d4-166">**디버그** -> **디버깅하지 않고 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-166">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="dd4d4-167">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-167">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="dd4d4-168">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-168">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-visual-studio-code"></a><span data-ttu-id="dd4d4-169">Visual Studio Code를 사용하여 C#으로 개발</span><span class="sxs-lookup"><span data-stu-id="dd4d4-169">Develop with C#, using Visual Studio Code</span></span>

<span data-ttu-id="dd4d4-170">VS Code(Visual Studio Code)는 Windows, Linux 및 Mac을 포함한 여러 컴퓨터 환경에서 Q# 프로그램을 개발할 수 있는 풍부한 환경을 제공하며, 개발자에게 애플리케이션 빌드 방법을 안내하는 코드 완성 및 구문 강조 표시 같은 유용한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-170">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs across many multiple computer environments, including Windows, Linux and Mac, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="dd4d4-171">Q# VS Code 확장에는 구문 강조 표시 및 Q# 코드 조각이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-171">The Q# VS Code extension contains syntax highlighting, and Q# code snippets.</span></span>

1. <span data-ttu-id="dd4d4-172">필수 조건</span><span class="sxs-lookup"><span data-stu-id="dd4d4-172">Pre-requisites</span></span>

   - [<span data-ttu-id="dd4d4-173">VS 코드</span><span class="sxs-lookup"><span data-stu-id="dd4d4-173">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="dd4d4-174">.NET Core SDK 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="dd4d4-174">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="dd4d4-175">Quantum VS Code 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-175">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="dd4d4-176">[VS Code 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-176">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="dd4d4-177">양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-177">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="dd4d4-178">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-178">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="dd4d4-179">**Q#: 프로젝트 템플릿 설치**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-179">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="dd4d4-180">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-180">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="dd4d4-181">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-181">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="dd4d4-182">새 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-182">Create a new project:</span></span>

        - <span data-ttu-id="dd4d4-183">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-183">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="dd4d4-184">**Q#: 새 프로젝트 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-184">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="dd4d4-185">애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-185">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="dd4d4-186">프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-186">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="dd4d4-187">애플리케이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-187">Run the application:</span></span>

        - <span data-ttu-id="dd4d4-188">**디버그** -> **디버깅하지 않고 시작**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-188">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="dd4d4-189">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="dd4d4-189">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="dd4d4-190">여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-190">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="dd4d4-191">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-191">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="dd4d4-192">`dotnet` 명령줄 도구를 사용하여 C#으로 개발</span><span class="sxs-lookup"><span data-stu-id="dd4d4-192">Develop with C#, using the `dotnet` command-line tool</span></span>

<span data-ttu-id="dd4d4-193">물론 간단하게 .NET Core SDK 및 QDK 프로젝트 템플릿을 설치하여 명령줄에서 Q# 프로그램을 빌드하고 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-193">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="dd4d4-194">필수 조건</span><span class="sxs-lookup"><span data-stu-id="dd4d4-194">Pre-requisites</span></span>

    - [<span data-ttu-id="dd4d4-195">.NET Core SDK 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="dd4d4-195">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="dd4d4-196">.NET용 양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-196">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="dd4d4-197">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-197">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="dd4d4-198">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-198">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="dd4d4-199">새 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="dd4d4-199">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="dd4d4-200">새 애플리케이션 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-200">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="dd4d4-201">애플리케이션의 프로젝트 파일과 함께 Q# 파일(`Operation.qs`) 및 C# 호스트 파일(`Driver.cs`)의 두 파일이 생성된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-201">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="dd4d4-202">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="dd4d4-202">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="dd4d4-203">다음 출력이 표시됩니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="dd4d4-203">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="dd4d4-204">다음 작업</span><span class="sxs-lookup"><span data-stu-id="dd4d4-204">What's next?</span></span>

<span data-ttu-id="dd4d4-205">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd4d4-205">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
