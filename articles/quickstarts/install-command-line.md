---
title: Q# 명령줄 애플리케이션을 사용하여 개발
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 15015d1673f47faf5a13dde516f834916b4319d6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884273"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="f2e53-102">Q# 명령줄 애플리케이션을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="f2e53-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="f2e53-103">Q# 프로그램은 C#, F# 또는 Python과 같은 호스트 언어로 된 드라이버 없이 단독 실행이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2e53-104">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="f2e53-104">Prerequisites</span></span>

- [<span data-ttu-id="f2e53-105">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="f2e53-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="f2e53-106">설치</span><span class="sxs-lookup"><span data-stu-id="f2e53-106">Installation</span></span>

<span data-ttu-id="f2e53-107">모든 IDE에서 Q# 명령줄 애플리케이션을 빌드할 수 있지만 Q# 애플리케이션용 VS Code(Visual Studio Code) 또는 Visual Studio IDE를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="f2e53-108">이러한 환경에서 개발하면 경고, 구문 강조 표시, 프로젝트 템플릿 등의 다양한 QDK 확장 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-108">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="f2e53-109">VS 코드를 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-109">To configure VS Code:</span></span>

1. <span data-ttu-id="f2e53-110">[VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="f2e53-111">[Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="f2e53-112">Visual Studio를 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="f2e53-113">.NET Core 플랫폼 간 개발 워크로드를 사용하도록 설정한 상태에서 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 이상을 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="f2e53-114">[Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)를 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="f2e53-115">다른 환경에 사용하도록 QDK를 설치하려면 명령줄에서 다음을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-115">To install the QDK for another environment, enter in the command line:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a><span data-ttu-id="f2e53-116">Q#으로 개발</span><span class="sxs-lookup"><span data-stu-id="f2e53-116">Develop with Q#</span></span>

<span data-ttu-id="f2e53-117">사용하는 환경에 해당하는 탭의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-117">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="f2e53-118">VS 코드</span><span class="sxs-lookup"><span data-stu-id="f2e53-118">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="f2e53-119">Q# 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-119">Install the Q# project templates:</span></span>

1. <span data-ttu-id="f2e53-120">VS Code를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-120">Open VS Code.</span></span>
2. <span data-ttu-id="f2e53-121">**보기** -> **명령 팔레트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-121">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="f2e53-122">**Q#: 프로젝트 템플릿 설치**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-122">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="f2e53-123">**Project templates installed successfully**(프로젝트 템플릿이 설치되었습니다)가 표시되면 자체 애플리케이션 및 라이브러리에서 QDK를 사용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-123">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="f2e53-124">새 프로젝트를 만들려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-124">To create a new project:</span></span>

1. <span data-ttu-id="f2e53-125">**보기** -> **명령 팔레트**를 클릭하고 **Q#: 새 프로젝트 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-125">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="f2e53-126">**Standalone console application**(독립 실행형 콘솔 애플리케이션)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-126">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="f2e53-127">프로젝트를 저장할 위치로 이동하여 **프로젝트 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-127">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="f2e53-128">프로젝트가 만들어지면 오른쪽 아래에서 **Open new project...** (새 프로젝트 열기)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-128">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="f2e53-129">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-129">Inspect the project.</span></span> <span data-ttu-id="f2e53-130">`Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-130">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="f2e53-131">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="f2e53-131">To run the application:</span></span>
1. <span data-ttu-id="f2e53-132">**터미널** -> **새 터미널**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-132">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="f2e53-133">터미널 프롬프트에 `dotnet run`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-133">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="f2e53-134">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="f2e53-134">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="f2e53-135">여러 루트 폴더가 있는 작업 영역은 현재 VS Code Q# 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-135">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="f2e53-136">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-136">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="f2e53-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2e53-137">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="f2e53-138">Q# `Hello World` 애플리케이션을 만들어서 Visual Studio 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-138">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="f2e53-139">새 Q# 애플리케이션을 만들려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-139">To create a new Q# application:</span></span>
1. <span data-ttu-id="f2e53-140">Visual Studio를 열고 **파일** -> **새로 만들기** -> **프로젝트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-140">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="f2e53-141">검색 상자에 `Q#`을 입력하고 **Q# 애플리케이션**을 선택한 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-141">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="f2e53-142">애플리케이션의 이름과 위치를 입력하고 **만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-142">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="f2e53-143">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-143">Inspect the project.</span></span> <span data-ttu-id="f2e53-144">`Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-144">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="f2e53-145">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="f2e53-145">To run the application:</span></span>
1. <span data-ttu-id="f2e53-146">**디버그** -> **디버그하지 않고 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-146">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="f2e53-147">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-147">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="f2e53-148">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-148">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-line"></a>[<span data-ttu-id="f2e53-149">명령줄을 사용하는 다른 편집기</span><span class="sxs-lookup"><span data-stu-id="f2e53-149">Other editors with the command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="f2e53-150">Q# `Hello World` 애플리케이션을 만들어서 현재 설치된 환경을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-150">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="f2e53-151">다음과 같이 새 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-151">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

2. <span data-ttu-id="f2e53-152">다음과 같이 새 애플리케이션 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-152">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="f2e53-153">이제 이 디렉터리에는 콘솔에 메시지를 출력하는 간단한 작업을 정의하는 Q# 프로그램인 `Program.qs` 파일이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-153">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="f2e53-154">텍스트 편집기를 사용하여 이 템플릿을 수정하고 개발자 고유의 퀀텀 애플리케이션으로 덮어쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-154">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

3. <span data-ttu-id="f2e53-155">다음과 같이 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-155">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

4. <span data-ttu-id="f2e53-156">`Hello quantum world!` 텍스트가 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-156">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="f2e53-157">다음 단계</span><span class="sxs-lookup"><span data-stu-id="f2e53-157">Next steps</span></span>

<span data-ttu-id="f2e53-158">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e53-158">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
