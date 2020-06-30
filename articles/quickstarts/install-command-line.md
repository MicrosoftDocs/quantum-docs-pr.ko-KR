---
title: Q# 명령줄 애플리케이션을 사용하여 개발
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274196"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="a5e7d-102">Q# 명령줄 애플리케이션을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="a5e7d-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="a5e7d-103">Q# 프로그램은 C#, F# 또는 Python과 같은 호스트 언어로 된 드라이버 없이 단독 실행이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a5e7d-104">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="a5e7d-104">Prerequisites</span></span>

- [<span data-ttu-id="a5e7d-105">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="a5e7d-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="a5e7d-106">설치</span><span class="sxs-lookup"><span data-stu-id="a5e7d-106">Installation</span></span>

<span data-ttu-id="a5e7d-107">모든 IDE에서 Q# 명령줄 애플리케이션을 빌드할 수 있지만 Q# 애플리케이션용 VS Code(Visual Studio Code) 또는 Visual Studio IDE를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="a5e7d-108">이러한 도구에서 개발하면 다양한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="a5e7d-109">VS 코드를 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-109">To configure VS Code:</span></span>

1. <span data-ttu-id="a5e7d-110">[VS Code](https://code.visualstudio.com/download)(Windows, Linux 및 Mac)를 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="a5e7d-111">[Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="a5e7d-112">Visual Studio를 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="a5e7d-113">.NET Core 플랫폼 간 개발 워크로드를 사용하도록 설정한 상태에서 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 이상을 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="a5e7d-114">[Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)를 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="a5e7d-115">VS Code를 사용하여 Q#으로 개발</span><span class="sxs-lookup"><span data-stu-id="a5e7d-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="a5e7d-116">Q# 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="a5e7d-117">VS Code를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-117">Open VS Code.</span></span>
2. <span data-ttu-id="a5e7d-118">**보기** -> **명령 팔레트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="a5e7d-119">**Q#: 프로젝트 템플릿 설치**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="a5e7d-120">**Project templates installed successfully**(프로젝트 템플릿이 설치되었습니다)가 표시되면 자체 애플리케이션 및 라이브러리에서 QDK를 사용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="a5e7d-121">새 프로젝트를 만들려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-121">To create a new project:</span></span>

1. <span data-ttu-id="a5e7d-122">**보기** -> **명령 팔레트**를 클릭하고 **Q#: 새 프로젝트 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="a5e7d-123">**Standalone console application**(독립 실행형 콘솔 애플리케이션)을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="a5e7d-124">프로젝트를 저장할 위치로 이동하여 **프로젝트 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="a5e7d-125">프로젝트가 만들어지면 오른쪽 아래에서 **Open new project...** (새 프로젝트 열기)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="a5e7d-126">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-126">Inspect the project.</span></span> <span data-ttu-id="a5e7d-127">`Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="a5e7d-128">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="a5e7d-128">To run the application:</span></span>
1. <span data-ttu-id="a5e7d-129">**터미널** -> **새 터미널**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="a5e7d-130">터미널 프롬프트에 `dotnet run`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="a5e7d-131">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="a5e7d-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="a5e7d-132">여러 루트 폴더가 있는 작업 영역은 현재 VS Code Q# 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="a5e7d-133">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="a5e7d-134">Visual Studio를 사용하여 Q#으로 개발</span><span class="sxs-lookup"><span data-stu-id="a5e7d-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="a5e7d-135">Q# `Hello World` 애플리케이션을 만들어서 Visual Studio 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="a5e7d-136">새 Q# 애플리케이션을 만들려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="a5e7d-137">Visual Studio를 열고 **파일** -> **새로 만들기** -> **프로젝트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="a5e7d-138">검색 상자에 `Q#`을 입력하고 **Q# 애플리케이션**을 선택한 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="a5e7d-139">애플리케이션의 이름과 위치를 입력하고 **만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="a5e7d-140">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-140">Inspect the project.</span></span> <span data-ttu-id="a5e7d-141">`Program.qs`라는 소스 파일이 보입니다. 이것은 콘솔에 메시지를 인쇄하는 간단한 작업을 정의하는 Q# 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="a5e7d-142">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="a5e7d-142">To run the application:</span></span>
1. <span data-ttu-id="a5e7d-143">**디버그** -> **디버그하지 않고 시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="a5e7d-144">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="a5e7d-145">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="a5e7d-146">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a5e7d-146">Next steps</span></span>

<span data-ttu-id="a5e7d-147">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e7d-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
