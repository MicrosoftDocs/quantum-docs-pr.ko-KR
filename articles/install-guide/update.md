---
title: QDK (퀀텀 개발 키트) 업데이트
description: 'Q # 프로젝트와 Microsoft Quantum Development Kit를 현재 버전으로 업데이트 하는 방법을 설명 합니다.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 3245f587493ce12cfec15c8f932fd092d85f688e
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327574"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="38e48-103">Microsoft Quantum Development Kit (QDK) 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="38e48-104">Microsoft Quantum Development Kit (QDK)를 최신 버전으로 업데이트 하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="38e48-105">이 문서에서는 QDK가 이미 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="38e48-106">를 처음 설치 하는 경우 [설치 가이드](xref:microsoft.quantum.install)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="38e48-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="38e48-107">최신 QDK 릴리스를 최신 상태로 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="38e48-108">최신 QDK 버전으로 업그레이드 하려면이 업데이트 가이드를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="38e48-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="38e48-109">프로세스는 다음 두 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="38e48-110">기존 Q # 파일 및 프로젝트를 업데이트 하 여 코드를 업데이트 된 구문에 맞게 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="38e48-111">선택한 개발 환경에 대해 QDK 자체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="38e48-112">Q # 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-112">Updating Q# Projects</span></span> 

<span data-ttu-id="38e48-113">C # 또는 Python을 사용 하 여 Q # 작업을 호스트 하는지 여부에 관계 없이 다음 지침에 따라 Q # 프로젝트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="38e48-114">먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download)의 최신 버전이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="38e48-115">명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="38e48-116">출력이 이상 인지 확인 `3.1.100` 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="38e48-117">그렇지 않은 경우 [최신 버전](https://dotnet.microsoft.com/download) 을 설치 하 고 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="38e48-118">그런 다음 설치 (Visual Studio, Visual Studio Code 또는 직접 명령줄)에 따라 아래 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="38e48-119">Visual Studio의 업데이트 Q # 프로젝트</span><span class="sxs-lookup"><span data-stu-id="38e48-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="38e48-120">최신 버전의 Visual Studio 2019 업데이트에 대 한 지침은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="38e48-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="38e48-121">Visual Studio에서 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="38e48-122">메뉴에서 **Build**  ->  **솔루션 정리**빌드를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="38e48-123">각 .csproj 파일에서 대상 프레임 워크를 `netcoreapp3.1` (또는 `netstandard2.1` 라이브러리 프로젝트인 경우)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="38e48-124">즉, 다음 폼의 줄을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="38e48-125">대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="38e48-126">각 .csproj 파일에서 `Microsoft.Quantum.Sdk` 아래 줄에 표시 된 것 처럼 SDK를로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="38e48-127">버전 번호가 사용 가능한 최신 버전 인지 확인 하 고 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토 하 여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="38e48-128">솔루션의 모든 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="38e48-129">**도구**  ->  **명령줄**  ->  **개발자 명령 프롬프트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="38e48-130">또는 Visual Studio에서 패키지 관리 콘솔을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="38e48-131">솔루션의 각 프로젝트에 대해 다음 명령을 실행 하 여이 패키지를 **제거** 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="38e48-132">프로젝트에서 다른 Microsoft 양자 또는 Microsoft. n a m a. i n i.. n a m a. n a m a 패키지를 사용 하는 경우이에 대 한 **추가** 명령을 실행 하 여 사용 되는 버전을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="38e48-133">명령 프롬프트를 닫고 빌드 솔루션 **빌드**  ->  **Build Solution** 를 선택 합니다 (솔루션 다시 빌드를 선택 *하지* 않음).</span><span class="sxs-lookup"><span data-stu-id="38e48-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="38e48-134">이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="38e48-135">Visual Studio Code에서 Q # 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="38e48-136">Visual Studio Code에서 업데이트할 프로젝트를 포함 하는 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="38e48-137">**터미널**  ->  **새 터미널**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="38e48-138">명령줄을 사용 하 여 업데이트 하는 방법에 대 한 지침을 따르세요 (바로 아래).</span><span class="sxs-lookup"><span data-stu-id="38e48-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="38e48-139">명령줄을 사용 하 여 업데이트 Q # 프로젝트</span><span class="sxs-lookup"><span data-stu-id="38e48-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="38e48-140">주 프로젝트 파일이 포함 된 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="38e48-141">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="38e48-142">QDK의 현재 버전을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="38e48-143">이를 찾으려면 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="38e48-144">버전은와 비슷한 형식으로 되어 `0.11.2006.207` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="38e48-145">각 `.csproj` 파일에서 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="38e48-146">대상 프레임 워크를 `netcoreapp3.1` (또는 `netstandard2.1` 라이브러리 프로젝트인 경우)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="38e48-147">즉, 다음 폼의 줄을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="38e48-148">대상 프레임 워크를 지정 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="38e48-149">프로젝트 정의에서 SDK에 대 한 참조를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="38e48-150">버전 번호가 **3 단계**에서 확인 한 값과 일치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="38e48-151">패키지에 대 한 참조를 제거 합니다 `Microsoft.Quantum.Development.Kit` .이 경우 다음 항목에 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="38e48-152">모든 Microsoft 퀀텀 패키지의 버전을 QDK ( **3 단계**에서 확인)의 가장 최근에 릴리스된 버전으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="38e48-153">이러한 패키지는 다음과 같은 패턴으로 이름이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="38e48-154">패키지에 대 한 참조는 다음과 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="38e48-155">업데이트된 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-155">Save the updated file.</span></span>

    - <span data-ttu-id="38e48-156">다음을 수행 하 여 프로젝트의 종속성을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="38e48-157">주 프로젝트가 포함 된 폴더로 다시 이동 하 여 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="38e48-158">이제 Q # 프로젝트를 업데이트 하 고 아래 지침에 따라 QDK 자체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="38e48-159">QDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-159">Updating the QDK</span></span>

