---
title: 퀀텀 컴퓨팅의 고 비트
description: 퀀텀 컴퓨팅의 기본 정보 단위인,이에 대해 알아봅니다.
author: QuantumWriter
uid: microsoft.quantum.concepts.qubit
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: f5e5c2a66899c552ad39e63703c34718818b1452
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426967"
---
# <a name="the-qubit"></a>고 비트

Bits가 기존 컴퓨팅 정보에 대 한 기본 개체인 것 [*처럼, (*](https://en.wikipedia.org/wiki/Qubit) 양자 비트)는 퀀텀 컴퓨팅에서 정보의 기본 개체입니다.  이러한 대응을 이해 하려면 가장 간단한 예 인 단일 기능을 살펴보겠습니다.

## <a name="representing-a-qubit"></a>고 비트를 나타내는

비트 또는 이진 숫자에는 $0 $ 또는 $1 $ 값이 있을 수 있지만,이 중 하나는 값을 가질 수 있으며,이 값은 $0 $ 및 $1 $의 퀀텀 superposition 수 있습니다.

단일 비트의 상태는 unit의 2 차원 열 벡터로 설명 됩니다. 즉, 항목의 제곱 크기는 $1 $로 합산 되어야 합니다. 퀀텀 상태 벡터 라고 하는이 벡터는 단일 비트가 이진 변수의 상태를 설명 하는 데 필요한 모든 정보를 보유 하는 것 처럼 단일 수준으로 된 퀀텀 시스템을 설명 하는 데 필요한 모든 정보를 저장 합니다.

일반적인 $1 $를 사용 하는 실수 또는 복소수의 모든 2 차원 열 벡터는 해당 하는 값이 있는 퀀텀 상태를 나타냅니다. 따라서 $ \\ \\ \alpha $ 및 $ \alpha $가 $ | \alpha | ^ 2 + | \alpha | ^ 2 = $1를 만족 하는 복소수 이면 $ \begin{bmatrix} \alpha \alpha \end{bmatrix} $는 stbit 상태를 나타냅니다. 이를 나타내는 유효한 퀀텀 상태 벡터의 몇 가지 예는 다음과 같습니다.

$ $ \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix}, \begin{bmatrix} \frac {1} {\sqrt {2} } \\ \\ \frac {1} {\sqrt {2} } \end{bmatrix}, \begin{bmatrix} \frac {1} {\sqrt {2} } \\ \\ \frac {-1} {\sqrt {2} } \end{bmatrix}, \frac and} \begin{bmatrix} \frac {1} {\sqrt {2} } \\ \\ \frac{i}{\sqrt {2} } \end{bmatrix}. $ $

퀀텀 상태 벡터 $ \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix} $ 및 $ \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix} $는 특별 한 역할을 수행 합니다. 이러한 두 벡터는 원하는 비트의 상태를 설명 하는 벡터 공간에 대 한 기본을 형성 합니다. 즉, 모든 퀀텀 상태 벡터는 이러한 기준 벡터의 합계로 작성 될 수 있습니다. 특히 vector $ \begin{bmatrix} x \\ \\ y \end{bmatrix} $는 $x \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix} + y \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix} $로 작성할 수 있습니다. 이러한 벡터의 회전은 원하는 비트에 대해 완벽 하 게 유효한 기본으로 사용 되는 반면,이를 *계산 기준*으로 호출 하 여이에 대 한 권한을 부여 하도록 선택 합니다.

이러한 두 퀀텀 상태는 고전 비트의 두 가지 상태 즉, $0 $ 및 $1 $에 해당 합니다. 표준 규칙은 다음을 선택 하는 것입니다.

$ $0 \ http-equiv \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix}, \qquad 1 \equiv \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix}, $ $

