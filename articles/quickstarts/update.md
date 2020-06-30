---
title: QDK(Quantum Development Kit) 업데이트
description: Q# 프로젝트와 Microsoft Quantum Development Kit를 현재 버전으로 업데이트하는 방법을 설명합니다.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 8d39716c4d4c96ad87862b4b185895aab66cd210
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274080"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="c63f8-103">Microsoft QDK(Quantum Development Kit) 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="c63f8-104">Microsoft QDK(Quantum Development Kit)를 최신 버전으로 업데이트하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="c63f8-105">이 문서에서는 QDK가 이미 설치되어 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="c63f8-106">처음 설치하는 경우에는 [설치 가이드](xref:microsoft.quantum.install)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c63f8-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="c63f8-107">최신 QDK 릴리스를 사용하여 최신 상태로 유지하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="c63f8-108">업데이트 가이드에 따라 최신 QDK 버전으로 업그레이드하세요.</span><span class="sxs-lookup"><span data-stu-id="c63f8-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="c63f8-109">프로세스는 다음 두 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="c63f8-110">기존 Q# 파일 및 프로젝트를 업데이트하여 업데이트된 구문에 맞게 코드를 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="c63f8-111">선택한 개발 환경에 맞게 QDK를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="c63f8-112">Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-112">Updating Q# Projects</span></span> 

<span data-ttu-id="c63f8-113">Q# 작업을 호스트하는 데 C#과 Python 중 무엇을 사용하든, 다음 지침에 따라 Q# 프로젝트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="c63f8-114">먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) 최신 버전이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="c63f8-115">명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="c63f8-116">출력이 `3.1.100` 이상인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="c63f8-117">그렇지 않으면, [최신 버전](https://dotnet.microsoft.com/download)을 설치하고 다시 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="c63f8-118">그런 다음, 설정(Visual Studio, Visual Studio Code 또는 명령줄에서 직접)에 따라 아래 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="c63f8-119">Visual Studio에서 Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="c63f8-120">최신 버전의 Visual Studio 2019로 업데이트합니다. (자세한 내용은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019)를 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="c63f8-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="c63f8-121">Visual Studio에서 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="c63f8-122">메뉴에서 **빌드** -> **솔루션 정리**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="c63f8-123">각 .csproj 파일에서 대상 프레임워크를 `netcoreapp3.1`(라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="c63f8-124">즉, 다음 형태의 줄을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="c63f8-125">대상 프레임워크를 지정하는 방법에 대한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c63f8-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="c63f8-126">아래 줄을 참조하여, 각 .csproj 파일에서 SDK를 `Microsoft.Quantum.Sdk`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="c63f8-127">버전 번호는 사용 가능한 최신 버전이어야 하며 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="c63f8-128">솔루션의 모든 파일을 저장하고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="c63f8-129">**도구** -> **명령줄** -> **개발자 명령 프롬프트**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="c63f8-130">또는 Visual Studio에서 패키지 관리 콘솔을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="c63f8-131">솔루션의 각 프로젝트에 대해 다음 명령을 실행하여 패키지를 **제거**합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="c63f8-132">프로젝트에서 다른 Microsoft.Quantum 또는 Microsoft.Azure.Quantum 패키지(예: Microsoft.Quantum.Numerics)를 사용하는 경우 **add** 명령을 실행하여 사용된 버전을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="c63f8-133">명령 프롬프트를 닫고 **빌드** -> **솔루션 빌드**를 선택합니다. (솔루션 다시 빌드는 선택하지 *마십시오*.)</span><span class="sxs-lookup"><span data-stu-id="c63f8-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="c63f8-134">이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="c63f8-135">Visual Studio Code에서 Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="c63f8-136">Visual Studio Code에서 업데이트할 프로젝트가 포함된 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="c63f8-137">**터미널** -> **새 터미널**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="c63f8-138">명령줄을 사용하여 업데이트하는 지침을 따릅니다(바로 아래).</span><span class="sxs-lookup"><span data-stu-id="c63f8-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="c63f8-139">명령줄을 사용하여 Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="c63f8-140">주 프로젝트 파일이 포함된 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="c63f8-141">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="c63f8-142">QDK의 현재 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="c63f8-143">알아보려면 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토하세요.</span><span class="sxs-lookup"><span data-stu-id="c63f8-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="c63f8-144">버전은 `0.11.2006.207`과 비슷한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="c63f8-145">각 `.csproj` 파일에서 다음 단계를 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="c63f8-146">대상 프레임워크를 `netcoreapp3.1`(라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="c63f8-147">즉, 다음 형태의 줄을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="c63f8-148">대상 프레임워크를 지정하는 방법에 대한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c63f8-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="c63f8-149">프로젝트 정의에서 SDK에 대한 참조를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="c63f8-150">버전 번호가 **3단계**에서 확인한 값과 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="c63f8-151">`Microsoft.Quantum.Development.Kit` 패키지에 대한 참조가 있으면(다음 항목에 지정됨) 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="c63f8-152">모든 Microsoft Quantum 패키지 버전을 가장 최근에 릴리스된 QDK 버전(**3단계**에서 확인함)으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="c63f8-153">해당 패키지는 다음과 같은 패턴으로 이름이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="c63f8-154">패키지에 대한 참조는 다음과 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="c63f8-155">업데이트된 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-155">Save the updated file.</span></span>

    - <span data-ttu-id="c63f8-156">다음을 수행하여 프로젝트의 종속성을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="c63f8-157">주 프로젝트가 포함된 폴더로 다시 이동하여 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="c63f8-158">Q# 프로젝트가 업데이트되었으면 아래 지침에 따라 QDK 자체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="c63f8-159">QDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-159">Updating the QDK</span></span>

