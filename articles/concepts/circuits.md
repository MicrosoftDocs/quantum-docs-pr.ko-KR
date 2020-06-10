---
title: 양자 회로
description: 퀀텀 회로 다이어그램을 사용 하 여 단순 하 고 복잡 한 퀀텀 작업을 시각적으로 표시 하는 방법을 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
ms.openlocfilehash: 745f0570bf62c5d98c2896cdc893ec385abd7115
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630400"
---
# <a name="quantum-circuits"></a>퀀텀 회로
그 순간에는 단일 변환 $ \text { cnot} _ {01 } (H \otimes 1) $을 고려 하십시오.
이 게이트 시퀀스는 최대 entangled의 2 상 비트 상태를 만들기 때문에 퀀텀 컴퓨팅에 대 한 근본적인 중요 한 사항입니다.

$ $ \mathrm{CNOT}_{01 } (H \otimes 1) \ket{00 } = \frac{1 } {\sqrt{2 } } \left (\ket{00 } + \ket{11 } \right), $ $

이러한 복잡성을 포함 하는 작업은 퀀텀 알고리즘과 퀀텀 오류 수정에서 사용할 수 있으므로 *퀀텀 회로 다이어그램*이라고 하는 시각화에 대 한 간단한 메서드가 있는 것이 좋습니다.
이 최대 entangled 퀀텀 상태를 준비 하기 위한 회로 다이어그램은 다음과 같습니다.

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![최대 entangled 2 상 비트 상태에 대 한 회로 다이어그램](~/media/1.svg)

## <a name="quantum-circuit-diagram-conventions"></a>퀀텀 회로 다이어그램 규칙
퀀텀 작업의 시각적 언어는 퀀텀 회로를 표현 하는 규칙을 이해 하 고 나면 동등한 행렬을 작성 하는 것 보다 훨씬 더 쉽게 좋게 수 있습니다.
아래에서 이러한 규칙을 검토 합니다.

회로 다이어그램에서 각 실선은 보다 일반적으로는 이상 비트 레지스터를 나타냅니다.
규칙에 따라 맨 위 줄은 이란 비트 레지스터 $0이 $ 고 나머지는 순차적으로 레이블이 지정 됩니다. 위의 예제 회로는 두 개의 비트에서 작동 하는 것으로 표시 됩니다.
하나 이상의 이상 비트 레지스터에서 동작 하는 게이트가 상자로 표시 됩니다.
예: 기호

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![단일 기능 비트 레지스터에서 작동 하는 Hadamard 작업에 대 한 기호](~/media/2.svg)

는 단일의 비트 레지스터에서 작동 하는 [Hadamard](xref:microsoft.quantum.intrinsic.h) 작업입니다.

퀀텀 게이트는 처음에는 관문을 중심으로 가장 왼쪽의 게이트가 있는 시간순으로 정렬 됩니다.
즉, 퀀텀을 퀀텀 상태를 유지 하는 경우 와이어는 다이어그램의 각 게이트를 통해 퀀텀 상태를 왼쪽에서 오른쪽으로 가져옵니다.
예를 들면 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![왼쪽에서 오른쪽으로 적용 되는 퀀텀 게이트 다이어그램](~/media/3.svg)

는 단일 행렬 $CBA입니다 $ .
행렬 곱셈은 반대 규칙을 따르는 합니다. 가장 오른쪽의 행렬이 먼저 적용 됩니다. 그러나 퀀텀 회로 다이어그램에서 가장 왼쪽의 게이트가 먼저 적용 됩니다.
이러한 차이는 때때로 혼란 스 러 울 수 있으므로 선형 대 수 표기법과 퀀텀 회로 다이어그램 간의 상당한 차이를 확인 하는 것이 중요 합니다.

## <a name="inputs-and-outputs-of-quantum-circuits"></a>퀀텀 회로의 입/출력
지정 된 앞의 모든 예제에는 퀀텀 게이트의 와이어 수와 동일한 수의 와이어 (는)를 퀀텀 게이트에 정확 하 게 입력 했습니다.
처음에는 퀀텀 회로가 일반적으로 입력 하는 것 보다 더 많거나 적을 수 있다는 것이 합리적입니다.
그러나 모든 퀀텀 작업을 저장 하는 것은 단일 작업 이므로 해독 가능 하기 때문에 불가능 합니다.
입력과 동일한 수의 출력을 포함 하지 않은 경우에는 해독 하지 않고 일치 하지 않는 단일 사용자가 아닙니다.
이러한 이유로 회로 다이어그램에 그려진 상자는 종료 하는 것과 정확히 동일한 수의 와이어로 입력 해야 합니다.

다중 기능 비트 회로 다이어그램은 유사한 규칙에 따라 단일 비트를 수행 합니다.
명확 하 게 예를 들어 $ $ (H S X) $로 $B 하는 두 개의 단일 비트 작업을 정의 하 \otimes 고 회로를 표현할 수 있습니다.

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![두 개의 단일 비트 작업의 회로 다이어그램](~/media/4.svg)

