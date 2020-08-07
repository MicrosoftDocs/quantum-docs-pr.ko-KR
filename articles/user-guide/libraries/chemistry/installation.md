---
title: Microsoft Q# 화학 라이브러리 설치
description: Microsoft 퀀텀 화학 라이브러리를 설치 하 고 NWChem 계산 화학 플랫폼과 함께 사용 하는 방법을 알아봅니다.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5fe973d24ceffd413cdbd3c543013dcc7ee379c0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869344"
---
# <a name="chemistry-library-installation"></a>화학 라이브러리 설치

[ **MolecularHydrogen** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) 은 수동으로 구성 된 분자 입력 데이터를 사용 합니다.
이는 작은 예의 경우에는 적합 하지만, 규모의 퀀텀 연금술에는 수백만 또는 수십억 개의 용어로 Hamiltonians 필요 합니다.
확장 가능한 계산 화학 패키지에 의해 생성 된 이러한 Hamiltonians는 너무 커서 수동으로 가져올 수 없습니다.

퀀텀 개발 키트에 대 한 퀀텀 화학 라이브러리는 계산 연금술 패키지에서 잘 작동 하도록 설계 되었습니다. 특히 태평양 연안 국가의 과학에 게는 EMSL (환경적 분자 연구소)에서 개발한 [**Nwchem**](http://www.nwchem-sw.org/) 계산 화학 플랫폼이 있습니다.
특히 [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)에 표시 되는 퀀텀 화학 시뮬레이션 문제의 인스턴스를 로드 하기 위한 도구 [ **Microsoft.Quantum.Chemistry** 를 제공 하며](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) , 최신 버전의 nwchem에서 내보내기도 지원 합니다.

또한 퀀텀 개발 키트 화학 라이브러리는 `qdk-chem` 레거시 형식 및 [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)를 변환 하는 데 사용할 수 있는 명령줄 도구인를 제공 합니다.

이 섹션에서는 NWChem 및 Broombridge 또는 레거시 형식과 함께 퀀텀 개발 키트를 사용 하는 방법에 대해 자세히 설명 합니다 `qdk-chem` .

## <a name="using-the-quantum-development-kit-with-nwchem"></a>NWChem에서 퀀텀 개발 키트 사용

퀀텀 개발 키트와 함께 NWChem을 사용 하 여 시작 하 고 실행 하려면 다음 방법 중 하나를 사용 합니다.

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

## <a name="using-the-quantum-development-kit-with-qdk-chem"></a>에서 퀀텀 개발 키트 사용`qdk-chem`

를 설치 하려면 `qdk-chem` 명령줄에서 .NET Core SDK를 사용할 수 있습니다.

```dotnetcli
dotnet tool install --global Microsoft.Quantum.Chemistry.Tools
```

를 설치한 후에는 `qdk-chem` 옵션을 사용 `--help` 하 여 도구에서 제공 하는 기능에 대 한 자세한 정보를 얻을 수 있습니다 `qdk-chem` .

Broombridge에서 변환 하려면 다음 명령을 사용할 수 있습니다 `qdk-chem convert` .

```
qdk-chem convert --from fcidump --to broombridge data.fcidump --out data.yml
```

`qdk-chem convert`이 명령은 표준 입력의 데이터를 수락 하 고 표준 출력에 쓸 수도 있습니다 .이는 특히 스크립트 내에서 사용 하 고 기존 형식으로 내보내는 도구와 통합 하는 데 유용 합니다.
예를 들어 Bash에서는 다음과 같습니다.

```bash
cat data.fcidump | qdk-convert --from fcidump --to broombridge - > data.yml
```
