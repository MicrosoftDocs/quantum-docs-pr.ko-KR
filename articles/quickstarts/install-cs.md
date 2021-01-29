---
title: Q# 및 .NET을 사용하여 개발
description: .NET 언어를 사용하여 Q# 애플리케이션을 만드는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: de79c361331766572f5608c341be766e071e01b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844298"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="d6041-103">Q# 및 .NET을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="d6041-103">Develop with Q# and .NET</span></span>

<span data-ttu-id="d6041-104">Q#은 C# 및 F#과 같은 .NET 언어와 잘 작동하도록 빌드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-104">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="d6041-105">이 가이드에서는 .NET 언어로 작성된 호스트 프로그램에서 Q#을 사용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-105">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="d6041-106">먼저 Q# 애플리케이션과 .NET 호스트를 만든 다음, 호스트에서 Q#을 호출하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-106">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d6041-107">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="d6041-107">Prerequisites</span></span>

- <span data-ttu-id="d6041-108">[Q# 프로젝트에서 사용할](xref:microsoft.quantum.install.standalone) Quantum Development Kit를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-108">Install the Quantum Development Kit [for use with Q# projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="d6041-109">Q# 라이브러리 및 .NET 호스트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6041-109">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="d6041-110">첫 번째 단계에서는 Q# 라이브러리용 프로젝트 및 Q# 라이브러리에 정의된 작업 및 함수를 호출할 .NET 호스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-110">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="d6041-111">사용하는 개발 환경에 해당하는 탭의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-111">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="d6041-112">Visual Studio 또는 VS Code 이외의 편집기를 사용하는 경우 간단하게 명령 프로그램 단계를 따르면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-112">If you are using an editor other than Visual Studio or VS Code, simply follow the command prompt steps.</span></span>

### <a name="visual-studio-code-or-command-prompt"></a>[<span data-ttu-id="d6041-113">Visual Studio Code 또는 명령 프롬프트</span><span class="sxs-lookup"><span data-stu-id="d6041-113">Visual Studio Code or command prompt</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="d6041-114">새 Q# 라이브러리 만들기</span><span class="sxs-lookup"><span data-stu-id="d6041-114">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="d6041-115">새 C# 또는 F# 콘솔 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="d6041-115">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="d6041-116">Q# 라이브러리를 호스트 프로그램에서 참조로 추가</span><span class="sxs-lookup"><span data-stu-id="d6041-116">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="d6041-117">[선택 사항] 두 프로젝트 모두에 대한 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="d6041-117">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="d6041-118">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="d6041-118">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="d6041-119">새 Q# 라이브러리 만들기</span><span class="sxs-lookup"><span data-stu-id="d6041-119">Create a new Q# library</span></span>
  - <span data-ttu-id="d6041-120">**파일** -> **새로 만들기** -> **프로젝트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="d6041-120">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="d6041-121">검색 상자에 “Q#” 입력</span><span class="sxs-lookup"><span data-stu-id="d6041-121">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="d6041-122">**Q# 라이브러리** 선택</span><span class="sxs-lookup"><span data-stu-id="d6041-122">Select **Q# Library**</span></span>
  - <span data-ttu-id="d6041-123">**다음** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-123">Select **Next**</span></span>
  - <span data-ttu-id="d6041-124">라이브러리의 이름 및 위치 선택</span><span class="sxs-lookup"><span data-stu-id="d6041-124">Choose a name and location for your library</span></span>
  - <span data-ttu-id="d6041-125">"솔루션 및 프로젝트를 같은 디렉터리에 배치"를 **선택하지 않아야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-125">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="d6041-126">**만들기**</span><span class="sxs-lookup"><span data-stu-id="d6041-126">Select **Create**</span></span>
- <span data-ttu-id="d6041-127">새 C# 또는 F# 호스트 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="d6041-127">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="d6041-128">**파일** → **새로 만들기** → **프로젝트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="d6041-128">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="d6041-129">C# 또는 F#에 대한 "콘솔 앱(.NET Core)" 선택</span><span class="sxs-lookup"><span data-stu-id="d6041-129">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="d6041-130">**다음** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-130">Select **Next**</span></span>
  - <span data-ttu-id="d6041-131">*솔루션* 에서 "솔루션에 추가" 선택</span><span class="sxs-lookup"><span data-stu-id="d6041-131">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="d6041-132">호스트 프로그램의 이름 선택</span><span class="sxs-lookup"><span data-stu-id="d6041-132">Choose a name for your host program</span></span>
  - <span data-ttu-id="d6041-133">**만들기**</span><span class="sxs-lookup"><span data-stu-id="d6041-133">Select **Create**</span></span>

<span data-ttu-id="d6041-134">\*\*_</span><span class="sxs-lookup"><span data-stu-id="d6041-134">\*\*_</span></span>

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="d6041-135">.NET에서 Q# 호출</span><span class="sxs-lookup"><span data-stu-id="d6041-135">Calling into Q# from .NET</span></span>

<span data-ttu-id="d6041-136">위의 지침에 따라 프로젝트를 설정한 후에는 .NET 콘솔 애플리케이션에서 Q#을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-136">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="d6041-137">Q# 컴파일러는 시뮬레이터에서 퀀텀 프로그램을 실행할 수 있도록 각 Q# 작업 및 함수에 대해 .NET 클래스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-137">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="d6041-138">예를 들어 [.NET 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)에는 다음과 같은 Q# 연산 예제가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-138">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="d6041-139">퀀텀 시뮬레이터의 .NET에서 이 작업을 호출하려면 Q# 컴파일러에서 생성된 `RunAlgorithm` .NET 클래스의 `Run` 메서드를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-139">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="d6041-140">C#</span><span class="sxs-lookup"><span data-stu-id="d6041-140">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="d6041-141">F#</span><span class="sxs-lookup"><span data-stu-id="d6041-141">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

<span data-ttu-id="d6041-142">_\*\*</span><span class="sxs-lookup"><span data-stu-id="d6041-142">_\*\*</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="d6041-143">다음 단계</span><span class="sxs-lookup"><span data-stu-id="d6041-143">Next steps</span></span>

<span data-ttu-id="d6041-144">Q# 애플리케이션 및 .NET과의 상호 운용성을 위한 Quantum Development Kit가 설정되었으면 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성하고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6041-144">Now that you have the Quantum Development Kit set up for both Q# applications and interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
