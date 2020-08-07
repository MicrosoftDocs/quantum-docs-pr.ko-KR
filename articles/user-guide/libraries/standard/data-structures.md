---
title: 표준 라이브러리의 데이터 구조 Q#
description: Microsoft standard 라이브러리의 데이터 구조, oracles 및 동적 생성기에 대해 알아봅니다 Q# .
author: QuantumWriter
uid: microsoft.quantum.libraries.data-structures
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 222fa7d0d33d4ac6c15e9ee9e6e97f380867a145
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868524"
---
# <a name="data-structures-and-modeling"></a>데이터 구조 및 모델링 #

## <a name="classical-data-structures"></a>기존 데이터 구조 ##

또한 라고은 퀀텀 개념을 나타내는 데 사용 되는 사용자 정의 형식과 함께 퀀텀 시스템의 제어에 사용 되는 기존 데이터로 작업 하기 위한 작업, 함수 및 유형도 제공 합니다.
예를 들어 <xref:microsoft.quantum.arrays.reversed> 함수는 배열을 입력으로 사용 하 고 동일한 배열을 역순으로 반환 합니다.
그러면 형식의 배열에서이를 사용 하 여 `Qubit[]` 양자의 퀀텀 표현 간에 변환 하는 동안 불필요 한 $ \operatorname{SWAP} $ 게이트를 적용할 필요가 없도록 할 수 있습니다.
마찬가지로, 이전 섹션에서 형식의 형식이 `(Int, Int -> T)` 임의 액세스 컬렉션을 표시 하는 데 유용할 수 있으므로 <xref:microsoft.quantum.arrays.lookupfunction> 함수는 배열 형식에서 이러한 형식을 생성 하는 편리한 방법을 제공 합니다.

### <a name="pairs"></a>문자짝 ###

라고은 분해에의 한 튜플 액세스를 보완 하는 함수에 대 한 함수 스타일 표기법을 지원 합니다.

```qsharp
let pair = (PauliZ, register); // type (Pauli, Qubit[])
ApplyToEach(H, Snd(pair)); // No need to deconstruct to access the register.
```

### <a name="arrays"></a>배열 ###

라고에서는 배열을 조작 하기 위한 여러 함수를 제공 합니다.
이러한 함수는 형식 매개 변수화 되므로 모든 형식의 배열과 함께 사용할 수 있습니다 Q# .
예를 들어, <xref:microsoft.quantum.arrays.reversed> 함수는 요소가 입력에서 역순으로 포함 된 새 배열을 반환 합니다.
이를 사용 하 여 작업을 호출할 때 퀀텀 레지스터가 표시 되는 방식을 변경할 수 있습니다.

```qsharp
let leRegister = LittleEndian(register);
// QFT expects a BigEndian, so we can reverse before calling.
QFT(BigEndian(Reversed(leRegister!)));
// This is how the LittleEndianAsBigEndian function is implemented:
QFT(LittleEndianAsBigEndian(leRegister));
```

마찬가지로 함수를 <xref:microsoft.quantum.arrays.subarray> 사용 하 여 배열 요소의 순서를 변경 하거나 하위 집합을 가져올 수 있습니다.

```qsharp
// Applies H to qubits 2 and 5.
ApplyToEach(H, Subarray([2, 5], register));
```

흐름 제어와 함께 사용 하는 경우와 같은 배열 조작 함수는 <xref:microsoft.quantum.arrays.zip> 퀀텀 프로그램을 표현할 수 있는 강력한 방법을 제공 합니다.

```qsharp
// Applies X₃ Y₁ Z₇ to a register of any size.
ApplyToEach(
    ApplyPauli(_, register),
    Map(
        EmbedPauli(_, _, Length(register)),
        Zip([PauliX, PauliY, PauliZ], [3, 1, 7])
    )
);
```

## <a name="oracles"></a>Oracles ##

