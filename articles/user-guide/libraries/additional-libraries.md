---
title: 추가 Q# 라이브러리 사용
description: Q#퀀텀 응용 프로그램에 라이브러리를 추가 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: 39bf7dc52f4670a6e4536efc437d001c96f9584a
ms.sourcegitcommit: 11bd357baeb6ab53a402882979e75964d0869b57
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2020
ms.locfileid: "88992142"
---
# <a name="using-additional-no-locq-libraries"></a><span data-ttu-id="9c912-103">추가 Q# 라이브러리 사용</span><span class="sxs-lookup"><span data-stu-id="9c912-103">Using Additional Q# Libraries</span></span>

<span data-ttu-id="9c912-104">퀀텀 개발 키트는 프로젝트에 추가할 수 있는 _NuGet 패키지_ 를 통해 추가 도메인별 기능을 제공 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="9c912-104">The Quantum Development Kit provides additional domain-specific functionality through _NuGet packages_ that can be added to your Q# projects.</span></span>

| <span data-ttu-id="9c912-105">Q# 라이브러리</span><span class="sxs-lookup"><span data-stu-id="9c912-105">Q# Library</span></span>  | <span data-ttu-id="9c912-106">NuGet 패키지</span><span class="sxs-lookup"><span data-stu-id="9c912-106">NuGet package</span></span> | <span data-ttu-id="9c912-107">메모</span><span class="sxs-lookup"><span data-stu-id="9c912-107">Notes</span></span> |
|---------|---------|--------|
| [<span data-ttu-id="9c912-108">Q# 표준 라이브러리</span><span class="sxs-lookup"><span data-stu-id="9c912-108">Q# standard library</span></span>](xref:microsoft.quantum.libraries.standard.intro) | [<span data-ttu-id="9c912-109">**Microsoft 양자 표준**</span><span class="sxs-lookup"><span data-stu-id="9c912-109">**Microsoft.Quantum.Standard**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | <span data-ttu-id="9c912-110">기본적으로 포함됨</span><span class="sxs-lookup"><span data-stu-id="9c912-110">Included by default</span></span> |
| [<span data-ttu-id="9c912-111">양자 화학 라이브러리</span><span class="sxs-lookup"><span data-stu-id="9c912-111">Quantum chemistry library</span></span>](xref:microsoft.quantum.chemistry.concepts.intro) | [<span data-ttu-id="9c912-112">**Microsoft.Quantum.Chemistry**</span><span class="sxs-lookup"><span data-stu-id="9c912-112">**Microsoft.Quantum.Chemistry**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [<span data-ttu-id="9c912-113">양자 숫자 라이브러리</span><span class="sxs-lookup"><span data-stu-id="9c912-113">Quantum numerics library</span></span>](xref:microsoft.quantum.numerics.intro) | [<span data-ttu-id="9c912-114">**Microsoft 양자**</span><span class="sxs-lookup"><span data-stu-id="9c912-114">**Microsoft.Quantum.Numerics**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [<span data-ttu-id="9c912-115">양자 기계 학습 라이브러리</span><span class="sxs-lookup"><span data-stu-id="9c912-115">Quantum machine learning library</span></span>](xref:microsoft.quantum.libraries.machine-learning.intro) | [<span data-ttu-id="9c912-116">**Microsoft.Quantum.MachineLearning**</span><span class="sxs-lookup"><span data-stu-id="9c912-116">**Microsoft.Quantum.MachineLearning**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

<span data-ttu-id="9c912-117">선호 하는 환경 및 호스트 언어와 함께 사용 하기 위해 퀀텀 개발 키트를 설치한 후에는 추가 설치 없이 개별 프로젝트에 라이브러리를 쉽게 추가할 수 있습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="9c912-117">Once you have installed the Quantum Development Kit for use with your preferred environment and host language, you can easily add libraries to individual Q# projects without any further installation.</span></span>

> [!NOTE]
> <span data-ttu-id="9c912-118">일부 Q# 라이브러리는 프로그램과 함께 작동 Q# 하거나 호스트 응용 프로그램과 통합 되는 추가 도구에서 제대로 작동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-118">Some Q# libraries may work well with additional tools that work alongside your Q# programs, or that integrate with your host applications.</span></span>
> <span data-ttu-id="9c912-119">예를 들어, [화학 라이브러리 설치 지침](xref:microsoft.quantum.chemistry.concepts.installation) 에서는 NWChem 계산 화학 플랫폼과 함께 [ **Microsoft 양자** 패키지](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) 를 사용 하는 방법과 `qdk-chem` 퀀텀 화학 데이터를 사용 하기 위한 명령줄 도구를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-119">For example, the [chemistry library installation instructions](xref:microsoft.quantum.chemistry.concepts.installation) describe how to use the [**Microsoft.Quantum.Chemistry** package](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) together with the NWChem computational chemistry platform, and how to install the `qdk-chem` command-line tools for working with quantum chemistry data.</span></span>

## <a name="no-locq-applications-or-net-interopability"></a>[<span data-ttu-id="9c912-120">Q# 응용 프로그램 또는 .NET interopability</span><span class="sxs-lookup"><span data-stu-id="9c912-120">Q# applications or .NET interopability</span></span>](#tab/tabid-csproj)

<span data-ttu-id="9c912-121">**명령 프롬프트 또는 Visual Studio Code:** 명령 프롬프트를 사용 하거나 Visual Studio Code 내에서 명령을 사용 하 여 `dotnet` NuGet 패키지 참조를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-121">**Command prompt or Visual Studio Code:** Using the command prompt on its own or from within Visual Studio Code, you can use the `dotnet` command to add a NuGet package reference to your project.</span></span>
<span data-ttu-id="9c912-122">예를 들어, [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) 패키지를 추가 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-122">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package, run the following command:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

<span data-ttu-id="9c912-123">**Visual Studio:** Visual Studio 2019 이상을 사용 하는 경우 Q# NuGet 패키지 관리자를 사용 하 여 패키지를 더 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-123">**Visual Studio:** If you are using Visual Studio 2019 or later, you can add additional Q# packages using the NuGet Package Manager.</span></span>
<span data-ttu-id="9c912-124">패키지를 로드 하려면:</span><span class="sxs-lookup"><span data-stu-id="9c912-124">To load a package:</span></span> 
1. <span data-ttu-id="9c912-125">Visual Studio에서 프로젝트를 열고 **프로젝트** 메뉴에서 **NuGet 패키지 관리 ...** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-125">With a project open in Visual Studio, select **Manage NuGet Packages...** from the **Project** menu.</span></span>

2. <span data-ttu-id="9c912-126">**찾아보기**를 클릭 하 고, **시험판 포함** 을 선택 하 고, 패키지 이름 "Microsoft. 양자"를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-126">Click **Browse**, select **Include prerelease** and search for the package name "Microsoft.Quantum.Numerics".</span></span> <span data-ttu-id="9c912-127">그러면 다운로드할 수 있는 패키지가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-127">This will list the packages available for download.</span></span>

3. <span data-ttu-id="9c912-128">**Microsoft. 양자** 를 마우스로 가리키고 버전 번호 오른쪽에 있는 아래쪽 화살표를 클릭 하 여 숫자 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-128">Hover over **Microsoft.Quantum.Numerics** and click the downward-pointing arrow to the right of the version number to install the numerics package.</span></span>

<span data-ttu-id="9c912-129">자세한 내용은 [패키지 관리자 UI 가이드](https://docs.microsoft.com/nuget/tools/package-manager-ui)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c912-129">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="9c912-130">또는 패키지 관리자 콘솔을 사용 하 여 명령줄 인터페이스를 통해 숫자 라이브러리를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-130">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![명령 프롬프트에서 패키지 관리자 콘솔 사용](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="9c912-132">패키지 관리자 콘솔에서 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-132">From the Package Manager Console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="9c912-133">자세한 내용은 [패키지 관리자 콘솔 가이드](https://docs.microsoft.com/nuget/tools/package-manager-console)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c912-133">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

## <a name="ino-locq-notebooks"></a>[<span data-ttu-id="9c912-134">Q#전자 필기장</span><span class="sxs-lookup"><span data-stu-id="9c912-134">IQ# Notebooks</span></span>](#tab/tabid-notebook)

<span data-ttu-id="9c912-135">Q# [ `%package` 매직 명령을](xref:microsoft.quantum.iqsharp.magic-ref.package)사용 하 여 I 노트북에서 추가 패키지를 사용할 수 있도록 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-135">You can make additional packages available for use in an IQ# Notebook by using the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="9c912-136">예를 들어 I 노트북에서 사용할 [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) 패키지를 추가 하려면 Q# 노트북 셀에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-136">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following command in a notebook cell:</span></span>

```
%package Microsoft.Quantum.Numerics
```

<span data-ttu-id="9c912-137">이 명령을 수행 하면 노트북 내의 모든 셀에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-137">Following this command, the package is available to any cells within the notebook.</span></span>
<span data-ttu-id="9c912-138">현재 작업 영역의 코드에서 패키지를 사용할 수 있도록 하려면 Q# 패키지를 추가한 후 작업 영역을 다시 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-138">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```
%workspace reload
```

## <a name="python-interoperability"></a>[<span data-ttu-id="9c912-139">Python 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="9c912-139">Python interoperability</span></span>](#tab/tabid-python)


<span data-ttu-id="9c912-140">메서드를 사용 하 여 Python 호스트 프로그램에서 추가 패키지를 사용할 수 있도록 만들 수 있습니다 [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages) .</span><span class="sxs-lookup"><span data-stu-id="9c912-140">You can make additional packages available for use in a Python host program by using the [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages) method.</span></span>
<span data-ttu-id="9c912-141">예를 들어 I 노트북에서 사용할 [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) 패키지를 추가 하려면 Q# 다음 Python 코드를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-141">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following Python code:</span></span>

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

<span data-ttu-id="9c912-142">이 명령을 수행 하면를 Q# 사용 하 여 컴파일된 모든 코드에서 패키지를 사용할 수 있습니다 `qsharp.compile` .</span><span class="sxs-lookup"><span data-stu-id="9c912-142">Following this command, the package will be made available to any Q# code compiled using `qsharp.compile`.</span></span>
<span data-ttu-id="9c912-143">현재 작업 영역의 코드에서 패키지를 사용할 수 있도록 하려면 Q# 패키지를 추가한 후 작업 영역을 다시 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c912-143">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```python
qsharp.reload()
```

***
