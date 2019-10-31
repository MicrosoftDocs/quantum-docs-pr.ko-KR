---
title: Microsoft QDK(Quantum Development Kit) 설치 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 3ec53934436b47908fd4d794a98933010f6059a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035302"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="711e6-102">Microsoft QDK(Quantum Development Kit) 설치</span><span class="sxs-lookup"><span data-stu-id="711e6-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="711e6-103">양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="711e6-104">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-104">The QDK consists of:</span></span>

- <span data-ttu-id="711e6-105">Go 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="711e6-105">the Q# programming language</span></span>
- <span data-ttu-id="711e6-106">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="711e6-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="711e6-107">Q#으로 작성된 양자 연산을 실행하는 호스트 애플리케이션(Python 또는 .NET 언어로 작성)</span><span class="sxs-lookup"><span data-stu-id="711e6-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="711e6-108">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="711e6-108">tools to facilitate your development</span></span>

<span data-ttu-id="711e6-109">선택한 개발 환경에 따라 여러 가지 설치 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="711e6-110">아래 섹션에서 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="711e6-111">Python으로 개발</span><span class="sxs-lookup"><span data-stu-id="711e6-111">Develop with Python</span></span>

1. <span data-ttu-id="711e6-112">필수 조건</span><span class="sxs-lookup"><span data-stu-id="711e6-112">Pre-requisites</span></span>

    - <span data-ttu-id="711e6-113">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="711e6-113">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="711e6-114">[PIP](https://pip.pypa.io/en/stable/installing) Python 패키지 관리자</span><span class="sxs-lookup"><span data-stu-id="711e6-114">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="711e6-115">.NET Core SDK 2.1 이상</span><span class="sxs-lookup"><span data-stu-id="711e6-115">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="711e6-116">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-116">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="711e6-117">`qsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-117">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="711e6-118">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="711e6-119">`Operation.qs`라는 파일을 만들고 다음 코드를 추가하여 최소 Q# 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

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

    - <span data-ttu-id="711e6-120">`hello_world.py`이라는 Python 프로그램을 만들어 Q# `SayHello()` 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="711e6-121">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-121">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="711e6-122">출력을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-122">Verify the output.</span></span> <span data-ttu-id="711e6-123">프로그램은 다음 줄을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-123">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="711e6-124">Jupyter Notebook을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="711e6-124">Develop with Jupyter notebooks</span></span>

1. <span data-ttu-id="711e6-125">필수 조건</span><span class="sxs-lookup"><span data-stu-id="711e6-125">Pre-requisites</span></span>

    - <span data-ttu-id="711e6-126">[Python](https://www.python.org/downloads/) 3.6 이상</span><span class="sxs-lookup"><span data-stu-id="711e6-126">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="711e6-127">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="711e6-127">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="711e6-128">.NET Core SDK 2.1 이상</span><span class="sxs-lookup"><span data-stu-id="711e6-128">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="711e6-129">`iqsharp` 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-129">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="711e6-130">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-130">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="711e6-131">다음 명령을 실행하여 Notebook 서버를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-131">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="711e6-132">명령줄에 표시된 URL로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-132">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="711e6-133">예: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="711e6-133">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="711e6-134">Q# 커널을 사용하여 Jupyter Notebook을 만들고 첫 번째 Notebook 셀에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-134">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="711e6-135">다음 Notebook 셀을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-135">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook 셀](~/media/install-guide-jupyter.png)

        <span data-ttu-id="711e6-137">셀의 출력에 `SayHello`가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-137">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="711e6-138">Jupyter Notebook에서 실행하는 경우 Q# 코드가 컴파일되고 Notebook은 검색된 작업의 이름을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-138">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="711e6-139">Windows C#에서 Visual Studio를 사용하여 C#으로 개발</span><span class="sxs-lookup"><span data-stu-id="711e6-139">Develop with C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="711e6-140">필수 조건</span><span class="sxs-lookup"><span data-stu-id="711e6-140">Pre-requisites</span></span>

    - <span data-ttu-id="711e6-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정</span><span class="sxs-lookup"><span data-stu-id="711e6-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="711e6-142">Q# Visual Studio 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-142">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="711e6-143">[Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-143">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="711e6-144">Visual Studio에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-144">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="711e6-145">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-145">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="711e6-146">새 Q# 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="711e6-146">Create a new Q# application</span></span>

        - <span data-ttu-id="711e6-147">**파일** -> **새로 만들기** -> **프로젝트**로 이동</span><span class="sxs-lookup"><span data-stu-id="711e6-147">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="711e6-148">검색 상자에 `Q#` 입력</span><span class="sxs-lookup"><span data-stu-id="711e6-148">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="711e6-149">**Q# 애플리케이션**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-149">Select **Q# Application**</span></span>
        - <span data-ttu-id="711e6-150">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-150">Select **Next**</span></span>
        - <span data-ttu-id="711e6-151">애플리케이션의 이름 및 위치를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-151">Choose a name and location for your application</span></span>
        - <span data-ttu-id="711e6-152">**만들기**</span><span class="sxs-lookup"><span data-stu-id="711e6-152">Select **Create**</span></span>

    - <span data-ttu-id="711e6-153">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-153">Inspect the project</span></span>

        <span data-ttu-id="711e6-154">C# 호스트 애플리케이션에 해당하는 `Driver.cs`와 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램에 해당하는 `Operation.qs`의 두 파일이 생성된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="711e6-155">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="711e6-155">Run the application</span></span>

        - <span data-ttu-id="711e6-156">**디버그** -> **디버깅하지 않고 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-156">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="711e6-157">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="711e6-158">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-158">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-vs-code"></a><span data-ttu-id="711e6-159">VS Code를 사용하여 C#으로 개발</span><span class="sxs-lookup"><span data-stu-id="711e6-159">Develop with C#, using VS Code</span></span>

1. <span data-ttu-id="711e6-160">필수 조건</span><span class="sxs-lookup"><span data-stu-id="711e6-160">Pre-requisites</span></span>

   - [<span data-ttu-id="711e6-161">VS 코드</span><span class="sxs-lookup"><span data-stu-id="711e6-161">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="711e6-162">.NET Core SDK 2.1 이상</span><span class="sxs-lookup"><span data-stu-id="711e6-162">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="711e6-163">Quantum VS Code 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-163">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="711e6-164">[VS Code 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-164">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="711e6-165">양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-165">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="711e6-166">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-166">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="711e6-167">**Q#: 프로젝트 템플릿 설치**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-167">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="711e6-168">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-168">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="711e6-169">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-169">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="711e6-170">새 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-170">Create a new project:</span></span>

        - <span data-ttu-id="711e6-171">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-171">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="711e6-172">**Q#: 새 프로젝트 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-172">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="711e6-173">애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-173">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="711e6-174">프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-174">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="711e6-175">애플리케이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-175">Run the application:</span></span>

        - <span data-ttu-id="711e6-176">**디버그** -> **디버깅하지 않고 시작**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-176">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="711e6-177">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="711e6-177">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="711e6-178">여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-178">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="711e6-179">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-179">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="711e6-180">`dotnet` 명령줄 도구를 사용하여 C#으로 개발</span><span class="sxs-lookup"><span data-stu-id="711e6-180">Develop with C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="711e6-181">필수 조건</span><span class="sxs-lookup"><span data-stu-id="711e6-181">Pre-requisites</span></span>

    - [<span data-ttu-id="711e6-182">.NET Core SDK 2.1 이상</span><span class="sxs-lookup"><span data-stu-id="711e6-182">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="711e6-183">.NET용 양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-183">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="711e6-184">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-184">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="711e6-185">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-185">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="711e6-186">새 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="711e6-186">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="711e6-187">새 애플리케이션 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-187">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="711e6-188">애플리케이션의 프로젝트 파일과 함께 Q# 파일(`Operation.qs`) 및 C# 호스트 파일(`Driver.cs`)의 두 파일이 생성된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-188">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="711e6-189">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="711e6-189">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="711e6-190">다음 출력이 표시됩니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="711e6-190">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="711e6-191">다음 작업</span><span class="sxs-lookup"><span data-stu-id="711e6-191">What's next?</span></span>

<span data-ttu-id="711e6-192">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="711e6-192">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
