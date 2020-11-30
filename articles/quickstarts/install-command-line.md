---
title: IDE에서 Q# 애플리케이션을 사용하여 개발
description: 명령 프롬프트에서 실행되는 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: eeb567dedc1b8123b32faf7ed3a42bb51f16a7d2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228732"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a><span data-ttu-id="73048-103">IDE에서 Q# 애플리케이션을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="73048-103">Develop with Q# applications in an IDE</span></span>

<span data-ttu-id="73048-104">Q# 프로그램은 C#, F# 또는 Python과 같은 호스트 언어로 된 드라이버 없이 단독 실행이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-104">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span> <span data-ttu-id="73048-105">Visual Studio Code(VS Code), Visual Studio, Visual Studio Codespaces 또는 편집기/IDE를 사용하여 Q# 애플리케이션을 개발하고 .NET 콘솔에서 애플리케이션을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-105">You can develop Q# applications in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces, or with any editor/IDE and run applications from the .NET console.</span></span> 

## <a name="prerequisites-for-all-environments"></a><span data-ttu-id="73048-106">모든 환경을 위한 사전 요구 사항</span><span class="sxs-lookup"><span data-stu-id="73048-106">Prerequisites for all environments</span></span>

- [<span data-ttu-id="73048-107">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="73048-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="73048-108">설치</span><span class="sxs-lookup"><span data-stu-id="73048-108">Installation</span></span>

<span data-ttu-id="73048-109">모든 IDE에서 Q# 애플리케이션을 빌드할 수 있지만 로컬에서 Q# 애플리케이션을 개발하기 위해 VS Code(Visual Studio Code) 또는 Visual Studio IDE를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="73048-110">웹 브라우저를 통해 클라우드에서 개발하려면 Visual Studio Codespaces를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="73048-111">이러한 환경에서 개발하면 경고, 구문 강조 표시, 프로젝트 템플릿 등의 다양한 QDK 확장 기능을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-111">Developing in these environments leverages the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

### <a name="to-configure-for-vs-code"></a><span data-ttu-id="73048-112">VS 코드에 맞게 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-112">To configure for VS Code:</span></span>

1. <span data-ttu-id="73048-113">[VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="73048-114">[Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

### <a name="to-configure-for-visual-studio"></a><span data-ttu-id="73048-115">Visual Studio에 맞게 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-115">To configure for Visual Studio:</span></span>

1. <span data-ttu-id="73048-116">.NET Core 플랫폼 간 개발 워크로드를 사용하도록 설정한 상태에서 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 이상을 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="73048-117">[Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)를 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

### <a name="to-configure-for-another-environment"></a><span data-ttu-id="73048-118">다른 환경에 맞게 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-118">To configure for another environment:</span></span> 

1. <span data-ttu-id="73048-119">명령 프롬프트에서 다음을 입력</span><span class="sxs-lookup"><span data-stu-id="73048-119">Enter the following at the command prompt</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a><span data-ttu-id="73048-120">Visual Studio Codespaces에 맞게 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-120">To configure for Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="73048-121">[Azure 계정](https://azure.microsoft.com/free/)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73048-121">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="73048-122">Codespaces 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73048-122">Create a Codespaces environment.</span></span> <span data-ttu-id="73048-123">[빠른 시작 가이드](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser)를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="73048-123">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="73048-124">Codespace를 만들 때 "Git 리포지토리" 필드에 `microsoft/Quantum`을 입력하여 QDK 특정 설정을 로드하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-124">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="73048-125">이제 [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments)를 통해 새 환경을 시작하고 브라우저에서 개발을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-125">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="73048-126">또는 VS Code를 로컬에 설치할 수 있고 Codespace를 [원격 환경](https://docs.microsoft.com/visualstudio/online/how-to/vscode)으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-126">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>

## <a name="develop-with-no-locq"></a><span data-ttu-id="73048-127">Q#으로 개발</span><span class="sxs-lookup"><span data-stu-id="73048-127">Develop with Q#</span></span>

<span data-ttu-id="73048-128">사용하는 개발 환경에 해당하는 탭의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="73048-128">Follow the instructions on the tab corresponding to your development environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="73048-129">VS 코드</span><span class="sxs-lookup"><span data-stu-id="73048-129">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="73048-130">새 프로젝트를 만들려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-130">To create a new project:</span></span>

1. <span data-ttu-id="73048-131">**보기** -> **명령 팔레트** 를 클릭하고 **Q#: 새 프로젝트 만들기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-131">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="73048-132">**Standalone console application**(독립 실행형 콘솔 애플리케이션)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-132">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="73048-133">문서를 저장할 위치로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-133">Navigate to the location to save the project.</span></span> <span data-ttu-id="73048-134">프로젝트 이름을 입력하고 **프로젝트 만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-134">Enter the project name and click **Create Project**.</span></span>
4. <span data-ttu-id="73048-135">프로젝트가 만들어지면 오른쪽 아래에서 **Open new project...** (새 프로젝트 열기)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-135">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="73048-136">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-136">Inspect the project.</span></span> <span data-ttu-id="73048-137">`Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="73048-137">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="73048-138">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="73048-138">To run the application:</span></span>

1. <span data-ttu-id="73048-139">**터미널** -> **새 터미널** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-139">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="73048-140">터미널 프롬프트에 `dotnet run`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-140">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="73048-141">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="73048-141">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="73048-142">여러 루트 폴더가 있는 작업 영역은 현재 VS Code Q# 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-142">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="73048-143">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-143">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="73048-144">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73048-144">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="73048-145">Q# `Hello World` 애플리케이션을 만들어서 Visual Studio 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-145">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="73048-146">새 Q# 애플리케이션을 만들려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-146">To create a new Q# application:</span></span>

1. <span data-ttu-id="73048-147">Visual Studio를 열고 **파일** -> **새로 만들기** -> **프로젝트** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-147">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="73048-148">검색 상자에 `Q#`을 입력하고 **Q# 애플리케이션** 을 선택한 후 **다음** 을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-148">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="73048-149">애플리케이션의 이름과 위치를 입력하고 **만들기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-149">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="73048-150">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-150">Inspect the project.</span></span> <span data-ttu-id="73048-151">`Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="73048-151">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="73048-152">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="73048-152">To run the application:</span></span>

1. <span data-ttu-id="73048-153">**디버그** -> **디버그하지 않고 시작** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-153">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="73048-154">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-154">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="73048-155">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-155">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="73048-156">명령 프롬프트를 사용하는 다른 편집기</span><span class="sxs-lookup"><span data-stu-id="73048-156">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="73048-157">Q# `Hello World` 애플리케이션을 만들어서 현재 설치된 환경을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-157">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="73048-158">다음과 같이 새 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73048-158">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="73048-159">다음과 같이 새 애플리케이션 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-159">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="73048-160">이제 이 디렉터리에는 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램인 `Program.qs` 파일이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-160">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="73048-161">텍스트 편집기를 사용하여 이 템플릿을 수정하고 개발자 고유의 퀀텀 애플리케이션으로 덮어쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-161">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="73048-162">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="73048-162">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="73048-163">`Hello quantum world!` 텍스트가 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="73048-163">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="73048-164">다음 단계</span><span class="sxs-lookup"><span data-stu-id="73048-164">Next steps</span></span>

<span data-ttu-id="73048-165">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73048-165">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
