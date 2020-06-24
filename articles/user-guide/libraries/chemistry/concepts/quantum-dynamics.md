---
title: 퀀텀 Dynamics
description: 퀀텀 dynamics와 클래식 dynamics의 유사성 및 차이점을 알아봅니다.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantumdynamics
ms.openlocfilehash: 9cb74ccd4b7806a90c0701300860d777fa8e5d75
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275906"
---
# <a name="quantum-dynamics"></a>퀀텀 Dynamics

퀀텀 메커니즘은 주로 초기 퀀텀 상태 $ \ket{\psi (0)} $가 시간에 따라 달라 지는 방식을 이해 하는 데 사용할 수 있는 퀀텀 dynamics의 연구입니다. Diac 표기법에 대 한 자세한 내용은 퀀텀 컴퓨팅에 대 한 [개념 문서](xref:microsoft.quantum.concepts.dirac) 를 참조 하세요.
특히,이 초기 조건에서 퀀텀 상태, 진화 시간 및 퀀텀 동적 시스템의 사양을 감안 하면 퀀텀 상태 $ \ket{\psi (t)} $가 검색 됩니다.
퀀텀 dynamics에 대 한 설명을 계속 하기 전에 먼저 이전 dynamics와 다른 퀀텀 메커니즘을 사용 하는 방법에 대 한 정보를 제공 하기 때문에 기존 dynamics에 대 한 단계를 수행 하 고 생각 하는 것이 유용 합니다.

기존 dynamics에서 뉴턴의 두 번째 동작 법칙에서 파티클의 위치가 $F (x, t) = ma = m\frac {\ dd ^ 2} {\dd t ^ 2} {x} (t) $에 따라 진화 하는 것을 알고 있습니다. 여기서 $F (x, t) $는 force이 고, $m $a $은 (는)입니다.
그런 다음 초기 위치 $x (0) $, 진화 시간 $t $ 및 파티클에 적용 되는 요인에 대 한 설명을 지정 하 고 나 서 $x (t) $에 대 한 뉴턴의 방정식에 지정 된 차등 수식을 해결 하 여 $x (t) $를 찾을 수 있습니다.
이러한 방식으로 강제를 지정 하는 것은 어려운 문제입니다.
따라서 시스템의 잠재적 에너지 면에서이를 의미 하는 경우가 많습니다 .이는 $-\ partial_x V (x, t) = m \frac{\dd ^ 2} {\dd t ^ 2} {x} (t) $를 제공 합니다.
따라서 파티클의 경우 시스템의 dynamics는 잠재적 에너지 함수, 파티클 질량 및 진화 시간에 의해서만 지정 됩니다.

