---
title: Quantum Katas 소개
description: Microsoft QDK(Quantum Development Kit)에서 제공하는 카타(학습 연습)에 대해 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/17/2019
ms.topic: overview
uid: microsoft.quantum.overview.katas
ms.openlocfilehash: af54a2260147b8ca07919b241548aac85ed0d8a1
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "76821102"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Quantum Katas에서 양자 컴퓨팅 알아보기

[Quantum Katas](https://github.com/Microsoft/QuantumKatas/)는 양자 컴퓨팅과 Q# 프로그래밍 요소를 동시에 가르치기 위한 자가 학습 자습서 및 프로그래밍 연습 세트로 구성된 오픈 소스 컬렉션입니다.

## <a name="learning-by-doing"></a>작업을 통한 학습

이 프로젝트에 수집되는 자습서와 연습은 작업을 수행하여 학습하는 방법을 강조합니다. 즉 매우 간단한 과제에서 상당히 까다로운 과제로 진행되는 특정 항목을 다루는 프로그래밍 작업을 제공합니다. 각 작업에서는 코드를 입력해야 합니다. 첫 번째 작업에서는 한 줄만 입력하면 되고, 마지막 작업에서는 상당한 크기의 코드 조각을 입력해야 합니다.

가장 중요한 점으로, katas는 작업에 대한 솔루션을 설정하고 실행하고 유효성을 검사하는 테스트 프레임워크를 포함하고 있습니다. 따라서 자신의 솔루션에 대한 피드백을 즉시 받을 수 있으며, 접근 방식이 잘못된 경우 방법을 다시 생각해 볼 수 있습니다.

다음 중 원하는 환경을 선택하여 Katas를 학습에 사용할 수 있습니다.

* 바인더 환경 내의 Jupyter Notebook 온라인
* 로컬 머신에서 실행되는 Jupyter Notebook
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>Quantum Katas에서 배울 수 있는 내용

다음은 Quantum Katas에서 다루는 주요 토픽의 요약 정보입니다. 처음에는 이 학습 경로를 따라 양자 컴퓨팅의 기본 개념을 확실하게 익히는 것이 좋습니다. 물론 복소수처럼 이미 잘 알고 있는 토픽을 건너뛰고, 원하는 순서로 알고리즘을 알아볼 수도 있습니다.

### <a name="introduction-to-quantum-computing-concepts"></a>양자 컴퓨팅 개념 소개

* [복소수](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)
* [선형 대수](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)
* [큐비트의 개념](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/Qubit)
* [단일 큐비트 양자 게이트](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates)
* [다중 큐비트 시스템](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitSystems)
* [다중 큐비트 게이트](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitGates)

### <a name="quantum-computing-fundamentals"></a>양자 컴퓨팅 기본 사항

* [양자 게이트 인식](https://github.com/microsoft/QuantumKatas/tree/master/BasicGates)
* [양자 중첩 만들기](https://github.com/microsoft/QuantumKatas/tree/master/Superposition)
* [측정값을 사용하여 양자 상태 구별](https://github.com/microsoft/QuantumKatas/tree/master/Measurements)
* [공동 측정값](https://github.com/microsoft/QuantumKatas/tree/master/JointMeasurements)

### <a name="algorithms"></a>알고리즘

* [양자 순간 이동](https://github.com/microsoft/QuantumKatas/tree/master/Teleportation)
* [초고밀도 코딩](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)
* [도이치–조사 알고리즘](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringDeutschJozsaAlgorithm)
* [Grover 검색 알고리즘 구현](https://github.com/microsoft/QuantumKatas/tree/master/GroversAlgorithm)
* [Grover 검색 알고리즘의 상위 수준 속성 살펴보기](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringGroversAlgorithm)
* Grover 알고리즘을 사용하여 실제 문제 해결: [SAT 문제](https://github.com/microsoft/QuantumKatas/tree/master/SolveSATWithGrover) 및 [그래프 색 지정 문제](https://github.com/microsoft/QuantumKatas/tree/master/GraphColoring)

### <a name="protocols-and-libraries"></a>프로토콜 및 라이브러리

* [양자 키 배포용 BB84 프로토콜](https://github.com/microsoft/QuantumKatas/tree/master/KeyDistribution_BB84)
* 양자 오류 수정: [비트 대칭 이동 오류 수정 코드](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)
* [단계 예측](https://github.com/microsoft/QuantumKatas/blob/master/PhaseEstimation)
* 양자 산술: [리플 캐리 가산기 빌드](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)

### <a name="entanglement-games"></a>얽힘 게임

* [CHSH 게임](https://github.com/microsoft/QuantumKatas/tree/master/CHSHGame)
* [GHZ 게임](https://github.com/microsoft/QuantumKatas/tree/master/GHZGame)
* [머민-페레스 매직 스퀘어 게임](https://github.com/microsoft/QuantumKatas/tree/master/MagicSquareGame)

## <a name="resources"></a>리소스

* [Quantum Katas의 전체 시리즈 참조](https://github.com/microsoft/QuantumKatas)
* [online에서 katas 실행](https://aka.ms/try-quantum-katas)
