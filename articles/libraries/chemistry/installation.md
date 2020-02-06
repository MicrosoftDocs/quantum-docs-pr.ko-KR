---
title: 화학 라이브러리 설치 및 유효성 검사 | Microsoft Docs
description: 화학 라이브러리 설치 및 유효성 검사
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: de13d1814821c612ed74a347dc8ffb5881063576
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036477"
---
# <a name="chemistry-library-installation-and-validation"></a><span data-ttu-id="14449-103">화학 라이브러리 설치 및 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="14449-103">Chemistry Library Installation and Validation</span></span>

<span data-ttu-id="14449-104">퀀텀 개발 키트는 [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) NuGet 패키지를 통해 퀀텀 화학 응용 프로그램에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-104">The Quantum Development Kit provides support for quantum chemistry applications through the [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) NuGet package.</span></span>
<span data-ttu-id="14449-105">다른 NuGet 패키지와 마찬가지로, 프로젝트에 화학 라이브러리를 추가 하는 것은 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-105">As with other NuGet packages, it's straightforward to add the chemistry library to your project.</span></span>

<span data-ttu-id="14449-106">**Visual Studio 2019:** Visual Studio 2019을 사용 하는 경우 NuGet 패키지 관리자를 사용 하 여 퀀텀 화학 패키지를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-106">**Visual Studio 2019:** If you are using Visual Studio 2019, you can add the quantum chemistry packages by using the NuGet Package Manager.</span></span>
<span data-ttu-id="14449-107">패키지 관리자를 열려면 아래 스크린샷에서와 같이 화학 라이브러리를 추가 하려는 프로젝트를 마우스 오른쪽 단추로 클릭 하 고 "NuGet 패키지 관리 ..."를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-107">To open the Package Manager, right-click on the project you'd like to add the chemistry library to and select "Manage NuGet Packages...," as in the screenshot below.</span></span>

![](~/media/vs2017-nuget-manage-packages.png)

<span data-ttu-id="14449-108">찾아보기 탭에서 패키지 이름 "Microsoft. m a."를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-108">From the Browse tab, search for the package name "Microsoft.Quantum.Chemistry."</span></span>

> [!NOTE]
> <span data-ttu-id="14449-109">"시험판 포함"을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-109">Make sure to tick "Include prerelease."</span></span>

![](~/media/vs2017-nuget-package-search.png)

<span data-ttu-id="14449-110">그러면 다운로드할 수 있는 패키지가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14449-110">This will list the packages available for download.</span></span>
<span data-ttu-id="14449-111">왼쪽 창에서 "Microsoft"를 클릭 하 고 오른쪽 창에서 최신 시험판 버전을 선택한 후 "설치"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-111">Click on the "Microsoft.Quantum.Chemistry on the left-hand pane, select the latest pre-release version on the right-hand pane, and click "Install":</span></span>

![](~/media/vs2017-nuget-select-chem.png)

