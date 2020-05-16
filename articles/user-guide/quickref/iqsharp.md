---
title: IQ# 매직 명령
description: 'R c 2를 사용 하 여 IQ # 매직 명령에 대 한 빠른 참조 페이지 Q # Jupyter 노트북'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431022"
---
# <a name="iq-magic-commands"></a>IQ# 매직 명령

### <a name="general"></a>일반

- `%config`: 구성 기본 설정을 설정 하거나 가져옵니다.
- `%estimate`: QuantumSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.
- `%lsmagic`: 현재 사용할 수 있는 모든 매직 명령의 목록을 반환 합니다.
- `%package`: Nuget 패키지를 로드 하는 기능을 제공 합니다.
- `%performance`:이 커널에 대 한 현재 성능 메트릭을 보고 합니다.
- `%simulate`: QuantumSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.
- `%toffoli`: ToffoliSimulator 시뮬레이터 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.
- `%who`: 현재 작업 영역과 관련 된 작업을 제공 합니다.
- `%workspace`: 현재 세션에 정의 된 모든 작업 및 함수 목록을 대화형으로 반환 하거나 현재 작업 영역에서 로드 합니다.

### <a name="chemistry"></a>화학

- `%chemistry.broombridge`: 지정 된 .yaml 파일에서 Broombridge 전자적 구조 문제 표현을 로드 하 고 반환 합니다.
- `%chemistry.encode`: Fermion Hamiltonian를 Q #에서 사용할 수 있는 형식으로 인코딩합니다.
- `%chemistry.fh.add_terms`: Fermion Hamiltonian에 용어를 추가 합니다.
- `%chemistry.fh.load`: 전자 구조 문제에 대 한 fermion Hamiltonian을 로드 합니다. 문제는 파일에서 로드되거나 인수로 전달됩니다.
- `%chemistry.inputstate.load`: Broombridge 전자적 구조 문제를 로드 하 고 선택한 입력 상태를 반환 합니다.

### <a name="from-microsoftquantumkatas-package"></a>Katas 패키지에서

- `%kata`: 단일 테스트를 실행 하 고 테스트 성공 여부를 보고 합니다.
- `%check_kata`: 단일 kata의 테스트에 대 한 참조 구현을 확인 합니다.
    특히 단일 작업에 대 한 참조 구현을 셀로 대체 하 고 테스트 성공 여부를 보고 합니다.
