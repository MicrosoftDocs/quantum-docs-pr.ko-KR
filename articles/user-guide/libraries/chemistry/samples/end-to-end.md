---
title: 샘플 NWChem 퀀텀 프로그램
description: NWChem 입력 데크를 사용 하 여 퀀텀 화학 시뮬레이션에 대 한 게이트 수를 가져오는 예제를 살펴봅니다.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/23/2018
uid: microsoft.quantum.chemistry.examples.endtoend
no-loc:
- Q#
- $$v
ms.openlocfilehash: 78d6488ed5e3972f85f1e6cf1ba2d197596c4cc3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869310"
---
# <a name="end-to-end-with-nwchem"></a><span data-ttu-id="0d29d-103">NWChem을 사용하는 엔드투엔드</span><span class="sxs-lookup"><span data-stu-id="0d29d-103">End-to-end with NWChem</span></span> #

<span data-ttu-id="0d29d-104">이 문서에서는 [Nwchem](http://www.nwchem-sw.org/index.php/Main_Page) 입력 데크에서 시작 하 여 퀀텀 화학 시뮬레이션에 대 한 게이트 수를 가져오는 예제를 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-104">In this article, you will walk through an example of getting gate counts for quantum chemistry simulation, starting from an [NWChem](http://www.nwchem-sw.org/index.php/Main_Page) input deck.</span></span>
<span data-ttu-id="0d29d-105">이 예제를 진행 하기 전에 [설치 및 유효성 검사 가이드](xref:microsoft.quantum.chemistry.concepts.installation)에 따라 Docker를 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-105">Before proceeding with this example, make sure that you've installed Docker, following the [installation and validation guide](xref:microsoft.quantum.chemistry.concepts.installation).</span></span>

<span data-ttu-id="0d29d-106">추가 정보</span><span class="sxs-lookup"><span data-stu-id="0d29d-106">For more information:</span></span>
- [<span data-ttu-id="0d29d-107">NWChem 입력 데크 구조</span><span class="sxs-lookup"><span data-stu-id="0d29d-107">Structure of NWChem input decks</span></span>](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [<span data-ttu-id="0d29d-108">퀀텀 개발 키트에 사용할 입력 데크 명령</span><span class="sxs-lookup"><span data-stu-id="0d29d-108">Input deck commands for use with the Quantum Development Kit</span></span>](https://github.com/nwchemgit/nwchem/tree/master/contrib/quasar)
- [<span data-ttu-id="0d29d-109">화학 라이브러리 및 종속성 설치</span><span class="sxs-lookup"><span data-stu-id="0d29d-109">Installing the chemistry library and dependencies</span></span>](xref:microsoft.quantum.chemistry.concepts.installation)
- [<span data-ttu-id="0d29d-110">리소스 계산</span><span class="sxs-lookup"><span data-stu-id="0d29d-110">Resource counting</span></span>](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> <span data-ttu-id="0d29d-111">이 예에서는 Windows PowerShell Core를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-111">This example requires Windows PowerShell Core to run.</span></span>
> <span data-ttu-id="0d29d-112">에서 Windows, macOS 또는 Linux 용 PowerShell Core를 다운로드 https://github.com/PowerShell/PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-112">Download PowerShell Core for Windows, macOS, or Linux at https://github.com/PowerShell/PowerShell.</span></span>

## <a name="importing-required-powershell-modules"></a><span data-ttu-id="0d29d-113">필수 PowerShell 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d29d-113">Importing Required PowerShell Modules</span></span> ##

<span data-ttu-id="0d29d-114">아직 수행 하지 않은 경우에는 퀀텀 개발 키트를 사용 하기 위한 샘플과 유틸리티가 포함 된 [Microsoft/퀀텀 리포지토리](https://github.com/Microsoft/Quantum)를 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-114">If you haven't already done so, clone the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum), which contains samples and utilities for working with the Quantum Development Kit:</span></span>

```powershell
git clone https://github.com/Microsoft/Quantum
```

<span data-ttu-id="0d29d-115">복제 한 후에 `Microsoft/Quantum` `cd` 는 폴더에 대 한 작업을 수행 `utilities/` 하 고 Docker 및 NWChem 작업을 위한 PowerShell 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-115">Once you've cloned `Microsoft/Quantum`, perform `cd` into the `utilities/` folder and import the PowerShell module for working with Docker and NWChem:</span></span>

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> <span data-ttu-id="0d29d-116">기본적으로 Windows는 보안 조치로 스크립트나 모듈을 실행 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-116">By default, Windows prevents the execution of any scripts or modules as a security measure.</span></span>
> <span data-ttu-id="0d29d-117">와 같은 모듈이 `Invoke-NWChem.psm1` Windows에서 실행 되도록 허용 하려면 실행 정책을 변경 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-117">To allow modules such as `Invoke-NWChem.psm1` to run on Windows, you may need to change the execution policy.</span></span>
> <span data-ttu-id="0d29d-118">이렇게 하려면 다음 명령을 실행 합니다 `Set-ExecutionPolicy` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-118">To do so, run the `Set-ExecutionPolicy` command:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> <span data-ttu-id="0d29d-119">그런 다음 PowerShell을 종료 하면 실행 정책이 되돌려집니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-119">The execution policy will then be reverted when you exit PowerShell.</span></span>
> <span data-ttu-id="0d29d-120">실행 정책을 저장 하려면 다음에 대해 다른 값을 사용 합니다 `-Scope` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-120">If you would like to save the execution policy, use a different value for `-Scope`:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

<span data-ttu-id="0d29d-121">이제 `Convert-NWChemToBroombridge` 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-121">You should now have the `Convert-NWChemToBroombridge` command available:</span></span>

```powershell
Get-Command -Module InvokeNWChem
```

<span data-ttu-id="0d29d-122">다음으로 `Get-GateCount` **GetGateCount** 샘플과 함께 제공 된 명령을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-122">Next, we'll import the `Get-GateCount` command provided with the **GetGateCount** sample.</span></span>
<span data-ttu-id="0d29d-123">자세한 내용은 [샘플에서 제공](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount)하는 지침을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d29d-123">For full details, see the [instructions provided with the sample](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount).</span></span>
<span data-ttu-id="0d29d-124">다음으로, `<runtime>` `win10-x64` `osx-x64` `linux-x64` 운영 체제에 따라, 또는로 대체 하 여 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-124">Next, run the following, substituting `<runtime>` with either `win10-x64`, `osx-x64`, or `linux-x64`, depending on your operating system:</span></span>

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

<span data-ttu-id="0d29d-125">이제 `Get-GateCount` 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-125">You should now have the `Get-GateCount` command available:</span></span>

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a><span data-ttu-id="0d29d-126">입력 데크</span><span class="sxs-lookup"><span data-stu-id="0d29d-126">Input Decks</span></span> ##

<span data-ttu-id="0d29d-127">NWChem 패키지는 메모리 할당 설정과 같은 다른 매개 변수와 함께 해결할 퀀텀 화학 문제를 지정 하는 _입력 데크_ 라는 텍스트 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-127">The NWChem package takes a text file called an _input deck_ which specifies a quantum chemistry problem to be solved, along with other parameters such as memory allocation settings.</span></span>
<span data-ttu-id="0d29d-128">이 예제에서는 NWChem과 함께 제공 되는 미리 작성 된 입력 데크 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-128">For this example, we'll use one of the pre-made input decks that comes with NWChem.</span></span>
<span data-ttu-id="0d29d-129">먼저 [nwchemgit/nwchem 리포지토리](https://github.com/nwchemgit/nwchem)를 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-129">First, clone the [nwchemgit/nwchem repository](https://github.com/nwchemgit/nwchem):</span></span>

> [!NOTE]
> <span data-ttu-id="0d29d-130">이는 매우 큰 저장소 이므로 인수를 사용 하 여 일부 대역폭과 디스크 공간을 절약 하기 위해 단순 클론을 수행할 수 있습니다 `--depth 1` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-130">Since this is a very large repository, we can do a shallow clone to save some bandwidth and disk space, using the `--depth 1` argument.</span></span>
> <span data-ttu-id="0d29d-131">그러나이는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-131">This is optional, however.</span></span>
> <span data-ttu-id="0d29d-132">복제는 없이도 제대로 작동 `--depth 1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-132">Cloning will work just fine without `--depth 1`.</span></span>

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

<span data-ttu-id="0d29d-133">`nwchemgit/nwchem`리포지토리는 [ `QA/chem_library_tests` 폴더](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests)아래에 나열 된 퀀텀 개발 키트와 함께 사용 하기 위한 다양 한 입력 데크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-133">The `nwchemgit/nwchem` repository comes with a variety of input decks intended for use with the Quantum Development Kit, listed under the [`QA/chem_library_tests` folder](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests).</span></span>
<span data-ttu-id="0d29d-134">이 예에서는 입력 데크를 사용 합니다 `H4` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-134">For this example, we'll use the `H4` input deck:</span></span>

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

<span data-ttu-id="0d29d-135">분자는 `alpha` 데크 이름에 표시 된 것 처럼 하나의 각도에 따라 달라 지는 특정 기 하 도형에 정렬 된 4 hydrogen 원소의 시스템입니다 `h4_sto6g_alpha.nw` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-135">The molecule in question is a system of 4 hydrogen atoms that are arranged in a certain geometry that depends on one angle, the parameter `alpha` as indicated in the name `h4_sto6g_alpha.nw` of the deck.</span></span> <span data-ttu-id="0d29d-136">H4은 1970 년대 이후 계산 연금술에 대해 알려진 [분자 벤치 마크](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) 입니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-136">H4 is a known [molecular benchmark](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) for computational chemistry since the 1970s.</span></span> <span data-ttu-id="0d29d-137">매개 변수는 `sto6g` 데크에서 Slater 형식 궤도와 관련 된 표현을 구현 하는 것을 의미 합니다. 특히, 6 가우스 기준 함수를 사용 하 여 [설정](https://en.wikipedia.org/wiki/STO-nG_basis_sets) 하는 방법에 대 한 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-137">The parameter `sto6g` is indicative that the deck implements a representation with respect to a Slater-type orbital, specifically, a representation with respect to an [STO-nG basis set](https://en.wikipedia.org/wiki/STO-nG_basis_sets) with 6 Gaussian basis functions.</span></span> <span data-ttu-id="0d29d-138">또한이 입력 데크는 NWChem을 사용 하 여 퀀텀 개발 키트와 상호 운용 하는 데 필요한 정보를 생성 하는 NWChem 텐서 축약 Engine (TCE)에 대 한 몇 가지 지침을 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-138">This input deck furthermore contains several instructions to the NWChem Tensor Contraction Engine (TCE) that direct NWChem to produce the information needed for interoperating with the Quantum Development Kit:</span></span>

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a><span data-ttu-id="0d29d-139">NWChem에서 Broombridge 출력 생성 및 소비</span><span class="sxs-lookup"><span data-stu-id="0d29d-139">Producing and Consuming Broombridge Output from NWChem</span></span> ##

<span data-ttu-id="0d29d-140">이제 Broombridge 문서를 생성 하 고 사용 하는 데 필요한 모든 것이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-140">You now have everything you need to produce and consume Broombridge documents.</span></span>
<span data-ttu-id="0d29d-141">NWChem을 실행 하 고 입력 데크 용 Broombridge 문서를 생성 하려면 `h4_sto6g_0.000.nw` 다음을 실행 합니다 `Convert-NWChemToBroombridge` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-141">To run NWChem and produce a Broombridge document for the `h4_sto6g_0.000.nw` input deck, run `Convert-NWChemToBroombridge`:</span></span>

> [!NOTE]
> <span data-ttu-id="0d29d-142">이 명령을 처음 실행 하는 경우 Docker가 이미지를 다운로드 `nwchemorg/nwchem-qc` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-142">The first time you run this command, Docker will download the `nwchemorg/nwchem-qc` image for you.</span></span>
> <span data-ttu-id="0d29d-143">연결 속도에 따라 시간이 오래 걸릴 수 있으며, 커피를 얻을 수 있는 기회를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-143">This may take a little while, depending on your connection speed, possibly providing an opportunity to get a cup of coffee.</span></span>

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

<span data-ttu-id="0d29d-144">그러면 `h4_sto6g_0.000.yaml` 에서 사용할 수 있는 라는 Broombridge 문서가 생성 됩니다 `Get-GateCount` .</span><span class="sxs-lookup"><span data-stu-id="0d29d-144">This will produce a Broombridge document called `h4_sto6g_0.000.yaml` that you can use with `Get-GateCount`:</span></span>

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

<span data-ttu-id="0d29d-145">이제 다양 한 퀀텀 시뮬레이션 방법에 대 한 T-카운트, 회전 수, CNOT count 등과 같은 리소스 예측을 포함 하는 콘솔 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-145">You should now see console output which contains resource estimation such as T-count, rotations count, CNOT count, etc. for various quantum simulation methods:</span></span>

```powershell 
IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Trotter
TCount              : 0
RotationsCount      : 92
CNOTCount           : 520
ElapsedMilliseconds : 327

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Qubitization
TCount              : 438
RotationsCount      : 516
CNOTCount           : 2150
ElapsedMilliseconds : 528

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Optimized Qubitization
TCount              : 3540
RotationsCount      : 18
CNOTCount           : 7932
ElapsedMilliseconds : 721
```

<span data-ttu-id="0d29d-146">여기에서 수행할 수 있는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-146">There are many things to go do from here:</span></span> 
- <span data-ttu-id="0d29d-147">의 매개 변수를 변경 하 여 다양 한 미리 정의 된 입력 데크를 사용해 보세요. `alpha` `h4_sto6g_alpha.nw`</span><span class="sxs-lookup"><span data-stu-id="0d29d-147">Try out different predefined input decks, e.g., by varying the parameter `alpha` in `h4_sto6g_alpha.nw`,</span></span> 
- <span data-ttu-id="0d29d-148">NWChem 데크를 직접 편집 하 여 (예: `STO-nG` 다양 한 n의 선택 항목에 대 한 모델 탐색) 데크를 수정 해 보세요.</span><span class="sxs-lookup"><span data-stu-id="0d29d-148">Try modifying the decks by editing the NWChem decks directly, e.g., exploring `STO-nG` models for various choices of n,</span></span> 
- <span data-ttu-id="0d29d-149">에서 사용할 수 있는 미리 정의 된 기타 NWChem 입력 데크를 사용해 보세요. `nwchem/qa/chem_library_tests`</span><span class="sxs-lookup"><span data-stu-id="0d29d-149">Try other predefined NWChem input decks that are available at `nwchem/qa/chem_library_tests`,</span></span>
- <span data-ttu-id="0d29d-150">NWChem에서 생성 되었으며 [Microsoft/퀀텀 리포지토리의](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)일부로 사용할 수 있는 미리 정의 된 Broombridge yaml 벤치 마크를 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="0d29d-150">Try out a suite of predefined Broombridge YAML benchmarks that were generated from NWChem and are available as part of the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span> <span data-ttu-id="0d29d-151">이러한 벤치 마크는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-151">These benchmarks include:</span></span> 
    - <span data-ttu-id="0d29d-152">분자 hydrogen (H2), molecules Yllium (be), 리튬 hydride (LiH)와 같은 small</span><span class="sxs-lookup"><span data-stu-id="0d29d-152">small molecules such as molecular hydrogen (H2), Beryllium (Be), Lithium hydride (LiH),</span></span>
    - <span data-ttu-id="0d29d-153">ozone (O3), beta-carotene, cytosine 등의 더 큰 molecules.</span><span class="sxs-lookup"><span data-stu-id="0d29d-153">larger molecules such as ozone (O3), beta-carotene, cytosine, and many more.</span></span> 
- <span data-ttu-id="0d29d-154">Microsoft Quantum Development Kit에 대 한 인터페이스 기능을 제공 하는 그래픽 프런트 엔드 [Emsl 화살표](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 를 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="0d29d-154">Try out the graphical front-end [EMSL Arrows](https://arrows.emsl.pnnl.gov/api/qsharp_chem) that features an interface to the Microsoft Quantum Development Kit.</span></span> 


## <a name="producing-broombridge-output-from-emsl-arrows"></a><span data-ttu-id="0d29d-155">EMSL 화살표에서 Broombridge 출력 생성</span><span class="sxs-lookup"><span data-stu-id="0d29d-155">Producing Broombridge Output from EMSL Arrows</span></span> ##

<span data-ttu-id="0d29d-156">웹 기반 프런트 엔드 EMSL 화살표를 시작 하려면 [여기](https://arrows.emsl.pnnl.gov/api/qsharp_chem)에서 브라우저를 탐색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-156">To get started with web-based front end EMSL Arrows, navigate a browser [here](https://arrows.emsl.pnnl.gov/api/qsharp_chem).</span></span> 

> [!NOTE]
> <span data-ttu-id="0d29d-157">웹 브라우저에서 EMSL 화살표를 실행 하려면 JavaScript를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-157">Running EMSL Arrows in a web browser requires JavaScript to be enabled.</span></span> <span data-ttu-id="0d29d-158">브라우저에서 JavaScript를 사용 하도록 설정 하는 방법에 대 한 다음 [지침](https://www.enable-javascript.com/) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d29d-158">Please refer to these [instructions](https://www.enable-javascript.com/) on how to enable JavaScript in your browser.</span></span> 

<span data-ttu-id="0d29d-159">먼저 쿼리 상자에 분자을 입력 합니다.``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span><span class="sxs-lookup"><span data-stu-id="0d29d-159">First, enter a molecule in the query box that says ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span></span> 

<span data-ttu-id="0d29d-160">통상적 이름으로 많은 molecules (예: "1, 3, 7-Trimethylxanthine" 대신 "caffeine")를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-160">You can enter many molecules by their colloquial name, such as "caffeine" instead of "1,3,7-Trimethylxanthine".</span></span> 

<span data-ttu-id="0d29d-161">그런 다음 표시 되는 단추를 클릭 ``theory{qsharp_chem}`` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-161">Next, click the button that says ``theory{qsharp_chem}``.</span></span> <span data-ttu-id="0d29d-162">이렇게 하면 쿼리 상자에 Broombridge YAML 형식으로 출력을 내보내도록 지시 하는 명령이 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-162">This will populate the query box further with an instruction that will tell the run to export output in the Broombridge YAML format.</span></span> 

<span data-ttu-id="0d29d-163">이제는 클록 ``Run Arrows`` 입니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-163">Now, clock on ``Run Arrows``.</span></span> <span data-ttu-id="0d29d-164">입력 크기에 따라 다소 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-164">Depending on the size of the input, this might take a while.</span></span> <span data-ttu-id="0d29d-165">또는 특정 모델이 이미 이전에 계산 된 경우에는 데이터베이스에서 조회만 수행 하므로 매우 빠르게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-165">Or, in case the particular model has already been computed before, it can be done extremely fast as it will only amount to a lookup in a database.</span></span> <span data-ttu-id="0d29d-166">두 경우 모두 입력으로 지정 된 데크를 기준으로 NWChem의 특정 실행에 대 한 다양 한 정보를 포함 하는 새 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-166">In either case, you will be taken to a new page that contains a plethora of information about the particular run of NWChem against the deck specified by your input.</span></span> 

<span data-ttu-id="0d29d-167">다음 헤더로 시작 하는 섹션에서 Broombridge YAML 파일을 다운로드 하 고 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-167">You can download and save the Broombridge YAML file from the section that starts with the following header:</span></span> 
```powershell
+==================================================+
||              Molecular Calculation             ||
+==================================================+

Id     = 48443

NWOutput = Link to NWChem Output (download)

Datafiles:
qsharp_chem.yaml-2018-10-23-14:37:42 (download)
...
```

<span data-ttu-id="0d29d-168">을 클릭 하 여 ``download`` 로컬 복사본을와 같은 고유한 파일 이름으로 저장 ``qsharp_chem48443.yaml`` 합니다. 각 실행 마다 특정 이름이 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-168">Click on ``download``, which saves a local copy with a unique file name such as ``qsharp_chem48443.yaml`` (the particular name will be different for each run).</span></span> <span data-ttu-id="0d29d-169">그러면 위와 같이이 파일을 추가로 처리할 수 있습니다. 예를 들어</span><span class="sxs-lookup"><span data-stu-id="0d29d-169">You can then further process this file as above, e.g., with</span></span> 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
<span data-ttu-id="0d29d-170">리소스 개수를 가져오려면</span><span class="sxs-lookup"><span data-stu-id="0d29d-170">to get resource counts.</span></span> 

<span data-ttu-id="0d29d-171">``Arrows Entry - 3D Builder``EMSL 화살표 시작 페이지의 탭에서 액세스할 수 있는 3d 분자 작성기를 즐길 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-171">You might enjoy the 3D molecule builder that can be accessed from the ``Arrows Entry - 3D Builder`` tab on the EMSL Arrows start page.</span></span> <span data-ttu-id="0d29d-172">표시 된 분자의 [JSMol](http://wiki.jmol.org/index.php/JSmol) 3d 그림을 클릭 하면 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-172">Clicking the [JSMol](http://wiki.jmol.org/index.php/JSmol) 3D picture of the shown molecule will let you allow to edit it.</span></span> <span data-ttu-id="0d29d-173">Atom을 이동 하 고, 분자 거리가 변경 되거나, 원소를 추가/제거 하는 등의 방법으로 atom을 끌어 놓을 수 있습니다. 이러한 각 선택 항목에 대해 ``theory{qsharp_chem}`` 쿼리 상자에를 추가한 후 Broombridge YAML 스키마의 인스턴스를 생성 하 고 퀀텀 화학 라이브러리를 사용 하 여이를 추가로 탐색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d29d-173">You can move atoms around, drag atoms apart so that their inter-molecular distances change, add/remove atoms, etc. For each of these choices, once you added ``theory{qsharp_chem}`` in the query box, you can then generate an instance of the Broombridge YAML schema and further explore it using the Quantum Chemistry Library.</span></span> 
