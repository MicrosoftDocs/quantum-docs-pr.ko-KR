---
title: Q#에서 양자 컴퓨팅을 배우려면 어떻게 해야 하나요?
description: ''
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: article
uid: microsoft.quantum.overview.learn
ms.openlocfilehash: 53682ae8ab9cb31fa0de68832cb3574aa4e30216
ms.sourcegitcommit: edcf15044d7bdf4f8b21fb8f6af4bde475eb13a0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/04/2019
ms.locfileid: "73529969"
---
# <a name="how-to-learn-quantum-computing"></a>양자 컴퓨팅을 학습하는 방법

양자 컴퓨팅을 학습하고 첫 번째 프로그램을 작성하는 방법에 대한 지침을 얻습니다. 이 가이드는 완전하지 않지만 시작하기에는 좋습니다.

## <a name="getting-started-overview"></a>시작 개요

[Microsoft Quantum Development Kit 시작](xref:microsoft.quantum.welcome)에서는 첫 번째 Q# 프로그램을 작성하기 위한 자습서, 시작 가이드, 양자 프로그램 개발용 Q# 양자 라이브러리 소개를 포함하여 Q#을 사용한 양자 컴퓨팅에 대해 개략적으로 설명합니다.

## <a name="learning-the-basics-what-do-you-need-to-know"></a>기본 사항 알아보기: 알아야 할 사항

Q#과 양자 컴퓨팅에 대해 알아보거나 양자 애플리케이션 작성을 시작하기 위해 양자 물리학을 알 필요가 없습니다.

이러한 개념은 양자 프로그램 코딩을 시작하는 데 필요한 기본적인 정보를 제공합니다.  

* [기본 양자 역학](xref:microsoft.quantum.concepts.intro): 단지 코딩을 시작하기 위해 양자 물리학을 알 필요가 없다고 말했습니다. 이는 사실입니다! 그러나 양자 역학에 대한 몇 가지 기본 개념과 해당 수학적 표기법은 양자 프로그래밍을 이해하는 데 도움이 됩니다.

* **선형 대수(벡터 및 행렬)** : 양자 컴퓨팅에서 양자 상태는 벡터로 표현되며, 양자 연산은 이러한 벡터에 적용되는 선형 변환입니다.  다음은 [선형 대수에 대한 Jupyter Notebook 자습서](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)입니다.  [벡터 및 행렬](xref:microsoft.quantum.concepts.vectors)에 대한 개념 가이드에서 선형 대수에 대해 더 자세히 알아볼 수도 있습니다.

* **복소수**: 양자 상태 벡터의 계수는 복소수입니다. 몇 가지 기본 양자 컴퓨팅 개념은 없어도 이해할 수 있지만, 양자 도구 키트에 조기에 통합해야 합니다.  다음은 양자 컴퓨팅을 사용하는 데 필요한 수학적 배경을 설명하는 [복소수에 대한 Jupyter Notebook 자습서](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)입니다. 

기본 사항을 알아보았으므로, 이제 양자 프로그램 작성 방법을 알아볼 수 있습니다.  다음과 같은 여러 가지 방법으로 양자 프로그램에 대해 알아볼 수 있습니다.

## <a name="do-the-quantum-katas"></a>Quantum Katas 수행

[Quantum Katas](xref:microsoft.quantum.overview.katas)는 양자 컴퓨팅과 Q# 프로그래밍의 요소를 동시에 가르치기 위한 자가 학습 자습서의 오픈 소스 시리즈입니다.  각 kata는 katas를 성공적으로 완료하는 데 필요한 양자 컴퓨팅 개념을 학습하는 데 사용할 수 있는 추가 학습 자료를 참조합니다.  

## <a name="dive-into-the-theory"></a>이론에 대한 심층적 이해

양자 역학과 양자 컴퓨팅에 대한 이론을 더 자세히 살펴보겠습니다. 유용한 자료 목록은 다음과 같습니다.

* [양자 컴퓨팅 개념](xref:microsoft.quantum.concepts.intro)에 대한 가이드부터 시작합니다. 이 가이드에서는 양자 컴퓨팅에 대한 기본 개념을 다루고 있습니다.
* _Python 및 Q#을 사용하여 양자 컴퓨팅 학습_(Sarah C. Kaiser 및 Christopher E. Granade) - 양자 역학에 대한 경험이 거의 또는 전혀 없지만 일부 프로그래밍 배경 지식을 갖춘 사용자를 위한 훌륭한 소개 문서입니다.
* _양자 계산 및 양자 정보_(Michael A. Nielsen, Isaac L. Chuang)는 양자 계산 분야에서 가장 많이 인용되는 텍스트이며 이 주제에 대한 표준 텍스트로 간주됩니다. 이 서적에서는 양자 역학과 컴퓨터 과학에 대한 최소한의 사전 경험을 가정합니다. 주제에 대한 엄격한 소개를 원하는 사용자뿐만 아니라 고급 개념에 대한 참고 자료를 찾고 있는 사용자에게도 매우 적합합니다.
* MIT OpenCourseWare에는 양자 역학의 기본 사항을 학습하기 위해 Allan Adams가 강의하는 뛰어난 [온라인 강좌](https://www.youtube.com/watch?v=lZ3bPUKo5zc&list=PLUl4u3cNGP61-9PEhRognw5vryrSEVLPr)가 있습니다. 기초 물리학을 더 잘 이해하려는 개발자에게 적합합니다.

## <a name="join-the-quantum-community"></a>양자 커뮤니티 참여

혼자서 학습할 필요가 없습니다. 기꺼이 도움을 줄 아마추어와 전문가들이 모두 참여하는 큰 커뮤니티가 있습니다. 망설임 없이 질문하세요!

* Q# 또는 양자 컴퓨팅에 대한 질문이 있는 경우 주저하지 말고 양자 컴퓨팅 StackExchange 사이트를 살펴보세요. 특정 질문을 찾을 수 없으면 언제든지 새 질문을 할 수 있습니다. 
* Q#에 대한 최신 뉴스와 리소스를 최신 상태로 유지하려면 [Q# 블로그](https://devblogs.microsoft.com/qsharp/) 및 [Microsoft Quantum 블로그](https://cloudblogs.microsoft.com/quantum/)를 확인하세요.
* 더 많은 리소스와 자료는 [Q# 커뮤니티](https://qsharp.community/) 및 [Awesome Q#](https://project-awesome.org/ebraminio/awesome-qsharp)을 확인하세요.

 양자 컴퓨팅에 대한 강좌를 개설하려는 경우 [Microsoft Quantum Network](https://info.microsoft.com/LearnMoreAboutMicrosoftQuantumNetwork.html)에서 커리큘럼 구성에 대한 도움을 받을 수 있습니다.  

