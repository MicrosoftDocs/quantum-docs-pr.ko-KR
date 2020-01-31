---
title: Microsoft Quantum Development Kit (QDK)를 업데이트 하는 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ed2a90749bbe245dde97424fc3191682f995d85b
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819742"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="6f54d-102">Microsoft Quantum Development Kit (QDK) 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="6f54d-103">Microsoft Quantum Development Kit (QDK)를 최신 버전으로 업데이트 하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="6f54d-104">이 문서에서는 QDK가 이미 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="6f54d-105">를 처음 설치 하는 경우 [설치 가이드](xref:microsoft.quantum.install)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f54d-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="6f54d-106">최신 QDK 릴리스를 최신 상태로 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-106">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="6f54d-107">최신 QDK 버전으로 업그레이드 하려면이 업데이트 가이드를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="6f54d-107">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="6f54d-108">프로세스는 다음 두 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-108">The process consists of two parts:</span></span>
1. <span data-ttu-id="6f54d-109">기존 Q # 파일 및 프로젝트를 업데이트 하 여 코드를 업데이트 된 구문에 맞게 정렬</span><span class="sxs-lookup"><span data-stu-id="6f54d-109">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="6f54d-110">선택한 개발 환경에 대 한 QDK 자체 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-110">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="6f54d-111">Q # 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-111">Updating Q# Projects</span></span> 

<span data-ttu-id="6f54d-112">Q # 작업을 호스트 하 C# 는 데 또는 Python을 사용 하는지 여부에 관계 없이 다음 지침에 따라 q # 프로젝트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-112">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="6f54d-113">먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download)의 최신 버전이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-113">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="6f54d-114">명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-114">Run the following command in the command prompt:</span></span>
    ```bash
    dotnet --version
    ```
<span data-ttu-id="6f54d-115">출력이 `3.1.100` 이상 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-115">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="6f54d-116">그렇지 않은 경우 [최신 버전](https://dotnet.microsoft.com/download) 을 설치 하 고 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-116">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="6f54d-117">그런 다음 설치 (Visual Studio, Visual Studio Code 또는 직접 명령줄)에 따라 아래 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-117">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="6f54d-118">Visual Studio의 업데이트 Q # 프로젝트</span><span class="sxs-lookup"><span data-stu-id="6f54d-118">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="6f54d-119">최신 버전의 Visual Studio 2019로 업데이트 합니다. 지침은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f54d-119">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="6f54d-120">Visual Studio에서 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-120">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="6f54d-121">메뉴에서 **빌드** -> **솔루션 정리** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-121">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="6f54d-122">각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.0` (또는 라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-122">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="6f54d-123">즉, 다음 폼의 줄을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-123">That is, edit lines of the form:</span></span>
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    <span data-ttu-id="6f54d-124">대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-124">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="6f54d-125">솔루션의 모든 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-125">Save and close all files in your solution</span></span>
6. <span data-ttu-id="6f54d-126">**도구** -> **명령줄** -> 를 선택 **개발자 명령 프롬프트**</span><span class="sxs-lookup"><span data-stu-id="6f54d-126">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="6f54d-127">솔루션의 각 프로젝트에 대해 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-127">For each project in the solution, run the following command:</span></span>
    ```bash
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```
    <span data-ttu-id="6f54d-128">프로젝트에서 다른 Microsoft 양자 패키지 (예: 양자)를 사용 하는 경우에도 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-128">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="6f54d-129">명령 프롬프트를 닫고 **빌드** -> **솔루션** 빌드를 선택 합니다 (다시 빌드는 처음에 실패 하므로 솔루션 다시 빌드를 선택 *하지* 않음).</span><span class="sxs-lookup"><span data-stu-id="6f54d-129">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

<span data-ttu-id="6f54d-130">이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-130">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="6f54d-131">Visual Studio Code에서 Q # 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-131">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="6f54d-132">Visual Studio Code에서 업데이트할 프로젝트를 포함 하는 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-132">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="6f54d-133">**터미널** -> **새 터미널** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-133">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="6f54d-134">명령줄을 사용 하 여 업데이트 하는 방법에 대 한 지침을 따르세요 (바로 아래).</span><span class="sxs-lookup"><span data-stu-id="6f54d-134">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="6f54d-135">명령줄을 사용 하 여 업데이트 Q # 프로젝트</span><span class="sxs-lookup"><span data-stu-id="6f54d-135">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="6f54d-136">프로젝트 파일이 포함 된 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-136">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="6f54d-137">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="6f54d-137">Run the following command:</span></span>
    ```bash
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="6f54d-138">각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.0` (또는 라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-138">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="6f54d-139">즉, 다음 폼의 줄을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-139">That is, edit lines of the form:</span></span>
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    <span data-ttu-id="6f54d-140">대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-140">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="6f54d-141">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="6f54d-141">Run the following command:</span></span>
    ```bash
    dotnet add package Microsoft.Quantum.Development.Kit
    ```
    <span data-ttu-id="6f54d-142">프로젝트에서 다른 Microsoft 양자 패키지 (예: 양자)를 사용 하는 경우에도 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-142">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="6f54d-143">모든 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-143">Save and close all files.</span></span>
6. <span data-ttu-id="6f54d-144">각 프로젝트 종속성에 대해 1-4을 반복한 다음 주 프로젝트가 포함 된 폴더로 다시 이동 하 고를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-144">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
    ```bash
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="6f54d-145">이제 Q # 프로젝트를 업데이트 하 고 아래 지침에 따라 QDK 자체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-145">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="6f54d-146">QDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-146">Updating the QDK</span></span>