회로를 사용 하는 $ 컨텍스트에 따라 2 1-가 비트 레지스터가 아닌 단일 2-가 비트 레지스터에 대해 작업을 수행 하는 것으로 $B를 볼 수도 있습니다. 이러한 추상 회로 다이어그램의 가장 유용한 속성은 기본 게이트로 컴파일하지 않고도 복잡 한 퀀텀 알고리즘을 높은 수준으로 설명할 수 있다는 것입니다.
즉, 알고리즘 내의 각 서브루틴이 작동 하는 방식에 대 한 모든 세부 정보를 이해 하지 않고도 대량 퀀텀 알고리즘에 대 한 데이터 흐름에 대 한 intuition를 가져올 수 있습니다.

## <a name="controlled-gates"></a>제어 된 게이트
Multi-factor bit 퀀텀 회로 다이어그램에 기본 제공 되는 다른 구문은 제어입니다.
퀀텀 단일 제어 출입문의 동작입니다. $ \Lambda (G) $로 표시 된 단일의 \ket{1 값은 $ $ \Lambda (G) $G (\lambda \ket{0 } + \lambda } ) \ket { \lambda } = \lambda \ket{0 } \ket { a\psi } + \lambda \ket{1 } \ket { n\psi } $의 다음 예제를 살펴보면 이해할 수 있습니다.
즉, 제어 되는 게이트는 컨트롤의 값이 $1를 사용 하는 경우에 $ 만 $ \psi를 포함 하는 레지스터에 $G 적용 됩니다 $ $ .
일반적으로 회로 다이어그램에서 이와 같이 제어 되는 작업을 설명 합니다.

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![단일 제어 게이트 회로 다이어그램](~/media/5.svg)

여기서 검은색 원은 게이트가 제어 되는 퀀텀 비트를 나타내며, 세로는 컨트롤의 값이 $1를 사용 하는 경우 적용 되는 단일를 나타냅니다 $ .
$G = X $ 및 $G = Z와 같은 특수 한 경우에는 $ 다음 표기법을 도입 하 여 게이트의 제어 된 버전을 설명 합니다 (제어 된 X 게이트는 [$CNOT $ 게이트](xref:microsoft.quantum.intrinsic.cnot)).

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![제어 되는 게이트의 특수 사례에 대 한 회로 다이어그램](~/media/6.svg)

Q #은 작업의 제어 된 버전을 자동으로 생성 하는 메서드를 제공 합니다. 그러면 프로그래머가 이러한 작업을 직접 코딩할 필요가 없습니다. 이에 대 한 예제는 다음과 같습니다.

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a>측정 연산자
회로 다이어그램에서 시각화 하는 나머지 작업은 측정입니다.
측정은 더 많은 비트 레지스터를 사용 하 여 측정 하 고 결과를 기존 정보로 출력 합니다.
측정 연산은 미터 기호로 표시 되 고 항상 (실선으로 표시 됨)에 대 한 입력으로 사용 되며, 이중 줄로 표시 되는 고전적인 정보를 출력 합니다.
특히 이러한 subcircuit는 다음과 같습니다.

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![측정 작업을 나타내는 기호](~/media/7.svg)

Q #에서는이 목적을 위해 [측정값 연산자](xref:microsoft.quantum.intrinsic.measure) 를 구현 합니다.
자세한 내용은 [측정에](xref:microsoft.quantum.libraries.standard.prelude#measurements) 대 한 섹션을 참조 하세요.

마찬가지로 subcircuit

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![제어 된 작업을 나타내는 회로 다이어그램](~/media/8.svg)

일반적으로 제어 되는 게이트를 제공 합니다 $ . 여기서 $G는 클래식 컨트롤 비트의 조건 화 된 값이 $1에 적용 됩니다 $ .

## <a name="teleportation-circuit-diagram"></a>Teleportation 회로 다이어그램
퀀텀 teleportation는 이러한 구성 요소를 보여 주는 최상의 퀀텀 알고리즘이 될 것입니다.
해당 하는 [퀀텀 Kata](xref:microsoft.quantum.overview.katas) 퀀텀 teleportation은 되거나 얽 히 및 측정을 사용 하 여 퀀텀 컴퓨터 내에서 (또는 퀀텀 네트워크의 먼 퀀텀 컴퓨터 간) 데이터를 이동 하는 방법에 대해 배울 수 있습니다.
흥미롭게도, 실제 값을 알고 있는 것이 아니라, 지정 된의 값을 한 가지 이상에서 다른 값으로 이동 하는 것은 사실입니다.
이는 프로토콜이 퀀텀 메커니즘의 법에 따라 작동 하는 데 필요 합니다.
퀀텀 teleportation 회로는 아래에 제공 됩니다. 또한 퀀텀 회로를 읽는 방법을 보여 주기 위해 주석이 추가 된 회로 버전을 제공 합니다.

<!--- ![](.\media\tp2.svg){ width=50% } --->
![퀀텀 teleportation 회로](~/media/tp2.svg)
