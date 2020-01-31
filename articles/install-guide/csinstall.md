---
title: 'Q # +를 사용 하 여 개발C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 1fd829c684502092bb7491b0f46b5f690320c941
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831021"
---
# <a name="develop-with-q--c"></a><span data-ttu-id="adf0e-102">Q # +를 사용 하 여 개발C#</span><span class="sxs-lookup"><span data-stu-id="adf0e-102">Develop with Q# + C#</span></span>

<span data-ttu-id="adf0e-103">Q # 작업을 호출 하 C# 는 호스트 프로그램을 개발 하려면 qdk를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-103">Install the QDK to develop C# host programs to call Q# operations.</span></span>

<span data-ttu-id="adf0e-104">Q #은 .NET 언어에서 잘 작동 하도록 빌드 되었습니다 (특히 C#).</span><span class="sxs-lookup"><span data-stu-id="adf0e-104">Q# is built to play well with .NET languages--specifically C#.</span></span> <span data-ttu-id="adf0e-105">다양 한 개발 환경 내에서이 페어링 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-105">You can work with this pairing inside different development environments:</span></span>

- [<span data-ttu-id="adf0e-106">Q # + C# Visual Studio 사용 (Windows)</span><span class="sxs-lookup"><span data-stu-id="adf0e-106">Q# + C# using Visual Studio (Windows)</span></span>](#VS)
- [<span data-ttu-id="adf0e-107">Q # + C# Visual Studio Code (Windows, Linux 및 Mac) 사용</span><span class="sxs-lookup"><span data-stu-id="adf0e-107">Q# + C# using Visual Studio Code (Windows, Linux and Mac)</span></span>](#VSC)
- [<span data-ttu-id="adf0e-108">Q # + C# `dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="adf0e-108">Q# + C# using the `dotnet` command-line tool</span></span>](#command)

## <span data-ttu-id="adf0e-109">Visual Studio를 사용 하 C# 여 Q # +를 사용 하 여 개발<a name="VS"></a></span><span class="sxs-lookup"><span data-stu-id="adf0e-109">Develop with Q# + C# using Visual Studio <a name="VS"></a></span></span>

<span data-ttu-id="adf0e-110">Visual Studio는 Q # 프로그램을 개발 하기 위한 풍부한 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-110">Visual Studio offers a rich environment for developing Q# programs.</span></span> <span data-ttu-id="adf0e-111">Q # Visual Studio 확장에는 구문 강조 표시, 코드 완성 및 IntelliSense 지원 뿐만 아니라 Q # 파일 및 프로젝트에 대 한 템플릿이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-111">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting, code completion and IntelliSense support.</span></span>


1. <span data-ttu-id="adf0e-112">필수 조건</span><span class="sxs-lookup"><span data-stu-id="adf0e-112">Pre-requisites</span></span>

    - <span data-ttu-id="adf0e-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정</span><span class="sxs-lookup"><span data-stu-id="adf0e-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="adf0e-114">Q# Visual Studio 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-114">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="adf0e-115">[Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="adf0e-115">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>

1. <span data-ttu-id="adf0e-116">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-116">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="adf0e-117">새 Q# 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="adf0e-117">Create a new Q# application</span></span>

        - <span data-ttu-id="adf0e-118">**파일** -> **새로 만들기** -> **프로젝트**로 이동</span><span class="sxs-lookup"><span data-stu-id="adf0e-118">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="adf0e-119">검색 상자에 `Q#` 입력</span><span class="sxs-lookup"><span data-stu-id="adf0e-119">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="adf0e-120">**Q# 애플리케이션**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-120">Select **Q# Application**</span></span>
        - <span data-ttu-id="adf0e-121">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-121">Select **Next**</span></span>
        - <span data-ttu-id="adf0e-122">애플리케이션의 이름 및 위치를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-122">Choose a name and location for your application</span></span>
        - <span data-ttu-id="adf0e-123">**만들기**</span><span class="sxs-lookup"><span data-stu-id="adf0e-123">Select **Create**</span></span>

    - <span data-ttu-id="adf0e-124">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-124">Inspect the project</span></span>

        <span data-ttu-id="adf0e-125">C# 호스트 애플리케이션에 해당하는 `Driver.cs`와 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램에 해당하는 `Operation.qs`의 두 파일이 생성된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-125">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="adf0e-126">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="adf0e-126">Run the application</span></span>

        - <span data-ttu-id="adf0e-127">**디버그** -> **디버깅하지 않고 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-127">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="adf0e-128">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-128">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="adf0e-129">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-129">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <span data-ttu-id="adf0e-130">Visual Studio Code를 사용 하 여 C# Q # + 개발<a name="VSC"></a></span><span class="sxs-lookup"><span data-stu-id="adf0e-130">Develop with Q# + C# using Visual Studio Code <a name="VSC"></a></span></span>

<span data-ttu-id="adf0e-131">Visual Studio Code (VS Code)는 Windows, Linux 및 Mac에서 Q # 프로그램을 개발 하기 위한 풍부한 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-131">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs on Windows, Linux and Mac.</span></span>  <span data-ttu-id="adf0e-132">Q # VS Code 확장에는 Q # 구문 강조 표시, 코드 완성 및 Q # 코드 조각을 위한 지원이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-132">The Q# VS Code extension includes support for Q# syntax highlighting, code completion, and Q# code snippets.</span></span>

1. <span data-ttu-id="adf0e-133">필수 조건</span><span class="sxs-lookup"><span data-stu-id="adf0e-133">Pre-requisites</span></span>

   - [<span data-ttu-id="adf0e-134">VS 코드</span><span class="sxs-lookup"><span data-stu-id="adf0e-134">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="adf0e-135">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="adf0e-135">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="adf0e-136">Quantum VS Code 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-136">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="adf0e-137">[VS Code 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-137">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="adf0e-138">양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-138">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="adf0e-139">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-139">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="adf0e-140">**Q #: 프로젝트 템플릿 설치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-140">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="adf0e-141">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-141">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="adf0e-142">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-142">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="adf0e-143">새 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-143">Create a new project:</span></span>

        - <span data-ttu-id="adf0e-144">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-144">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="adf0e-145">**Q #: 새 프로젝트 만들기를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-145">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="adf0e-146">**독립 실행형 콘솔 응용 프로그램** 선택</span><span class="sxs-lookup"><span data-stu-id="adf0e-146">Select **Standalone console application**</span></span>
        - <span data-ttu-id="adf0e-147">애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-147">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="adf0e-148">프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-148">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="adf0e-149">VS Code에 대 한 C# 확장을 아직 설치 하지 않은 경우 팝업이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-149">If you don't already have the C# extension for VS Code installed, a pop-up will appear.</span></span> <span data-ttu-id="adf0e-150">확장을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-150">Install the extension.</span></span> 

    - <span data-ttu-id="adf0e-151">애플리케이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-151">Run the application:</span></span>

        - <span data-ttu-id="adf0e-152">**터미널** -> **새 터미널** 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-152">Go to **Terminal** -> **New Terminal**</span></span>
        - <span data-ttu-id="adf0e-153">`dotnet run`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-153">Enter `dotnet run`</span></span>
        - <span data-ttu-id="adf0e-154">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="adf0e-154">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="adf0e-155">여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-155">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="adf0e-156">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-156">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <span data-ttu-id="adf0e-157">`dotnet` 명령줄 도구를 사용 C# 하 여 Q # +를 사용 하 여 개발<a name="command"></a></span><span class="sxs-lookup"><span data-stu-id="adf0e-157">Develop with Q# + C# using the `dotnet` command-line tool <a name="command"></a></span></span>

<span data-ttu-id="adf0e-158">물론 간단하게 .NET Core SDK 및 QDK 프로젝트 템플릿을 설치하여 명령줄에서 Q# 프로그램을 빌드하고 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-158">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="adf0e-159">필수 조건</span><span class="sxs-lookup"><span data-stu-id="adf0e-159">Pre-requisites</span></span>

    - [<span data-ttu-id="adf0e-160">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="adf0e-160">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="adf0e-161">.NET용 양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-161">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="adf0e-162">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-162">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="adf0e-163">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-163">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="adf0e-164">새 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="adf0e-164">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="adf0e-165">새 애플리케이션 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-165">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="adf0e-166">애플리케이션의 프로젝트 파일과 함께 Q# 파일(`Operation.qs`) 및 C# 호스트 파일(`Driver.cs`)의 두 파일이 생성된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-166">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="adf0e-167">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="adf0e-167">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="adf0e-168">다음 출력이 표시됩니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="adf0e-168">You should see the following output: `Hello quantum world!`</span></span>

    
## <a name="whats-next"></a><span data-ttu-id="adf0e-169">다음은 무엇일까요?</span><span class="sxs-lookup"><span data-stu-id="adf0e-169">What's next?</span></span>

<span data-ttu-id="adf0e-170">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adf0e-170">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