[단계 예측](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm) 및 [진폭 증폭](https://en.wikipedia.org/wiki/Amplitude_amplification) 홍보 자료에서 oracle의 개념은 자주 나타납니다.
여기서 oracle 이라는 용어는 다양 한 비트 집합에 적용 되는 블랙 박스 퀀텀 서브루틴을 나타내며 단계로 서 답변을 반환 합니다.
이 서브루틴은 다른 몇 가지 매개 변수와 함께 oracle을 허용 하는 퀀텀 알고리즘에 대 한 입력으로, 일련의 퀀텀 작업을 적용 하 고이 퀀텀 서브루틴에 대 한 호출을 기본 게이트 처럼 처리 하는 것으로 간주할 수 있습니다.
분명히 큰 알고리즘을 실제로 구현 하기 위해 oracle을 기본 게이트로 구체적으로 분해 해야 하지만 oracle을 호출 하는 알고리즘을 이해 하기 위해 이러한 분해는 필요 하지 않습니다.
에서 Q# 이 추상화는 작업을 첫 번째 클래스 값으로 사용 하 여 표현 됩니다. 이러한 작업은 블랙 박스 방식으로 퀀텀 알고리즘의 구현에 전달 될 수 있습니다.
또한 사용자 정의 형식은 형식이 안전한 방식으로 다양 한 oracle 표현의 레이블을 지정 하는 데 사용 되므로 실수로 다른 종류의 블랙 박스 작업을 conflate 어렵습니다.

이러한 oracles는 [Grover의 검색](https://en.wikipedia.org/wiki/Grover%27s_algorithm) 및 퀀텀 시뮬레이션 알고리즘과 같은 유명한 예를 포함 하 여 다양 한 컨텍스트에서 표시 됩니다.
여기서는 두 가지 응용 프로그램 (진폭 증폭 및 단계 예측)에 필요한 oracles에 중점을 둡니다.
단계 예측을 진행 하기 전에 먼저 진폭 증폭 oracles에 대해 설명 합니다.

### <a name="amplitude-amplification-oracles"></a>진폭 증폭 Oracles ###

진폭 증폭 알고리즘은 상태의 반사 시퀀스를 적용 하 여 초기 상태와 최종 상태 간의 회전을 수행 합니다.
알고리즘이 작동 하려면 이러한 두 상태를 모두 지정 해야 합니다.
이러한 사양은 두 oracles에 의해 제공 됩니다.
이러한 oracles는 입력을 두 개의 공백, "대상" 하위 공간 및 "초기" 하위 공간으로 분리 하 여 작동 합니다.
Oracles는 이러한 공간에 $ \pm $1 단계를 적용 하 여 Pauli 연산자가 두 공간을 식별 하는 방식과 유사 하 게 이러한 하위 공간을 식별 합니다.
주요 차이점은이 응용 프로그램에서 이러한 공간을 절반으로 사용할 필요가 없다는 것입니다.
또한 이러한 두 개의 하위 공간은 일반적으로 함께 사용할 수 없습니다. 두 공간의 멤버인 벡터가 있습니다.
이 값이 true가 아니면 진폭 증폭은 아무런 영향도 주지 않으므로 초기 하위 공간에서 0이 아닌 대상 하위 공간에 겹치지 않도록 해야 합니다.

\_다음 작업을 수행 하도록 정의 된 진폭 증폭에 필요한 첫 번째 oracle이 $0을 $P 합니다.  모든 상태 $ \ket{x} $의 "초기" 하위 공간 $P \_ 0 \ket{x} =-\ket{x} $ 이며이 하위 공간에 없는 모든 상태 $ \ket{y} $에 대해 \_ 0 \ket{y} = \ket{y} $ $P 있습니다.
대상 하위 공간 $P _1 $을 표시 하는 oracle은 정확히 동일한 형식을 사용 합니다.
대상 하위 공간의 모든 상태 $ \ket{x} $에 대해 (즉, 출력 하는 알고리즘에 대 한 모든 상태) _1 \ k {x} =-\ket{x} $를 $P 합니다.
마찬가지로 대상 하위 공간에 없는 모든 상태 $ \ket{y} $에 대해 _1 \ k {y} = \ket{y} $를 $P 합니다.
그런 다음이 두 반사를 결합 하 여 진폭 시행의 단일 단계를 구성 하는 연산자를 형성 합니다. $Q = P_0 P_1 $. 여기서 전체 빼기 기호는 제어 되는 응용 프로그램에서 고려 하는 경우에만 중요 합니다.
그런 다음 초기 하위 공간에 있는 $ \ket{\psi} $ 초기 상태를 수행 하 고 $ \ket{\psi} \mapsq ^ m \ket{\psi} $를 수행 하 여 진폭 증폭을 진행 합니다.
이러한 반복을 수행 하는 경우에는 표시 된 공간을 사용 하 여 $ \sin ^ 2 (\sin) $ 겹치는 초기 상태로 시작 하는 경우 $2m 다음 $m에이 겹치는 항목은 $ \sin ^ 2 ([+ 1] \sin) $가 됩니다.
따라서 일반적 $m으로 $ [2m + 1] \theta = \ pi/2 $;를 사용 하 여 $ [ 그러나 이러한 고정 선택은 고정 소수점 진폭 증폭과 같은 일부 형태의 진폭 증폭에는 중요 하지 않습니다.
이 프로세스를 통해 표시 함수에 대 한 쿼리 수를 quadratically를 사용 하 여 표시 된 하위 공간에서 상태를 준비할 수 있습니다.
이러한 이유로, 진폭 증폭은 많은 퀀텀 컴퓨팅 응용 프로그램에 대 한 중요 한 빌딩 블록입니다.

알고리즘을 사용 하는 방법을 이해 하려면 oracles 생성을 제공 하는 예제를 제공 하는 것이 유용 합니다.  이 설정에서 데이터베이스 검색에 대 한 Grover 알고리즘을 수행 하는 것이 좋습니다.
Grover의 목표 검색에서 목표는 상태 $ \ket{+} ^ {\otimes n} = H ^ {\otimes n} \ket {0} $를 표시 된 많은 상태 중 하나로 변환 하는 것입니다.
보다 간소화 하기 위해 표시 된 상태만 $ \ket $ 인 경우만 살펴보겠습니다 {0} .
그런 다음 두 개의 oracles를 디자인 했습니다. 첫 번째 상태 $ \ket{+} ^ {\otimes n} $만 빼기 기호로 표시 하 고 다른 하나는 표시 된 상태 $ \ket {0} $를 빼기 기호로 표시 합니다.
다음 처리 작업을 사용 하 여 canon의 제어 흐름 작업을 사용 하 여 두 번째 게이트를 구현할 수 있습니다.

```qsharp
operation ReflectAboutAllZeros(register : Qubit[]) : Unit 
is Adj + Ctl {

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);

    // Apply an $n-1$ controlled $Z$-gate to the $n^{\text{th}}$ qubit.
    // This gate will lead to a sign flip if and only if every qubit is
    // $1$, which happens only if each of the qubits were $0$ before step 1.
    Controlled Z(Most(register), Tail(register));

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);
}
```

이 oracle은 작업의 특별 한 경우입니다 <xref:microsoft.quantum.canon.rall1> .이 경우 리플렉션 사례 $ \a= \phi $ 대신 임의의 단계로 회전할 수 있습니다.
이 경우 `RAll1` 는 prelude 작업과 유사 하며,이 <xref:microsoft.quantum.intrinsic.r1> 는 단일가 나 비트 상태 $ \ket $ 대신 $ \ket{11\cdots1} $를 회전 {1} 합니다.

초기 하위 공간을 표시 하는 oracle을 유사 하 게 생성할 수 있습니다.
의사 코드:

1. 모든 고 비트에 $H $ 게이트를 적용 합니다.
2. 모든 고 비트에 $X $ 게이트를 적용 합니다.
3. $N ^ {\text{th}} $ stbit에 $n-$1 제어 $Z $ gate를 적용 합니다.
4. 모든 고 비트에 $X $ 게이트를 적용 합니다.
5. 모든 고 비트에 $H $ 게이트를 적용 합니다.

이번에는 <xref:microsoft.quantum.canon.applywith> 위에서 설명한 작업과 함께를 사용 하는 방법도 보여 줍니다 <xref:microsoft.quantum.canon.rall1> .

```qsharp
operation ReflectAboutInitial(register : Qubit[]) : Unit
is Adj + Ctl {
    ApplyWithCA(ApplyToEach(H, _), ApplyWith(ApplyToEach(X, _), RAll1(_, PI()), _), register);
}
```

그런 다음 이러한 두 oracles를 결합 하 여 두 상태 사이를 회전 하 고 $ \ket{+} ^ {\otimes n} $를 $ \ket $로 변형 하 여 $ {0} \sqrt{2 ^ n}에 비례 하는 Hadamard 게이트의 여러 계층을 사용할 수 있습니다. (ie $m \otimes \sqrt{2 ^ n} $) 및 {0} 결과 $0 $가 관찰 될 때까지 초기 상태를 준비 하 고 측정 하 여 $ \ket $ 상태를 명확 하 게 준비 하는 데 필요한 약 $2 ^ n $ 계층에 대 한 것입니다.

### <a name="phase-estimation-oracles"></a>단계 추정 Oracles ###

단계 예측의 경우 oracles는 다소 자연스럽 게 됩니다.
단계 추정의 목표는 단일 행렬의 고유 값에서 샘플링할 수 있는 서브루틴을 디자인 하는 것입니다.
이 메서드는 화학 및 자재 과학의 많은 물리적 문제를 발생 시키기 때문에 퀀텀 시뮬레이션의 필수적인 기능입니다. 이러한 고유 값은 주력할의 단계 다이어그램에 대 한 중요 한 정보를 제공 하는 퀀텀 시스템의 그라운드 상태를 제공 합니다.
단계 추정의 모든 버전에는 입력이 필요 합니다.
이는 두 가지 유형의 oracles 중 하나로 설명 되는 일반적으로입니다.

> [!TIP]
> 아래에 설명 된 두 oracle 형식은 모두 샘플에서 설명 합니다.
> 연속 쿼리 oracles 대해 자세히 알아보려면 [ **PhaseEstimation** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation)을 참조 하세요.
> 불연속 쿼리 oracles에 대해 자세히 알아보려면 [ **IsingPhaseEstimation** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/phase-estimation)을 참조 하세요.

Oracle의 첫 번째 유형은 개별 쿼리를 호출 하 고 사용자 정의 유형을 사용 하 여 표시 하는 oracle은 <xref:microsoft.quantum.oracles.discreteoracle> 단일 행렬을 포함 합니다.
$U $가 예측 하려는 고유 값의 단일 인 경우 $U $에 대 한 oracle은 단순히 $U $를 구현 하는 서브루틴에 대 한 독립 실행형입니다.
예를 들어, $ $U를 사용 하 여 진폭에 대해 앞에서 정의한 oracle $Q $를 사용할 수 있습니다.
이 행렬의 고유 값를 사용 하 여 초기 및 대상 상태 $ \sin ^ 2 (\sin) $ 사이에서 겹치는 항목을 추정 하는 데 사용할 수 있습니다. 그 외에도 quadratically를 사용 하는 경우 보다 작은 샘플을 사용 해야 합니다.
이는 Grover oracle $Q $를 사용 하 여 진폭 추정의 모니커를 입력으로 적용 하는 단계 예측의 적용을 획득 합니다.
퀀텀 metrology에서 널리 사용 되는 또 다른 일반적인 응용 프로그램에는 작은 회전 각도를 계산 하는 작업이 포함 됩니다.
즉, \theta ($R _z) $ 형식의 알 수 없는 회전 게이트를 위해 $ \theta $를 추정 하고자 합니다.
이러한 경우, 게이트에서 $ \theta $의이 고정 된 값을 학습 하기 위해 상호 작용 하는 서브루틴이 $ $ \begin{align} U & = R_z (\theta) \\ \\ & = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {a\ 테타/2} \end{bmatrix}.
\end{align} $ $

단계 예측에 사용 되는 oracle의 두 번째 유형은 형식으로 표현 되는 연속 쿼리 oracle입니다 <xref:microsoft.quantum.oracles.continuousoracle> .
단계 예측을 위한 연속 쿼리 oracle은 $U (t) $를 사용 합니다. 여기서 $t $은 알려진 일반적으로입니다.
$를 고정 된 단일 형식으로 $U 수 있는 경우 연속 쿼리 oracle은 $U (t) = U ^ t $ 형식으로 사용 됩니다.
이렇게 하면 불연속 쿼리 모델에서 직접 구현할 수 없는 $ \sqrt{U} $와 같은 행렬을 쿼리할 수 있습니다.

이 유형의 oracle은 특정 단일 사용자를 검색 하지 않고 단일의 생성기 속성을 배우는 경우에 유용 합니다.
예를 들어 동적 퀀텀 시뮬레이션에서 목표는 Hermitian 행렬 $H $ 및 진화 시간 $t $에 대해 $U (t) = e ^ {-i H t} $와 긴밀 하 게 근접 한 퀀텀 회로를 고안 하는 것입니다.
$U (t) $의 고유 값는 $H $의 고유 값와 직접 관련 됩니다.
이를 확인 하려면 $H $: $H \ket{E} = E\ket {E} $ 인 것으로 간주 합니다. 그러면 $U (t) \ket{E} = e ^ {i\eml\ k {E} = e ^ {-iEt} \ket{E} $와 같은 매트릭스 지 수의 전원 계열 정의에서 쉽게 볼 수 있습니다.
따라서 $U (t) $의 eigenphase를 예측 하면 eigenvector $ \ket{E} $가 단계 추정 알고리즘에 입력 된 것으로 가정 하 고 eigenphase $E $가 제공 됩니다.
그러나이 경우에는 $t $ 값을 사용자의 판단에 따라 선택할 수 있습니다 .이 값은 $t의 충분 한 작은 값이 있으므로 eigenvalue $E $는 $E =-\ o s o/t $를 통해 고유 하 게 반전 될 수 있습니다.
퀀텀 시뮬레이션 메서드는 소수 부분 진화를 수행 하는 기능을 제공 하기 때문에, 특히 불연속 쿼리 모델이 정수 $j에 적용 되는 $U ^ j $ 형식의 unitaries만 허용 하는 반면 연속 쿼리 oracle을 사용 하면 실제 값 $t $에 대해 $U ^ t $ 형식의 근사치를 얻을 수 있습니다.
이는 $E $;에 대 한 대부분의 정보를 제공 하는 실험을 정확 하 게 선택할 수 있기 때문에, 효율성의 마지막 온스를 모두 단계 예측 알고리즘에서 잡은 것이 중요 합니다. 반면 불연속 쿼리를 기반으로 하는 메서드는 알고리즘에서 가장 적합 한 정수 수의 쿼리를 선택 하 여 해당 메서드를 손상 된 상태로 만들어야 합니다.

이에 대 한 구체적인 예로, 출입문의 회전 각도는 아니지만 회전 퀀텀 시스템의 procession 빈도를 추정 하는 문제를 고려해 야 합니다.
이러한 퀀텀 dynamics를 설명 하는 단일는 진화 $t 시간에 대 한 $U (t) = R_z (2 \ 오메가 t) $이 고 알 수 없는 frequency $ \000s $입니다.
이 컨텍스트에서는 단일 $R _z $ gate를 사용 하 여 모든 $t $에 대 한 $U (t) $를 시뮬레이션할 수 있으며,이 경우에는 불연속 쿼리로만 제한 하지 않아도 됩니다.
이러한 연속 모델에는 또한 로그 함수의 분기 컷에 의해 마스킹 될 수 있는 단계 정보는 $t $의 비 비례하여 값에서 수행 되는 실험 결과에서 표시 될 수 있기 때문에 연속 쿼리를 사용 하는 단계 예측 프로세스에서 확인할 수 있습니다.
따라서 단계 예측 oracle의 이러한 연속 쿼리 모델과 같은 문제의 경우에는 적합 하지 않지만 불연속 쿼리 모델에도 적합 합니다.
이러한 이유로 Q# 두 쿼리 형태 모두에 대 한 기능을 제공 하 고 사용자에 게 제공 하 여 요구 사항 및 사용 가능한 oracle 유형에 맞는 단계 추정 알고리즘을 결정 합니다.

## <a name="dynamical-generator-modeling"></a>동적 생성기 모델링 ##

시간 이동의 생성기는 시간에 따라 상태가 어떻게 향상 됨을 설명 합니다. 예를 들어 퀀텀 상태의 dynamics $ \ket{\psi} $은 Schrödinger 수식 $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = H \ket{\psi (t)}, \end{align} $ $ $H (Hermitian)를 동작의 생성기로 사용 하 여 제어 합니다. 지정 된 초기 상태 $ \ket{\psi (0)} $ at time $t = $0,이 수식에 대 한 공식 솔루션 ($t $)은 원칙적으로 $ $ \begin{align} \ket{\psi (t)} = U (t) \ket{\psi (0)}, \end{align} $ $로 작성 될 수 있습니다. 여기서 행렬 지 수 $U (t) = e ^ {-i H t} $는 단일 시간 진화 연산자 라고 합니다. 다음에서이 폼의 생성기에 중점을 두고 있기는 하지만,이 개념은 개방형 퀀텀 시스템의 시뮬레이션 또는 보다 복잡 한 차등 방정식과 같이 더 광범위 하 게 적용 된다는 것을 강조 합니다.

동적 시뮬레이션의 기본 목표는 퀀텀 컴퓨터의 비트 단위에서 인코딩된 일부 퀀텀 상태에서 시간 진화 연산자를 구현 하는 것입니다.  대부분의 경우 Hamiltonian를 몇 $d $ 보다 더 간단한 용어로 나눌 수 있습니다.

$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} H_j, \end{align} $ $

각 용어에의 한 시간-진화는 퀀텀 컴퓨터에서 쉽게 구현할 수 있습니다. 예를 들어 $H _j $가 valbit 레지스터의 첫 번째 및 두 번째 요소에 대해 작동 하는 _1X_2 $ 연산자 $X 하는 경우 `qubits` 언제 든 지 시간을 기준으로 시간을 증가 시킬 수 있습니다. $t $는 서명을 포함 하는 작업을 호출 하 여 간단히 구현할 수 있습니다 `Exp([PauliX,PauliX], t, qubits[1..2])` `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` . Hamiltonian 시뮬레이션의 뒷부분에서 설명 했 듯이, 한 가지 해결 방법은 $H $에서 간단한 작업의 시퀀스로 대략적인 시간 진화를 수행 하는 것입니다.

$ $ \begin{align} U (t) & = \left (e ^ {-iH \_ 0 t/r} e ^ {-ih \_ 1 t/r} \c도트 e ^ {-ih \_ {d-1} t/r} \left) ^ {r} + \mathcal{O} (d ^ 2 \ max_j \\ | H \_ j \\ | ^ 2 t ^ 2/r), \end{align} $ $

여기서 정수 $r > $0는 근사값 오류를 제어 합니다.

동적 생성기 모델링 라이브러리는 간단한 생성기를 기준으로 복잡 한 생성기를 위한 프레임 워크를 제공 합니다. 이러한 설명은 시뮬레이션 라이브러리를 사용 하 여 선택의 시뮬레이션 알고리즘에의 한 시간 진화를 구현 하는 것과 같은 여러 세부 정보가 자동으로 처리 되는 것을 말합니다.

> [!TIP]
> 아래에 설명 된 동적 생성기 라이브러리는 샘플에서 설명 합니다. Ising 모델을 기반으로 하는 예제는 [ **Isinggenerators** 샘플](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/generators)을 참조 하세요.
> 분자 Hydrogen를 기반으로 하는 예제는 [**H2SimulationCmdLine**](https://github.com/microsoft/Quantum/tree/master/samples/simulation/h2/command-line) 및 [**H2SimulationGUI**](https://github.com/microsoft/Quantum/tree/master/samples/simulation/h2/gui) 샘플을 참조 하세요.

### <a name="complete-description-of-a-generator"></a>생성기의 전체 설명 ###

최상위 수준에서 Hamiltonian에 대 한 전체 설명은 `EvolutionGenerator` 두 개의 구성 요소가 포함 된 사용자 정의 형식에 포함 되어 있습니다.

```qsharp
newtype EvolutionGenerator = (EvolutionSet, GeneratorSystem);
```

`GeneratorSystem`사용자 정의 형식은 Hamiltonian에 대 한 기존 설명입니다.

```qsharp
newtype GeneratorSystem = (Int, (Int -> GeneratorIndex));
```

튜플의 첫 번째 요소는 `Int` Hamiltonian의 용어 $d $ 수를 저장 하 고, 두 번째 요소는 `(Int -> GeneratorIndex)` \{ \} `GeneratorIndex` Hamiltonian의 각 기본 용어를 고유 하 게 식별 하는 사용자 정의 형식에 $0, 1,..., d-1 $의 정수 인덱스를 매핑하는 함수입니다. Hamiltonian의 용어 컬렉션을 배열이 아니라 함수로 표현 하 여의 `GeneratorIndex[]` 즉시 계산을 수행할 수 있습니다 .이는 `GeneratorIndex` 많은 수의 용어로 Hamiltonians를 설명할 때 특히 유용 합니다.

매우에 의해 식별 되는 기본 용어에 대 한 규칙을 적용 하는 것 `GeneratorIndex` 은 쉽지 않습니다. 예를 들어, 기본 용어는 위에서 설명한 대로 Pauli 연산자 일 수 있지만, 일반적으로 퀀텀 화학 시뮬레이션에서 사용 되는 Fermionic annihilation 및 만들기 연산자 일 수 있습니다. 즉,가 `GeneratorIndex` 가리키는 용어의 시간 혁신을 퀀텀 회로로 구현할 수 있으므로는 의미가 없습니다.

`EvolutionSet` `GeneratorIndex` 일부 정식 집합에서 가져온 임의의를 퀀텀 회로로 표현 된 단일 연산자 ()로 매핑하는 사용자 정의 형식을 지정 하 여이를 확인 합니다 `EvolutionUnitary` . 는 `EvolutionSet` 이 구성 되는 방식에 대 한 규칙을 정의 하 `GeneratorIndex` 고 가능한 집합을 정의 합니다 `GeneratorIndex` .

```qsharp
newtype EvolutionSet = (GeneratorIndex -> EvolutionUnitary);
```

### <a name="pauli-operator-generators"></a>Pauli 연산자 생성기 ###

구체적이 고 유용한 생성기 예제는 각각 다른 계수를 사용 하 여 Pauli 연산자의 합계인 Hamiltonians입니다.
$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} a_j H_j, \end{align} $ $ 여기서 각 $ \sum H_j $는 이제 Pauli 그룹에서 그려집니다. 이러한 시스템의 경우 `PauliEvolutionSet()` `EvolutionSet` Pauli 그룹의 요소와 계수를에 의해 식별 되는 방법에 대 한 규칙을 정의 하는 형식의를 제공 합니다. 여기에는 `GeneratorIndex` 다음과 같은 시그니처가 있습니다.

```qsharp
newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```

이 인코딩에서 첫 번째 매개 변수는 `Int[]` Pauli 문자열을 지정 합니다. 여기서 $ \Hat I\rightarrow $0, $ \Hat X\rightarrow $1, $ \Hat Y\rightarrow $2 및 $ \Hat Z\rightarrow $3입니다. 두 번째 매개 변수는 `Double[]` Hamiltonian에서 Pauli 문자열의 계수를 저장 합니다. 이 배열의 첫 번째 요소만 사용 됩니다. 세 번째 매개 변수는 `Int[]` 이 Pauli 문자열이 작동 하는 요소를 인덱싱하고 중복 된 요소가 없어야 합니다. 따라서 Hamiltonian term $0.4 \hat X_0 \hat Y_8 \hat I_2 \hat Z_1 $는로 나타낼 수 있습니다.

```qsharp
let generatorIndexExample = GeneratorIndex(([1,2,0,3], [0.4]]), [0,8,2,1]);
```

는 `PauliEvolutionSet()` 다음 서명을 사용 하 여이 폼을에 매핑하는 함수입니다 `GeneratorIndex` `EvolutionUnitary` .

```qsharp
newtype EvolutionUnitary = ((Double, Qubit[]) => Unit is Adj + Ctl);
```

첫 번째 매개 변수는 단일 진화의 계수를 곱하여 하는 시간 기간을 나타냅니다 `GeneratorIndex` . 두 번째 매개 변수는 단일 역할을 수행 하는 고 비트 레지스터입니다. 

### <a name="time-dependent-generators"></a>시간 종속 생성기 ###

대부분의 경우에는 Schrödinger 수식 $ $ \begin{align} i\frac {d \ket{\psi (t)} {d t} & = \hat H (t) \ket{\psi (t)}, \end{align} $ $에서 발생 하는 것 처럼 시간 종속 생성기에도 관심이 있습니다. $ \hat H (t) $는 이제 시간에 따라 다릅니다 위의 시간 독립적 생성기에서이 경우의 확장은 간단 합니다. $T $에 대해 Hamiltonian를 설명 하는 고정을 사용 하는 대신 `GeneratorSystem` `GeneratorSystemTimeDependent` 사용자 정의 형식이 있습니다.

```qsharp
newtype GeneratorSystemTimeDependent = (Double -> GeneratorSystem);
```

첫 번째 매개 변수는 [0, 1] $ 인 $s 연속 일정 매개 변수이 고이 형식의 함수는 `GeneratorSystem` 해당 일정에 대해를 반환 합니다. 일정 매개 변수는 실제 시간 매개 변수 (예: $s = t/T $)와 선형으로 관련 될 수 있습니다. 예를 들어 총 시뮬레이션 시간은 $T $입니다. 그러나이 경우에는 일반적이 지 않아도 됩니다.

마찬가지로이 생성기의 전체 설명에는가 필요 `EvolutionSet` 하므로 `EvolutionSchedule` 사용자 정의 형식을 정의 합니다.

```qsharp
newtype EvolutionSchedule = (EvolutionSet, GeneratorSystemTimeDependent);
```