<span data-ttu-id="6f54d-147">QDK를 업데이트 하는 프로세스는 개발 언어 및 환경에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-147">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="6f54d-148">아래에서 개발 환경을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-148">Select your development environment below.</span></span>

* [<span data-ttu-id="6f54d-149">Python: IQ # 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-149">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="6f54d-150">Jupyter 노트북: IQ # 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-150">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="6f54d-151">Visual Studio: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-151">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="6f54d-152">VS Code: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-152">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="6f54d-153">명령줄 및 C#: 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-153">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="6f54d-154">Python 용 IQ # 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-154">Update IQ# for Python</span></span>

1. <span data-ttu-id="6f54d-155">`iqsharp` 커널을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-155">Update the `iqsharp` kernel</span></span> 

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="6f54d-156">`iqsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6f54d-156">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="6f54d-157">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-157">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    <span data-ttu-id="6f54d-158">`iqsharp` 버전이 더 높기 때문에 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-158">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="6f54d-159">`qsharp` 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-159">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="6f54d-160">`qsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6f54d-160">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="6f54d-161">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-161">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
5. <span data-ttu-id="6f54d-162">`.qs` 파일의 위치에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-162">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="6f54d-163">이제 업데이트 된 QDK 버전을 사용 하 여 기존 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-163">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="6f54d-164">Jupyter 노트북용 IQ # 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-164">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="6f54d-165">`iqsharp` 커널을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-165">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="6f54d-166">`iqsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6f54d-166">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="6f54d-167">다음과 유사하게 출력될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-167">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    <span data-ttu-id="6f54d-168">`iqsharp` 버전이 더 높기 때문에 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-168">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="6f54d-169">Jupyter Notebook의 셀에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-169">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

4. <span data-ttu-id="6f54d-170">이제 기존 Jupyter 노트북을 열고 업데이트 된 QDK를 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-170">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="6f54d-171">Visual Studio QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-171">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="6f54d-172">Q # Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-172">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="6f54d-173">Visual Studio에서 [퀀텀 Visual studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 에 대 한 업데이트를 승인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-173">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="6f54d-174">업데이트 수락</span><span class="sxs-lookup"><span data-stu-id="6f54d-174">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f54d-175">프로젝트 템플릿이 확장으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-175">The project templates are updated with the extension.</span></span> <span data-ttu-id="6f54d-176">업데이트 된 템플릿은 새로 만든 프로젝트에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-176">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="6f54d-177">확장이 업데이트 될 때 기존 프로젝트에 대 한 코드는 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-177">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="6f54d-178">VS Code QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-178">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="6f54d-179">퀀텀 VS Code 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-179">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="6f54d-180">다시 시작 VS Code</span><span class="sxs-lookup"><span data-stu-id="6f54d-180">Restart VS Code</span></span>
    - <span data-ttu-id="6f54d-181">**확장** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-181">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="6f54d-182">Visual Studio Code 확장 **에 대 한 Microsoft Quantum Development Kit** 선택</span><span class="sxs-lookup"><span data-stu-id="6f54d-182">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="6f54d-183">확장 다시 로드</span><span class="sxs-lookup"><span data-stu-id="6f54d-183">Reload the extension</span></span>

2. <span data-ttu-id="6f54d-184">퀀텀 프로젝트 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-184">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="6f54d-185">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-185">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="6f54d-186">**Q #: 프로젝트 템플릿 설치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-186">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="6f54d-187">몇 초 후에 "프로젝트 템플릿을 설치 했습니다."를 확인 하는 팝업이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-187">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="6f54d-188">C#`dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="6f54d-188">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="6f54d-189">.NET 용 퀀텀 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="6f54d-189">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="6f54d-190">다음은 무엇일까요?</span><span class="sxs-lookup"><span data-stu-id="6f54d-190">What's next?</span></span>

<span data-ttu-id="6f54d-191">선호 하는 환경에서 퀀텀 개발 키트를 업데이트 했으므로 계속 해 서 퀀텀 프로그램을 개발 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-191">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="6f54d-192">프로그램을 아직 작성 하지 않은 경우 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.write-program)을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f54d-192">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
