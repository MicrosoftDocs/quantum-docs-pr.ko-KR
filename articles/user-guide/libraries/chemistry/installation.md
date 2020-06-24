---
title: 'Microsoft Q # 화학 라이브러리 설치 및 유효성 검사'
description: Microsoft 퀀텀 화학 라이브러리를 설치 하 고 NWChem 계산 화학 플랫폼과 함께 사용 하는 방법을 알아봅니다.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: 48bf7bc980e238e622053f5c2bdd09604c572596
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276104"
---
# <a name="chemistry-library-installation-and-validation"></a>화학 라이브러리 설치 및 유효성 검사

퀀텀 개발 키트는 NuGet 패키지를 통해 퀀텀 화학 응용 프로그램에 대 한 지원을 제공 합니다 [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) .
다른 NuGet 패키지와 마찬가지로, 프로젝트에 화학 라이브러리를 추가 하는 것은 간단 합니다.

**Visual Studio 2019:** Visual Studio 2019을 사용 하는 경우 NuGet 패키지 관리자를 사용 하 여 퀀텀 화학 패키지를 추가할 수 있습니다.
패키지 관리자를 열려면 아래 스크린샷에서와 같이 화학 라이브러리를 추가 하려는 프로젝트를 마우스 오른쪽 단추로 클릭 하 고 "NuGet 패키지 관리 ..."를 선택 합니다.

![Visual Studio 2019에서 NuGet 패키지 관리자 사용](~/media/vs2017-nuget-manage-packages.png)

찾아보기 탭에서 패키지 이름 "Microsoft. m a."를 검색 합니다.

> [!NOTE]
> "시험판 포함"을 사용 해야 합니다.

![시험판 포함 확인란](~/media/vs2017-nuget-package-search.png)

그러면 다운로드할 수 있는 패키지가 나열 됩니다.
왼쪽 창에서 "Microsoft"를 클릭 하 고 오른쪽 창에서 최신 시험판 버전을 선택한 후 "설치"를 클릭 합니다.

![최신 Microsoft 양자 패키지를 설치 합니다.](~/media/vs2017-nuget-select-chem.png)

