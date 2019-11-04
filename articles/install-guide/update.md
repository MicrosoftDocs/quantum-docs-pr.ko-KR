---
title: Learn how to update the Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ebf1f15d65a12c921cd3f04e4111d463d1060f8e
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463291"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="d411a-102">Update the Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="d411a-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="d411a-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span><span class="sxs-lookup"><span data-stu-id="d411a-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="d411a-104">This article assumes that you already have the QDK installed.</span><span class="sxs-lookup"><span data-stu-id="d411a-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="d411a-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="d411a-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>


## <a name="updating-q-projects"></a><span data-ttu-id="d411a-106">Updating Q# Projects</span><span class="sxs-lookup"><span data-stu-id="d411a-106">Updating Q# Projects</span></span> 

1. <span data-ttu-id="d411a-107">First, install the latest version of the [.NET Core SDK 3.0](https://dotnet.microsoft.com/download) and run the following command in the command prompt:</span><span class="sxs-lookup"><span data-stu-id="d411a-107">First, install the latest version of the [.NET Core SDK 3.0](https://dotnet.microsoft.com/download) and run the following command in the command prompt:</span></span>
```bash
dotnet --version
```
 <span data-ttu-id="d411a-108">Verify the output is 3.0.100 or higher, then follow the instructions below depending on your setup.</span><span class="sxs-lookup"><span data-stu-id="d411a-108">Verify the output is 3.0.100 or higher, then follow the instructions below depending on your setup.</span></span>

### <a name="in-visual-studio"></a><span data-ttu-id="d411a-109">Visual Studio에서</span><span class="sxs-lookup"><span data-stu-id="d411a-109">In Visual Studio</span></span>
 
 1. <span data-ttu-id="d411a-110">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span><span class="sxs-lookup"><span data-stu-id="d411a-110">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
 2. <span data-ttu-id="d411a-111">Open your solution in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d411a-111">Open your solution in Visual Studio</span></span>
 3. <span data-ttu-id="d411a-112">From the menu, select Build > Clean Solution</span><span class="sxs-lookup"><span data-stu-id="d411a-112">From the menu, select Build > Clean Solution</span></span> 
 4. <span data-ttu-id="d411a-113">[Update the target framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span><span class="sxs-lookup"><span data-stu-id="d411a-113">[Update the target framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
 5. <span data-ttu-id="d411a-114">Save and close all files in your solution</span><span class="sxs-lookup"><span data-stu-id="d411a-114">Save and close all files in your solution</span></span>
 6. <span data-ttu-id="d411a-115">Select Tools > Command Line > Developer Command Prompt</span><span class="sxs-lookup"><span data-stu-id="d411a-115">Select Tools > Command Line > Developer Command Prompt</span></span>
 7. <span data-ttu-id="d411a-116">For each project in the solution, run the following command:</span><span class="sxs-lookup"><span data-stu-id="d411a-116">For each project in the solution, run the following command:</span></span>
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
<span data-ttu-id="d411a-117">If your projects use any other Microsoft.Quantum packages, run the command for these too.</span><span class="sxs-lookup"><span data-stu-id="d411a-117">If your projects use any other Microsoft.Quantum packages, run the command for these too.</span></span> 
 8. <span data-ttu-id="d411a-118">Close the command prompt and select Build > Build Solution (do *not* select Rebuild Solution, as rebuilding will initially fail)</span><span class="sxs-lookup"><span data-stu-id="d411a-118">Close the command prompt and select Build > Build Solution (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

### <a name="in-visual-studio-code"></a><span data-ttu-id="d411a-119">In Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="d411a-119">In Visual Studio Code</span></span>

1. <span data-ttu-id="d411a-120">In Visual Studio Code, open the folder containing the project to update</span><span class="sxs-lookup"><span data-stu-id="d411a-120">In Visual Studio Code, open the folder containing the project to update</span></span>
1. <span data-ttu-id="d411a-121">Select Terminal > New Terminal</span><span class="sxs-lookup"><span data-stu-id="d411a-121">Select Terminal > New Terminal</span></span>
1. <span data-ttu-id="d411a-122">Follow the instructions for updating using the command line</span><span class="sxs-lookup"><span data-stu-id="d411a-122">Follow the instructions for updating using the command line</span></span>

### <a name="using-the-command-line"></a><span data-ttu-id="d411a-123">Using the command line</span><span class="sxs-lookup"><span data-stu-id="d411a-123">Using the command line</span></span>

1. <span data-ttu-id="d411a-124">Navigate to the folder containing your project file</span><span class="sxs-lookup"><span data-stu-id="d411a-124">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="d411a-125">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="d411a-125">Run the following command:</span></span>
```bash
dotnet clean [project_name].csproj
```

3. <span data-ttu-id="d411a-126">[Update the target framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span><span class="sxs-lookup"><span data-stu-id="d411a-126">[Update the target framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
4. <span data-ttu-id="d411a-127">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="d411a-127">Run the following command:</span></span>
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
<span data-ttu-id="d411a-128">if your project uses any other Microsoft.Quantum packages, run the command for these too.</span><span class="sxs-lookup"><span data-stu-id="d411a-128">if your project uses any other Microsoft.Quantum packages, run the command for these too.</span></span>

5. <span data-ttu-id="d411a-129">Save and close all files</span><span class="sxs-lookup"><span data-stu-id="d411a-129">Save and close all files</span></span>
6. <span data-ttu-id="d411a-130">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span><span class="sxs-lookup"><span data-stu-id="d411a-130">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a><span data-ttu-id="d411a-131">Update IQ# for Python</span><span class="sxs-lookup"><span data-stu-id="d411a-131">Update IQ# for Python</span></span>

1. <span data-ttu-id="d411a-132">Update the `iqsharp` kernel</span><span class="sxs-lookup"><span data-stu-id="d411a-132">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="d411a-133">Verify the `iqsharp` version</span><span class="sxs-lookup"><span data-stu-id="d411a-133">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="d411a-134">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d411a-134">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```

1. <span data-ttu-id="d411a-135">Update the `qsharp` package</span><span class="sxs-lookup"><span data-stu-id="d411a-135">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="d411a-136">Verify the `qsharp` version</span><span class="sxs-lookup"><span data-stu-id="d411a-136">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="d411a-137">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d411a-137">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. <span data-ttu-id="d411a-138">Run the following command from the location of your `.qs` files</span><span class="sxs-lookup"><span data-stu-id="d411a-138">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. <span data-ttu-id="d411a-139">You can now use the updated QDK version to run your existing quantum programs.</span><span class="sxs-lookup"><span data-stu-id="d411a-139">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="d411a-140">Update IQ# for Jupyter notebooks</span><span class="sxs-lookup"><span data-stu-id="d411a-140">Update IQ# for Jupyter notebooks</span></span>

1. <span data-ttu-id="d411a-141">Update the `iqsharp` kernel</span><span class="sxs-lookup"><span data-stu-id="d411a-141">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="d411a-142">Verify the `iqsharp` version</span><span class="sxs-lookup"><span data-stu-id="d411a-142">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="d411a-143">다음 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d411a-143">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. <span data-ttu-id="d411a-144">Run the following command from a cell in your Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="d411a-144">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

1. <span data-ttu-id="d411a-145">You can now open an existing Jupyter notebook and run it with the updated QDK.</span><span class="sxs-lookup"><span data-stu-id="d411a-145">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="d411a-146">Update Visual Studio QDK extension</span><span class="sxs-lookup"><span data-stu-id="d411a-146">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="d411a-147">Update the Q# Visual Studio extension</span><span class="sxs-lookup"><span data-stu-id="d411a-147">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="d411a-148">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="d411a-148">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="d411a-149">Accept the update</span><span class="sxs-lookup"><span data-stu-id="d411a-149">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="d411a-150">The project templates are updated with the extension.</span><span class="sxs-lookup"><span data-stu-id="d411a-150">The project templates are updated with the extension.</span></span> <span data-ttu-id="d411a-151">The updated templates apply to newly created projects only.</span><span class="sxs-lookup"><span data-stu-id="d411a-151">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="d411a-152">The code for your existing projects is not updated when the extension is updated.</span><span class="sxs-lookup"><span data-stu-id="d411a-152">The code for your existing projects is not updated when the extension is updated.</span></span>

## <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="d411a-153">Update VS Code QDK extension</span><span class="sxs-lookup"><span data-stu-id="d411a-153">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="d411a-154">Update the Quantum VS Code extension</span><span class="sxs-lookup"><span data-stu-id="d411a-154">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="d411a-155">Restart VS Code</span><span class="sxs-lookup"><span data-stu-id="d411a-155">Restart VS Code</span></span>
    - <span data-ttu-id="d411a-156">Navigate to the **Extensions** tab</span><span class="sxs-lookup"><span data-stu-id="d411a-156">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="d411a-157">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span><span class="sxs-lookup"><span data-stu-id="d411a-157">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="d411a-158">Reload the extension</span><span class="sxs-lookup"><span data-stu-id="d411a-158">Reload the extension</span></span>

1. <span data-ttu-id="d411a-159">Update the Quantum project templates:</span><span class="sxs-lookup"><span data-stu-id="d411a-159">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="d411a-160">**보기** -> **명령 팔레트**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="d411a-160">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="d411a-161">Select **Q#: Install project templates**</span><span class="sxs-lookup"><span data-stu-id="d411a-161">Select **Q#: Install project templates**</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="d411a-162">C#, using the `dotnet` command-line tool</span><span class="sxs-lookup"><span data-stu-id="d411a-162">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="d411a-163">Update the Quantum project templates for .NET</span><span class="sxs-lookup"><span data-stu-id="d411a-163">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="d411a-164">다음은 무엇일까요?</span><span class="sxs-lookup"><span data-stu-id="d411a-164">What's next?</span></span>

<span data-ttu-id="d411a-165">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span><span class="sxs-lookup"><span data-stu-id="d411a-165">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="d411a-166">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="d411a-166">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
