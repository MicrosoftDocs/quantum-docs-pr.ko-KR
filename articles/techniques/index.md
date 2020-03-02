---
title: 양자 개발 기술
description: Q# 프로그램 개발의 기본 사항을 알아보고, 작업, 함수, 변수 및 큐비트를 사용하고, 간단한 양자 프로그램을 만듭니다.
keywords: SEO champ와 상담하지 않고 키워드를 추가하거나 편집하지 마세요.
author: QuantumWriter
ms.author: MSFT-alias-person-or-DL
ms.date: 9/20/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.techniques.intro
ms.openlocfilehash: e5b7fbde18afbc0333d89f70c5e4596848e30f4f
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907718"
---
# <a name="quantum-development-techniques"></a>양자 개발 기술

설명서의 이번 섹션에서는 Q#에서 양자 프로그램을 만드는 데 사용되는 핵심 개념을 자세히 설명하고, 클래식 애플리케이션에서 이러한 프로그램과 상호 작용하는 방법을 알아봅니다.
[양자 컴퓨팅 개념](xref:microsoft.quantum.concepts.intro)에 설명된 개념을 포함하여 양자 컴퓨팅 개념을 *약간* 알고 있어야 하지만, 양자 컴퓨팅 전문가가 아니어도 다음 섹션에서 많은 것을 배울 수 있습니다.

섹션의 내용은 다음과 같습니다.

- [Q# 프로그램 개요](xref:microsoft.quantum.techniques.file-structure)에서는 Q# 프로그래밍 언어의 목적 및 기능을 간략하게 설명합니다. 
    특히 Q#은 전체 상태 시뮬레이터를 통해 양자 역학을 시뮬레이션하는 기능을 제공하지만, 단순히 양자 역학을 시뮬레이션하기 위한 언어가 *아니라는* 점을 명확하게 설명합니다. 
    Q#은 미래를 내다보고 설계되었으며, 해당 프로그램은 클래식 제어 컴퓨터가 큐비트와 *상호 작용*하는 방식을 설명합니다. 

- [작업 및 함수](xref:microsoft.quantum.techniques.opsandfunctions)에서는 Q# 언어의 두 가지 호출 가능 형식, 즉, 큐비트 및 양자 시스템에 대한 동작을 포함하는 *작업*, 그리고 클래식 정보를 엄격하게 사용하는 *함수*에 대해 자세히 설명합니다. 
    클래식 정보와 양자 정보가 함께 작동하지 않으면 양자 컴퓨팅에 도달할 수 없습니다. 
    이 섹션에서는 Q# 프로그램의 제어 흐름 내에서 이러한 호출 가능 함수를 정의하고 사용하는 방법을 설명합니다.

- [지역 변수](xref:microsoft.quantum.techniques.local-variables)에서는 Q# 프로그램 내 변수의 역할 및 변수를 효과적으로 활용하는 방법을 설명합니다. 
    특히 변경이 불가능한 변수와 변경 가능한 변수의 차이점 및 이러한 변수를 할당/재할당하는 방법을 알아봅니다.

- [큐비트 사용](xref:microsoft.quantum.techniques.qubits)에서는 개별 큐비트 및 큐비트 시스템을 처리하는 데 사용할 수 있는 Q# 기능에 대해 설명합니다. 
    구체적으로 말하자면, 큐비트를 할당하고, 큐비트에 대한 작업을 수행하고, 궁극적으로 큐비트를 측정하는 방법을 설명합니다. 
    또한 몇 가지 유용한 제어 흐름 기술을 배울 것입니다.

- [종합](xref:microsoft.quantum.techniques.puttingittogether)섹션에서는 위에서 배운 기술을 활용해 기존 2비트로 1큐비트를 통째로 다른 큐비트로 "텔레포트"하는 **양자 텔레포트** 프로그램을 만들어 보겠습니다.

- [더 알아보기](xref:microsoft.quantum.techniques.going-further)에서는 좀 더 복잡한 양자 프로그래밍으로 넘어갈 때 유용하게 사용할 수 있는 고급 기술을 소개합니다. 
    특히, 입력/출력의 형식 및 큐비트 *빌리기*와 관계없이 고차 제어 흐름을 사용할 수 있는 Q#의 *형식 매개 변수가 있는* 작업 및 함수의 사용 방법을 설명합니다. 
    후자는 Q# 작업에서 계산을 도와주기 위해 "더티" 큐비트를 사용할 수 있다는 점에서(큐비트는 반드시 알려진 상태로 초기화되는 것은 아님) 기본 큐비트 할당과는 다릅니다.

- [테스트 및 디버그](xref:microsoft.quantum.techniques.testing-and-debugging)에서는 코드가 본래 목적을 수행하게 만들 수 있는 몇 가지 기술을 자세히 설명합니다. 
    양자 정보는 일반적으로 불투명하기 때문에 양자 프로그램을 디버깅하려면 특수 기술이 필요할 수 있습니다. 
    다행히 Q#은 양자 관련 기술 외에도 프로그래머들에게 익숙한 여러 기존 디버깅 기술을 지원합니다. 여기에는 Q#에서 단위 테스트를 만들고/실행하는 기능, 그리고 코드의 값 및 확률과 대상 머신의 상태를 출력하는 `Dump` 함수에 대한 *어설션*을 포함하는 기능이 포함됩니다. 
    후자는 전체 상태 시뮬레이터와 함께 사용하여 일부 양자 제한을 회피(예: 복사 불가능성 정리)하는 방식으로 계산의 특정 부분을 디버그할 수 있습니다.


![양자](~/media/mobius_strip_preview.png)
