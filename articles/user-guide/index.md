---
title: Q# 사용자 가이드
description: 사용자 가이드의 용도 및 내용 개요
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: f0680e773c8233d6c4f1acb742b3cc38dbc069d5
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834757"
---
# <a name="the-no-locq-user-guide"></a>Q# 사용자 가이드

Q# 사용자 가이드 시작! 

이 가이드의 여러 토픽에서 Q# 언어의 핵심 개념과 퀀텀 프로그램을 작성하는 데 필요한 모든 정보를 자세히 설명합니다.

## <a name="user-guide-contents"></a>사용자 가이드 내용

- [Q# 기본 사항](xref:microsoft.quantum.guide.basics): Q# 프로그래밍 언어의 목적과 기능에 대한 소개 개요입니다. 

- [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs): Q# 프로그램을 실행하는 방법을 설명하고, 프로그램을 호출할 수 있는 다양한 방법(명령줄에서, Q# Jupyter Notebook에서 또는 Python이나 .NET 언어로 작성된 기존 호스트 프로그램에서)에 대한 개요를 제공합니다.

### <a name="no-locq-language"></a>Q# 언어

- [Q#의 형식](xref:microsoft.quantum.guide.types): Q# 형식 모델을 배치하고 형식을 지정하고 사용하는 구문을 설명합니다.

- [Type 식](xref:microsoft.quantum.guide.expressions): Q#에서 각 형식의 값을 지정하고, 참조하고, 결합하고, 연산하는 방법을 자세히 설명합니다. 

### <a name="using-no-locq"></a>Q# 사용

- [Q#파일 구조](xref:microsoft.quantum.guide.filestructure): `*.qs` Q# 파일의 구문과 구조를 설명합니다.

- [연산 및 함수](xref:microsoft.quantum.guide.operationsfunctions): Q# 언어의 두 가지 호출 가능 형식, 즉, 큐비트 레지스터에 대한 동작을 포함하는 *연산* 및 클래식 정보와 엄격하게 작동하는 *함수*에 대해 자세히 설명합니다. 
    여기에서는 수반(adjoint) 및 제어된 양자 연산 버전을 포함하여 이러한 형식을 정의하고 호출하는 방법을 알아봅니다.

- [변수](xref:microsoft.quantum.guide.variables): Q# 프로그램 내 변수의 역할 및 변수를 효과적으로 활용하는 방법을 설명합니다. 
    예를 들어, 바인딩 범위에 대한 정보는 물론 변경 불가능 및 변경 가능 변수의 차이와 이러한 변수를 할당 또는 재할당하는 방법에 대한 정보를 찾을 수 있습니다.

- [큐비트 작업](xref:microsoft.quantum.guide.qubits): 개별 큐비트 및 큐비트 시스템을 처리하는 데 사용되는 Q#의 기능, 특히 할당, 작업 수행 및 측정에 대해 설명합니다. 

- [제어 흐름](xref:microsoft.quantum.guide.controlflow): Q#에서 사용 가능한 프로그래밍 제어 흐름 패턴에 대해 자세히 설명합니다. 여기에는 다양한 표준 기술(예: 조건부 실행, *for* 루프, *while* 루프)은 물론 퀀텀 관련 *Repeat-Until-Success(성공할 때까지 반복)* 패턴이 포함됩니다.

- [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging): 코드가 수행해야 하는 작업을 수행하도록 만드는 몇 가지 기술을 자세히 설명합니다. 
    양자 정보는 일반적으로 불투명하기 때문에 양자 프로그램을 디버깅하려면 특수 기술이 필요할 수 있습니다. 
    다행히 Q#은 퀀텀 관련 기술 외에도 프로그래머들에게 익숙한 여러 기존 디버깅 기술을 지원합니다. 여기에는 Q#에서 단위 테스트를 만들어 실행하는 기능, 그리고 코드의 값 및 확률과 대상 머신의 상태를 출력하는 `Dump` 함수에 대한 *어설션*을 포함하는 기능이 포함됩니다. 
    후자는 전체 상태 시뮬레이터와 함께 사용하여 일부 퀀텀 제한을 회피(예: [복사 불가능성 정리](xref:microsoft.quantum.concepts.pauli))하는 방식으로 계산의 특정 부분을 디버그할 수 있습니다.

### <a name="quantum-simulators-and-resource-estimators"></a>양자 시뮬레이터 및 리소스 예측 도구

- [퀀텀 시뮬레이터 및 호스트 애플리케이션](xref:microsoft.quantum.machines): 사용 가능한 여러 시뮬레이터에 대한 개요 및 호스트 프로그램과 대상 머신 간의 일반적인 실행 모델입니다.

- [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator): 전체 퀀텀 상태를 시뮬레이션하는 대상 머신입니다. 소규모 프로그램(몇십 큐비트 미만)을 완전히 실행하거나 디버그하는 데 유용합니다.

- [리소스 추정기](xref:microsoft.quantum.machines.resources-estimator): 퀀텀 컴퓨터에서 지정된 Q# 연산 인스턴스를 실행하는 데 필요한 리소스를 예측합니다.

- [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro): 실제로 퀀텀 컴퓨터의 상태를 시뮬레이션하지 않고 퀀텀 프로그램을 실행하기 때문에 수천 큐비트를 사용하는 퀀텀 프로그램을 실행할 수 있습니다. 양자 프로그램 내에서 클래식 코드를 디버그하는 것은 물론 필요한 리소스를 예측하는 데 유용합니다.

- [Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator): 수백만 큐비트에 사용할 수 있는 특수 목적의 퀀텀 시뮬레이터입니다. 단, 제한된 퀀텀 연산 세트(X, CNOT 및 다중 제어 X)가 있는 프로그램에만 사용할 수 있습니다.

### <a name="quick-reference-pages"></a>빠른 참조 페이지

- [IQ# 매직 명령](xref:microsoft.quantum.guide.quickref.iqsharp): Q# Jupyter Notebook 내 IQ# 매직 명령에 대한 빠른 참조 페이지입니다.
