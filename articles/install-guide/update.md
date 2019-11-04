---
title: Microsoft Quantum Development Kit (QDK)를 업데이트 하는 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185854"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="6d6fa-102">Microsoft Quantum Development Kit (QDK) 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="6d6fa-103">Microsoft Quantum Development Kit (QDK)를 최신 버전으로 업데이트 하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="6d6fa-104">이 문서에서는 QDK가 이미 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="6d6fa-105">를 처음 설치 하는 경우 [설치 가이드](xref:microsoft.quantum.install)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="6d6fa-106">업데이트 단계는 개발 환경에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-106">The update steps depend on your development environment.</span></span> <span data-ttu-id="6d6fa-107">다음 섹션에서 환경을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-107">Choose your environment from the following sections.</span></span>

## <a name="python"></a><span data-ttu-id="6d6fa-108">파이썬</span><span class="sxs-lookup"><span data-stu-id="6d6fa-108">Python</span></span>

1. <span data-ttu-id="6d6fa-109">`iqsharp` 커널을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-109">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="6d6fa-110">`iqsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6d6fa-110">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="6d6fa-111">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-111">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="6d6fa-112">`qsharp` 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-112">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="6d6fa-113">`qsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6d6fa-113">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="6d6fa-114">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-114">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="6d6fa-115">이제 업데이트 된 QDK 버전을 사용 하 여 기존 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-115">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="jupyter-notebooks"></a><span data-ttu-id="6d6fa-116">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="6d6fa-116">Jupyter notebooks</span></span>

1. <span data-ttu-id="6d6fa-117">`iqsharp` 커널을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-117">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="6d6fa-118">`iqsharp` 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6d6fa-118">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="6d6fa-119">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-119">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="6d6fa-120">이제 기존 Jupyter 노트북을 열고 업데이트 된 QDK를 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-120">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="c-on-windows-using-visual-studio"></a><span data-ttu-id="6d6fa-121">C#Windows에서 Visual Studio 사용</span><span class="sxs-lookup"><span data-stu-id="6d6fa-121">C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="6d6fa-122">Q # Visual Studio 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-122">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="6d6fa-123">Visual Studio에서 [퀀텀 Visual studio 확장](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) 에 대 한 업데이트를 승인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-123">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="6d6fa-124">업데이트 수락</span><span class="sxs-lookup"><span data-stu-id="6d6fa-124">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="6d6fa-125">프로젝트 템플릿이 확장으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-125">The project templates are updated with the extension.</span></span> <span data-ttu-id="6d6fa-126">업데이트 된 템플릿은 새로 만든 프로젝트에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-126">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="6d6fa-127">확장이 업데이트 될 때 기존 프로젝트에 대 한 코드는 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-127">The code for your existing projects is not updated when the extension is updated.</span></span>

1. <span data-ttu-id="6d6fa-128">QDK 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-128">Update the QDK packages</span></span>

    - <span data-ttu-id="6d6fa-129">기존 응용 프로그램 열기</span><span class="sxs-lookup"><span data-stu-id="6d6fa-129">Open an existing application</span></span>
    - <span data-ttu-id="6d6fa-130">솔루션 탐색기에서 **종속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-130">Select **Dependencies** in the Solution Explorer</span></span>
    - <span data-ttu-id="6d6fa-131">**NuGet 패키지 관리** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-131">Select **Manage NuGet Packages**</span></span>
    - <span data-ttu-id="6d6fa-132">**Microsoft 양자** 패키지를 최신 버전으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-132">Update the **Microsoft.Quantum** packages to the latest version</span></span>

1. <span data-ttu-id="6d6fa-133">이제 최신 QDK를 사용 하 여 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-133">You can now run your application with the latest QDK.</span></span>

## <a name="c-using-vs-code"></a><span data-ttu-id="6d6fa-134">C#, VS Code 사용</span><span class="sxs-lookup"><span data-stu-id="6d6fa-134">C#, using VS Code</span></span>

1. <span data-ttu-id="6d6fa-135">퀀텀 VS Code 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-135">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="6d6fa-136">다시 시작 VS Code</span><span class="sxs-lookup"><span data-stu-id="6d6fa-136">Restart VS Code</span></span>
    - <span data-ttu-id="6d6fa-137">**확장** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-137">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="6d6fa-138">Visual Studio Code 확장 **에 대 한 Microsoft Quantum Development Kit** 선택</span><span class="sxs-lookup"><span data-stu-id="6d6fa-138">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="6d6fa-139">확장 다시 로드</span><span class="sxs-lookup"><span data-stu-id="6d6fa-139">Reload the extension</span></span>

1. <span data-ttu-id="6d6fa-140">퀀텀 프로젝트 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-140">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="6d6fa-141">**보기** -> **명령 팔레트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="6d6fa-141">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="6d6fa-142">**Q #: 프로젝트 템플릿 설치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-142">Select **Q#: Install project templates**</span></span>

1. <span data-ttu-id="6d6fa-143">VS Code에서 기존 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-143">Open an existing application in VS Code</span></span>

   - <span data-ttu-id="6d6fa-144">.Csproj 파일을 편집 하 여 새 패키지 버전을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-144">Edit the .csproj file to add the new package versions</span></span>

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    <span data-ttu-id="6d6fa-145">다른 `Microsoft.Quantum` 패키지를 사용 하는 경우에도 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-145">If you use other `Microsoft.Quantum` packages, update these too.</span></span>

1. <span data-ttu-id="6d6fa-146">이제 업데이트 된 QDK를 사용 하 여 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-146">You can now run your application with the updated QDK</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="6d6fa-147">C#`dotnet` 명령줄 도구 사용</span><span class="sxs-lookup"><span data-stu-id="6d6fa-147">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="6d6fa-148">.NET 용 퀀텀 프로젝트 템플릿 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-148">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="6d6fa-149">기존 응용 프로그램 업데이트 및 실행</span><span class="sxs-lookup"><span data-stu-id="6d6fa-149">Update and run an existing application</span></span>

    - <span data-ttu-id="6d6fa-150">응용 프로그램에서 QDK 패키지 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6d6fa-150">Update the QDK package versions in your application</span></span>

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        <span data-ttu-id="6d6fa-151">응용 프로그램에서 다른 `Microsoft.Quantum` 패키지를 사용 하는 경우에도 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-151">If your application uses any other `Microsoft.Quantum` packages, update these too.</span></span>

    - <span data-ttu-id="6d6fa-152">애플리케이션 실행</span><span class="sxs-lookup"><span data-stu-id="6d6fa-152">Run the application</span></span>

        ```bash
        dotnet run
        ```

    - <span data-ttu-id="6d6fa-153">새 패키지 버전으로 응용 프로그램이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-153">Your application will run with the new package versions</span></span>

## <a name="whats-next"></a><span data-ttu-id="6d6fa-154">다음은 무엇일까요?</span><span class="sxs-lookup"><span data-stu-id="6d6fa-154">What's next?</span></span>

<span data-ttu-id="6d6fa-155">선호 하는 환경에서 퀀텀 개발 키트를 업데이트 했으므로 계속 해 서 퀀텀 프로그램을 개발 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-155">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="6d6fa-156">프로그램을 아직 작성 하지 않은 경우 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.write-program)을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-156">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
