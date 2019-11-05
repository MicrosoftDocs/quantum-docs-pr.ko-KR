---
title: Q#이란?
description: 양자 컴퓨터 애플리케이션을 개발하기 위해 Microsoft에서 만든 프로그래밍 언어인 Q#에 대해 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: e04228ff62092a15c529297bd56b9ee48399f4a5
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443956"
---
# <a name="what-is-q"></a>Q#이란?

Q#은 양자 컴퓨팅에 특화된 기능이 포함된 프로그래밍 언어입니다. Q#은 양자 프로그래머에게 게이트 시퀀스 최적화 또는 양자 컴퓨터의 물리적 구현과 같은 기술적 세부 정보를 고려하지 않고도 알고리즘에 집중할 수 있는 프레임워크를 제공합니다.

Q#프로그래밍 언어는 양자 컴퓨터의 내부의 논리에 대해 걱정할 필요 없이 알고리즘을 개발할 수 있도록 형식, 연산 및 논리 식의 직관적인 세트를 제공합니다.

## <a name="code-algorithms"></a>코드 알고리즘

초기 시대의 양자 컴퓨팅 알고리즘은 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되었습니다.  회로 모델은 Microsoft에서 수년간 양자 컴퓨팅 연구에 매우 유용했지만, 개발자는 양자 회로를 넘어서 Q#을 사용하여 양자 알고리즘과 애플리케이션을 개발할 수 있다고 생각합니다. Q# 언어는 수십 년간 클래식 소프트웨어 개발을 통해 습득한 것을 활용하고, 특히 양자 컴퓨팅을 대상으로 하는 고급 언어 기능을 양자 개발자에게 제공합니다.


## <a name="how-does-q-work"></a>Q#은 어떻게 작동하나요?

Q#의 기본 구성 요소 중 하나는 `Qubit` 형식이며, 실제 큐비트처럼 복사하거나 직접 액세스할 수 없습니다. 대신, 이를 측정하여 `Zero` 및 `One`의 두 가지 가능한 값을 사용할 수 있는 Q# 형식의 `Result` 변수에 측정 결과를 저장할 수 있습니다. 이와 같은 구문을 통해 알고리즘은 항상 양자 물리학의 법칙을 준수하며 양자 컴퓨터 또는 시뮬레이터에서 올바르게 실행될 수 있습니다.

또한 Q#에는 모든 양자 규칙이 적용될 수 있도록 조건 또는 루프 같은 클래식 논리 기능도 포함되어 있습니다. 예를 들어 양자 연산은 되돌릴 수 있어야 합니다. 이렇게 하면 루프가 실행되는 방식에 일부 제약 조건이 적용됩니다.

Q# 프로그램은 종종 C# 또는 Python으로 작성된 호스트 프로그램과 쌍을 이루어 클래식 코드와 양자 코드를 편리하게 구성할 수 있습니다. QDK는 C# 및 Python과 같은 .NET 언어를 지원하는 것 외에도 IQ# Juppyter 커널을 사용하여 Jupyter Notebook을 지원합니다.

## <a name="use-q-to-learn-quantum-computing"></a>Q#을 사용하여 양자 컴퓨팅 학습

지금까지 양자 컴퓨팅을 학습하려면 순서가 지정된 양자 게이트와 측정의 시퀀스 형식으로 알고리즘을 이해하기 위해 회로 모델을 학습해야 했습니다. Q#을 사용하면 양자 프로그램을 작성하여 양자 컴퓨팅을 학습할 수 있는 다른 경로를 사용할 수 있습니다.

## <a name="use-q-to-design-quantum-algorithms"></a>Q#을 사용하여 양자 알고리즘 디자인

Q#은 고급 양자 알고리즘을 빌드하는 데 도움이 되는 라이브러리와 사용자 정의 형식을 점점 더 많이 제공합니다. 예를 들어 q1과 q2의 두 큐비트를 얽어야 할까요? 필요한 게이트를 개별적으로 적용하여 큐비트를 얽는 대신, 이미 기본 제공된 `PrepareEntangledState([q1], [q2])` 연산을 사용할 수 있습니다.

## <a name="use-q-to-estimate-quantum-resources"></a>Q#을 사용하여 양자 리소스 예측

QDK(Quantum Development Kit)와 함께 제공되는 전체 상태 양자 시뮬레이터를 사용하여 Q# 프로그램 실행을 시뮬레이션할 수 있습니다.  QDK는 너무 커서 시뮬레이터에서 실행할 수 없는 Q# 프로그램에 대한 인사이트를 제공하는 리소스 예측기도 제공합니다.  알고리즘 디자이너는 더 적은 리소스를 사용하도록(즉, 더 적은 수의 작업에 대해 더 적은 수의 큐비트가 실행되도록), 초기에 더 작은 규모의 양자 하드웨어에서 실행되도록 프로그램을 튜닝할 수 있습니다.   

## <a name="use-q-to-validate-hardware-performance"></a>Q#을 사용하여 하드웨어 성능 확인

Q#의 장점은 프로그램을 한 번 작성하여 양자 시뮬레이터에서 실행하면 여러 양자 컴퓨터 하드웨어에서 실행할 수 있다는 것입니다.  양자 컴퓨터가 진화하여 새로운 양자 컴퓨터를 사용할 수 있게 될 때 Q#으로 작성된 벤치마크 프로그램을 실행하여 하드웨어 성능을 확인하고 결과를 비교할 수 있습니다.  

## <a name="next-steps"></a>다음 단계

* [양자 컴퓨팅을 학습하려면 어떻게 하나요?](xref:microsoft.quantum.overview.learn)
* [Microsoft Quantum Development Kit 시작](xref:microsoft.quantum.welcome)
