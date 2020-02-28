---
title: Microsoft Quantum Development Kit (QDK)를 업데이트 하는 방법 알아보기
description: 'Q # 프로젝트와 Microsoft Quantum Development Kit를 현재 버전으로 업데이트 하는 방법을 설명 합니다.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 264b5640216b2c0a468b625cdef4b9e0123d8b39
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904760"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="d4afd-103">Microsoft Quantum Development Kit (QDK) 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="d4afd-104">Microsoft Quantum Development Kit (QDK)를 최신 버전으로 업데이트 하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="d4afd-105">이 문서에서는 QDK가 이미 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="d4afd-106">를 처음 설치 하는 경우 [설치 가이드](xref:microsoft.quantum.install)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4afd-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="d4afd-107">최신 QDK 릴리스를 최신 상태로 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="d4afd-108">최신 QDK 버전으로 업그레이드 하려면이 업데이트 가이드를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="d4afd-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="d4afd-109">프로세스는 다음 두 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="d4afd-110">기존 Q # 파일 및 프로젝트를 업데이트 하 여 코드를 업데이트 된 구문에 맞게 정렬</span><span class="sxs-lookup"><span data-stu-id="d4afd-110">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="d4afd-111">선택한 개발 환경에 대 한 QDK 자체 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-111">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="d4afd-112">Q # 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-112">Updating Q# Projects</span></span> 

<span data-ttu-id="d4afd-113">Q # 작업을 호스트 하 C# 는 데 또는 Python을 사용 하는지 여부에 관계 없이 다음 지침에 따라 q # 프로젝트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="d4afd-114">먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download)의 최신 버전이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="d4afd-115">명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="d4afd-116">출력이 `3.1.100` 이상 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="d4afd-117">그렇지 않은 경우 [최신 버전](https://dotnet.microsoft.com/download) 을 설치 하 고 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="d4afd-118">그런 다음 설치 (Visual Studio, Visual Studio Code 또는 직접 명령줄)에 따라 아래 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="d4afd-119">Visual Studio의 업데이트 Q # 프로젝트</span><span class="sxs-lookup"><span data-stu-id="d4afd-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="d4afd-120">최신 버전의 Visual Studio 2019로 업데이트 합니다. 지침은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4afd-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="d4afd-121">Visual Studio에서 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-121">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="d4afd-122">메뉴에서 **빌드** -> **솔루션 정리** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-122">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="d4afd-123">각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.0` (또는 라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-123">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="d4afd-124">즉, 다음 폼의 줄을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    <span data-ttu-id="d4afd-125">대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="d4afd-126">솔루션의 모든 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-126">Save and close all files in your solution</span></span>
6. <span data-ttu-id="d4afd-127">**도구** -> **명령줄** -> 를 선택 **개발자 명령 프롬프트**</span><span class="sxs-lookup"><span data-stu-id="d4afd-127">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="d4afd-128">솔루션의 각 프로젝트에 대해 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-128">For each project in the solution, run the following command:</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="d4afd-129">프로젝트에서 다른 Microsoft 양자 패키지 (예: 양자)를 사용 하는 경우에도 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-129">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="d4afd-130">명령 프롬프트를 닫고 **빌드** -> **솔루션 빌드** 를 선택 합니다 (솔루션 다시 빌드를 선택 *하지* 않음).</span><span class="sxs-lookup"><span data-stu-id="d4afd-130">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution)</span></span>

<span data-ttu-id="d4afd-131">이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-131">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="d4afd-132">Visual Studio Code에서 Q # 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-132">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="d4afd-133">Visual Studio Code에서 업데이트할 프로젝트를 포함 하는 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-133">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="d4afd-134">**터미널** -> **새 터미널** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-134">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="d4afd-135">명령줄을 사용 하 여 업데이트 하는 방법에 대 한 지침을 따르세요 (바로 아래).</span><span class="sxs-lookup"><span data-stu-id="d4afd-135">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="d4afd-136">명령줄을 사용 하 여 업데이트 Q # 프로젝트</span><span class="sxs-lookup"><span data-stu-id="d4afd-136">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="d4afd-137">프로젝트 파일이 포함 된 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-137">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="d4afd-138">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="d4afd-138">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="d4afd-139">각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.0` (또는 라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-139">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="d4afd-140">즉, 다음 폼의 줄을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-140">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    <span data-ttu-id="d4afd-141">대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-141">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="d4afd-142">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="d4afd-142">Run the following command:</span></span>

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    <span data-ttu-id="d4afd-143">프로젝트에서 다른 Microsoft 양자 패키지 (예: 양자)를 사용 하는 경우에도 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-143">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="d4afd-144">모든 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-144">Save and close all files.</span></span>
6. <span data-ttu-id="d4afd-145">각 프로젝트 종속성에 대해 1-4을 반복한 다음 주 프로젝트가 포함 된 폴더로 다시 이동 하 고를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-145">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="d4afd-146">이제 Q # 프로젝트를 업데이트 하 고 아래 지침에 따라 QDK 자체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-146">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="d4afd-147">QDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-147">Updating the QDK</span></span>

