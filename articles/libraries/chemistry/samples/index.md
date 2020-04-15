---
title: 양자 화학 샘플 애플리케이션
description: Microsoft 양자 화학 라이브러리의 샘플 애플리케이션을 살펴봅니다.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples
ms.openlocfilehash: 5168fc8592d34a32ba67e5a0c4793aa17599fd35
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/13/2020
ms.locfileid: "77906494"
---
# <a name="quantum-chemistry-examples"></a>양자 화학 예

양자 화학 개념에서 페르미온 해밀턴 예를 수동으로 생성했습니다. 이제 [해밀턴 역학 시뮬레이션](xref:microsoft.quantum.libraries.standard.algorithms)에 설명된 화학 시뮬레이션 알고리즘과 Canon 라이브러리의 [양자 단계 예측](xref:microsoft.quantum.libraries.characterization)을 결합합니다. 이 결합을 통해 양자 컴퓨터에서 양자 화학의 주요 애플리케이션 중 하나인 표현된 분자에서 에너지 수준의 추정 값을 얻을 수 있습니다. 

해밀턴 용어를 하나씩 지정하는 대신, 양자 화학 실험을 규모에 맞게 수행할 수 있는 몇 가지 예도 진행합니다. 먼저 [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)에 인코딩된 화학 해밀턴을 로드하는 예부터 시작합니다.

[전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)에서 시뮬레이션하기에는 너무 큰 분자의 경우 흥미로운 과학을 계속 수행할 수 있습니다. 예를 들어 대규모 화학 시뮬레이션을 수행하는 데 드는 리소스 비용은 [추적 시뮬레이터](xref:microsoft.quantum.machines.qc-trace-simulator.intro)를 대상으로 하여 계속 평가할 수 있습니다.

이제 몇 가지 제공된 샘플을 통해 화학 시뮬레이션 라이브러리의 흥미로운 애플리케이션을 설명하겠습니다.