보다 광범위 한 언어는 $F = ma $를 초과 하는 기존 dynamics에 대해 도입 되는 경우가 많습니다.
퀀텀 메커니즘에서 특히 유용한 공식화 하나는 Hamiltonian 메커니즘입니다.
Hamiltonian 메커니즘에서 시스템의 총 에너지와 (일반화 된) 위치 및 momenta는 임의의 고전 개체의 동작을 설명 하는 데 필요한 모든 정보를 제공 합니다.
특히 $f (x, p, t) $는 시스템의 일반화 된 위치 $x $ 및 momenta $p $의 일부 함수 이며 $H (x, p, t) $를 Hamiltonian 함수로 사용 하면 됩니다.
예를 들어 $f (x, p, t) = x (t) $ 및 $H (x, p, t) = p ^ 2 (t)/2m-V (x, t) $를 사용 하는 경우 Newtonian dynamics의 위 사례를 복구 합니다.
일반 성을에서 \begin{align} \frac{d}{dt} f &= \ partial_t f-(\ partial_x H \ partial_p f + \ partial_p H \ partial_x f) \\ \\ & \defeq \ partial_t f + \\ {f, h}를 사용할 수 있습니다 \\ .
\end{align} 여기 \\ 에서 $ {f, H \\ } $를 [포아송 괄호로](https://en.wikipedia.org/wiki/Poisson_bracket) 지칭 하 고 dynamics를 정의 하는 중앙 역할로 인해 클래식 dynamics에서 ubiquitously 표시 됩니다.

퀀텀 dynamics는 정확히 동일한 언어를 사용 하 여 설명할 수 있습니다.
Hamiltonian 또는 총 에너지는 closed 퀀텀 시스템의 dynamics를 완전히 지정 합니다.
그러나 두 이론 간에는 상당한 차이가 있습니다.
기존 메커니즘에서 $x $ 및 $p $는 숫자만 이지만 퀀텀 메커니즘에서는 그렇지 않습니다.
실제로 commute: $xp \ne px $를 포함 하지 않습니다.

이러한 비 통근 이나 출장 개체를 설명 하는 오른쪽 수학적 개념은 연산자입니다. 예를 들어 $x $ 및 $p $는 행렬의 개념과 일치 하는 불연속 값 집합만 사용할 수 있습니다.
따라서 간단 하 게 하기 위해 퀀텀 시스템이 유한 하 여 [벡터 및 매트릭스](xref:microsoft.quantum.concepts.vectors)를 사용 하 여 설명할 수 있다고 가정 합니다.
이러한 행렬을 Hermitian 해야 합니다 (행렬의 켤레 복소수는 원래 매트릭스와 동일 함).
이렇게 하면 행렬의 고유 값가 실제 값이 됩니다. 허수 값을 백오프 하지 않는 위치와 같은 수량을 측정 하기 위해 적용 하는 조건입니다.

퀀텀 메커니즘에서 position 및 모멘텀의 analogues를 연산자로 교체 해야 하는 것 처럼 Hamiltonian 함수는 비슷한 연산자로 대체 되어야 합니다.
예를 들어 사용 가능한 공간의 파티클에는 $H (x, p) = p ^ 2/2m $가 있지만 퀀텀 메커니즘에서 Hamiltonian operator $ \hat{H} $은 $ \hat{H} = \hat{p} ^ 2/2m $입니다. 여기서 $ \hat{p} $은 모멘텀 연산자입니다.
이 관점에서, 클래식에서 퀀텀 dynamics로 전환 하는 것은 일반 dynamics에서 사용 되는 변수를 연산자로 바꾸는 것만 포함 합니다.
일반적인 고전 Hamiltonian를 퀀텀 언어로 변환 하 여 Hamiltonian 연산자를 생성 한 후에는 임의의 퀀텀 기계적 수량 (예: 퀀텀 기계적 연산자) $ \hat{f} (t) $ via \begin{align} \frac{d}{dt} \hat{f} = \ partial_t \hat{f} + [\hat{f}, \hat{H}], \end{align} where $ [f, H] = fH-Hf $를 commutator 라고 합니다.
이 식은 위에 지정 된 기존 식과 정확히 비슷하며, 포아송 괄호 $ \\ {f, H \\ } $가 $f $ 및 $H $ 사이의 commutator 대체 된다는 차이가 있습니다.
기존 Hamiltonian을 사용 하 고이를 사용 하 여 퀀텀 Hamiltonian를 찾는이 프로세스는 퀀텀 용어에서 정식 양자화으로 알려져 있습니다.

가장 관심이 있는 연산자 $f는 무엇 인가요?  이에 대 한 대답은 해결 하려는 문제에 따라 달라 집니다.
가장 유용 하 게 사용할 수 있는 것은 이전 개념 문서에서 설명 하는 것 처럼 dynamics에 대해 알아볼 모든 항목을 추출 하는 데 사용할 수 있는 퀀텀 상태 연산자입니다.
이 작업을 수행 하 고 결과를 순수 상태를 포함 하는 경우로 단순화 한 후에는 퀀텀 상태에 대 한 Schrödinger 수식이 \begin{align} a\ partial_t \ket{\psi (t)} = \hat{H} (t) \ket{\psi (t)}로 검색 됩니다.
\end{align}

이 수식은 위에 제공 된 것 보다 직관적이 지 않지만 퀀텀 또는 클래식 컴퓨터에서 퀀텀 dynamics를 시뮬레이션 하는 방법을 이해 하는 가장 간단한 식을 생성 합니다.
이는 Hamiltonian이 상수 $t $) \begin{align} \ket{\psi (t)} = e ^ {-iHt} \ket{\psi (0)} 인 경우에는 차등 수식에 대 한 솔루션을 다음 형식으로 표현할 수 있기 때문입니다.
\end{align} 여기 $e ^ {-iHt} $는 단일 행렬입니다.
이는 퀀텀 컴퓨터가 모든 단일 매트릭스를 긴밀 하 게 대략적으로 사용할 수 있기 때문에이를 수행 하도록 디자인할 수 있는 퀀텀 회로가 있음을 의미 합니다.
퀀텀 시간 진화 연산자를 구현 하는 퀀텀 회로를 찾는 작업은 $e ^ {-iHt} $은 퀀텀 시뮬레이션 또는 특히 동적 퀀텀 시뮬레이션 이라고 합니다.