<span data-ttu-id="c63f8-160">QDK를 업데이트하는 프로세스는 개발 언어와 환경에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="c63f8-161">아래에서 개발 환경을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="c63f8-161">Select your development environment below.</span></span>

* [<span data-ttu-id="c63f8-162">Python: IQ# 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="c63f8-163">Jupyter Notebook: IQ# 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="c63f8-164">Visual Studio: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="c63f8-165">VS Code: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="c63f8-166">명령줄 및 C#: 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="c63f8-167">Python용 IQ# 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="c63f8-168">`iqsharp` 커널을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="c63f8-169">`iqsharp` 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="c63f8-170">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-170">You should see the following output:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="c63f8-171">`iqsharp` 버전이 더 높아도 [최신 릴리스](xref:microsoft.quantum.relnotes)와 일치하면 괜찮습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="c63f8-172">`qsharp` 패키지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-172">Update the `qsharp` package</span></span>

    ```
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="c63f8-173">`qsharp` 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-173">Verify the `qsharp` version</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="c63f8-174">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-174">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="c63f8-175">`.qs` 파일의 위치에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-175">Run the following command from the location of your `.qs` files</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="c63f8-176">이제 업데이트된 QDK 버전을 사용하여 기존 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="c63f8-177">Jupyter Notebook용 IQ# 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="c63f8-178">`iqsharp` 커널을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="c63f8-179">`iqsharp` 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="c63f8-180">다음과 유사하게 출력될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-180">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="c63f8-181">`iqsharp` 버전이 더 높아도 [최신 릴리스](xref:microsoft.quantum.relnotes)와 일치하면 괜찮습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="c63f8-182">Jupyter Notebook의 셀에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="c63f8-183">이제 기존 Jupyter Notebook을 열고 업데이트된 QDK를 사용하여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="c63f8-184">Visual Studio QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="c63f8-185">Q# Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="c63f8-186">[Quantum Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)에 대한 업데이트를 수락하라는 메시지가 Visual Studio에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="c63f8-187">업데이트를 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="c63f8-188">프로젝트 템플릿이 확장으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="c63f8-189">업데이트된 템플릿은 새로 만든 프로젝트에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="c63f8-190">확장이 업데이트될 때 기존 프로젝트에 대한 코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="c63f8-191">VS Code QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="c63f8-192">Quantum VS Code 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="c63f8-193">VS Code를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-193">Restart VS Code</span></span>
    - <span data-ttu-id="c63f8-194">**확장** 탭으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="c63f8-195">**Microsoft Quantum Development Kit for Visual Studio Code** 확장을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="c63f8-196">확장을 다시 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-196">Reload the extension</span></span>

2. <span data-ttu-id="c63f8-197">Quantum 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="c63f8-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="c63f8-198">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="c63f8-199">**Q#: 프로젝트 템플릿 설치**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="c63f8-200">몇 초 후에 "project templates installed successfully"(프로젝트 템플릿이 설치되었습니다)라는 팝업이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="c63f8-201">C#, `dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="c63f8-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="c63f8-202">.NET용 Quantum 프로젝트 템플릿을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c63f8-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