<span data-ttu-id="14449-112">자세한 내용은 [패키지 관리자 UI 가이드](https://docs.microsoft.com/nuget/tools/package-manager-ui)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="14449-113">또는 패키지 관리자 콘솔을 사용 하 여 명령줄 인터페이스를 통해 퀀텀 화학 라이브러리를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-113">Alternatively, you can use the Package Manager Console to add the quantum chemistry library to your project with a command line interface.</span></span>

![](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="14449-114">패키지 관리자 콘솔에서 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-114">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Chemistry
```

<span data-ttu-id="14449-115">자세한 내용은 [패키지 관리자 콘솔 가이드](https://docs.microsoft.com/nuget/tools/package-manager-console)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-115">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="14449-116">**명령줄 또는 Visual Studio Code:** 명령줄을 사용 하거나 Visual Studio Code 내에서 `dotnet` 명령을 사용 하 여 NuGet 패키지 참조를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-116">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a><span data-ttu-id="14449-117">설치 확인</span><span class="sxs-lookup"><span data-stu-id="14449-117">Verifying Your Installation</span></span> 

<span data-ttu-id="14449-118">퀀텀 개발 키트의 나머지와 마찬가지로 퀀텀 화학 라이브러리에는 신속 하 게 시작 및 실행 하는 데 도움이 되는 여러 가지 문서화 된 샘플이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14449-118">Like the rest of the Quantum Development Kit, the quantum chemistry library comes with a number of fully documented samples to help you get up and running quickly.</span></span>
<span data-ttu-id="14449-119">이러한 예제를 사용 하 여 설치를 테스트 하려면 [주 샘플 리포지토리](https://github.com/Microsoft/Quantum)를 복제 한 다음 샘플 중 하나를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-119">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum), then run one of the samples.</span></span>  <span data-ttu-id="14449-120">예를 들어 [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) 샘플을 실행 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-120">For example, to run the [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

<span data-ttu-id="14449-121">리포지토리를 복제 한 후 Microsoft Visual Studio를 사용 하 여 퀀텀 화학 라이브러리의 설치를 확인 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-121">To verify the installation of the quantum chemistry library using Microsoft Visual Studio after cloning the repository:</span></span>
    1. <span data-ttu-id="14449-122">화학 폴더에서 ChemistrySamples 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="14449-122">Open the ChemistrySamples.sln solution in the Chemistry folder.</span></span>  
    2. <span data-ttu-id="14449-123">샘플/1을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-123">Select Samples/1.</span></span> <span data-ttu-id="14449-124">Simple Molecules/MolecularHydrogen를 시작 프로젝트로</span><span class="sxs-lookup"><span data-stu-id="14449-124">Simple Molecules/MolecularHydrogen as the StartUp project.</span></span>
    3. <span data-ttu-id="14449-125">F5 키를 눌러 분자 Hydrogen 퀀텀 단계 예측 데모를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-125">Press F5 to run the molecular Hydrogen quantum phase estimation demo.</span></span>

<span data-ttu-id="14449-126">에너지 수준 값을 예측 하는 방법에 대 한 자세한 내용은 [에너지 수준 예측 가져오기](xref:microsoft.quantum.chemistry.examples.energyestimate) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-126">See [Obtaining energy level estimates](xref:microsoft.quantum.chemistry.examples.energyestimate) for more information on estimating the values of energy levels.</span></span>   


## <a name="using-the-quantum-development-kit-with-nwchem"></a><span data-ttu-id="14449-127">NWChem에서 퀀텀 개발 키트 사용</span><span class="sxs-lookup"><span data-stu-id="14449-127">Using the Quantum Development Kit with NWChem</span></span> ##

<span data-ttu-id="14449-128">MolecularHydrogen 샘플은 수동으로 구성 된 분자 입력 데이터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-128">The MolecularHydrogen sample uses molecular input data that is manually configured.</span></span>  <span data-ttu-id="14449-129">이는 작은 예제에 적합 하지만, 규모의 퀀텀 연금술에는 수백만 또는 수십억 개의 용어로 Hamiltonians 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-129">While this is fine for small examples, quantum chemistry at scale require Hamiltonians with millions or billions of terms.</span></span> <span data-ttu-id="14449-130">확장 가능한 계산 화학 패키지에 의해 생성 된 이러한 Hamiltonians는 너무 커서 수동으로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-130">Such Hamiltonians, generated by scalable computational chemistry packages are too large to import by hand.</span></span> 

<span data-ttu-id="14449-131">퀀텀 개발 키트에 대 한 퀀텀 화학 라이브러리는 계산 연금술 패키지에서 잘 작동 하도록 설계 되었습니다. 특히 태평양 연안 국가의 과학에 게는 EMSL (환경적 분자 연구소)에서 개발한 [**Nwchem**](http://www.nwchem-sw.org/) 계산 화학 플랫폼이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-131">The quantum chemistry library for the Quantum Development Kit is designed to work well with computational chemistry packages, most notably the [**NWChem**](http://www.nwchem-sw.org/) computational chemistry platform developed by the Environmental Molecular Sciences Laboratory (EMSL) at Pacific Northwest National Laboratory.</span></span>
<span data-ttu-id="14449-132">특히 `Microsoft.Quantum.Chemistry` 패키지는 [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)에 표시 되는 퀀텀 화학 시뮬레이션 문제의 인스턴스를 로드 하기 위한 도구를 제공 하며, 최신 버전의 NWChem에서 내보내기도 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-132">In particular, the `Microsoft.Quantum.Chemistry` package provides tools for loading instances of quantum chemistry simulation problems represented in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), also supported for export by recent versions of NWChem.</span></span>

<span data-ttu-id="14449-133">퀀텀 개발 키트와 함께 NWChem을 사용 하 여 시작 하 고 실행 하려면 다음 방법 중 하나를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-133">To get up and running using NWChem together with the Quantum Development Kit, we suggest one of the following methods:</span></span>
- <span data-ttu-id="14449-134">기존 Broombridge [파일을 사용](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)하 여 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-134">Get started using existing Broombridge files provided with the samples at [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span>
- <span data-ttu-id="14449-135">웹 기반 프런트 엔드를 사용 하는 [Microsoft Quantum Development Kit에 대 한 Emsl 화살표 작성기](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 를 사용 하 여 새 Broombridge 분자 입력 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-135">Use the [EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) which is a web-based frontend to NWChem, to generate new Broombridge-formated molecular input files.</span></span>  
- <span data-ttu-id="14449-136">PNNL에서 제공 하는 [Docker 이미지](https://hub.docker.com/r/nwchemorg/nwchem-qc/) 를 사용 하 여 NWChem을 실행 하거나</span><span class="sxs-lookup"><span data-stu-id="14449-136">Use the [Docker image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) provided by PNNL to run NWChem, or</span></span>
- <span data-ttu-id="14449-137">플랫폼용 [NWChem을 컴파일합니다](http://www.nwchem-sw.org/index.php/Compiling_NWChem) .</span><span class="sxs-lookup"><span data-stu-id="14449-137">[Compile NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) for your platform.</span></span>

<span data-ttu-id="14449-138">NWChem을 사용 하 여 퀀텀 개발 ... Kit 화학 라이브러리로 분석 하는 방법에 대 한 자세한 내용은 [NWChem을 사용](xref:microsoft.quantum.chemistry.examples.endtoend) 하 여 종단 간을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-138">See [End-to-end with NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) for more information on how to work with NWChem to chemical models to analyze with the Quantum Developmen Kit chemistry library.</span></span>

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a><span data-ttu-id="14449-139">샘플과 함께 제공 되는 Broombridge 파일을 사용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="14449-139">Getting started using Broombridge files provided with the samples</span></span>

<span data-ttu-id="14449-140">퀀텀 개발 키트 샘플 리포지토리의 [Broombridge 폴더에](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) 는 형식이 인 분자 데이터 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-140">The [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) folder in the Quantum Development Kit Samples repository contains Broombridge-formated molecule data files.</span></span>  

<span data-ttu-id="14449-141">간단한 예로, 화학 라이브러리 샘플 [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) 를 사용 하 여 Broombridge 파일 중 하나에서 Hamiltonian를 로드 하 고 퀀텀 시뮬레이션 algorigthms의 게이트 예측을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-141">As a simple example, use the chemistry library sample, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) to load the Hamiltonian from one of Broombridge files and perform gate estimates of quantum simulation algorigthms:</span></span>

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

<span data-ttu-id="14449-142">Broombridge 스키마가 나타내는 molecules를 입력 하는 방법에 대 한 자세한 내용은 [파일에서 Hamiltonian 로드](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-142">See [Loading a Hamiltonian from file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) for more information on how to input molecules represented by the Broombridge schema.</span></span>  

<span data-ttu-id="14449-143">리소스 [계산](xref:microsoft.quantum.chemistry.examples.resourcecounts) 에 대 한 자세한 내용은 리소스 수 가져오기를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-143">See [Obtaining resource counts](xref:microsoft.quantum.chemistry.examples.resourcecounts) for more information on resource estimation.</span></span>  

### <a name="getting-started-using-the-emsl-arrows-builder"></a><span data-ttu-id="14449-144">EMSL 화살표 작성기를 사용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="14449-144">Getting started using the EMSL Arrows Builder</span></span>

<span data-ttu-id="14449-145">EMSL 화살표는 NWChem 및 화학 계산 데이터베이스를 사용 하 여 분자 데이터를 생성 하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="14449-145">EMSL Arrows is a tool that uses NWChem and chemical computational databases to generate molecule data.</span></span>  <span data-ttu-id="14449-146">[Microsoft Quantum Development Kit에 대 한 Emsl 화살표 작성기](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 를 사용 하면 여러 분자 모델 빌더를 사용 하 여 모델을 입력 하 고 퀀텀 개발 키트에서 사용할 Broombridge 데이터 데이터를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-146">[EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) allows you to enter your model using multiple molecular model builders and generate the Broombridge datafile to be used by the Quantum Development Kit.</span></span>  

<span data-ttu-id="14449-147">EMSL 페이지에서 [' 실행 중인 작업 '] 탭을 클릭 하 고 [' 간단한 예제 '] 지침에 따라 Broombridge 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-147">From the EMSL page, click on the ['Instuctions'] tab, and follow the ['Simple Examples'] instructions to generate Broombridge files.</span></span>  <span data-ttu-id="14449-148">그런 다음 [' GetGateCount ']를 실행 하 여 이러한 molecules에 대 한 퀀텀 리소스 예상치를 확인 하십시오.</span><span class="sxs-lookup"><span data-stu-id="14449-148">Then try running the ['GetGateCount'] to see the quantum resource estimates for these molecules.</span></span>

### <a name="installing-nwchem-from-source"></a><span data-ttu-id="14449-149">원본에서 NWChem 설치</span><span class="sxs-lookup"><span data-stu-id="14449-149">Installing NWChem from Source</span></span>

<span data-ttu-id="14449-150">원본에서 NWChem을 설치 하는 방법에 대 한 전체 지침은 [PNNL에서 제공](http://www.nwchem-sw.org/index.php/Compiling_NWChem)합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-150">Full instructions on how to install NWChem from source [are provided by PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span></span>

> [!TIP]
> <span data-ttu-id="14449-151">Windows 10에서 NWChem을 사용 하려는 경우 Linux 용 Windows 하위 시스템을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-151">If you wish to use NWChem from Windows 10, the Windows Subsystem for Linux is a great option.</span></span>
> <span data-ttu-id="14449-152">[Ubuntu 18.04 LTS For Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)를 설치한 후에는 즐겨 찾는 터미널에서 `ubuntu18.04`를 실행 하 고 위의 지침에 따라 원본에서 NWChem을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-152">Once you have installed [Ubuntu 18.04 LTS for Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), run `ubuntu18.04` from your favorite terminal and follow the instructions above to install NWChem from source.</span></span>

<span data-ttu-id="14449-153">원본에서 NWChem을 컴파일한 후 NWChem과 함께 제공 되는 `yaml_driver` 스크립트를 실행 하 여 NWChem 입력 데크에서 Broombridge 인스턴스를 빠르게 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-153">Once you have compiled NWChem from source, you can run the `yaml_driver` script provided with NWChem to quickly produce Broombridge instances from NWChem input decks:</span></span>

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

<span data-ttu-id="14449-154">이 명령은 현재 디렉터리 내에서 Broombridge 형식으로 새 `input.yaml` 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14449-154">This command will create a new `input.yaml` file in the Broombridge format within your current directory.</span></span>

### <a name="using-nwchem-with-docker"></a><span data-ttu-id="14449-155">Docker에서 NWChem 사용</span><span class="sxs-lookup"><span data-stu-id="14449-155">Using NWChem with Docker</span></span>

<span data-ttu-id="14449-156">NWChem을 사용 하기 위한 미리 빌드된 이미지는 [Docker 허브](https://hub.docker.com)를 통해 플랫폼 간 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14449-156">Pre-built images for using NWChem are available cross-platform via [Docker Hub](https://hub.docker.com).</span></span>
<span data-ttu-id="14449-157">시작 하려면 플랫폼에 대 한 Docker 설치 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="14449-157">To get started, follow the Docker installation instructions for your platform:</span></span>

- [<span data-ttu-id="14449-158">Ubuntu 용 Docker 설치</span><span class="sxs-lookup"><span data-stu-id="14449-158">Install Docker for Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [<span data-ttu-id="14449-159">MacOS 용 Docker 설치</span><span class="sxs-lookup"><span data-stu-id="14449-159">Install Docker for macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)
- [<span data-ttu-id="14449-160">Windows용 Docker 10 설치</span><span class="sxs-lookup"><span data-stu-id="14449-160">Install Docker for Windows 10</span></span>](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> <span data-ttu-id="14449-161">Windows용 Docker를 사용 하는 경우 임시 디렉터리 (일반적으로 `C:\` 드라이브)를 포함 하는 드라이브를 Docker 디먼과 공유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-161">If you are using Docker for Windows, you will need to share the drive containing your temporary directory (usually this is the `C:\` drive) with the Docker daemon.</span></span> <span data-ttu-id="14449-162">자세한 내용은 [Docker 설명서](https://docs.docker.com/docker-for-windows/#shared-drives) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-162">See the [Docker documentation](https://docs.docker.com/docker-for-windows/#shared-drives) for more details.</span></span>

<span data-ttu-id="14449-163">Docker를 설치한 후에는 퀀텀 Development Kit 샘플과 함께 제공 된 PowerShell 모듈을 사용 하 여 이미지를 실행 하거나 이미지를 수동으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-163">Once you have Docker installed, you can either use the PowerShell module provided with the Quantum Development Kit samples to run the image, or you can run the image manually.</span></span>
<span data-ttu-id="14449-164">PowerShell 사용에 대 한 자세한 내용은 여기를 참조 하세요. Docker 이미지를 수동으로 사용 하려는 경우 [이미지와 함께 제공 되는 설명서](https://hub.docker.com/r/nwchemorg/nwchem-qc/)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14449-164">We detail using PowerShell here; if you would like to use the Docker image manually, please see the [documentation provided with the image](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span></span>

#### <a name="running-nwchem-through-powershell-core"></a><span data-ttu-id="14449-165">PowerShell Core를 통해 NWChem 실행</span><span class="sxs-lookup"><span data-stu-id="14449-165">Running NWChem through PowerShell Core</span></span>

<span data-ttu-id="14449-166">퀀텀 개발 키트에서 NWChem Docker 이미지를 사용 하려면 NWChem에서 파일을 이동 하는 것을 처리 하는 작은 PowerShell 모듈을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-166">To use the NWChem Docker image with the Quantum Development Kit, we provide a small PowerShell module that handles moving files in and out of NWChem for you.</span></span>
<span data-ttu-id="14449-167">PowerShell Core를 아직 설치 하지 않은 경우 [GitHub의 powershell 리포지토리에서](https://github.com/PowerShell/PowerShell#get-powershell)플랫폼 간 다운로드를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-167">If you don't already have PowerShell Core installed, you can download it cross-platform from the [PowerShell repository on GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span></span>

> [!NOTE]
> <span data-ttu-id="14449-168">PowerShell Core는 데이터 과학 및 비즈니스 분석 워크플로와의 상호 운용성을 보여 주기 위해 일부 샘플에도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14449-168">PowerShell Core is also used for some samples to demonstrate interoperability with data science and business analytics workflows.</span></span>

<span data-ttu-id="14449-169">PowerShell Core가 설치 되 면 현재 세션에서 NWChem 명령을 사용할 수 있도록 `InvokeNWChem.psm1`를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14449-169">Once you have PowerShell Core installed, import `InvokeNWChem.psm1` to make NWChem commands available in your current session:</span></span>

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

<span data-ttu-id="14449-170">이렇게 하면 현재 PowerShell 세션에서 `Convert-NWChemToBroombridge` 명령을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14449-170">This will make the `Convert-NWChemToBroombridge` command available in your current PowerShell session.</span></span>
<span data-ttu-id="14449-171">Docker에서 필요한 이미지를 다운로드 하 고이를 사용 하 여 NWChem 입력 데크를 실행 하 고 Broombridge에 대 한 출력을 캡처하려면 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="14449-171">To download any needed images from Docker and use them to run NWChem input decks and capture output to Broombridge, run the following:</span></span>

```powershell
Convert-NWChemToBroombridge ./input.nw
```

<span data-ttu-id="14449-172">이렇게 하면 `input.nw`에서 NWChem을 실행 하 여 Broombridge 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14449-172">This will create a Broombridge file by running NWChem on `input.nw`.</span></span>
<span data-ttu-id="14449-173">기본적으로 Broombridge 출력은 입력 데크와 동일한 이름과 경로를 가지 며 `.nw` 확장은 `.yaml`으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14449-173">By default, the Broombridge output will have the same name and path as the input deck, with the `.nw` extension replaced by `.yaml`.</span></span>
<span data-ttu-id="14449-174">`Convert-NWChemToBroombridge`하려면 `-DestinationPath` 매개 변수를 사용 하 여이를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-174">This can be overridden by using the `-DestinationPath` parameter to `Convert-NWChemToBroombridge`.</span></span>
<span data-ttu-id="14449-175">PowerShell의 기본 제공 도움말 기능을 사용 하 여 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14449-175">More information can be obtained by using PowerShell's built-in help functionality:</span></span>

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