<span data-ttu-id="38e48-160">QDK를 업데이트 하는 프로세스는 개발 언어 및 환경에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="38e48-161">아래에서 개발 환경을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-161">Select your development environment below.</span></span>

* [<span data-ttu-id="38e48-162">Python: IQ # 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="38e48-163">Jupyter 노트북: IQ # 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="38e48-164">Visual Studio: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="38e48-165">VS Code: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="38e48-166">명령줄 및 c #: 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="38e48-167">Python 용 IQ # 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="38e48-168">커널을 업데이트 합니다. `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="38e48-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="38e48-169">버전 확인 `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="38e48-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="38e48-170">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-170">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="38e48-171">`iqsharp`버전이 더 높을 경우 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="38e48-172">패키지 업데이트 `qsharp`</span><span class="sxs-lookup"><span data-stu-id="38e48-172">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="38e48-173">버전 확인 `qsharp`</span><span class="sxs-lookup"><span data-stu-id="38e48-173">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="38e48-174">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-174">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="38e48-175">파일의 위치에서 다음 명령을 실행 합니다. `.qs`</span><span class="sxs-lookup"><span data-stu-id="38e48-175">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="38e48-176">이제 업데이트 된 QDK 버전을 사용 하 여 기존 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="38e48-177">Jupyter 노트북용 IQ # 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="38e48-178">커널을 업데이트 합니다. `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="38e48-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="38e48-179">버전 확인 `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="38e48-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="38e48-180">다음과 유사하게 출력될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-180">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="38e48-181">`iqsharp`버전이 더 높을 경우 [최신 릴리스와](xref:microsoft.quantum.relnotes)일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="38e48-182">Jupyter Notebook의 셀에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="38e48-183">이제 기존 Jupyter 노트북을 열고 업데이트 된 QDK를 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="38e48-184">Visual Studio QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="38e48-185">Q # Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="38e48-186">Visual Studio에서 [퀀텀 Visual studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 에 대 한 업데이트를 승인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="38e48-187">업데이트 수락</span><span class="sxs-lookup"><span data-stu-id="38e48-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="38e48-188">프로젝트 템플릿이 확장으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="38e48-189">업데이트 된 템플릿은 새로 만든 프로젝트에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="38e48-190">확장이 업데이트 될 때 기존 프로젝트에 대 한 코드는 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="38e48-191">VS Code QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="38e48-192">퀀텀 VS Code 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="38e48-193">다시 시작 VS Code</span><span class="sxs-lookup"><span data-stu-id="38e48-193">Restart VS Code</span></span>
    - <span data-ttu-id="38e48-194">**확장** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="38e48-195">Visual Studio Code 확장 **에 대 한 Microsoft Quantum Development Kit** 선택</span><span class="sxs-lookup"><span data-stu-id="38e48-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="38e48-196">확장 다시 로드</span><span class="sxs-lookup"><span data-stu-id="38e48-196">Reload the extension</span></span>

2. <span data-ttu-id="38e48-197">퀀텀 프로젝트 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="38e48-198">**보기**  ->  **명령 팔레트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="38e48-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="38e48-199">**Q #: 프로젝트 템플릿 설치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="38e48-200">몇 초 후에 "프로젝트 템플릿을 설치 했습니다."를 확인 하는 팝업이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38e48-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="38e48-201">C #, `dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="38e48-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="38e48-202">.NET 용 퀀텀 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="38e48-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
