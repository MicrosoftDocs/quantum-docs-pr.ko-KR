---
title: Broombridge 퀀텀 화학 스키마
description: Microsoft Quantum Development Kit에 대 한 실제 화학 문제를 모델링 하는 데 사용 되는 Broombridge 퀀텀 화학 스키마의 개요입니다.
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: 708c4277080c358cb35a49fbf1dde0394d331043
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275873"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge 퀀텀 화학 스키마 # 

[Nwchem](http://www.nwchem-sw.org/) 과 같은 강력한 컴퓨팅 화학 소프트웨어를 사용 하면 다양 한 실제 화학 문제를 모델링할 수 있습니다. Microsoft 퀀텀 화학 라이브러리를 사용 하 여 NWChem 분자 모델에 액세스 하려면 **Broombridge**라는 [yaml](https://en.wikipedia.org/wiki/YAML)기반 스키마를 사용 합니다. 이 이름은 일부 원에서 Hamiltonians의 여행지로 탄생는 [이정표](https://en.wikipedia.org/wiki/Broom_Bridge) 에 대 한 참조에서 선택 되었습니다. 

[Nwchem](https://github.com/nwchemgit/nwchem) 은 허용 된 Ecl (교육용 커뮤니티 라이선스) 2.0 라이선스에 따라 사용이 허가 된 오픈 소스 프로젝트입니다. [Broombridge 퀀텀 화학 스키마](https://docs.microsoft.com/quantum/libraries/chemistry/schema/spec_v_0_2)는 [RFC 2119](https://tools.ietf.org/html/rfc2119) 다음에 [정의](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) 및 MIT 라이선스에 따라 사용이 허가 된 [유효성 검사기 스크립트](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) 를 포함 하는 오픈 소스 스키마입니다. 

YAML 기반 인 Broombridge는 전자적으로 읽을 수 있고 사람이 읽을 수 있으며 전자적 구조 문제를 나타내는 사람이 편집할 수 있는 방법입니다. 특히 다음 데이터를 나타낼 수 있습니다.
- Fermionic Hamiltonians는 1 ~ 2-전자 정수를 사용 하 여 나타낼 수 있습니다.
- 만들기 시퀀스를 사용 하 여 지상 및 기쁜 상태를 표시할 수 있습니다.
- 에너지 수준의 상한 및 하 한 범위를 지정할 수 있습니다.

Nwchem 전체 설치를 사용 하 여 화학 데크를 실행 하는 경우 (예: Broombridge를 실행의 일부로 출력 하는 [nwchem 라이브러리](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) 에서 제공 된 항목) 또는 화학 데크에서 Broombridge를 생성 하는 데 사용할 수 있는 nwchem의 docker 이미지와 같은 다양 한 방법을 사용 하 여 nwchem에서 데이터를 생성할 수 있습니다. 화학 소프트웨어를 설치할 필요 없이 신속 하 게 계산을 시작 하려면 [Emsl 화살표가](https://arrows.emsl.pnnl.gov/api/qsharp_chem)제공한 NWChem에 시각적 인터페이스를 사용할 수 있습니다.

높은 수준에서 NWChem과 Microsoft Quantum Development Kit 사이에 있는 상호 작용는 다음과 같이 시각화할 수 있습니다. ![ 화학 스택 ](~/media/broombridge.png) 파란색 회색 상자는 Broombridge 스키마를 나타내고, 다양 한 회색 음영 상자는 실제 화학 문제를 기준으로 계산을 위한 퀀텀 알고리즘을 표시 하 고 처리 하기 위해 선택한 기타 내부 데이터 표현을 나타냅니다.

퀀텀 개발 키트 샘플 리포지토리의 [정수 및 YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) 폴더에는 Broombridge 스키마를 사용 하 여 정의 된 여러 개의 화학 표현이 포함 되어 있습니다.
