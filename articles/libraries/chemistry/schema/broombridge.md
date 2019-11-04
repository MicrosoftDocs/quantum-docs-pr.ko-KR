---
title: Broombridge-퀀텀 화학 스키마
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: c2a7636d0b3f07419e3312e04da5d811229ad854
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185327"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge 퀀텀 화학 스키마 # 

[Nwchem](http://www.nwchem-sw.org/) 과 같은 강력한 컴퓨팅 화학 소프트웨어를 통해 다양 한 실제 화학 문제를 모델링할 수 있습니다. Microsoft 퀀텀 화학 라이브러리를 사용 하 여 NWChem 분자 모델에 액세스 하기 위해 **Broombridge**를 호출 하는 [yaml](https://en.wikipedia.org/wiki/YAML)기반 스키마를 사용 합니다. 이 이름은 일부 원에서 Hamiltonians의 여행지로 탄생는 [이정표](https://en.wikipedia.org/wiki/Broom_Bridge) 에 대 한 참조에서 선택 되었습니다. 

[Nwchem](https://github.com/nwchemgit/nwchem) 은 허용 된 Ecl (교육용 커뮤니티 라이선스) 2.0 라이선스에 따라 사용이 허가 된 오픈 소스 프로젝트입니다. Broombridge는 [여기](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) 에 지정 된 오픈 소스 스키마로, MIT 라이선스에 따라 사용이 허가 된 [RFC 2119](https://tools.ietf.org/html/rfc2119) 및 [유효성 검사기 스크립트](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) 다음에 [정의가](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) 제공 됩니다. 

YAML 기반 인 Broombridge는 전자적으로 읽을 수 있고 사람이 읽을 수 있으며 전자적 구조 문제를 나타내는 사람이 편집할 수 있는 방법입니다. 특히 다음 데이터를 나타낼 수 있습니다. 
- Fermionic Hamiltonians는 1 ~ 2-전자 정수를 사용 하 여 나타낼 수 있습니다. 
- 만들기 시퀀스를 사용 하 여 지상 및 기쁜 상태를 표시할 수 있습니다.
- 에너지 수준의 상한 및 하 한 범위를 지정할 수 있습니다.

데이터 형식은 NWChem에서 간편 하 게 생성할 수 있습니다. NWChem 전체 설치에서 [여기](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) 에 제공 되는 것과 같은 화학 데크를 실행 하 고, docker를 통해 Broombridge을 실행의 일부로 출력 하는 다양 한 방법을 사용할 수 있습니다. 화학 데크에서 Broombridge를 생성 하는 데 사용할 수 있는 NWchem 이미지입니다. 마지막으로, 화학 소프트웨어를 설치할 필요 없이 신속 하 게 계산을 시작 하는 시각적 메서드는 [Nsl 화살표](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 인터페이스에서 NWChem으로 제공 됩니다. 

높은 수준에서 NWChem과 Microsoft Quantum Development Kit 간 상호 작용는 다음과 같이 시각화할 수 있습니다. ![화학 stack](~/media/broombridge.png) 파란색 음영 상자는 Broombridge 스키마를 나타내고, 다양 한 회색 음영 상자는 다른 내부를 나타냅니다. 실제 화학 문제를 기준으로 계산 화학의 퀀텀 알고리즘을 나타내고 처리 하기 위해 선택한 데이터 표현입니다. 

Broombridge 스키마를 사용 하 여 정의 된 여러 화학 표현은 [여기](https://github.com/microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML)에 제공 됩니다.

