---
title: '- Q# 매직 명령'
description: Q#Jupyter 노트북을 사용 하는 매직 명령에 대 한 빠른 참조 페이지 Q#
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: fb7b5543ef9222e6bab2b1cbbc7e3ebb54863438
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867984"
---
# <a name="ino-locq-magic-commands"></a>- Q# 매직 명령

### <a name="general"></a>일반

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): 구성 옵션을 설정 하거나 쿼리할 수 있습니다.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): ResourcesEstimator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): 현재 사용할 수 있는 모든 매직 명령의 목록을 반환 합니다.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): NuGet 패키지를 로드 하는 기능을 제공 합니다.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance):이 커널에 대 한 현재 성능 메트릭을 보고 합니다.
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): QuantumSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): ToffoliSimulator 대상 컴퓨터에서 지정 된 함수 또는 작업을 실행 합니다.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Q# 현재 세션에서 사용할 수 있는 작업을 나열 합니다.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): 현재 작업 영역과 관련 된 작업을 제공 합니다.

### <a name="azure-quantum-integration"></a>Azure 퀀텀 통합

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Azure 퀀텀 작업 영역에 연결 하거나 현재 연결 상태를 표시 합니다.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Azure 퀀텀 작업 영역에서 작업을 실행 합니다.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): 현재 Azure 퀀텀 작업 영역에서 작업 목록을 표시 합니다.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): 현재 Azure 퀀텀 작업 영역에서 작업에 대 한 결과를 표시 합니다.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): 현재 Azure 퀀텀 작업 영역에서 작업의 상태를 표시 합니다.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Azure 퀀텀 작업 영역에 작업을 제출 합니다.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Q# Azure 퀀텀 작업 영역에서 작업 제출에 대 한 활성 실행 대상을 설정 하거나 표시 합니다.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>화학 (Microsoft.

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): 지정 된 .yaml 파일에서 Broombridge 전자적 구조 문제 표현을 로드 하 고 반환 합니다.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Fermion Hamiltonian을에서 사용할 수 있는 형식으로 인코딩합니다 Q# .
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Fermion Hamiltonian에 용어를 추가 합니다.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): 전자 구조 문제에 대 한 fermion Hamiltonian을 로드 합니다. 문제는 파일에서 로드되거나 인수로 전달됩니다.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Broombridge 전자적 구조 문제를 로드 하 고 선택한 입력 상태를 반환 합니다.

### <a name="katas-from-microsoftquantumkatas-package"></a>Katas (Katas 패키지에서)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): 단일 테스트를 실행 하 고 테스트 성공 여부를 보고 합니다.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): 단일 kata의 테스트에 대 한 참조 구현을 확인 합니다.
    특히 단일 작업에 대 한 참조 구현을 셀로 대체 하 고 테스트 성공 여부를 보고 합니다.