자세한 내용은 [패키지 관리자 UI 가이드](https://docs.microsoft.com/nuget/tools/package-manager-ui)를 참조 하세요.

또는 패키지 관리자 콘솔을 사용 하 여 명령줄 인터페이스를 통해 퀀텀 화학 라이브러리를 프로젝트에 추가할 수 있습니다.

![명령줄에서 패키지 관리자 콘솔 사용](~/media/vs2017-nuget-console-menu.png)

패키지 관리자 콘솔에서 다음을 실행 합니다.

```
Install-Package Microsoft.Quantum.Chemistry
```

자세한 내용은 [패키지 관리자 콘솔 가이드](https://docs.microsoft.com/nuget/tools/package-manager-console)를 참조 하세요.

**명령줄 또는 Visual Studio Code:** 명령줄을 사용 하거나 Visual Studio Code 내에서 명령을 사용 하 여 `dotnet` NuGet 패키지 참조를 프로젝트에 추가할 수 있습니다.

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a>설치 확인 

퀀텀 개발 키트의 나머지와 마찬가지로 퀀텀 화학 라이브러리에는 신속 하 게 시작 및 실행 하는 데 도움이 되는 여러 가지 문서화 된 샘플이 제공 됩니다.
이러한 예제를 사용 하 여 설치를 테스트 하려면 [주 샘플 리포지토리](https://github.com/Microsoft/Quantum)를 복제 한 다음 샘플 중 하나를 실행 합니다.  예를 들어 예제를 실행 하려면 다음을 수행 합니다 [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) .

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

리포지토리를 복제 한 후 Microsoft Visual Studio를 사용 하 여 퀀텀 화학 라이브러리의 설치를 확인 하려면 다음을 수행 합니다.
    1. 화학 폴더에서 ChemistrySamples 솔루션을 엽니다.  
    2. 샘플/1을 선택 합니다. Simple Molecules/MolecularHydrogen를 시작 프로젝트로
    3. F5 키를 눌러 분자 Hydrogen 퀀텀 단계 예측 데모를 실행 합니다.

에너지 수준 값을 예측 하는 방법에 대 한 자세한 내용은 [에너지 수준 예측 가져오기](xref:microsoft.quantum.chemistry.examples.energyestimate) 를 참조 하세요.   


## <a name="using-the-quantum-development-kit-with-nwchem"></a>NWChem에서 퀀텀 개발 키트 사용 ##

MolecularHydrogen 샘플은 수동으로 구성 된 분자 입력 데이터를 사용 합니다.  이는 작은 예제에 적합 하지만, 규모의 퀀텀 연금술에는 수백만 또는 수십억 개의 용어로 Hamiltonians 필요 합니다. 확장 가능한 계산 화학 패키지에 의해 생성 된 이러한 Hamiltonians는 너무 커서 수동으로 가져올 수 없습니다. 

퀀텀 개발 키트에 대 한 퀀텀 화학 라이브러리는 계산 연금술 패키지에서 잘 작동 하도록 설계 되었습니다. 특히 태평양 연안 국가의 과학에 게는 EMSL (환경적 분자 연구소)에서 개발한 [**Nwchem**](http://www.nwchem-sw.org/) 계산 화학 플랫폼이 있습니다.
특히 `Microsoft.Quantum.Chemistry` 패키지는 [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)에 표시 되는 퀀텀 화학 시뮬레이션 문제의 인스턴스를 로드 하기 위한 도구를 제공 하며, 최신 버전의 NWChem에서 내보내기도 지원 합니다.

퀀텀 개발 키트와 함께 NWChem을 사용 하 여 시작 하 고 실행 하려면 다음 방법 중 하나를 사용 하는 것이 좋습니다.
- 기존 Broombridge [파일을 사용](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)하 여 시작 합니다.
- 웹 기반 프런트 엔드를 사용 하는 [Microsoft Quantum Development Kit에 대 한 Emsl 화살표 작성기](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 를 사용 하 여 새 Broombridge 분자 입력 파일을 생성 합니다.  
- PNNL에서 제공 하는 [Docker 이미지](https://hub.docker.com/r/nwchemorg/nwchem-qc/) 를 사용 하 여 NWChem을 실행 하거나
- 플랫폼용 [NWChem을 컴파일합니다](http://www.nwchem-sw.org/index.php/Compiling_NWChem) .

NWChem을 사용 하 여 퀀텀 개발 ... Kit 화학 라이브러리로 분석 하는 방법에 대 한 자세한 내용은 [NWChem을 사용](xref:microsoft.quantum.chemistry.examples.endtoend) 하 여 종단 간을 참조 하세요.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>샘플과 함께 제공 되는 Broombridge 파일을 사용 하 여 시작

퀀텀 개발 키트 샘플 리포지토리의 [Broombridge 폴더에](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) 는 형식이 인 분자 데이터 파일이 포함 되어 있습니다.  

간단한 예로, 화학 라이브러리 샘플 [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) 를 사용 하 여 Broombridge 파일 중 하나에서 Hamiltonian를 로드 하 고 퀀텀 시뮬레이션 algorigthms의 게이트 예측을 수행 합니다.

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

Broombridge 스키마가 나타내는 molecules를 입력 하는 방법에 대 한 자세한 내용은 [파일에서 Hamiltonian 로드](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) 를 참조 하세요.  

리소스 [계산](xref:microsoft.quantum.chemistry.examples.resourcecounts) 에 대 한 자세한 내용은 리소스 수 가져오기를 참조 하세요.  

### <a name="getting-started-using-the-emsl-arrows-builder"></a>EMSL 화살표 작성기를 사용 하 여 시작

EMSL 화살표는 NWChem 및 화학 계산 데이터베이스를 사용 하 여 분자 데이터를 생성 하는 도구입니다.  [Microsoft Quantum Development Kit에 대 한 Emsl 화살표 작성기](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 를 사용 하면 여러 분자 모델 빌더를 사용 하 여 모델을 입력 하 고 퀀텀 개발 키트에서 사용할 Broombridge 데이터 데이터를 생성할 수 있습니다.  

EMSL 페이지에서 [' 실행 중인 작업 '] 탭을 클릭 하 고 [' 간단한 예제 '] 지침에 따라 Broombridge 파일을 생성 합니다.  그런 다음 [' GetGateCount ']를 실행 하 여 이러한 molecules에 대 한 퀀텀 리소스 예상치를 확인 하십시오.

### <a name="installing-nwchem-from-source"></a>원본에서 NWChem 설치

원본에서 NWChem을 설치 하는 방법에 대 한 전체 지침은 [PNNL에서 제공](http://www.nwchem-sw.org/index.php/Compiling_NWChem)합니다.

> [!TIP]
> Windows 10에서 NWChem을 사용 하려는 경우 Linux 용 Windows 하위 시스템을 사용 하는 것이 좋습니다.
> [Ubuntu 18.04 LTS For Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)를 설치한 후 `ubuntu18.04` 즐겨 찾는 터미널에서 실행 하 고 위의 지침에 따라 원본에서 NWChem을 설치 합니다.

원본에서 NWChem을 컴파일한 후 `yaml_driver` nwchem과 함께 제공 된 스크립트를 실행 하 여 nwchem 입력 데크에서 Broombridge 인스턴스를 빠르게 생성할 수 있습니다.

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

이 명령은 `input.yaml` 현재 디렉터리 내에서 Broombridge 형식으로 새 파일을 만듭니다.

### <a name="using-nwchem-with-docker"></a>Docker에서 NWChem 사용

NWChem을 사용 하기 위한 미리 빌드된 이미지는 [Docker 허브](https://hub.docker.com)를 통해 플랫폼 간 제공 됩니다.
시작 하려면 플랫폼에 대 한 Docker 설치 지침을 따르세요.

- [Ubuntu 용 Docker 설치](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [MacOS 용 Docker 설치](https://docs.docker.com/docker-for-mac/install/)
- [Windows용 Docker 10 설치](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> Windows용 Docker를 사용 하는 경우 임시 디렉터리 (일반적으로 드라이브)가 포함 된 드라이브를 `C:\` Docker 디먼과 공유 해야 합니다. 자세한 내용은 [Docker 설명서](https://docs.docker.com/docker-for-windows/#shared-drives) 를 참조 하세요.

Docker를 설치한 후에는 퀀텀 Development Kit 샘플과 함께 제공 된 PowerShell 모듈을 사용 하 여 이미지를 실행 하거나 이미지를 수동으로 실행할 수 있습니다.
PowerShell 사용에 대 한 자세한 내용은 여기를 참조 하세요. Docker 이미지를 수동으로 사용 하려는 경우 [이미지와 함께 제공 되는 설명서](https://hub.docker.com/r/nwchemorg/nwchem-qc/)를 참조 하세요.

#### <a name="running-nwchem-through-powershell-core"></a>PowerShell Core를 통해 NWChem 실행

퀀텀 개발 키트에서 NWChem Docker 이미지를 사용 하려면 NWChem에서 파일을 이동 하는 것을 처리 하는 작은 PowerShell 모듈을 제공 합니다.
PowerShell Core를 아직 설치 하지 않은 경우 [GitHub의 powershell 리포지토리에서](https://github.com/PowerShell/PowerShell#get-powershell)플랫폼 간 다운로드를 다운로드할 수 있습니다.

> [!NOTE]
> PowerShell Core는 데이터 과학 및 비즈니스 분석 워크플로와의 상호 운용성을 보여 주기 위해 일부 샘플에도 사용 됩니다.

PowerShell Core가 설치 되 면 가져오기 `InvokeNWChem.psm1` : 현재 세션에서 NWChem 명령을 사용할 수 있도록 합니다.

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

그러면 `Convert-NWChemToBroombridge` 현재 PowerShell 세션에서 명령을 사용할 수 있습니다.
Docker에서 필요한 이미지를 다운로드 하 고이를 사용 하 여 NWChem 입력 데크를 실행 하 고 Broombridge에 대 한 출력을 캡처하려면 다음을 실행 합니다.

```powershell
Convert-NWChemToBroombridge ./input.nw
```

이렇게 하면 NWChem on을 실행 하 여 Broombridge 파일을 만듭니다 `input.nw` .
기본적으로 Broombridge 출력은 입력 데크와 동일한 이름과 경로를 가지 며 `.nw` 확장명은로 대체 됩니다 `.yaml` .
매개 변수를로 사용 하 여이를 재정의할 수 있습니다 `-DestinationPath` `Convert-NWChemToBroombridge` .
PowerShell의 기본 제공 도움말 기능을 사용 하 여 자세한 정보를 얻을 수 있습니다.

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
