---
title: Quantum Katas 소개
description: Microsoft QDK(Quantum Development Kit)에서 제공하는 카타(학습 연습)에 대해 알아봅니다.
author: bradben
ms.author: bradben
ms.date: 06/02/2020
ms.topic: overview
uid: microsoft.quantum.overview.katas
ms.openlocfilehash: 1c4dfa5c47aa38935cd5936cd256e357b6605371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276215"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Quantum Katas에서 퀀텀 컴퓨팅 알아보기

[Quantum Kata](https://github.com/Microsoft/QuantumKatas/)는 퀀텀 컴퓨팅과 Q# 프로그래밍의 요소를 동시에 가르치기 위한 자가 오픈 소스, 학습 자습서 및 프로그래밍 연습입니다.

## <a name="learning-by-doing"></a>작업을 통한 학습

이 프로젝트에 수집되는 자습서와 연습은 작업을 수행하여 학습하는 방법을 강조합니다. 즉 매우 간단한 과제에서 상당히 까다로운 과제로 진행되는 특정 항목을 다루는 프로그래밍 작업을 제공합니다. 각 작업에서는 코드를 입력해야 합니다. 첫 번째 작업에서는 한 줄만 입력하면 되고, 마지막 작업에서는 상당한 크기의 코드 조각을 입력해야 합니다.

가장 중요한 점으로, Kata는 작업에 대한 솔루션을 설정하고 실행하고 유효성을 검사하는 테스트 프레임워크를 포함하고 있습니다. 따라서 자신의 솔루션에 대한 피드백을 즉시 받을 수 있으며, 접근 방식이 잘못된 경우 방법을 다시 생각해 볼 수 있습니다.

다음 중 원하는 환경을 선택하여 Kata를 학습에 사용할 수 있습니다.

* 바인더 환경 내의 Jupyter Notebook 온라인
* 로컬 머신에서 실행되는 Jupyter Notebook
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>Quantum Katas에서 배울 수 있는 내용

퀀텀 컴퓨팅의 기본 내용을 살펴보거나 퀀텀 알고리즘 및 프로토콜에 대해 자세히 알아봅니다. 처음에는 이 학습 경로를 따라 퀀텀 컴퓨팅의 기본 개념을 확실하게 익히는 것이 좋습니다. 물론 복소수처럼 이미 잘 알고 있는 토픽을 건너뛰고, 원하는 순서로 알고리즘을 알아볼 수도 있습니다.

### <a name="introduction-to-quantum-computing-concepts"></a>퀀텀 컴퓨팅 개념 소개

| Kata | 설명 |
|:-----|-------------|
|[복소수](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)|이 자습서에서는 퀀텀 컴퓨팅으로 작업하는 데 필요한 몇 가지 수학적 배경(예: 허수 및 복소수)을 설명합니다.|
|[선형 대수](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)|선형 대수학은 퀀텀 컴퓨팅에서 퀀텀 상태와 연산을 나타내기 위해 사용됩니다. 이 자습서는 행렬과 벡터를 포함한 기본 내용을 다룹니다.|
|[큐비트의 개념](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/Qubit)|퀀텀 컴퓨팅의 핵심 개념 중 하나인 큐비트에 대해 알아보세요. |
|[단일 큐비트 퀀텀 게이트](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates)|이 자습서에서는 퀀텀 알고리즘의 기본 구성 요소 역할을 하고 퀀텀 큐비트 상태를 다양한 방식으로 변환하는 단일 큐비트 퀀텀 게이트를 소개합니다.|
|[다중 큐비트 시스템](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitSystems)|이 자습서에서는 다중 큐비트 시스템, 이것의 수학적 표기법과 Q# 코드로의 표현 그리고 얽힘 개념을 소개합니다.|
|[다중 큐비트 퀀텀 게이트](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitGates)|이 자습서는 [단일 퀀텀 게이트](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates) 자습서를 따르며 다중 큐비트 시스템에 다중 퀀텀 게이트를 적용하는 데 초점을 두고 있습니다.|

### <a name="quantum-computing-fundamentals"></a>퀀텀 컴퓨팅 기본 사항

| Kata | 설명 |
|:-----|-------------|
|[퀀텀 게이트 인식](https://github.com/microsoft/QuantumKatas/tree/master/BasicGates)|Q#의 기본 퀀텀 게이트에 익숙해지도록 고안된 일련의 연습입니다. 기본 단일 큐비트 및 다중 큐비트 게이트, 수반 및 제어된 게이트, 게이트를 사용하여 큐비트 상태를 수정하는 방법을 포함합니다.|
|[퀀텀 중첩 만들기](https://github.com/microsoft/QuantumKatas/tree/master/Superposition)|Q#에서 중첩과 프로그래밍의 개념을 숙지하기 위해 이 연습을 활용합니다. Q#에서 기본 단일 큐비트 및 멀티 큐비트 게이트, 중첩 및 흐름 제어 및 재귀 연습을 포함합니다.|
|[측정값을 사용하여 퀀텀 상태 구별](https://github.com/microsoft/QuantumKatas/tree/master/Measurements)|퀀텀 측정과 직교 및 비직교 상태에 대해 배우면서 이들 연습 과제를 해결합니다. |
|[공동 측정값](https://github.com/microsoft/QuantumKatas/tree/master/JointMeasurements)|조인트 패리티 측정 및 [Measure](xref:microsoft.quantum.intrinsic.measure) 연산을 사용하여 퀀텀 상태를 구분하는 방법에 대해 알아봅니다.|

### <a name="algorithms"></a>알고리즘

| Kata | 설명 |
|:-----|-------------|
|[퀀텀 순간 이동](https://github.com/microsoft/QuantumKatas/tree/master/Teleportation)|이 kata는 기존 전용 통신과 이전에 공유된 퀀텀 얽힘만을 사용하여 퀀텀 상태를 전달할 수 있는 프로토콜인 퀀텀 순간 이동을 살펴봅니다.|
|[초고밀도 코딩](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)|슈퍼덴스 코딩은 기존에 공유된 퀀텀 얽힘을 사용하여 단 하나의 큐비트를 전송하여 2비트의 클래식 정보를 전송할 수 있는 프로토콜입니다.  |
|[도이치–조사 알고리즘](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringDeutschJozsaAlgorithm)|이 알고리즘은 결정적 기존 알고리즘보다 상당히 빠른 퀀텀 알고리즘의 첫 번째 예 중 하나입니다.|
|[Grover 검색 알고리즘의 상위 수준 속성 살펴보기](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringGroversAlgorithm)|퀀텀 컴퓨팅에서 가장 유명한 알고리즘 중 하나에 대한 개략적인 소개입니다. 특정 출력을 생성하는 블랙 박스(oracle)에 입력을 찾는 문제를 해결합니다. |
|[Grover 검색 알고리즘 구현](https://github.com/microsoft/QuantumKatas/tree/master/GroversAlgorithm)|이 kata는 Grover의 검색 알고리즘에 더 자세히 알아보며, oracles 쓰기, 알고리즘 단계 수행 및 마지막으로 이를 모두 종합합니다.|
|[Grover 알고리즘을 사용하여 실제 문제 해결: SAT 문제](https://github.com/microsoft/QuantumKatas/tree/master/SolveSATWithGrover)|Grover 알고리즘을 사용하여 [부울 만족도 문제](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem)(SAT)를 예로 들어 현실적인 문제를 해결하는 일련의 연습입니다.  |
|[Grover 알고리즘을 사용하여 실제 문제 해결: 그래프 색 지정 문제](https://github.com/microsoft/QuantumKatas/tree/master/GraphColoring)| 이 kata는 Grover의 알고리즘을 좀 더 살펴보고, 이번에는 그래프 색 지정 문제를 예로 들어 [제약 조건 만족 문제](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)를 해결합니다. |

### <a name="protocols-and-libraries"></a>프로토콜 및 라이브러리

| Kata | 설명 |
|:-----|-------------|
|[퀀텀 키 배포용 BB84 프로토콜](https://github.com/microsoft/QuantumKatas/tree/master/KeyDistribution_BB84)|큐비트를 사용하여 암호 키를 교환하는 퀀텀 키 배포 프로토콜 [BB84](https://en.wikipedia.org/wiki/BB84)에 대해 알아보고 구현합니다. |
|[비트 대칭 이동 오류 수정 코드](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)|가장 간단한 QEC(퀀텀 오류 수정) 코드인 3큐비트 대칭 이동 코드를 사용하여 퀀텀 오류 수정에 대해 살펴봅니다.|
|[단계 예측](https://github.com/microsoft/QuantumKatas/blob/master/PhaseEstimation)|위상 추정 알고리즘은 퀀텀 컴퓨팅의 가장 기본적인 구성 요소의 일부입니다. 퀀텀 위상 추정을 다루는 이러한 연습을 통한 위상 추적과 Q#에서 위상 추정 루틴을 준비하고 실행하는 방법에 대해 알아봅니다.|
|[퀀텀 산술: 리플 캐리 가산기 만들기](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)|퀀텀 컴퓨터에서 [리플 캐리](https://en.wikipedia.org/wiki/Adder_(electronics)#Ripple-carry_adder) 추가에 대해 살펴보는 일련의 심층 연습입니다. 인플레이스 퀀텀 가산기를 만들고 다른 알고리즘으로 확장한 다음, 마지막으로 인플레이스 퀀텀 감산기를 만듭니다.   |

### <a name="entanglement-games"></a>얽힘 게임

| Kata | 설명 |
|:-----|-------------|
|[CHSH 게임](https://github.com/microsoft/QuantumKatas/tree/master/CHSHGame)|[CHSH](https://en.wikipedia.org/wiki/CHSH_inequality) 게임을 구현하여 퀀텀 얽힘에 대해 살펴봅니다. 이 [비로컬](https://en.wikipedia.org/wiki/Quantum_refereed_game) 게임은 퀀텀 얽힘을 사용하여 단순한 고전적인 전략만으로도 플레이어의 승률을 높이는 방법을 보여줍니다.|
|[GHZ 게임](https://github.com/microsoft/QuantumKatas/tree/master/GHZGame)|GHZ 게임은 또 다른 비로컬 게임이지만 3명의 플레이어가 참여할 수 있습니다.|
|[머민-페레스 매직 스퀘어 게임](https://github.com/microsoft/QuantumKatas/tree/master/MagicSquareGame)|마법의 정사각형 게임을 통해 [퀀텀 의사 텔레파시](https://en.wikipedia.org/wiki/Quantum_pseudo-telepathy#The_Mermin%E2%80%93Peres_magic_square_game)에 대해 살펴보는 일련의 연습입니다.  |

## <a name="resources"></a>리소스

[Quantum Katas의 전체 시리즈 참조](https://github.com/microsoft/QuantumKatas)

[online에서 katas 실행](https://aka.ms/try-quantum-katas)
