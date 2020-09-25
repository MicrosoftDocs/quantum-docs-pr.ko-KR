---
title: 양자 컴퓨팅 소개
description: 양자 컴퓨팅이란 무엇인지, 양자 컴퓨터로 무엇을 할 수 있는지, 양자 컴퓨팅을 배우려면 어떻게 해야 하는지 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 05/05/2020
ms.topic: overview
uid: microsoft.quantum.overview.introduction
no-loc:
- Q#
- $$v
ms.openlocfilehash: c3374e9fae07cc38761e404be7819e7cf699ce2b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834519"
---
# <a name="introduction-to-quantum-computing-and-the-quantum-development-kit"></a>양자 컴퓨팅 및 Quantum Development Kit 소개

Microsoft QDK(Quantum Development Kit)는 개발자가 양자 알고리즘을 학습하고 양자 프로그램을 작성할 수 있도록 설계된 오픈 소스 도구 세트입니다. 양자 컴퓨팅은 환경, 농업, 의료, 에너지, 기후, 재료 과학 및 아직 접하지 않은 다른 분야에서 지구의 가장 큰 도전 과제 중 일부를 해결할 것이라고 약속하고 있습니다.  

이러한 문제 중 일부는 가장 강력한 컴퓨터에도 문제가 발생한다는 것입니다. 양자 기술은 이제 막 컴퓨팅 세계에 영향을 미치기 시작했지만, 컴퓨팅에 대해 생각하는 방식을 광범위하게 변화시킬 수 있습니다.

## <a name="what-is-quantum-computing"></a>양자 컴퓨팅이란?

현대의 언어 용법에서 양자라는 단어는 일반적으로 원자 또는 아원자 입자의 속성을 가리키는 모든 물리적 속성에서 가능한 가장 작은 개별 단위를 의미합니다. 양자 컴퓨터는 실제 양자 입자, 인공 원자 또는 양자 입자의 집합적 속성을 처리 단위로 사용하며, 크고 복잡하며 비용이 많이 드는 디바이스입니다.

양자 물리학의 고유한 동작을 활용하여 이를 컴퓨팅에 적용하면 양자 컴퓨터에서 새로운 개념을 기존 프로그래밍 방식에 도입하여 중첩, 얽힘, 양자 간섭과 같은 양자 물리학적 동작을 활용합니다.

## <a name="what-can-a-quantum-computer-do"></a>양자 컴퓨터에서 수행할 수 있는 작업은 무엇인가요?

양자 컴퓨터는 모든 작업을 더 빠르게 수행할 수 있는 슈퍼 컴퓨터가 아니지만, 양자 컴퓨터가 매우 효율적으로 작동하는 몇 가지 영역이 있습니다.