이와 반대로 선택 하는 것도 동일 하 게 사용할 수 있습니다. 따라서 가능한 단일 값 비트 퀀텀 상태 벡터의 수를 초과 하는 경우 두 가지만 클래식 비트의 상태에 해당 합니다. 다른 모든 퀀텀 상태는 그렇지 않습니다.

## <a name="measuring-a-qubit"></a>고 비트 측정

이제는 원하는 비트를 나타내는 방법을 배웠으므로 [*측정*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)개념에 대해 설명 하 여 이러한 상태에 대 한 몇 가지 intuition을 얻을 수 있습니다. 측정값은 "찾는 중" 이라는 비공식적 개념에 해당 하며,이는 퀀텀 상태를 두 가지 클래식 상태 $ \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix} $ 또는 $ \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix} $ 중 하나로 즉시 축소 합니다. 퀀텀 상태 vector $ \begin{bmatrix} \alpha \\ \\ \alpha \end{bmatrix} $에서 지정 된를 측정 하는 경우 결과 $0 $은 확률 $ | \alpha | ^ 2 $로, 결과 $1 $는 확률 $ | \alpha | ^ 2 $로 구합니다. 결과 $0 $에서, \end{bmatrix}의 새 상태는 $ \begin{bmatrix} 1 \\ \\ 0 $입니다. 결과 $1 $에서 해당 상태는 $ \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix} $입니다. 이러한 확률은 정규화 조건 $ | \alpha | ^ 2 + | \alpha | ^ 2 = $1 때문에 최대 $1 $로 합산 됩니다.

