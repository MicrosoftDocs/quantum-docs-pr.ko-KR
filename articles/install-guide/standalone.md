---
title: 'Q # 명령줄 응용 프로그램을 사용 하 여 개발'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630270"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="e3760-102">Q # 명령줄 응용 프로그램을 사용 하 여 개발</span><span class="sxs-lookup"><span data-stu-id="e3760-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="e3760-103">Q # 프로그램은 c #, F #, Python 등의 호스트 언어로 드라이버를 사용 하지 않고 직접 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3760-104">전제 조건</span><span class="sxs-lookup"><span data-stu-id="e3760-104">Prerequisites</span></span>

- [<span data-ttu-id="e3760-105">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="e3760-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="e3760-106">설치</span><span class="sxs-lookup"><span data-stu-id="e3760-106">Installation</span></span>

<span data-ttu-id="e3760-107">모든 IDE에서 Q # 명령줄 응용 프로그램을 빌드할 수 있지만, Q # 응용 프로그램에 Visual Studio Code (VS Code) 또는 Visual Studio IDE를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="e3760-108">이러한 도구에서 개발 하면 다양 한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="e3760-109">VS Code를 구성 하려면:</span><span class="sxs-lookup"><span data-stu-id="e3760-109">To configure VS Code:</span></span>

1. <span data-ttu-id="e3760-110">[VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac)를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="e3760-111">[Microsoft QDK VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="e3760-112">Visual Studio를 구성 하려면:</span><span class="sxs-lookup"><span data-stu-id="e3760-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="e3760-113">.NET Core 플랫폼 간 개발 워크 로드를 사용 하 여 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 이상을 다운로드 하 고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="e3760-114">[Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="e3760-115">VS Code를 사용 하 여 개발:</span><span class="sxs-lookup"><span data-stu-id="e3760-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="e3760-116">Q # 프로젝트 템플릿을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="e3760-117">VS Code를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-117">Open VS Code.</span></span>
2. <span data-ttu-id="e3760-118">**보기**  ->  **명령 팔레트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="e3760-119">**Q #: 프로젝트 템플릿 설치**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="e3760-120">**프로젝트 템플릿이 성공적으로** 표시 되 면 qdk 응용 프로그램 및 라이브러리에서 사용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="e3760-121">새 프로젝트를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-121">To create a new project:</span></span>

1. <span data-ttu-id="e3760-122">**보기**  ->  **명령 팔레트** 를 클릭 하 고 **Q #: 새 프로젝트 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="e3760-123">**독립 실행형 콘솔 응용 프로그램**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="e3760-124">프로젝트를 저장할 위치로 이동 하 고 **프로젝트 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="e3760-125">프로젝트가 성공적으로 생성 되 면 오른쪽 아래에서 **새 프로젝트 열기** ...를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="e3760-126">프로젝트를 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-126">Inspect the project.</span></span> <span data-ttu-id="e3760-127">`Program.qs`콘솔에 메시지를 인쇄 하는 간단한 작업을 정의 하는 Q # 프로그램인 라는 원본 파일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="e3760-128">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="e3760-128">To run the application:</span></span>
1. <span data-ttu-id="e3760-129">**터미널**  ->  **새 터미널**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="e3760-130">터미널 프롬프트에서을 입력 `dotnet run` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="e3760-131">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="e3760-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="e3760-132">여러 루트 폴더가 있는 작업 영역은 현재 VS Code Q # 확장에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="e3760-133">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="e3760-134">Visual Studio를 사용 하 여 Q #을 사용 하 여 개발</span><span class="sxs-lookup"><span data-stu-id="e3760-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="e3760-135">Q # 응용 프로그램을 만들어 Visual Studio 설치를 확인 `Hello World` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="e3760-136">새 Q # 응용 프로그램을 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="e3760-137">Visual Studio를 열고 **파일**  ->  **새로 만들기**  ->  **프로젝트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="e3760-138">`Q#`검색 상자에를 입력 하 고 **Q # 응용 프로그램** 을 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="e3760-139">응용 프로그램의 이름과 위치를 입력 하 고 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="e3760-140">프로젝트를 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-140">Inspect the project.</span></span> <span data-ttu-id="e3760-141">`Program.qs`콘솔에 메시지를 인쇄 하는 간단한 작업을 정의 하는 Q # 프로그램인 라는 원본 파일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="e3760-142">애플리케이션을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="e3760-142">To run the application:</span></span>
1. <span data-ttu-id="e3760-143">**Debug**  ->  **디버깅 하지 않고 시작**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="e3760-144">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="e3760-145">하나의 Visual Studio 솔루션에 여러 프로젝트가 있는 경우 솔루션에 포함 된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="e3760-146">다음 단계</span><span class="sxs-lookup"><span data-stu-id="e3760-146">Next steps</span></span>

<span data-ttu-id="e3760-147">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3760-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
