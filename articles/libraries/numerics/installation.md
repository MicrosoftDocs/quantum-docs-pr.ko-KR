---
title: 숫자 라이브러리 설치 및 유효성 검사 | Microsoft Docs
description: 숫자 라이브러리 설치 및 유효성 검사
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: c41bb73ea484271689eea2ca1b59ce6639dc15a7
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036460"
---
# <a name="numerics-library-installation-and-validation"></a><span data-ttu-id="f134c-103">숫자 라이브러리 설치 및 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="f134c-103">Numerics Library Installation and Validation</span></span>

<span data-ttu-id="f134c-104">퀀텀 개발 키트는 [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet 패키지를 통해 숫자 기능을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-104">The Quantum Development Kit provides support for numerics functionality through the [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet package.</span></span>

<span data-ttu-id="f134c-105">**Visual Studio > = 2019:** Visual Studio 2019 이상을 사용 하는 경우 NuGet 패키지 관리자를 사용 하 여 숫자 패키지를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-105">**Visual Studio >=2019:** If you are using Visual Studio 2019 or later, you can add the numerics package using the NuGet Package Manager.</span></span>
<span data-ttu-id="f134c-106">이렇게 하려면 "NuGet 패키지 관리 ..."를 선택 합니다. Visual Studio의 "프로젝트" 메뉴 항목에서</span><span class="sxs-lookup"><span data-stu-id="f134c-106">To do so, select "Manage NuGet Packages..." from the "Project" menu item in Visual Studio.</span></span>

<span data-ttu-id="f134c-107">찾아보기 탭에서 "Microsoft. 양자" 패키지 이름을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-107">From the Browse tab, search for the package name "Microsoft.Quantum.Numerics"</span></span>

> [!NOTE]
> <span data-ttu-id="f134c-108">"시험판 포함"을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-108">Make sure to tick "Include prerelease"</span></span>

<span data-ttu-id="f134c-109">그러면 다운로드할 수 있는 패키지가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-109">This will list the packages available for download.</span></span>
<span data-ttu-id="f134c-110">"Microsoft. 양자"를 가리키면 버전 번호 오른쪽에 아래쪽 화살표가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-110">Hovering over "Microsoft.Quantum.Numerics" reveals a downward-pointing arrow to the right of the version number.</span></span>
<span data-ttu-id="f134c-111">숫자 패키지를 설치 하려면 화살표를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-111">Click on the arrow in order to install the numerics package.</span></span>

<span data-ttu-id="f134c-112">자세한 내용은 [패키지 관리자 UI 가이드](https://docs.microsoft.com/nuget/tools/package-manager-ui)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f134c-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="f134c-113">또는 패키지 관리자 콘솔을 사용 하 여 명령줄 인터페이스를 통해 숫자 라이브러리를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-113">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![](../../media/vs2017-nuget-console-menu.png)

<span data-ttu-id="f134c-114">패키지 관리자 콘솔에서 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-114">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="f134c-115">자세한 내용은 [패키지 관리자 콘솔 가이드](https://docs.microsoft.com/nuget/tools/package-manager-console)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f134c-115">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="f134c-116">**명령줄 또는 Visual Studio Code:** 명령줄을 사용 하거나 Visual Studio Code 내에서 `dotnet` 명령을 사용 하 여 NuGet 패키지 참조를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-116">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a><span data-ttu-id="f134c-117">설치 확인</span><span class="sxs-lookup"><span data-stu-id="f134c-117">Verifying your installation</span></span>

<span data-ttu-id="f134c-118">퀀텀 개발 키트의 나머지와 마찬가지로 숫자 라이브러리에는 최대한 빨리 시작 하는 데 도움이 되는 샘플이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-118">Like the rest of the Quantum Development Kit, the numerics library comes with samples that help you get started as quickly as possible.</span></span>
<span data-ttu-id="f134c-119">이러한 예제를 사용 하 여 설치를 테스트 하려면 [주 샘플 리포지토리](https://github.com/Microsoft/Quantum) 를 복제 한 다음 샘플 중 하나를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-119">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum) and then run one of the samples.</span></span>

<span data-ttu-id="f134c-120">[`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) 샘플을 실행 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f134c-120">To run the [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
