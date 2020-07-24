---
title: QDK(Quantum Development Kit) 업데이트
description: Q# 프로젝트와 Microsoft Quantum Development Kit를 현재 버전으로 업데이트하는 방법을 설명합니다.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 69b83997773896583258a4996a61b6f334edf407
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871402"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="a6923-103">Microsoft QDK(Quantum Development Kit) 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="a6923-104">Microsoft QDK(Quantum Development Kit)를 최신 버전으로 업데이트하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="a6923-105">이 문서에서는 QDK가 이미 설치되어 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="a6923-106">처음 설치하는 경우에는 [설치 가이드](xref:microsoft.quantum.install)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6923-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="a6923-107">최신 QDK 릴리스를 사용하여 최신 상태로 유지하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="a6923-108">업데이트 가이드에 따라 최신 QDK 버전으로 업그레이드하세요.</span><span class="sxs-lookup"><span data-stu-id="a6923-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="a6923-109">프로세스는 다음 두 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="a6923-110">기존 Q# 파일 및 프로젝트를 업데이트하여 업데이트된 구문에 맞게 코드를 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="a6923-111">선택한 개발 환경에 맞게 QDK를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="a6923-112">Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-112">Updating Q# Projects</span></span> 

<span data-ttu-id="a6923-113">Q# 작업을 호스트하는 데 C#과 Python 중 무엇을 사용하든, 다음 지침에 따라 Q# 프로젝트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="a6923-114">먼저 [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) 최신 버전이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="a6923-115">명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="a6923-116">출력이 `3.1.100` 이상인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="a6923-117">그렇지 않으면, [최신 버전](https://dotnet.microsoft.com/download)을 설치하고 다시 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="a6923-118">그런 다음, 설정(Visual Studio, Visual Studio Code 또는 명령줄에서 직접)에 따라 아래 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="a6923-119">Visual Studio에서 Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="a6923-120">최신 버전의 Visual Studio 2019로 업데이트합니다. (자세한 내용은 [여기](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019)를 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="a6923-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="a6923-121">Visual Studio에서 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="a6923-122">메뉴에서 **빌드** -> **솔루션 정리**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="a6923-123">각 .csproj 파일에서 대상 프레임워크를 `netcoreapp3.1`(라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="a6923-124">즉, 다음 형태의 줄을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="a6923-125">대상 프레임워크를 지정하는 방법에 대한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6923-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="a6923-126">아래 줄을 참조하여, 각 .csproj 파일에서 SDK를 `Microsoft.Quantum.Sdk`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="a6923-127">버전 번호는 사용 가능한 최신 버전이어야 하며 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    ```

6. <span data-ttu-id="a6923-128">솔루션의 모든 파일을 저장하고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="a6923-129">**도구** -> **명령줄** -> **개발자 명령 프롬프트**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="a6923-130">또는 Visual Studio에서 패키지 관리 콘솔을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="a6923-131">솔루션의 각 프로젝트에 대해 다음 명령을 실행하여 패키지를 **제거**합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="a6923-132">프로젝트에서 다른 Microsoft.Quantum 또는 Microsoft.Azure.Quantum 패키지(예: Microsoft.Quantum.Numerics)를 사용하는 경우 **add** 명령을 실행하여 사용된 버전을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="a6923-133">명령 프롬프트를 닫고 **빌드** -> **솔루션 빌드**를 선택합니다. (솔루션 다시 빌드는 선택하지 *마십시오*.)</span><span class="sxs-lookup"><span data-stu-id="a6923-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="a6923-134">이제 [Visual Studio QDK 확장 업데이트](#update-visual-studio-qdk-extension)로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="a6923-135">Visual Studio Code에서 Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="a6923-136">Visual Studio Code에서 업데이트할 프로젝트가 포함된 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="a6923-137">**터미널** -> **새 터미널**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="a6923-138">명령줄을 사용하여 업데이트하는 지침을 따릅니다(바로 아래).</span><span class="sxs-lookup"><span data-stu-id="a6923-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="a6923-139">명령줄을 사용하여 Q# 프로젝트 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="a6923-140">주 프로젝트 파일이 포함된 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="a6923-141">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="a6923-142">QDK의 현재 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="a6923-143">알아보려면 [릴리스 정보](https://docs.microsoft.com/quantum/relnotes/)를 검토하세요.</span><span class="sxs-lookup"><span data-stu-id="a6923-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="a6923-144">버전은 `0.12.20072031`과 비슷한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-144">The version will be in a format similar to `0.12.20072031`.</span></span>

