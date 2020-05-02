---
title: '드라이버 및 호스트 언어 없이 Q # 프로그램 실행'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706804"
---
# <a name="q-command-line-applications"></a><span data-ttu-id="b9bc4-102">Q # 명령줄 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="b9bc4-102">Q# Command Line Applications</span></span>

<span data-ttu-id="b9bc4-103">Q # 프로그램은 c #, F #, Python 등의 호스트 언어로 드라이버를 사용 하지 않고 직접 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="b9bc4-104">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="b9bc4-104">Pre-requisites</span></span>

- [<span data-ttu-id="b9bc4-105">.NET Core SDK 3.1 이상</span><span class="sxs-lookup"><span data-stu-id="b9bc4-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="b9bc4-106">설치</span><span class="sxs-lookup"><span data-stu-id="b9bc4-106">Installation</span></span>

<span data-ttu-id="b9bc4-107">모든 IDE에서 Q # 명령줄 응용 프로그램을 빌드할 수 있지만, Q # 응용 프로그램에 Visual Studio Code (VS Code) 또는 Visual Studio IDE를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-107">While you can build Q# command line applications in any IDE, we highly recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="b9bc4-108">VS Code 또는 Visual Studio와 QDK Visual Studio Code 확장을 사용 하 여 보다 다양 한 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-108">By using VS Code or Visual Studio and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

- <span data-ttu-id="b9bc4-109">[VS Code](https://code.visualstudio.com/download) (Windows, Linux 및 Mac) 설치</span><span class="sxs-lookup"><span data-stu-id="b9bc4-109">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
- <span data-ttu-id="b9bc4-110">VS Code 또는 [용 Qdk 확장](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) 을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-110">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) OR</span></span>
- <span data-ttu-id="b9bc4-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, .NET Core 플랫폼 간 개발 워크로드 설정</span><span class="sxs-lookup"><span data-stu-id="b9bc4-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>
- <span data-ttu-id="b9bc4-112">[Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="b9bc4-112">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="b9bc4-113">VS Code를 사용 하 여 개발:</span><span class="sxs-lookup"><span data-stu-id="b9bc4-113">Develop with Q# using VS Code</span></span>

<span data-ttu-id="b9bc4-114">양자 프로젝트 템플릿을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-114">Install the Quantum project templates:</span></span>

- <span data-ttu-id="b9bc4-115">**보기** -> **명령 팔레트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="b9bc4-115">Go to **View** -> **Command Palette**</span></span>
- <span data-ttu-id="b9bc4-116">**Q #: 프로젝트 템플릿 설치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-116">Select **Q#: Install project templates**</span></span>

<span data-ttu-id="b9bc4-117">이제 Quantum Development Kit가 설치되었으며 사용자의 애플리케이션 및 라이브러리에서 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-117">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>
- <span data-ttu-id="b9bc4-118">새 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-118">Create a new project:</span></span>
  - <span data-ttu-id="b9bc4-119">**보기** -> **명령 팔레트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="b9bc4-119">Go to **View** -> **Command Palette**</span></span>
  - <span data-ttu-id="b9bc4-120">**Q #: 새 프로젝트 만들기를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-120">Select **Q#: Create New Project**</span></span>
  - <span data-ttu-id="b9bc4-121">**독립 실행형 콘솔 응용 프로그램** 선택</span><span class="sxs-lookup"><span data-stu-id="b9bc4-121">Select **Standalone console application**</span></span>
  - <span data-ttu-id="b9bc4-122">애플리케이션을 만들려는 파일 시스템의 위치로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-122">Navigate to the location on the file system where you would like to create the application</span></span>
  - <span data-ttu-id="b9bc4-123">프로젝트를 만든 후에 **새 프로젝트 열기...** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-123">Click on the **Open new project...** button, once the project has been created</span></span>
        
- <span data-ttu-id="b9bc4-124">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-124">Inspect the project</span></span>
  - <span data-ttu-id="b9bc4-125">메시지를 콘솔에 출력 하는 `Program.qs` 간단한 작업을 정의 하는 Q # 프로그램인 이라는 파일이 생성 된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-125">You should see that a file called `Program.qs` created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="b9bc4-126">애플리케이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-126">Run the application:</span></span>
  - <span data-ttu-id="b9bc4-127">**터미널** -> **새 터미널** 로 이동</span><span class="sxs-lookup"><span data-stu-id="b9bc4-127">Go to **Terminal** -> **New Terminal**</span></span>
  - <span data-ttu-id="b9bc4-128">`dotnet run`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-128">Enter `dotnet run`</span></span>
  - <span data-ttu-id="b9bc4-129">출력 창에 다음 텍스트가 표시되어야 합니다. `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="b9bc4-129">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="b9bc4-130">여러 루트 폴더가 있는 작업 영역은 현재 Visual Studio Code 확장에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-130">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="b9bc4-131">단일 VS Code 작업 영역에 여러 프로젝트가 있는 경우 모든 프로젝트가 동일한 루트 폴더 내에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-131">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="b9bc4-132">Visual Studio를 사용 하 여 Q #을 사용 하 여 개발</span><span class="sxs-lookup"><span data-stu-id="b9bc4-132">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="b9bc4-133">`Hello World` 애플리케이션을 만들어 설치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-133">Verify the installation by creating a `Hello World` application</span></span>

- <span data-ttu-id="b9bc4-134">새 Q# 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="b9bc4-134">Create a new Q# application</span></span>
  - <span data-ttu-id="b9bc4-135">**파일** -> **새로 만들기** -> **프로젝트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="b9bc4-135">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="b9bc4-136">검색 상자에 `Q#` 입력</span><span class="sxs-lookup"><span data-stu-id="b9bc4-136">Type `Q#` in the search box</span></span>
  - <span data-ttu-id="b9bc4-137">**Q# 애플리케이션**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-137">Select **Q# Application**</span></span>
  - <span data-ttu-id="b9bc4-138">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-138">Select **Next**</span></span>
  - <span data-ttu-id="b9bc4-139">애플리케이션의 이름 및 위치를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-139">Choose a name and location for your application</span></span>
  - <span data-ttu-id="b9bc4-140">**만들기** 선택</span><span class="sxs-lookup"><span data-stu-id="b9bc4-140">Select **Create**</span></span>

- <span data-ttu-id="b9bc4-141">프로젝트를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-141">Inspect the project</span></span>
  - <span data-ttu-id="b9bc4-142">라는 `Program.qs` 파일이 만들어진 것을 확인할 수 있습니다 .이는 콘솔에 메시지를 인쇄 하는 간단한 작업을 정의 하는 Q # 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-142">You should see that a file called `Program.qs` has been created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="b9bc4-143">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="b9bc4-143">Run the application</span></span>
  - <span data-ttu-id="b9bc4-144"> -> **디버깅 하지 않고 시작** **을 선택 합니다**.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-144">Select **Debug** -> **Start Without Debugging**</span></span>
  - <span data-ttu-id="b9bc4-145">콘솔 창에 `Hello quantum world!`가 출력된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-145">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="b9bc4-146">단일 Visual Studio 솔루션 내에 여러 프로젝트가 있는 경우 솔루션에 포함된 모든 프로젝트는 솔루션과 동일한 폴더 또는 해당 하위 폴더 중 하나에 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-146">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  


## <a name="whats-next"></a><span data-ttu-id="b9bc4-147">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="b9bc4-147">What's next?</span></span>

<span data-ttu-id="b9bc4-148">지금까지 기본 설정 환경에 Quantum Development Kit를 설치했으므로 [첫 번째 양자 프로그램](xref:microsoft.quantum.write-program)을 작성 및 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc4-148">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
