---
title: Hamiltonian Dynamics 시뮬레이션 | Microsoft Docs
description: Hamiltonian Dynamics 개념 문서 시뮬레이션
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
ms.openlocfilehash: 69c7923ea447af320a413889df54716abd5475ea
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820643"
---
# <a name="simulating-hamiltonian-dynamics"></a>Hamiltonian Dynamics 시뮬레이션

Hamiltonian가 기본 연산자의 합계로 표시 된 후에는 잘 알려진 기술 호스트를 사용 하 여 기본 게이트 작업으로 dynamics를 컴파일할 수 있습니다.
Trotter – Suzuki 수식, unitaries의 선형 조합, 등 세 가지 효율적인 방법이 있습니다.
이 세 가지 방법에 대해 설명 하 고 Hamiltonian 시뮬레이션 라이브러리를 사용 하 여 이러한 메서드를 구현 하는 방법에 대 한 구체적인 Q # 예제를 제공 합니다.


## <a name="trottersuzuki-formulas"></a>Trotter – Suzuki 수식
Trotter – Suzuki 수식의 개념은 간단 합니다. 즉, Hamiltonian를 시뮬레이션을 위한 합계로 표현 하 고, 총 진화를 이러한 간단한 evolutions의 시퀀스로 대략적으로 표현 합니다.
특히 $H = \ sum_ {j = 1} ^ m H_j $를 사용 하 여 Hamiltonian 수 있습니다.
그런 다음 $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \ prod_ {j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $이는 $t \ll $1 인 경우이 근사값의 오류는 무시 됩니다.
$E ^ {-i H t} $가 일반 지 수 인 경우이 근사값의 오류는 $O 되지 않습니다 (m ^ 2 t ^ 2) $: 0입니다.
이 오류는 $e ^ {-iHt} $이 (가) 연산자 지 수이 고 $H _j $ 용어가 commute (예 *:* $H _j H_k \ne H_k H_j $) 때문에이 수식을 사용할 때 오류가 발생 하는 경우에 발생 합니다.

$T $가 큰 경우에는 Trotter – Suzuki 수식을 사용 하 여 간단한 시간 단계 시퀀스로 분리 하 여 dynamics를 정확 하 게 시뮬레이션할 수 있습니다.
$R $를 사용 하 여 단계를 진행 하는 동안 수행 된 단계 수를 지정 합니다.
그런 다음 $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \left (\ prod_ {j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r)를 사용할 수 있습니다. $ $-$가 $m ^ 2 t ^ 2/\ 엡실론 $로 확장 하는 경우 $ \left > 0 $에 대해 최대 $ \left $로 오류를 만들 수 있음을 의미 합니다. $r

오류 용어가 취소 되는 연산자 지 수 시퀀스를 구성 하 여 보다 정확한 근사치을 작성할 수 있습니다.
가장 간단한 이러한 수식인 대칭 Trotter 수식 또는 Strang 분할은 $ $ U_1 (t) = \ prod_ {j = 1} ^ m e ^ {-iH_j t/2} \ prod_ {j = m} ^ 1 e ^ {-iH_j t} = e ^ {-iHt} + O (m ^ 3 t ^ 3) 형식으로 사용 됩니다. $ $를 선택 하 여 $ \epsilon > 0 $의 $ \epsilon $ 보다 작게 만들 수 있습니다. $r $를 선택 하 여 $m ^ {3/2} t ^ {3/2}/\sqrt {\ 엡실론} $로 크기를 조정할 수 있습니다.

Trotter $U를 사용 하 여 고차 수식을 만들 수 있습니다.
가장 간단한 방법은 다음 네 번째 주문 수식입니다. 원래 Suzuki: $ $ U_2 (t) = U_1 ^ 2 (s_1t) U_1 ([1-4s_1] t) U_1 ^ 2 (s_1 t) = e ^ {-iHt} + O (m ^ 5t ^ 5), $ $ where $s _1 = (4-4 ^ {1/3}) ^{-1}$입니다.
일반적으로는 임의의 상위 수식이 비슷하게 생성 될 수 있습니다. 그러나 더 복잡 한 통합자를 사용 하 여 발생 하는 비용은 대부분의 실질적인 문제에 대 한 네 번째 순서의 이점 보다 더 큽니다.

위의 전략이 작동 하려면 $e ^ {iH_j t} $의 광범위 한 클래스를 시뮬레이트하는 메서드가 필요 합니다.
여기에서 사용할 수 있는 가장 간단한 Hamiltonians 패밀리는 Pauli 연산자입니다.
Pauli 연산자는 Clifford 작업 (양자 컴퓨팅의 표준 게이트)을 사용 하 여 diagonalized 수 있으므로 쉽게 시뮬레이션할 수 있습니다.
또한 diagonalized 된 후에는 해당 고유 값가 작동 하는 eibits의 패리티를 계산 하 여 찾을 수 있습니다.

예: $ $ e ^ {-iX\otimes X t} = (H\otimes H) e ^ {-iZ\otimes Z t} (H\otimes H), $ $ where $ $ e ^ {-i Z Z \otimes Z t} = \begin{bmatrix} e ^ {-it} & 0 & 0 & 0 \\\
        0 & e ^ {i t} & 0 & 0 \\\
        0 & 0 & e ^ {it} & 0 \\\
        0 & 0 & 0 & e ^ {-it} \end{bmatrix}.
$ $ 여기에서 $e ^ {-iHt} \ket{00} = e ^ {it} \ket{00}$ 및 $e ^ {-iHt} \ket{01} = e ^ {it} \ket{01}$ .이는 $0 $의 패리티가 $0 $이 고 비트 문자열 $1 $의 패리티는 $1 $입니다.

<xref:microsoft.quantum.intrinsic.exp> 작업을 사용 하 여 Q #에서 직접 지 수의 Pauli 연산자를 구현할 수 있습니다.
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies 𝑒^{- 𝑖 𝑋⊗𝑋 𝑡} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

Fermionic Hamiltonians의 경우 [요르단 – Wigner 분해](xref:microsoft.quantum.chemistry.concepts.jordanwigner) 는 Hamiltonian를 Pauli 연산자의 합계에 편리 하 게 매핑합니다.
즉, 위와 같은 방법으로 화학 시뮬레이션을 쉽게 적용할 수 있습니다.
아래는 Wigner 표현의 모든 Pauli를 수동으로 반복 하는 대신, 이러한 시뮬레이션을 실행 하는 방법을 보여 주는 간단한 예입니다.
시작 지점은 코드에서 `JordanWignerEncoding` 클래스의 인스턴스로 표현 된 Fermionic Hamiltonian의 [요르단 – Wigner 인코딩입니다](xref:microsoft.quantum.chemistry.concepts.jordanwigner) .

```csharp
    // This example uses the following namespaces:
    // using Microsoft.Quantum.Chemistry.OrbitalIntegrals;
    // using Microsoft.Quantum.Chemistry.Fermion;
    // using Microsoft.Quantum.Chemistry.Pauli;
    // using Microsoft.Quantum.Chemistry.QSharpFormat;

    // We create an instance of the `FermionHamiltonian` objecclasst to store the terms.
    var hamiltonian = new OrbitalIntegralHamiltonian(new[] 
    {
        new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123),
        new OrbitalIntegral(new[] { 0, 1 }, 0.456)
    }).ToFermionHamiltonian(IndexConvention.UpDown);

    // We convert this fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = hamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);

    // We now convert this representation into a format consumable by Q#.
    var qSharpData = jordanWignerEncoding.ToQSharpFormat();
```

Q # 시뮬레이션 알고리즘에서 사용할 수 있는 요르단 – Wigner 표현의 형식은 `JordanWignerEncodingData`사용자 정의 형식입니다.
Q # 내에서이 형식은 Trotter (Suzuki 통합자)를 사용 하 여 실행에 필요한 다른 매개 변수와 함께 시간 진화를 사용 하는 연산자를 반환 하는 편리한 `TrotterStepOracle` 함수에 전달 됩니다.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single time-step.
using(qubits = Qubit[nQubits]){

    // Apply single step of time-evolution
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

중요 한 점은이 구현은 [퀀텀 컴퓨터를 사용 하 여 전자 구조 Hamiltonians의 시뮬레이션](https://arxiv.org/abs/1001.3855) 에 설명 된 몇 가지 최적화를 적용 하며, 필요한 단일 비트 회전 수를 최소화 하 고 시뮬레이션 오류를 줄이는 데 퀀텀 [에 대 한 퀀텀 알고리즘을 개선](https://arxiv.org/abs/1403.1539) 합니다.

## <a name="qubitization"></a>고 비트

이는 퀀텀 워크의 아이디어를 사용 하 여 퀀텀 dynamics를 시뮬레이트하는 다른 시뮬레이션 방법입니다.
Trotter 수식 보다 더 많은 비트를 필요로 하는 반면,이 메서드는 진화 시간 및 오류 허용 오차를 사용 하 여 최적의 확장을 약속 합니다.
이러한 이유로, 일반적으로 Hamiltonian dynamics를 시뮬레이션 하 고 특히 전자 구조 문제를 해결 하기 위한 선호 하는 방법이 되었습니다.

높은 수준에서 다음과 같은 단계를 통해이 작업을 수행 합니다.
첫째, $H = \ sum_j h_j H_j $ (단일 및 Hermitian $H _j $ 및 $h _j \ge $0)를 사용 합니다.
한 쌍의 반사를 수행 하 여, stbitsourcea는 $ $W = e ^ {\pm i \pm ^{-1}(H/| h | _1)}, $ $ where $ | h | _1 = \ sum_j | h_j | $에 해당 하는 연산자를 구현 합니다.
다음 단계에서는 연습 연산자의 고유 값을 $e ^ {i\pm \cos ^{-1}(E_k/| h | _1)} $로 변환 합니다. 여기서 $E _k $은 $H $ to $e ^ {-iE_k t} $의 고유 값입니다.
이는 [퀀텀 신호 처리](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501)를 포함 하 여 다양 한 퀀텀 단일 값 변환 방법을 사용 하 여 달성할 수 있습니다.

또는 정적 수량 (예: Hamiltonian의 그라운드 상태 에너지)만 필요한 경우에는 결과의 코사인을 수행 하 여 결과에서 그라운드 상태 에너지를 추정 하기 위해 [단계 예측](xref:microsoft.quantum.libraries.characterization) 을 $W $에 직접 적용 접미사 합니다.
이는 퀀텀 단수형 value 변환 메서드를 사용 하는 대신 spectral 변환을 일반적으로 수행할 수 있도록 하기 때문에 중요 합니다.

좀 더 자세한 수준에서 구현 하려면 Hamiltonian에 대 한 인터페이스를 제공 하는 두 개의 서브루틴이 필요 합니다.
Trotter – Suzuki 메서드와 달리 이러한 서브루틴은 기존이 아닌 양자 이며 구현에는 Trotter 기반 시뮬레이션에 필요한 것 보다 더 많은 로그를 사용 해야 합니다.

\Operatorname{Select}를 사용 하는 첫 번째 퀀텀 서브루틴은 $ \operatorname{Select} $ 라고 하며, 각 $H _j $이 \Ket{j}로 간주 되는 \begin{c} \ket{j} \ket{\psi} = \ket{\psi} H_j Hermitian, \end{ 및 단일.
이는 제한적이 지 않은 것 처럼 보일 수 있지만, Pauli 연산자는 Hermitian 및 단일 이며, 따라서 퀀텀 화학 시뮬레이션 같은 응용 프로그램은이 프레임 워크에 자연스럽 게 속합니다.
$ \Operatorname{Select} $ 연산은 실제로 리플렉션 작업입니다.
$ \Operatorname{Select} ^ 2 \ k {j} \ket{\psi} = \ket{j} \ket{\psi} $는 각 $H _j $가 단일 및 Hermitian 이므로 고유 값 $ \pm $1을 포함 하기 때문에이를 볼 수 있습니다.

두 번째 서브루틴을 $ \operatorname{Prepare} $ 이라고 합니다.
Select 작업은 각 Hamiltonian 약관 $H에 대 한 액세스를 제공 하는 수단을 제공 하지만 _j $ 준비 서브루틴은 _j $, \begin{\ket{j}. ation} \operatorname{Prepare}\ket{0} = \ sum_j \sqrt{\frac{h_j} {| H | _1}}에 $h 액세스 하기 위한 메서드를 제공 합니다.
\end{equation} 다음에는 곱하기 제어 단계 게이트를 사용 하 여 $ $ \Lambda\ket{0}^ {\otimes n} = \begin{cases} \-\ket{x} & \text{if} x = 0 \\\
        \ket{x} & \text{otherwise} \end{cases}.
$$

$ \Operatorname{Prepare} $ 작업은 \operatorname{Prepare}에서 직접 사용 되지 않지만 $ $이 $ $ \begin{align} R &amp; = 1-2 \ a m e {Prepare} \ket{0}\bra{0} \operatorname{Prepare} ^{-1} \\\\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare} ^{-1}을 만드는 상태에 대 한 리플렉션을 구현 하는 데 사용 됩니다.
\end{align} $ $

$ \Operatorname{Select} $ 및 $R $ 작업을 $ $ W = \operatorname{Select} R, $ $로 설명 하는 연습 연산자 ($W ${-1}$e)는 $ $ W = R, $ $로 표현할 수 있습니다 .이는 isometry에 해당 하는 연산자를 구현 하는 데 다시 표시 될 수 있습니다.

이러한 서브루틴은 Q #에서 쉽게 설정할 수 있습니다.
예를 들어 단순 Ising Hamiltonian $H = X_1 + X_2 + Z_1 Z_2 $를 예로 들어 보겠습니다.
이 경우 $ \operatorname{Select} $ 작업을 구현 하는 Q # 코드는 <xref:microsoft.quantum.canon.multiplexoperations>에 의해 호출 되는 반면 $ \operatorname{Prepare} $ 작업은 <xref:microsoft.quantum.preparation.preparearbitrarystate>를 사용 하 여 구현할 수 있습니다.
Hubbard 모델 시뮬레이션을 포함 하는 예제는 [Q # 샘플](https://github.com/microsoft/Quantum/tree/master/samples/simulation/hubbard)로 볼 수 있습니다.

임의 화학 문제에 대해 이러한 단계를 수동으로 지정 하려면 화학 라이브러리를 사용 하지 않는 것이 좋습니다.
위의 Trotter – Suzuki 시뮬레이션 알고리즘과 마찬가지로 `JordanWignerEncodingData`는를 실행 하는 데 필요한 다른 매개 변수와 함께 안내 연산자를 반환 하는 편의 함수 `QubitizationOracle`에 전달 됩니다.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/oneNorm`, where oneNorm is the sum of absolute values of all probabilities in state prepared by `Prepare`.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  QubitizationOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single step of the quantum walk.
using(qubits = Qubit[nQubits]){

    // Apply single step of quantum walk.
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

중요 한 점은 구현 <xref:microsoft.quantum.chemistry.jordanwigner.qubitizationoracle>는 Pauli 문자열의 선형 조합으로 지정 된 임의의 Hamiltonians에 적용 됩니다.
화학 시뮬레이션에 최적화 된 버전은 <xref:microsoft.quantum.chemistry.jordanwigner.optimizedqubitizationoracle>를 사용 하 여 호출 됩니다.
이 버전은 [선형 t 복잡성을 사용 하 여 퀀텀 회로의 전자 Spectra Encoding](https://arxiv.org/abs/1805.03662)에 설명 된 기술을 사용 하 여 T 게이트 수를 최소화 하도록 최적화 되었습니다.