<span data-ttu-id="d4afd-148">QDK를 업데이트 하는 프로세스는 개발 언어 및 환경에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-148">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="d4afd-149">아래에서 개발 환경을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-149">Select your development environment below.</span></span>

* [<span data-ttu-id="d4afd-150">Python: IQ # 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-150">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="d4afd-151">Jupyter 노트북: IQ # 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-151">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="d4afd-152">Visual Studio: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-152">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="d4afd-153">VS Code: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-153">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="d4afd-154">명령줄 및 C#: 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-154">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="d4afd-155">Python 용 IQ # 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-155">Update IQ# for Python</span></span>

1. <span data-ttu-id="d4afd-156">`iqsharp` 커널을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-156">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="d4afd-157">`iqsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="d4afd-157">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="d4afd-158">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-158">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="d4afd-159">`iqsharp` 버전이 더 높기 때문에 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-159">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="d4afd-160">`qsharp` 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-160">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="d4afd-161">`qsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="d4afd-161">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="d4afd-162">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-162">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="d4afd-163">`.qs` 파일의 위치에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-163">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="d4afd-164">이제 업데이트 된 QDK 버전을 사용 하 여 기존 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-164">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="d4afd-165">Jupyter 노트북용 IQ # 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-165">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="d4afd-166">`iqsharp` 커널을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-166">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="d4afd-167">`iqsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="d4afd-167">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="d4afd-168">다음과 유사하게 출력될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-168">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="d4afd-169">`iqsharp` 버전이 더 높기 때문에 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-169">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="d4afd-170">Jupyter Notebook의 셀에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-170">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="d4afd-171">이제 기존 Jupyter 노트북을 열고 업데이트 된 QDK를 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-171">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="d4afd-172">Visual Studio QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-172">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="d4afd-173">Q # Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-173">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="d4afd-174">Visual Studio에서 [퀀텀 Visual studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 에 대 한 업데이트를 승인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-174">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="d4afd-175">업데이트 수락</span><span class="sxs-lookup"><span data-stu-id="d4afd-175">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4afd-176">프로젝트 템플릿이 확장으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-176">The project templates are updated with the extension.</span></span> <span data-ttu-id="d4afd-177">업데이트 된 템플릿은 새로 만든 프로젝트에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-177">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="d4afd-178">확장이 업데이트 될 때 기존 프로젝트에 대 한 코드는 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-178">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="d4afd-179">VS Code QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-179">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="d4afd-180">퀀텀 VS Code 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-180">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="d4afd-181">다시 시작 VS Code</span><span class="sxs-lookup"><span data-stu-id="d4afd-181">Restart VS Code</span></span>
    - <span data-ttu-id="d4afd-182">**확장** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-182">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="d4afd-183">Visual Studio Code 확장 **에 대 한 Microsoft Quantum Development Kit** 선택</span><span class="sxs-lookup"><span data-stu-id="d4afd-183">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="d4afd-184">확장 다시 로드</span><span class="sxs-lookup"><span data-stu-id="d4afd-184">Reload the extension</span></span>

2. <span data-ttu-id="d4afd-185">퀀텀 프로젝트 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-185">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="d4afd-186">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-186">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="d4afd-187">**Q #: 프로젝트 템플릿 설치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-187">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="d4afd-188">몇 초 후에 "프로젝트 템플릿을 설치 했습니다."를 확인 하는 팝업이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-188">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="d4afd-189">C#`dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="d4afd-189">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="d4afd-190">.NET 용 퀀텀 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4afd-190">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="d4afd-191">다음 단계</span><span class="sxs-lookup"><span data-stu-id="d4afd-191">What's next?</span></span>

<span data-ttu-id="d4afd-192">선호 하는 환경에서 퀀텀 개발 키트를 업데이트 했으므로 계속 해 서 퀀텀 프로그램을 개발 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-192">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="d4afd-193">프로그램을 아직 작성 하지 않은 경우 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.write-program)을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4afd-193">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
