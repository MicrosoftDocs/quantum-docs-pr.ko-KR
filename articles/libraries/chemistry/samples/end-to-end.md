---
title: 샘플 NWChem 퀀텀 프로그램
description: NWChem 입력 데크를 사용 하 여 퀀텀 화학 시뮬레이션에 대 한 게이트 수를 가져오는 예제를 살펴봅니다.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/23/2018
uid: microsoft.quantum.chemistry.examples.endtoend
ms.openlocfilehash: 7605676e05ee352e47791657eeaafceef5dbb493
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022503"
---
# <a name="end-to-end-with-nwchem"></a>NWChem을 사용하는 엔드투엔드 #

이 문서에서는 [Nwchem](http://www.nwchem-sw.org/index.php/Main_Page) 입력 데크에서 시작 하 여 퀀텀 화학 시뮬레이션에 대 한 게이트 수를 가져오는 예제를 안내 합니다.
이 예제를 진행 하기 전에 [설치 및 유효성 검사 가이드](xref:microsoft.quantum.chemistry.concepts.installation)에 따라 Docker를 설치 했는지 확인 합니다.

자세한 내용은 다음을 참조하세요.
- [NWChem 입력 데크 구조](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [퀀텀 개발 키트에 사용할 입력 데크 명령](https://github.com/nwchemgit/nwchem/tree/master/contrib/quasar)
- [화학 라이브러리 및 종속성 설치](xref:microsoft.quantum.chemistry.concepts.installation)
- [리소스 계산](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> 이 예에서는 Windows PowerShell Core를 실행 해야 합니다.
> https://github.com/PowerShell/PowerShell에서 Windows, macOS 또는 Linux 용 PowerShell Core를 다운로드 합니다.

## <a name="importing-required-powershell-modules"></a>필수 PowerShell 모듈 가져오기 ##

아직 수행 하지 않은 경우에는 퀀텀 개발 키트를 사용 하기 위한 샘플과 유틸리티가 포함 된 [Microsoft/퀀텀 리포지토리](https://github.com/Microsoft/Quantum)를 복제 합니다.

```powershell
git clone https://github.com/Microsoft/Quantum
```

`Microsoft/Quantum`복제 한 후에는 `utilities/` 폴더에 `cd`을 수행 하 고 Docker 및 NWChem 작업을 위한 PowerShell 모듈을 가져옵니다.

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> 기본적으로 Windows는 보안 조치로 스크립트나 모듈을 실행 하는 것을 방지 합니다.
> `Invoke-NWChem.psm1`와 같은 모듈이 Windows에서 실행 되도록 허용 하려면 실행 정책을 변경 해야 할 수 있습니다.
> 이렇게 하려면 `Set-ExecutionPolicy` 명령을 실행 합니다.
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> 그런 다음 PowerShell을 종료 하면 실행 정책이 되돌려집니다.
> 실행 정책을 저장 하려는 경우 `-Scope`에 대해 다른 값을 사용 합니다.
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

이제 `Convert-NWChemToBroombridge` 명령을 사용할 수 있습니다.

```powershell
Get-Command -Module InvokeNWChem
```

다음으로 **GetGateCount** 샘플과 함께 제공 되는 `Get-GateCount` 명령을 가져옵니다.
자세한 내용은 [샘플에서 제공](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount)하는 지침을 참조 하세요.
다음으로, 운영 체제에 따라 `win10-x64`, `osx-x64`또는 `linux-x64`로 `<runtime>` 대체 하 여 다음을 실행 합니다.

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

이제 `Get-GateCount` 명령을 사용할 수 있습니다.

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a>입력 데크 ##

NWChem 패키지는 메모리 할당 설정과 같은 다른 매개 변수와 함께 해결할 퀀텀 화학 문제를 지정 하는 _입력 데크_ 라는 텍스트 파일을 사용 합니다.
이 예제에서는 NWChem과 함께 제공 되는 미리 작성 된 입력 데크 중 하나를 사용 합니다.
먼저 [nwchemgit/nwchem 리포지토리](https://github.com/nwchemgit/nwchem)를 복제 합니다.

> [!NOTE]
> 이는 매우 큰 리포지토리입니다. `--depth 1` 인수를 사용 하 여 일부 대역폭과 디스크 공간을 절약 하기 위해 단순 클론을 수행할 수 있습니다.
> 그러나이는 선택 사항입니다.
> `--depth 1`없이 복제는 정상적으로 작동 합니다.

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

`nwchemgit/nwchem` 리포지토리는 [`QA/chem_library_tests` 폴더](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests)아래에 나열 된 퀀텀 개발 키트와 함께 사용 하기 위한 다양 한 입력 데크를 제공 합니다.
이 예에서는 `H4` 입력 데크를 사용 합니다.

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

분자는 1 개의 각도에 의존 하는 특정 기 하 도형에 정렬 된 4 hydrogen 원소의 시스템입니다 .이 시스템은 데크 이름 `h4_sto6g_alpha.nw`에 표시 된 대로 `alpha` 매개 변수입니다. H4은 1970 년대 이후 계산 연금술에 대해 알려진 [분자 벤치 마크](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) 입니다. 매개 변수 `sto6g`은 데크를 A이후 형식 궤도와 관련 된 표현을 구현 하는 것을 의미 합니다. 특히, 6 가우스 기준 함수를 사용 하 여 [설정](https://en.wikipedia.org/wiki/STO-nG_basis_sets) 하는 방법에 대 한 표현입니다. 또한이 입력 데크는 NWChem을 사용 하 여 퀀텀 개발 키트와 상호 운용 하는 데 필요한 정보를 생성 하는 NWChem 텐서 축약 Engine (TCE)에 대 한 몇 가지 지침을 포함 하 고 있습니다.

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a>NWChem에서 Broombridge 출력 생성 및 소비 ##

이제 Broombridge 문서를 생성 하 고 사용 하는 데 필요한 모든 것이 있습니다.
NWChem을 실행 하 고 `h4_sto6g_0.000.nw` 입력 데크 용 Broombridge 문서를 생성 하려면 `Convert-NWChemToBroombridge`를 실행 합니다.

> [!NOTE]
> 이 명령을 처음 실행 하는 경우 Docker는 `nwchemorg/nwchem-qc` 이미지를 다운로드 합니다.
> 연결 속도에 따라 시간이 오래 걸릴 수 있으며, 커피를 얻을 수 있는 기회를 제공할 수 있습니다.

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

그러면 `Get-GateCount`에서 사용할 수 있는 `h4_sto6g_0.000.yaml` 이라는 Broombridge 문서가 생성 됩니다.

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

이제 다양 한 퀀텀 시뮬레이션 방법에 대 한 T-카운트, 회전 수, CNOT count 등과 같은 리소스 예측을 포함 하는 콘솔 출력이 표시 됩니다.

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

여기에서 수행할 수 있는 작업은 다음과 같습니다. 
- `h4_sto6g_alpha.nw`에서 매개 변수 `alpha`를 변경 하 여 다양 한 미리 정의 된 입력 데크를 사용해 보세요. 
- NWChem 데크를 직접 편집 하 여 (예: 다양 한 n 가지 선택 항목에 대 한 `STO-nG` 모델 탐색) 데크를 수정 해 보세요. 
- `nwchem/qa/chem_library_tests`에서 사용할 수 있는 미리 정의 된 기타 NWChem 입력 데크를 사용해 보세요.
- NWChem에서 생성 되었으며 [Microsoft/퀀텀 리포지토리의](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)일부로 사용할 수 있는 미리 정의 된 Broombridge yaml 벤치 마크를 사용해 보세요. 이러한 벤치 마크는 다음과 같습니다. 
    - 분자 hydrogen (H2), molecules Yllium (be), 리튬 hydride (LiH)와 같은 small
    - ozone (O3), beta-carotene, cytosine 등의 더 큰 molecules. 
- Microsoft Quantum Development Kit에 대 한 인터페이스 기능을 제공 하는 그래픽 프런트 엔드 [Emsl 화살표](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 를 사용해 보세요. 


## <a name="producing-broombridge-output-from-emsl-arrows"></a>EMSL 화살표에서 Broombridge 출력 생성 ##

웹 기반 프런트 엔드 EMSL 화살표를 시작 하려면 [여기](https://arrows.emsl.pnnl.gov/api/qsharp_chem)에서 브라우저를 탐색 합니다. 

> [!NOTE]
> 웹 브라우저에서 EMSL 화살표를 실행 하려면 JavaScript를 사용 하도록 설정 해야 합니다. 브라우저에서 JavaScript를 사용 하도록 설정 하는 방법에 대 한 다음 [지침](https://www.enable-javascript.com/) 을 참조 하세요. 

먼저 ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.`` 표시 되는 쿼리 상자에 분자를 입력 합니다. 

통상적 이름으로 많은 molecules (예: "1, 3, 7-Trimethylxanthine" 대신 "caffeine")를 입력할 수 있습니다. 

그런 다음 ``theory{qsharp_chem}``단추를 클릭 합니다. 이렇게 하면 쿼리 상자에 Broombridge YAML 형식으로 출력을 내보내도록 지시 하는 명령이 추가 됩니다. 

이제 ``Run Arrows``클록입니다. 입력 크기에 따라 다소 시간이 걸릴 수 있습니다. 또는 특정 모델이 이미 이전에 계산 된 경우에는 데이터베이스에서 조회만 수행 하므로 매우 빠르게 수행할 수 있습니다. 두 경우 모두 입력으로 지정 된 데크를 기준으로 NWChem의 특정 실행에 대 한 다양 한 정보를 포함 하는 새 페이지로 이동 합니다. 

다음 헤더로 시작 하는 섹션에서 Broombridge YAML 파일을 다운로드 하 고 저장할 수 있습니다. 
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

``qsharp_chem48443.yaml``와 같은 고유한 파일 이름으로 로컬 복사본을 저장 하는 ``download``를 클릭 합니다. 각 실행 마다 특정 이름이 달라 집니다. 그러면 위와 같이이 파일을 추가로 처리할 수 있습니다. 예를 들어 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
리소스 개수를 가져오려면 

EMSL 화살표 시작 페이지의 ``Arrows Entry - 3D Builder`` 탭에서 액세스할 수 있는 3D 분자 작성기를 즐길 수 있습니다. 표시 된 분자의 [JSMol](http://wiki.jmol.org/index.php/JSmol) 3d 그림을 클릭 하면 편집할 수 있습니다. Atom을 이동 하 고, 분자 거리가 변경 되거나, 원소를 추가/제거 하는 등의 방법으로 atom을 끌어 놓을 수 있습니다. 이러한 각 선택 항목에 대해 쿼리 상자에 ``theory{qsharp_chem}``를 추가한 후 Broombridge YAML 스키마의 인스턴스를 생성 하 고 퀀텀 화학 라이브러리를 사용 하 여이를 추가로 탐색할 수 있습니다. 
