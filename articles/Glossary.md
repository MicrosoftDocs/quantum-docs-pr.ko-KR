---
title: 용어집 | Microsoft Docs
description: 퀀텀 용어 용어집
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: bfa275b3330ea2c2a541b08f137893b63b6213aa
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183627"
---
|조건|정의|
|-------------|----------|
|Adjoint|작업의 복소수 복소수입니다. 단일 연산자를 구현 하는 작업의 경우 adjoint는 작업의 역함수입니다.|
|호출|작업 및 함수를 통칭 하 여 *callables*이라고 합니다.|
|Standard|Q #에 정의 된 작업 및 함수는 prelude에 정의 된 논리에 따라 작성 됩니다. 표준 라이브러리 구현은 대상 컴퓨터와는 독립적입니다.|
|Clifford 그룹|Bloch 구의 octants을 차지 하는 작업 집합입니다. 여기에는 `X`, `Y`, `Z`, `H` 및 `S`가 포함 됩니다.|
|제어|대상 작업에 대 한 조력자로 하나 이상의 이상 비트를 사용 하는 퀀텀 작업입니다.|
|기타 ac 표기법|퀀텀 상태를 간단 하 게 표현한 것입니다. 자세한 내용은 [Diac 표기법](xref:microsoft.quantum.concepts.dirac) 섹션을 참조 하세요.|
|Eigenvalues 및 고유 벡터|자세한 내용은 [고급 행렬 단원을](xref:microsoft.quantum.concepts.matrix-advanced) 참조 하세요.|
|EPR 쌍|[종 상태](https://en.wikipedia.org/wiki/Bell_state) 라고도 함|
|진화|시간이 지남에 따라 상태를 변경 하는 방법입니다. 예는 <xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials>에 대 한 섹션을 참조 하세요. |
|함수|Q # 언어의 순수 클래식 루틴|
| <a id="global-phase"></a>글로벌 단계 | 복소수 $e ^ {i\\\a} $과 (와) 동일한 두 가지 상태는 글로벌 단계에 따라 달라 집니다. 로컬 단계와 달리 전역 단계는 모든 측정값을 통해 관찰할 수 없습니다. 자세한 내용은 [Pauli 측정값](xref:microsoft.quantum.concepts.pauli) 을 참조 하세요. |
|측정|이상 비트 (또는 나머지 비트 집합)에서 고전적인 비트를 가져옵니다. 자세한 내용은 [다음을 참조](xref:microsoft.quantum.concepts.qubit) 하세요.|
|변경 가능|값을 만든 후 해당 값을 변경할 수 있는 변수입니다.|
|네임스페이스|관련 된 이름 (일반적으로 작업, 함수 및 형식)의 컬렉션에 대 한 레이블입니다. 예를 들어, 네임 스페이스 [`Microsoft.Quantum.Preparation`](xref:microsoft.quantum.preparation) 초기 상태를 준비 하는 데 도움이 되는 표준 라이브러리에 정의 된 모든 기호에 레이블을 지정 합니다.|
|작업(Operation)|Q #에서 퀀텀 실행의 기본 단위입니다. 이는 C, C++ 또는 Python의 함수 또는 C# 또는 Java의 정적 메서드와 거의 동일합니다.|
|운영자 응용 프로그램|퀀텀 작업을 수행 하는 중입니다. 일반적으로 현재 상태 벡터에 단일 행렬을 적용 합니다. 자세한 내용은 [퀀텀 개념 소개를](xref:microsoft.quantum.concepts.intro) 참조 하세요.|
|Oracle|런타임에 퀀텀 알고리즘에 데이터 종속 정보를 제공 하는 서브루틴입니다. 일반적으로 superposition에 있는 입력에 해당 하는 출력의 superposition을 제공 하는 것이 목표입니다.   |
|부분 응용 프로그램|모든 필수 매개 변수 없이 함수 또는 작업을 호출 합니다. 는 이후 응용 프로그램에서 제공 된 누락 된 매개 변수만 필요한 새 호출 가능를 반환 합니다.|
|Pauli 연산자|`X`, `Y` 및 `Z` 퀀텀 게이트입니다.|
|Prelude|Q # 수준이 아닌 각 개별 대상 컴퓨터에서 정의 되는 기본 및 클래식 작업 및 함수 집합입니다.|
|퀀텀 회로|퀀텀 컴퓨터의 프로그램 표현입니다. 자세한 내용은 <xref:microsoft.quantum.concepts.circuits> 섹션을 참조 하세요.|
|퀀텀 상태|시스템의 그래픽 표현입니다. 이는 일반적으로 복잡 한 열 벡터로 표시 됩니다. 자세한 내용은 <xref:microsoft.quantum.concepts.vectors>을 참조하세요. |
|고 비트|퀀텀 저장소의 단위입니다. 자세한 내용은 <xref:microsoft.quantum.concepts.qubit> 섹션을 참조 하세요.|
|반복-성공-성공|확률적가 성공 하는 퀀텀 알고리즘입니다. 오류가 발생 하면 루틴이 성공 하거나 제한에 도달할 때까지 다시 시도 됩니다. |
|소프트웨어 스택|퀀텀 컴퓨터를 작동 하는 데 필요한 컴파일러, 시뮬레이터 및 런타임 뿐만 아니라 기존 및 퀀텀 소프트웨어의 전체 집합입니다. 자세한 내용은 <xref:microsoft.quantum.concepts.software-stack> 섹션을 참조 하세요. |
|대상 컴퓨터|추상 퀀텀 프로그램을 하드웨어 또는 시뮬레이션으로 낮추는 컴파일 대상입니다. 여기에는 일반적으로 게이트 교체, 오류 수정 인코딩, 기 하 도형 레이아웃 등을 비롯 한 많은 용도로 다시 쓰기가 포함 됩니다.|
|튜플이|괄호를 통해 쉼표로 구분 된 형식으로 그룹화 합니다. |
|사용자 정의 형식|단일 단위로 참조 될 수 있는 기본 제공 또는 이전에 정의 된 형식의 컬렉션입니다.|