4. <span data-ttu-id="a6923-145">각 `.csproj` 파일에서 다음 단계를 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="a6923-146">대상 프레임워크를 `netcoreapp3.1`(라이브러리 프로젝트인 경우 `netstandard2.1`)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="a6923-147">즉, 다음 형태의 줄을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="a6923-148">대상 프레임워크를 지정하는 방법에 대한 자세한 내용은 [여기](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6923-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="a6923-149">프로젝트 정의에서 SDK에 대한 참조를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="a6923-150">버전 번호가 **3단계**에서 확인한 값과 일치하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
        ```

    - <span data-ttu-id="a6923-151">`Microsoft.Quantum.Development.Kit` 패키지에 대한 참조가 있으면(다음 항목에 지정됨) 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="a6923-152">모든 Microsoft Quantum 패키지 버전을 가장 최근에 릴리스된 QDK 버전(**3단계**에서 확인함)으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="a6923-153">해당 패키지는 다음과 같은 패턴으로 이름이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="a6923-154">패키지에 대한 참조는 다음과 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.12.20072031" />
        ```

    - <span data-ttu-id="a6923-155">업데이트된 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-155">Save the updated file.</span></span>

    - <span data-ttu-id="a6923-156">다음을 수행하여 프로젝트의 종속성을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="a6923-157">주 프로젝트가 포함된 폴더로 다시 이동하여 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="a6923-158">Q# 프로젝트가 업데이트되었으면 아래 지침에 따라 QDK 자체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="a6923-159">QDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-159">Updating the QDK</span></span>

<span data-ttu-id="a6923-160">QDK를 업데이트하는 프로세스는 개발 언어와 환경에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="a6923-161">아래에서 개발 환경을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="a6923-161">Select your development environment below.</span></span>

* [<span data-ttu-id="a6923-162">Python: `qsharp` 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-162">Python: update the `qsharp` package</span></span>](#update-the-qsharp-python-package)
* [<span data-ttu-id="a6923-163">Jupyter Notebook: IQ# 커널 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-163">Jupyter Notebooks: update the IQ# kernel</span></span>](#update-the-iq-jupyter-kernel)
* [<span data-ttu-id="a6923-164">Visual Studio: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="a6923-165">VS Code: QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="a6923-166">명령줄 및 C#: 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a><span data-ttu-id="a6923-167">`qsharp` Python 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-167">Update the `qsharp` Python package</span></span>

<span data-ttu-id="a6923-168">업데이트 절차는 처음에 conda를 사용하여 설치했는지 아니면 .NET CLI와 pip를 사용하여 설치했는지에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-168">The update procedure depends on whether you originally installed using conda or using the .NET CLI and pip.</span></span>

#### <a name="update-using-conda-recommended"></a>[<span data-ttu-id="a6923-169">conda를 사용하여 업데이트(권장)</span><span class="sxs-lookup"><span data-stu-id="a6923-169">Update using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="a6923-170">`qsharp` 패키지를 설치한 conda 환경을 활성화하고, 다음 명령을 실행하여 환경을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-170">Activate the conda environment where you installed the `qsharp` package, and then run this command to update it:</span></span>

    ```
    conda update -c quantum-engineering qsharp
    ```

1. <span data-ttu-id="a6923-171">`.qs` 파일이 있는 위치에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-171">Run the following command from the location of your `.qs` files:</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="a6923-172">.NET CLI 및 pip를 사용하여 업데이트(고급)</span><span class="sxs-lookup"><span data-stu-id="a6923-172">Update using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="a6923-173">`iqsharp` 커널을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-173">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="a6923-174">`iqsharp` 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-174">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="a6923-175">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-175">You should see the following output:</span></span>

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    <span data-ttu-id="a6923-176">`iqsharp` 버전이 더 높은 경우에는 걱정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-176">Don't worry if your `iqsharp` version is higher.</span></span> <span data-ttu-id="a6923-177">[최신 릴리스](xref:microsoft.quantum.relnotes)와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-177">It should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

1. <span data-ttu-id="a6923-178">다음과 같이 `qsharp` 패키지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-178">Update the `qsharp` package:</span></span>

    ```
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="a6923-179">다음과 같이 `qsharp` 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-179">Verify the `qsharp` version:</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="a6923-180">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-180">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.12.2007.2031
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="a6923-181">`.qs` 파일이 있는 위치에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-181">Run the following command from the location of your `.qs` files:</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

<span data-ttu-id="a6923-182">이제 업데이트된 `qsharp` Python 패키지를 사용하여 기존 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-182">You can now use the updated `qsharp` Python package to run your existing quantum programs.</span></span>

### <a name="update-the-iq-jupyter-kernel"></a><span data-ttu-id="a6923-183">IQ# Jupyter 커널 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-183">Update the IQ# Jupyter kernel</span></span>

<span data-ttu-id="a6923-184">업데이트 절차는 처음에 conda를 사용하여 설치했는지 아니면 .NET CLI와 pip를 사용하여 설치했는지에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-184">The update procedure depends on whether you originally installed using conda or using the .NET CLI and pip.</span></span>

#### <a name="update-using-conda-recommended"></a>[<span data-ttu-id="a6923-185">conda를 사용하여 업데이트(권장)</span><span class="sxs-lookup"><span data-stu-id="a6923-185">Update using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="a6923-186">`qsharp` 패키지를 설치한 conda 환경을 활성화하고, 다음 명령을 실행하여 환경을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-186">Activate the conda environment where you installed the `qsharp` package, and then run this command to update it:</span></span>

    ```
    conda update -c quantum-engineering qsharp
    ```

1. <span data-ttu-id="a6923-187">기존 Q# Jupyter Notebook의 각 셀에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-187">Run the following command from a cell in each of your existing Q# Jupyter Notebooks:</span></span>

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="a6923-188">.NET CLI 및 pip를 사용하여 업데이트(고급)</span><span class="sxs-lookup"><span data-stu-id="a6923-188">Update using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="a6923-189">다음과 같이 `Microsoft.Quantum.IQSharp` 패키지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-189">Update the `Microsoft.Quantum.IQSharp` package:</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="a6923-190">다음과 같이 `iqsharp` 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-190">Verify the `iqsharp` version:</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="a6923-191">다음과 유사하게 출력될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-191">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    <span data-ttu-id="a6923-192">`iqsharp` 버전이 더 높은 경우에는 걱정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-192">Don't worry if your `iqsharp` version is higher.</span></span> <span data-ttu-id="a6923-193">[최신 릴리스](xref:microsoft.quantum.relnotes)와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-193">It should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

1. <span data-ttu-id="a6923-194">기존 Q# Jupyter Notebook의 각 셀에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-194">Run the following command from a cell in each of your existing Q# Jupyter Notebooks:</span></span>

    ```
    %workspace reload
    ```

***

<span data-ttu-id="a6923-195">이제 업데이트된 IQ# 커널을 사용하여 기존 Q# Jupyter Notebook을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-195">You can now use the updated IQ# kernel to run your existing Q# Jupyter Notebooks.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="a6923-196">Visual Studio QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-196">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="a6923-197">Q# Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-197">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="a6923-198">[Quantum Visual Studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)에 대한 업데이트를 수락하라는 메시지가 Visual Studio에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-198">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="a6923-199">업데이트를 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-199">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="a6923-200">프로젝트 템플릿이 확장으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-200">The project templates are updated with the extension.</span></span> <span data-ttu-id="a6923-201">업데이트된 템플릿은 새로 만든 프로젝트에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-201">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="a6923-202">확장이 업데이트될 때 기존 프로젝트에 대한 코드는 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-202">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="a6923-203">VS Code QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-203">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="a6923-204">Quantum VS Code 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-204">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="a6923-205">VS Code를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-205">Restart VS Code</span></span>
    - <span data-ttu-id="a6923-206">**확장** 탭으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-206">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="a6923-207">**Microsoft Quantum Development Kit for Visual Studio Code** 확장을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-207">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="a6923-208">확장을 다시 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-208">Reload the extension</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="a6923-209">C#, `dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="a6923-209">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="a6923-210">.NET용 Quantum 프로젝트 템플릿을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-210">Update the Quantum project templates for .NET</span></span>

    <span data-ttu-id="a6923-211">명령줄에서:</span><span class="sxs-lookup"><span data-stu-id="a6923-211">From the command line:</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

   <span data-ttu-id="a6923-212">또는 명령줄 템플릿을 사용하고 VS Code QDK 확장이 이미 설치되어 있는 경우 확장 자체에서 프로젝트 템플릿을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-212">Alternatively, if you intend to use the command line templates, and already have the VS Code QDK extension installed, you can update the project templates from the extension itself:</span></span>

   - [<span data-ttu-id="a6923-213">QDK 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6923-213">Update the QDK extension</span></span>](#update-vs-code-qdk-extension)
   - <span data-ttu-id="a6923-214">VS Code에서 **보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-214">In VS Code, go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="a6923-215">**Q#: 명령줄 프로젝트 템플릿 설치**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-215">Select **Q#: Install command line project templates**</span></span>
   - <span data-ttu-id="a6923-216">몇 초 후에 "project templates installed successfully"(프로젝트 템플릿이 설치되었습니다)라는 팝업이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a6923-216">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>