또한 측정의 속성은 퀀텀 상태 벡터의 전체 부호가 관련이 없다는 것을 의미 합니다. 벡터 부정은 $ \alpha \rightarrow-\alpha $ 및 $ \alpha \rightarrow-\alpha $와 동일 합니다. $0 $ 및 $1 $의 확률은 조건의 제곱 크기에 따라 달라 지므로 이러한 기호를 삽입 해도 확률은 변경 되지 않습니다. 이러한 단계를 일반적으로 [ `` *전역 단계*' '](https://en.wikipedia.org/wiki/Phase_factor) 이라고 하며, 일반적으로 $ \pm $1이 아닌 $e ^ {i \phi} $ 형식으로 지정할 수 있습니다.

최종 중요 한 측정 속성은 모든 퀀텀 상태 벡터를 손상 시킬 필요는 없다는 것입니다. \\ \\ 클래식 상태 $0 $에 해당 하는 $ \begin{bmatrix} 1 0 \end{bmatrix} $ 상태에서로 시작 하는 경우이 상태를 측정 하면 항상 $0 $ 결과가 발생 하 고 퀀텀 상태가 변경 되지 않습니다. 이러한 점에서 기존 비트만 있는 경우 (즉, $ \begin{bmatrix}1 \\ \\ 0 \end{bmatrix} $ 또는 $ \begin{bmatrix}0 \\ \\ 1 \end{bmatrix} $ 인 경우) 측정은 시스템을 손상 시 키 지 않습니다. 즉, 기존 데이터를 복제 하 고 기존 컴퓨터에서 수행할 수 있는 것 처럼 퀀텀 컴퓨터에서 조작할 수 있습니다. 그러나 두 상태에 정보를 한 번에 저장 하는 기능은 퀀텀 데이터 무제한 증가할을 복사 [하는 기능](https://en.wikipedia.org/wiki/No-cloning_theorem)에 대 한 가능한 일반적으로 및 추가 robs 컴퓨터를 초과 하는 퀀텀 컴퓨팅을 제공 합니다.

## <a name="visualizing-qubits-and-transformations-using-the-bloch-sphere"></a>Bloch 구를 사용 하 여 고 비트 및 변형 시각화

[*Bloch 구에*](https://en.wikipedia.org/wiki/Bloch_sphere) 표시를 사용 하 여 $3 $ D에도 표시 될 수 있습니다.  Bloch 구는 단일 값 비트 퀀텀 상태 (2 차원 복합 벡터)를 3 차원 실제 값 벡터로 설명 하는 방법을 제공 합니다.  이는 단일 수준 비트 상태를 시각화 하 여 여러 번째 비트 상태를 이해 하는 데 중요 한 이유를 개발할 수 있도록 하는 것이 중요 합니다 (sadly Bloch 구 표현이 중단 됨).  Bloch 구는 다음과 같이 시각화할 수 있습니다.

<!--- ![](.\media\bloch.svg){ width=50% } --->
![Bloch 구](~/media/concepts_bloch.png)

이 다이어그램의 화살표는 퀀텀 상태 벡터가 가리키는 방향을 보여 주고 화살표의 각 변환은 카디 날 축 중 하나에 대 한 회전으로 간주할 수 있습니다.
계산 시퀀스로 퀀텀 계산을 고려 하는 것은 강력한 intuition이 intuition를 사용 하 여 알고리즘을 설계 하 고 설명 하는 것이 어렵습니다. Q #에서는 이러한 회전을 설명 하는 언어를 제공 하 여이 문제를 완화 합니다.

## <a name="single-qubit-operations"></a>단일 비트 작업

퀀텀 컴퓨터는 퀀텀 상태 벡터의 회전을 에뮬레이트할 수 있는 유니버설 퀀텀 게이트 집합을 적용 하 여 데이터를 처리 합니다.
이 보편성 개념은 입력 비트의 모든 변환이 유한 길이 회로를 사용 하 여 수행 될 수 있는 경우 게이트 집합이 유니버설로 간주 되는 기존 (즉, 일반) 컴퓨팅의 보편성 개념과 유사 합니다.
퀀텀 컴퓨팅에서 원하는 비트에 대해 수행할 수 있는 유효한 변환은 단일 변환 및 측정입니다.
*Adjoint 작업* 또는 복소수 복소수는 퀀텀 변환을 반전 해야 하므로 퀀텀 컴퓨팅에 중요 한 중요 한 부분입니다.
Q #은 게이트 시퀀스를 해당 adjoint로 자동으로 컴파일하는 메서드를 제공 하 여이를 반영 합니다. 그러면 프로그래머가 많은 경우에 코드를 직접 만들지 않아도 됩니다. 이에 대 한 예제는 다음과 같습니다.

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Adj { // Auto-generate the adjoint of the operation
    H(qubit);
}
```

이는 간단한 예제 이지만 ( <xref:microsoft.quantum.intrinsic.h> 작업은 자체 adjoint)이는 보다 복잡 한 추가 비트 작업에 유용 하다는 것을 알 수 있습니다.
자세한 내용은 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.

기존 컴퓨터에서 1 비트를 1 비트에 매핑하는 함수는 네 개만 있습니다. 이와 대조적으로 퀀텀 컴퓨터의 단일 비트에는 무한 한 수의 단일 변환만 있습니다. 따라서 [*게이트*](https://en.wikipedia.org/wiki/Quantum_logic_gate)라는 한정 된 기본 퀀텀 작업 집합은 퀀텀 컴퓨팅에서 허용 되는 무한 한 단일 변환 집합을 정확 하 게 복제할 수 없습니다. 즉, 기존 컴퓨터와는 달리 퀀텀 컴퓨터에서 한정 된 수의 게이트를 사용 하 여 가능한 모든 퀀텀 프로그램을 정확 하 게 구현할 수는 없습니다. 따라서 기존 컴퓨터와 동일한 의미로 퀀텀 컴퓨터를 사용할 수 없습니다. 결과적으로, 게이트 집합이 퀀텀 컴퓨팅에 대 한 *유니버설* 이라는 것을 알게 되 면 실제로는 기존 컴퓨팅을 사용 하는 것 보다 약간 약한 것을 의미 합니다.
보편성의 경우 퀀텀 컴퓨터는 유한 길이 게이트 시퀀스를 사용 하 여 유한 오류 내에서 모든 단일 행렬에만 *근사치* 를 기울여야 합니다.
즉, 단일 변환을이 집합에서 게이트의 곱으로 대략적으로 작성할 수 있는 경우 게이트 집합이 범용 게이트 집합입니다. 지정 된 모든 오류를 발생 시키려면 {1} {2} 게이트 집합에서 _, G_, \ldots, G_N $ $G 게이트가 존재 합니다.

$ $ G_N G_ {N-1} \cdots G_2 G_1 \aau. $ $

행렬 곱셈에 대 한 규칙은이 시퀀스에서 첫 번째 게이트 연산을 오른쪽에서 왼쪽으로 곱하는 것 이기 때문에 $G _N $는 실제로 퀀텀 상태 벡터에 적용 됩니다. 보다 공식적으로, 이러한 게이트 집합은 모든 오류 허용 오차 $ \ec>$0에 대해 _N G_1 \llt $U $ 및 $ $G 사이의 거리가 최대 $ \epsilon $로 설정 되도록 $G _1, \l도트, G_N $가 있습니다. 이상적으로 $ \epsilon $의이 거리에 도달 하는 데 필요한 $N $ 값은 로그를 $1/\ 엡실론 $로 조정 해야 합니다.

이러한 범용 게이트 집합은 실제로 어떤 모습 인가요?  단일 고 비트 게이트에 대 한 가장 간단한 이러한 범용 게이트 집합은 Hadamard gate $H $ 및 $T $-게이트 ($ \ pi/8 $ gate 라고도 함) 라는 두 개의 게이트로만 구성 됩니다.

$ $ H = \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ 1 &-1 \end{bmatrix}, \qquad T = \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \ pi/4} \end{bmatrix}.
$$

그러나 퀀텀 오류 수정과 관련 된 실질적인 이유 때문에 $H $ 및 $T $를 사용 하 여 생성할 수 있는 보다 큰 게이트 집합을 고려 하는 것이 더 편리할 수 있습니다.
퀀텀 게이트를 두 가지 범주 (Clifford 게이트 및 $T $-게이트)로 분류할 수 있습니다.
이 하위 작업은 여러 퀀텀 오류 수정 체계에서 Clifford 게이트를 구현 하기 쉬우므로, 오류 tolerantly을 구현 하기 위한 작업 및 뛰어난 비트의 리소스를 거의 필요로 하지 않는 반면, Clifford 없는 게이트는 내결함성이 필요한 경우 비용이 많이 듭니다. [Q #에서 기본적으로 포함](xref:microsoft.quantum.libraries.standard.prelude)되는 단일가 비트 Clifford 게이트의 표준 집합은 다음과 같습니다.

$ $ H = \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ 1 &-1 \end{bmatrix}, \qquad S = \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix} = T ^ 2, \qquad X = \begin{bmatrix} 0 &1 \\ \\ 1& 0 \end{bmatrix} = HT ^ 4H, $ $

$ $ Y = \begin{bmatrix} 0 &-i \\ \\ & 0 \End{bmatrix} = t ^ 2 ht ^ 4 ht ^ 6, \qquad Z = \begin{bmatrix}1&0 \\ \\ 0&-1 \end{bmatrix} = T ^ 4.
$$

여기서 $X $, $Y $ 및 $Z $ 연산은 특히 자주 사용 되며 작성자 Wolfgang Pauli 후에 [*pauli 연산자*](https://en.wikipedia.org/wiki/Pauli_matrices) 라고 합니다.
비 Clifford 게이트 ($T $ gate)와 함께 이러한 작업을 단일 비트의 모든 단일 변환에 대 한 근사치로 구성할 수 있습니다.

이러한 작업, 해당 Bloch 구 표현 및 Q # 구현에 대 한 자세한 내용은 [내장 작업 및 함수](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions)를 참조 하세요.

이러한 기본 형식에서 단일 변환을 작성 하는 방법의 예로, 위의 Bloch 구에 나오는 세 가지 변환은 게이트 시퀀스 $ \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix} \MAPSHZH \begin{bmatrix} 1 \\ \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ \\ 1 \end{bmatrix} $에 해당 합니다.

이전에는 스택의 논리 수준에 대 한 작업을 설명 하는 데 가장 많이 사용 되는 기본 게이트가 구성 되어 있지만 (논리 수준을 퀀텀 알고리즘의 수준으로 생각), 함수 설명 수준에 가까운 작업과 같이 알고리즘 수준에서 더 작은 기본 작업을 고려 하는 것이 편리한 경우가 많습니다. 다행히 Q #에는 더 높은 수준의 unitaries을 구현 하는 데 사용할 수 있는 메서드도 있습니다. 그러면 모든 것을 명시적으로 분해 하 여 Clifford 및 $T $-게이트를 사용 하지 않고도 높은 수준의 알고리즘이 구현 될 수 있습니다.

가장 간단한 이러한 기본 형식은 단일의 비트 회전입니다. 일반적으로 $R _x $, $R _y $ 및 $R _z $의 세 가지 단일 비트 회전이 고려 됩니다. 예를 들어, 회전 $R _x (\theta) $의 동작을 시각화 하려면 예를 들어, Bloch 구의 $x $ 축 방향을 따라 오른쪽 엄지 단추를 가리키고 $ \ 테타/2 $ 라디안의 각도를 통해 손으로 벡터를 회전 한다고 가정 합니다. $2 $의 이러한 혼동 요인은 Bloch 구에 표시 될 때 직교 벡터가 $180 ^ \circ $를 분리 하는 것이 아니라 실제로 $90 ^ \circ $도 함께 사용할 수 있다는 사실입니다. 해당 하는 단일 매트릭스는 다음과 같습니다.

\begin{align *} &R_z (\테타) = e ^ {-I\theta z/2} = \begin{bmatrix} e ^ {-i \ 테타/2} & 0 \\ \\ 0& e ^ {a\ 테타/2} \end{bmatrix} \\ \\ &R_x (\테타) = e ^ {-i\theta x/2} = HR_z (\테타) H = \begin{bmatrix} \cos (\ 테타/2) &-i\theta (\ 테타/2)-i\theta (\ 테타/2) \\ \\ & \cos (\ 테타/2) \end{bmatrix}, \\ \\ &R_y (\테타) = e ^ {-i\theta y/2} = SHR_z (\테타) HS ^ \\end{bmatrix}. = \begin{bmatrix} \cos (\ 테타/2) &-\sin (\ 테타/2) \sin (\ 테타/2) \\ \\ & \cos (\ 테타/2) \begin{align*}

세 개의 회전을 함께 결합 하 여 세 개의 차원에서 임의의 회전을 수행할 수 있는 것 처럼 Bloch 구의 표현에서 볼 수 있습니다. 구체적으로 말해서, 모든 단일 $U 행렬에 대해 $ \alpha, \alpha, \alpha, \alpha $가 있습니다 .이는 $U = e ^ {i\alpha} R_x (\alpha) R_z (\alpha) R_x (\bin) $입니다. 따라서 $ \theta $는 모든 값을 사용할 수 있기 때문에 $R _z (\theta) $ 및 $H $는 불연속 집합이 아닌 경우에도 유니버설 게이트 집합을 형성 합니다. 이러한 이유로 퀀텀 시뮬레이션의 응용 프로그램 때문에, 특히 퀀텀 알고리즘 디자인 수준에서 퀀텀 계산에는 이러한 연속 게이트가 중요 합니다. 내결함성이 있는 하드웨어 구현을 위해 궁극적으로 이러한 회전이 거의 근접 한 불연속 게이트 시퀀스로 컴파일됩니다.