- [양자 시뮬레이션](xref:microsoft.quantum.overview.introduction#quantum-simulation)
- [암호화](xref:microsoft.quantum.overview.introduction#cryptography-and-shors-algorithm)
- [검색](xref:microsoft.quantum.overview.introduction#search-and-grovers-algorithm)
- [최적화](xref:microsoft.quantum.overview.introduction#quantum-inspired-computing-and-optimization)
- [기계 학습](xref:microsoft.quantum.overview.introduction#quantum-machine-learning)

## <a name="quantum-simulation"></a>양자 시뮬레이션

양자 컴퓨터는 계산에서 양자 현상을 사용하므로 다른 양자 시스템을 모델링하는 데 적합합니다. 광합성, 초전도체 그리고 복합 분자 형성은 양자 프로그램에서 시뮬레이션할 수 있는 양자 메커니즘의 예입니다.

## <a name="cryptography-and-shors-algorithm"></a>암호화 및 Shor 알고리즘

1994년 Peter Shor는 확장 가능한 양자 컴퓨터에서 RSA 알고리즘과 같이 널리 사용되는 암호화 기술을 해제할 수 있음을 보여 주었습니다. 클래식 암호화는 정수 인수 분해 또는 이산 로그와 같이 다루기 힘든 문제의 영향을 받으며, 이 중 상당 부분은 양자 컴퓨터를 사용하여 더 효율적으로 해결할 수 있습니다.

## <a name="search-and-grovers-algorithm"></a>검색 및 Grover 알고리즘

1996년 Lov Grover는 비정형 데이터를 검색하는 솔루션의 속도를 획기적으로 높여 클래식 알고리즘보다 더 적은 수의 단계로 검색을 실행하는 양자 알고리즘을 개발했습니다.

## <a name="quantum-inspired-computing-and-optimization"></a>양자 유도 컴퓨팅 및 최적화

양자 유도 알고리즘은 속도와 정확도를 높이기 위해 양자 원리를 사용하지만 클래식 컴퓨터 시스템에서 구현됩니다. 이 접근 방식을 통해 개발자는 아직 새로운 산업인 양자 하드웨어를 기다리지 않고도 오늘날 새로운 양자 기술의 강력한 기능을 활용할 수 있습니다.

최적화는 원하는 결과와 제약 조건을 고려하여 문제에 대한 최상의 솔루션을 찾는 프로세스입니다. 비용, 품질 또는 생산 시간과 같은 요소는 모두 산업과 과학의 중요한 결정에 영향을 줍니다. 오늘날의 클래식 컴퓨터에서 실행되는 양자 유도 최적화 알고리즘은 지금까지 불가능했던 솔루션을 찾을 수 있습니다. 혼잡을 줄이기 위해 교통 흐름을 최적화하는 것 외에도 비행기 탑승구 할당, 패키지 배송, 작업 예약 등이 있습니다. 재료 과학의 획기적인 발전을 통해 새로운 형태의 에너지, 더 큰 용량의 배터리, 더 가볍고 내구성이 뛰어난 재료가 나타날 것입니다.

> [!NOTE]
> Microsoft 양자 유도 컴퓨팅을 [재료 과학](https://cloudblogs.microsoft.com/quantum/2020/01/21/oti-lumionics-accelerating-materials-design-microsoft-azure-quantum/), [위험 관리](https://cloudblogs.microsoft.com/quantum/2019/05/22/microsoft-quantum-collaborates-with-willis-towers-watson-to-transform-risk-management-solutions/) 및 [의학](https://blogs.microsoft.com/blog/2018/05/18/microsoft-quantum-helps-case-western-reserve-university-advance-mri-research/) 분야에서 사용하는 방법에 대해 자세히 알아보세요.

## <a name="quantum-machine-learning"></a>양자 기계 학습

클래식 컴퓨터의 기계 학습은 과학과 비즈니스의 세계를 혁신적으로 변화시키고 있습니다. 그러나 모델 학습에 들어가는 높은 계산 비용은 이 분야의 개발 및 범위를 넓히는 데 방해가 됩니다. 양자 기계 학습 영역은 클래식 컴퓨터보다 더 빠르게 실행되는 기계 학습을 가능하게 하는 양자 소프트웨어를 고안하고 구현하는 방법을 검색합니다.

Quantum Development Kit는 하이브리드 양자/클래식 기계 학습 실험을 실행할 수 있는 [양자 기계 학습 라이브러리](xref:microsoft.quantum.machine-learning.concepts.intro)와 함께 제공됩니다. 이 라이브러리는 샘플과 자습서를 포함하고 있으며, 감독된 분류 문제를 해결하기 위해 새 하이브리드 양자 클래식 알고리즘인 회로 중심 양자 분류자를 구현하는 데 필요한 도구를 제공합니다.

## <a name="no-locq-and-the-microsoft-quantum-development-kit-qdk"></a>Q# 및 Microsoft QDK(Quantum Development Kit)

Q#은 퀀텀 알고리즘을 개발하고 실행하기 위한 Microsoft의 오픈 소스 프로그래밍 언어입니다. 완전한 기능을 갖춘 Q#용 개발 키트인 [QDK](https://docs.microsoft.com/quantum/)의 일부로서, 표준 도구 및 언어와 함께 사용하여 다양한 환경에서 실행할 수 있는 퀀텀 애플리케이션(기본 제공되는 전체 상태 퀀텀 시뮬레이터 포함)을 개발할 수 있습니다.

Visual Studio 및 VS Code용 확장과 Python 및 Jupyter Notebook에서 사용할 수 있는 패키지가 있습니다.

QDK에는 전문적인 화학, 기계 학습 및 숫자 라이브러리와 함께 표준 라이브러리가 포함되어 있습니다.

설명서에는 Q# 언어 가이드, 자습서 및 샘플 코드가 포함되어 있어 빠르게 시작할 수 있으며, 다양한 문서를 통해 양자 컴퓨팅 개념을 더 깊이 이해할 수 있습니다.  

## <a name="microsoft-quantum-hardware-partners"></a>Microsoft 양자 하드웨어 파트너

Microsoft는 개발자에게 양자 하드웨어에 대한 클라우드 액세스를 제공하기 위해 양자 하드웨어 회사와 파트너 관계를 맺고 있습니다. 개발자는 [Azure Quantum](https://azure.microsoft.com/services/quantum/) 플랫폼과 Q# 언어를 활용하여 퀀텀 알고리즘을 검색하고 다양한 유형의 퀀텀 하드웨어에서 퀀텀 프로그램을 실행할 수 있습니다.

[IonQ](https://ionq.com/news/november-4-2019-microsoft-partnership) 및 [Honeywell](https://www.honeywell.com/en-us/newsroom/news/2019/11/the-future-of-quantum-computing)은 모두 **포획 이온(trapped ion) 기반** 프로세서를 사용하여 전자장에서 포획된 개별 이온을 활용하는 반면, [QCI](https://quantumcircuits.com/news-and-publications/quantum-circuits-partners-with-microsoft-on-azure-quantum)는 초전도 회로를 사용합니다.

## <a name="next-steps"></a>다음 단계

[양자 컴퓨팅의 주요 개념](xref:microsoft.quantum.overview.understanding)
[빠른 시작](xref:microsoft.quantum.welcome)