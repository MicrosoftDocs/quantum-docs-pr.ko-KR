---
title: Q# 및 .NET을 사용하여 개발
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 155367dbb1373f00e2b0bd732a5319b32462c9f9
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426496"
---
# <a name="develop-with-q-and-net"></a><span data-ttu-id="86505-102">Q# 및 .NET을 사용하여 개발</span><span class="sxs-lookup"><span data-stu-id="86505-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="86505-103">Q #은 c # 및 F #과 같은 .NET 언어에서 잘 작동 하도록 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="86505-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="86505-104">이 가이드에서는 .NET 언어로 작성 된 호스트 프로그램과 함께 Q #을 사용 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86505-105">사전 요구 사항</span><span class="sxs-lookup"><span data-stu-id="86505-105">Prerequisites</span></span>

- <span data-ttu-id="86505-106">[Q # 명령줄 프로젝트와 함께 사용 하기 위해](xref:microsoft.quantum.install.standalone)퀀텀 개발 키트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="86505-107">Q # 라이브러리 및 .NET 호스트 만들기</span><span class="sxs-lookup"><span data-stu-id="86505-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="86505-108">첫 번째 단계는 q # 라이브러리에 대 한 프로젝트와 Q # 라이브러리에 정의 된 작업 및 함수를 호출 하는 .NET 호스트에 대 한 프로젝트를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="86505-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="86505-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="86505-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="86505-110">새 Q # 라이브러리 만들기</span><span class="sxs-lookup"><span data-stu-id="86505-110">Create a new Q# library</span></span>
  - <span data-ttu-id="86505-111">**파일**  ->  **새로 만들기**  ->  **프로젝트** 로 이동</span><span class="sxs-lookup"><span data-stu-id="86505-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="86505-112">검색 상자에 "Q #" 입력</span><span class="sxs-lookup"><span data-stu-id="86505-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="86505-113">**Q # 라이브러리** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="86505-114">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-114">Select **Next**</span></span>
  - <span data-ttu-id="86505-115">라이브러리의 이름 및 위치 선택</span><span class="sxs-lookup"><span data-stu-id="86505-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="86505-116">"프로젝트 및 솔루션을 동일한 디렉터리에 저장"이 **선택 취소** 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="86505-117">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-117">Select **Create**</span></span>
- <span data-ttu-id="86505-118">새 c # 또는 F # 호스트 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="86505-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="86505-119">**파일** → **새로 만들기** → **프로젝트** 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="86505-120">C # 또는 F에 대해 "콘솔 앱 (.NET Core") "을 선택 합니다. #</span><span class="sxs-lookup"><span data-stu-id="86505-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="86505-121">**다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-121">Select **Next**</span></span>
  - <span data-ttu-id="86505-122">*솔루션*에서 "솔루션에 추가"를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="86505-123">호스트 프로그램의 이름 선택</span><span class="sxs-lookup"><span data-stu-id="86505-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="86505-124">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="86505-125">Visual Studio Code 또는 명령줄</span><span class="sxs-lookup"><span data-stu-id="86505-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="86505-126">새 Q # 라이브러리 만들기</span><span class="sxs-lookup"><span data-stu-id="86505-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="86505-127">새 c # 또는 F # 콘솔 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="86505-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="86505-128">호스트 프로그램에서 참조로 Q # 라이브러리를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="86505-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="86505-129">필드 두 프로젝트에 대 한 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86505-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="86505-130">.NET에서 Q #으로 호출</span><span class="sxs-lookup"><span data-stu-id="86505-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="86505-131">위의 지침에 따라 프로젝트를 설정한 후에는 .NET 콘솔 응용 프로그램에서 Q #을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86505-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="86505-132">Q # 컴파일러는 시뮬레이터에서 퀀텀 프로그램을 실행할 수 있도록 하는 각 Q # 작업 및 함수에 대 한 .NET 클래스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86505-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="86505-133">예를 들어 [.net 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) 에는 다음 Q # 작업 예제가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86505-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="86505-134">퀀텀 시뮬레이터의 .NET에서이 작업을 호출 하려면 `Run` `RunAlgorithm` Q # 컴파일러에 의해 생성 된 .net 클래스의 메서드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86505-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="86505-135">C#</span><span class="sxs-lookup"><span data-stu-id="86505-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="86505-136">F#</span><span class="sxs-lookup"><span data-stu-id="86505-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="86505-137">다음 단계</span><span class="sxs-lookup"><span data-stu-id="86505-137">Next steps</span></span>

<span data-ttu-id="86505-138">이제 Q # 명령줄 프로그램 모두에 대 한 퀀텀 개발 키트를 설정 하 고 .NET과의 상호 운용성을 위해 [첫 번째 퀀텀 프로그램](xref:microsoft.quantum.quickstarts.qrng)을 작성 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86505-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
