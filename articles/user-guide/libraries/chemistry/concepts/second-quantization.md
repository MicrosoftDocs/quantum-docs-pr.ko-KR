---
title: 두 번째 양자화
description: 퀀텀 프로그래밍에서 전자 구조를 모델링 하는 두 번째 양자화 방법에 대해 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.secondquantization
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6becd348f7b3957cb60b16bbd5a28228527e1d4c
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835811"
---
# <a name="second-quantization"></a>두 번째 양자화

두 번째 양자화는 다른 렌즈를 통해 전자 구조 문제를 살펴봅니다.
각 $N _e $ 파괴를 특정 상태 (또는 궤도)에 할당 하는 대신 두 번째 양자화는 각 궤도를 추적 하 고 각 궤도에 전자가 있는지 여부를 저장 하며, 동시에 해당 wave 함수의 대칭 속성을 자동으로 보장 합니다.
Fermions에 필요 하므로 symmetrizing는 입력 상태를 방지 하 고, 두 번째 양자화는 작은 퀀텀 컴퓨터를 사용 하 여 이러한 모델을 시뮬레이션 하는 것을 걱정 하지 않고 퀀텀 화학 모델을 지정할 수 있기 때문에 중요 합니다.

두 번째 양자화의 예로, $ \ psi_0 \cit\ psi_ {N-1} $가 orthonormal 공간 orbitals 집합 이라고 가정 하겠습니다.
이러한 orbitals는 고려 되는 유한 기준 집합 내에서 가능한 한 정확 하 게 시스템을 나타내기 위해 선택 됩니다.
이러한 orbitals의 일반적인 예는 hydrogen atom의 eigenbasis을 형성 하는 원자성 orbitals입니다.
파괴에는 두 개의 spin 상태가 있으므로 두 파괴 각각의 공간 궤도로 crammed 수 있습니다.
즉, 다음을 예로 들 수 있습니다. 유효한 기본 상태는 $ \ psi_ {0, \uparrow}, \ldots, \ psi_ {N-1, \uparrow}, \ psi_ {0, \downarrow}, \ldots, \ psi_ {N-1, \downarrow} $ where $ \uparrow $ 및 $ \ldots $ 형식으로, 회전 각도의 두 eigenstates를 지정 하는 레이블입니다.
$ \Sigma \sigma의 $ (j, \sigma) $에 대 한이 결합 \{ \} 된 인덱스는 공간을 모두 저장 하 고 회전 각도를 저장 하기 때문에 스핀 궤도 라고 합니다.
화학 라이브러리에서 spin-orbitals는 데이터 구조에 저장 되며 `SpinOrbital` 다음과 같이 생성 됩니다.

```csharp
    // First, we load the namespace containing spin-orbital objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // First, we assign an orbital index, say `5`. Note that we use 0-indexing,
    // so this is the 6th orbital.
    var orbitalIdx = 5;

    // Second, we assign a spin index, say `Spin.u` for spin up or `Spin.d` for spin down.
    var spin = Spin.d;

    // the spin-orbital (5, ↓) is then
    var spinOrbital = new SpinOrbital(orbitalIdx, spin);

    // A tuple `(int, Spin)` is also implicitly recognized as a spin-orbital.
    (int, Spin) tuple = (orbitalIdx, spin);

    // We explicitly specify the type of `spinOrbital1` to demonstrate
    // the implicit cast to `SpinOrbital`.
    SpinOrbital spinOrbital1 = tuple;
```

즉, 웨이브 함수의 회전 및 공간 부분 모두를 $ \ psi_ \csts\ psi_ {2N} $로 사용 하는 것이 공식적으로 생각 될 수 있습니다 {0} . 여기서 각 인덱스는 이제 $ (j, \시그마) $의 열거형입니다.
가능한 열거형 중 하나는 $g (j, \sigma) = j + N\sigma ' $입니다.
가능한 또 다른 열거형은 $h (j, \sigma) = 2 * j + \sigma $입니다.
퀀텀 화학 라이브러리는 이러한 규칙을 사용할 수 있으며, 이러한 인코딩의 spin orbitals는 다음과 같이 인스턴스화할 수 있습니다.

```csharp
    // Let us use the spin orbital created in the previous snippet.
   var spinOrbital = new SpinOrbital(5, Spin.d);

   // Let us set the total number of orbitals to be say, `7`.
   var nOrbitals = 7;

    // This converts a spin-orbital index to a unique integer, in this case `12`,
    // using the formula `g(j,σ)`.
    var integerIndexHalfUp = spinOrbital.ToInt(IndexConvention.HalfUp);

    // This converts a spin-orbital index to a unique integer, in this case `11`,
    // using the formula `h(j,σ)`.
    var integerIndexUpDown = spinOrbital.ToInt(IndexConvention.UpDown);

    // The default conversion uses the formula `h(j,σ)`, in this case `11`.
    var integerIndexDefault = spinOrbital.ToInt();
```

Fermionic 시스템의 경우 Pauli 제외 원칙은 둘 이상의 전자 프로그램을 동시에 모든 회전 궤도에 제공 하는 것을 방지 합니다.
즉, $ \ psi_1 $에 대 한 두 가지 법적 상태를 \begin{equation} \ psi_1 \rightarrow \begin{cases} \ket {0} ec& \text{s ($ \ psi_1 $가 사용 되지 않는 경우)로 작성할 수 있습니다. \\\
\ket {1} _1 & \text{if $ \ psi_1 $가 차지 하는 경우} \end{cases} \end{c}이 인코딩은 단일 퀀텀 비트로 전자 직업을 저장할 수 있으므로 퀀텀 컴퓨터에 유용 합니다.

$2N $ spin orbitals의 직업 상태는 비슷한 방법으로 $2N $에 저장 될 수 있습니다.
예를 들어 $N = $2 인 경우 상태 $ $ \ket {0} \ket {1} \ket {1} \ket {0} , $ $

는 spin orbitals $1 $ 및 $2 $가 나머지 빈를 사용 하는 것과 일치 합니다.
마찬가지로 $ $ \ket {0} \equiv \ket {0} _ {0} \ci\ket {0} _{n-1}, $ $ 상태

는 파괴 없고 ' 진공 state ' 라고 합니다.

두 번째 양자화의 부작용은 더 이상 퀀텀 상태의 앤티앨리어싱을 추적 하지 않아도 된다는 것입니다.
이는 표시 되는 것 처럼, 회전 궤도의 전자 직업를 만들고 삭제 하는 연산자의 통신 규칙을 통해서가 아니라 상태의 앤티 대칭을 나타내는 것입니다.

## <a name="fermionic-operators"></a>Fermionic 연산자

두 번째 양자화 기반 벡터에 대해 작동 하는 두 가지 기본 연산자를 생성 및 annihilation 연산자 라고 합니다.
이러한 연산자는 특정 위치에 파괴를 삽입 하거나 제거 합니다.
이는 각각 $a ^ \ dagger_j $ 및 $a _j $로 표시 됩니다.

예를 들어, \begin{align} a ^ \ dagger_1 \ket {0} _1 = \ket {1} _1, \quad a ^ \ dagger_1 \ket {1} _1 = 0, \quad a_1 \ket {0} _1 = 0, \quad a_1 \ket {1} _1 = \ket {0} _1.
여기 $a ^ \ dagger_1 \ket {1} _1 = 0 $ 및 $a _1 \ket {0} _1 $은 0-vector not $ \ket _1 $을 생성 합니다 {0} .
따라서 이러한 연산자는 Hermitian도 아닙니다.
이 형식을 사용 하 여 일반 생성 및 annihilation 연산자 <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> 를 나타냅니다.
예를 들어 단일 생성 연산자는 다음과 같이 표시 됩니다.

```csharp
    // We load the namespace containing ladder operator objects.
    using Microsoft.Quantum.Chemistry.LadderOperators;

    // Let us use the spin orbital created in the previous snippet.
    var spinOrbitalInteger = new SpinOrbital(5, Spin.d).ToInt();

    // We specify either a creation or annihilation operator using 
    // the enumerable type `RaisingLowering.u` or `RaisingLowering.d`
    // respectively;
    var creationEnum = RaisingLowering.u;

    // The type representing a creation operator is then initialized 
    // as follows. Here, we index these operators with integers.
    // Hence we initialize the generic ladder operator with an
    // integer index type.
    var ladderOperator0 = new LadderOperator<int>(creationEnum, spinOrbitalInteger);

    // An alternate constructor for a LadderOperator instead uses
    // a tuple.
    var ladderOperator1 = new LadderOperator<int>((creationEnum, spinOrbitalInteger));
```

이러한 연산자를 사용 하 여 $ $ \ket {0} \ket {1} \ket {1} \ket {0} = a ^ \ dagger_1 a ^ \ dagger_2 \ket {0} ^ {\otimes 4}를 표현할 수도 있습니다.
$ $이 연산자 시퀀스는 위의 위에서 설명한 단일 스핀 궤도 케이스와 비슷한 c # 코드를 사용 하 여 Hamiltonian 시뮬레이션 라이브러리 내에서 생성 됩니다.
```csharp
    // We load the namespace containing fermion-related objects.
    using Microsoft.Quantum.Chemistry.Fermion;

    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We can convert this array of tuples to a sequence of ladder
    // operators using the `ToLadderSequence()` methods.
    var ladderSequences = indices.ToLadderSequence();

    // Sequences of ladder operators are quite general. For instance,
    // they could be bosonic operators, instead of fermionic operators.
    // We specialize them by constructing a `FermionTerm` representing 
    // a fermion creation operator on the index `2` followed by `1`.
    var fermionTerm = new FermionTerm(ladderSequences);
```

$K $ Fermions 시스템의 경우 두 번째 양자화 만들기 연산자 $a ^ \ dagger_i $은 $ $ a ^ \ dagger_i \ket{n_1, n_2, \ldots, 0_i, \lsts, n_k} = (-1) ^ {S_i} \ket{n_1, n_2, \lsts, 1_i, \lsts에 의해 지정 됩니다. n_k}, $ $ 및 $ $ a ^ \ dagger_i \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k} = 0, $ $ where $S _i = \ sum_ {j<i} a ^ \ dagger_j a_j $는 단일 파티클의 상태에 있는 Fermions의 총 수를 측정 하 고 $j i $ 인덱스를 포함 합니다.

세 번째 연산자는 두 번째 양자화 표현 에서도 종종 사용 됩니다.
이 연산자를 number 연산자 라고 하며 \begin{equation} n_i = a ^ \ dagger_i a_i에 의해 정의 됩니다.
\end{equation}이 연산자는 지정 된 spin 궤도의 직업을 계산 합니다. 즉, \begin{align} n_i \ket {0} _i &= 0 \ nonumber입니다.\\\
n_i \ket {1} _i &= \ket {1} _i.
위의 `FermionTerm` 예와 마찬가지로이 숫자 연산자는 다음과 같이 생성 됩니다 \end{align}.
```csharp
    // Let us use a new method to compactly create a sequence of ladder
    // operators. Note that we have omitted specifying whether the 
    // operators are raising or lowering. In this case, the first half
    // will be raising operators, and the second half will be lowering 
    // operators.
    var indices = new[] { 1, 1 }.ToLadderSequence();

    // We now construct a `FermionTerm` representing an annihilation operator
    // on the index 1 followed by the creation operator on the index 1.
    var fermionTerm0 = new FermionTerm(indices);
```

미묘한는 fermionic 시스템에서 만들기 또는 annihilation 연산자를 사용 하는 경우에도 나타납니다.
레이블 교환의 모든 유효한 퀀텀 상태가 대칭이 되어야 합니다.
즉, $ $ a ^ \ dagger_2 ^ \ dagger_1 \ket {0} =-a ^ \ dagger_1 ^ \ dagger_2 \ket {0} 합니다.
$ $ 이러한 연산자는 ' commute '로, 일반적으로 모든 $i에 대해 \begin{align} a ^ \ dagger_i a ^ \ dagger_j =-(1-\ delta_ {i, j}) ^ \ dagger_j a ^ \ dagger_i, \quad a ^ \ dagger_i a_j = \ delta_ {i, j}-a_j a ^ \ dagger_i 있습니다.
\end{align} 다음과 같은 두 <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> 인스턴스는 inequivalent 것으로 간주 됩니다.
```csharp
    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We now construct a `LadderSequence` representing a creation operator
    // on the index 1 followed by 2, then a term with the reverse ordering.
    var laddderSeqeunce = indices.ToLadderSequence();
    var laddderSeqeunceReversed = indices.Reverse().ToLadderSequence();

    // The following Boolean is `false`.
    var equal = laddderSeqeunce == laddderSeqeunceReversed;
```

각 생성 연산자가 commute 한다는 요구 사항은 두 번째 양자화 표현을 사용 하면 Fermions의 앤티앨리어싱을 통해 직면 하는 과제를 필요성 제거 한다는 것입니다.
대신 생성 연산자의 정의에서 챌린지를 다시 제시 합니다. 

통신 규칙을 사용 하는 경우 일부 `LadderSequence` 인스턴스는 실제로 빼기 기호까지 동일한 fermionic 연산자 시퀀스에 해당 합니다.
예를 들어 Hamiltonian $a _0 ^ \kaa_1 ^ \aaa_1 a_0 =-a_1 ^ \aaa_0 ^ \dagger a_1 a_0 $를 고려 하십시오.
이렇게 하면 모든에 대 한 정식 순서를 정의할 motivates `FermionTerm` .
`FermionTerm`는 다음과 같이 정식 순서로 자동으로 배치 됩니다.
```csharp
    // We now construct two `FermionTerms` that are equivalent with respect to
    // anti-commutation up to a sign change.
    var fermionTerm0 = new FermionTerm(new[] { 0, 1, 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 1, 0, 1, 0 }.ToLadderSequence());

    // The following Boolean is `true`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // The change in sign is not compared above, but is an internally tracked
    // property of `FermionTerm`.
    int sign0 = fermionTerm0.Coefficient;
    var sign1 = fermionTerm1.Coefficient;

    // The following Boolean is `false`.
    var signEqual = sign0 == sign1;
```

## <a name="second-quantized-fermionic-hamiltonian"></a>두 번째-양자화 Fermionic Hamiltonian

[전자 시스템에 대 한 퀀텀 모델](xref:microsoft.quantum.chemistry.concepts.quantummodels) 의 Hamiltonian는 생성 및 annihilation 연산자를 기준으로 작성 될 수 있습니다.
특히 $ \psi \_ j $가 기본을 형성 하는 spin orbitals 인 경우

\begin{equation} \hat{H} = \pqrs \_ {pq} h \_ {pq} a ^ \ \_ p a \_ q + \frac {1} {2} \sum \_ {pqrs} h \_ {} a ^ \_ \aap a ^ \aaa ^ \ \_ q a \_ ra \_ s + H \_ {\textrm nuc}, \label{eq: totalHam} \begin{equation}. 여기서 $H \_ {\textrm nuc} $은 핵 에너지 (steiglitz 근사값에서 상수)입니다.

\begin{align} h \_ {pq} &= \int \_ {-\infty} ^ \infty \int ^ \* \_ p (x 1) \_ \int (-\Frac{\nabla ^ 2} {2} + V (x \_ 1) \int) \int \_ q (x \_ 1) \mathrm{d} ^ 3 x \_ 1, \end{align}

여기서 $V (x) $는 평균 현장 잠재력 이며

\begin{align} h \_ {pqrs} &= \int \_ {-\infty} ^ \infty \int \_ {-\infty} ^ \infty\psi \_ p ^ \* (x \_ 1) \int \_ q ^ \* (x \_ 2) \\frac {1} {| x_1-x_2 |} \int) \int \_ r (x \_ 2) \int \_ s (x \_ 1) \mathrm{d} ^ \_ 3 x 1 \ mathrm {d} ^ 3 x \_ 2. \ 레이블 {eq: 적분} \end{align}

\_이러한 모든 용어에는 단일 파괴 포함 되 $h 고 \_ pqrs {} $는 두 개의 전자 pq 이라는 용어를 포함 하기 때문에 $h {} $는 1-전자 적분 이라고 합니다.
이러한 계수 값을 계산 하려면 정수 계열이 필요 하므로 이러한 계수를 적분 이라고 합니다.
한 가지 전자 용어는 개별 파괴의 kinetic 에너지와 nuclei의 전기 필드와의 상호 작용을 설명 합니다.
반면에 두 전자/반자 정수는 파괴 간의 상호 작용을 설명 합니다.

이러한 용어의 의미에 대 한 intuition는 각 용어를 구성 하는 생성 및 annihilation 연산자에서 통해 수집할 수 있습니다.
예를 들어 $h _ {pq} a ^ \ dagger_p a_q $는 전자 도약가 spin 궤도 $q $에서 spin 궤도 $p $로의 전자을 설명 합니다.
마찬가지로 $h _ {pqrs} a ^ \ dagger_p a ^ \ dagger_q a_r a_s $ (distinct $p, q, r, s $)는 두 파괴 (distinct $r, q, r, s $)를 회전 하는 두 가지를 설명 합니다.
$R = q $ 및 $p = s $ $h _ {prrp} a ^ \ dagger_p ^ \ dagger_r a_r a_p = h_ {prrp} n_p n_r $를 사용 하면 두 파괴 관련 된 에너지 벌점이 서로 가까이 있지만 동적 프로세스를 설명 하지는 않습니다.

클래스를 사용 하 여 이러한 Hamiltonians를 나타낼 수 있으며 `FermionHamiltonian` ,이는 기본적으로 원하는 모든 인스턴스를 포함 하는 목록입니다 `FermionTerm` .
Hamiltonians는 정의에 의해 Hermitian `HermitianFermionTerm` 용어 인지 여부를 확인할 때 Hermitian 대칭을 사용 하는 보다 특수화 된 형식을 사용 하 여 용어를 인덱싱합니다.

몇 가지 설명 예제를 생성 해 보세요.
Hamiltonian $ \hat{H} = a_0 ^ \aa_1 + a_1 ^ \aaa_0 $를 고려 합니다.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the terms to be added.
    var fermionTerm0 = new FermionTerm(new[] { 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 0, 1 }.ToLadderSequence());

    // These fermion terms are not equal. The following Boolean is `false`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // However, these terms are equal under Hermitian symmetry.
    // We also take the opportunity to demonstrate equivalent constructors
    // for hermitian fermion terms
    var hermitianFermionTerm0 = new HermitianFermionTerm(fermionTerm0);
    var hermitianFermionTerm1 = new HermitianFermionTerm(new[] { 0, 1 });

    // These Hermitian fermion terms are equal. The following Boolean is `true`.
    var hermitianSequenceEqual = hermitianFermionTerm0 == hermitianFermionTerm1;

    // We add the terms to the Hamiltonian with the appropriate coefficient.
    // Note that these terms are identical.
    hamiltonian.Add(hermitianFermionTerm0, 1.0);
    hamiltonian.Add(hermitianFermionTerm1, 1.0);
```
Hamiltonian 연산자가 Hermitian 연산자 임을 고려 하 여이 생성을 단순화할 수 있습니다.
을 사용 하 여 Hamiltonian에 용어를 추가 하는 경우 `Add` 와 같은 모든 비 Hermitian 용어 `fermionTerm0` 는 Hermitian 켤레와 쌍으로 간주 됩니다.
따라서 다음 코드 조각은 동일한 Hamiltonian를 나타냅니다.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

통신 규칙을 사용 하는 경우 Hamiltonian의 일부 `FermionTerm` 인스턴스는 실제로 빼기 기호까지 동일한 fermionic 연산자 시퀀스에 해당 합니다.
예를 들어 Hamiltonian $H = a_0 ^ \aaa_1 ^ \aaa_1 a_0-a_1 ^ \aatea_0 ^ \dagger a_1 a_0 2a_0 ^ \aaa_1 ^ \dagger a_1 a_0 $ (위에서 생성 된 용어의 합계)를 고려 합니다.
사용자에 게는 동일한 용어 이므로 항상 명확 하지 않을 수 있으므로 Hamiltonian에 별도로 추가 될 수 있습니다.
또는 Hamiltonian에서 이미 존재 하는 용어를 수정 하는 데 관심이 있을 수 있습니다.
이러한 경우 다음과 같이 이와 동일한 용어를 결합할 수 있습니다.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We now create two Hermitian fermion terms that are equivalent with respect to
    // anti-commutation and Hermitian symmetry.
    var terms = new[] {
        (new[] { 0, 1, 1, 0 }, 1.0),
        (new[] { 1, 0, 1, 0 }, 1.0) }
    .Select(o => (new HermitianFermionTerm(o.Item1.ToLadderSequence()), o.Item2.ToDoubleCoeff()));

    // Now add `terms` to the Hamiltonian.
    hamiltonian.AddRange(terms);

    // There is only one unique term. `nTerms == 1` is `true`.
    var nTerms = hamiltonian.CountTerms();
```
동등한 용어의 계수를 결합 하 여 Hamiltonian의 총 용어 수를 줄입니다.
이후에는 Hamiltonian를 시뮬레이션 하는 데 필요한 퀀텀 게이트의 수를 줄입니다.

### <a name="internal-representation"></a>내부 표현

1 ~ 2 개의 본문 상호 작용이 있는 fermionic Hamiltonian는 두 번째 양자화 표기법으로 표시 됩니다.

$ $ \begin{align} H = \sum \_ {pq} h \_ {pq} a ^ \sum \_ {p} a \_ {q} + \frac {1} {2} \sum \_ {pqrs} H \_ {} a ^ \sum \_ {p} a ^ \sum \_ {q} a { \_ r} a { \_ s}.
\end{align} $ $

이 표기법에는 최대 $N ^ 2 + N ^ 4 $ 계수가 있습니다.
그러나 이러한 계수 중 상당수는 동일한 연산자에 해당 하는 것으로 수집할 수 있습니다.
예를 들어 $p, q, r 등의 경우 s $는 고유 인덱스입니다. 통신 규칙을 사용 하 여 다음을 표시할 수 있습니다. $ $ a ^ \_ \aa{p} a ^ \ \_ {q} a \_ {r} a { \_ s} =-a ^ \aa{ \_ q} a ^ \aa{ \_ p} a \_ {r} a \_ {s} =-a ^ \aa{ \_ p} a ^ \aa{q} a {q} a {r} a { \_ \_ \_ r} = a ^ \ara^ \_ \_ \_ \_ \aa{p} a {p} a {s} a {r}.
$$

뿐만 아니라 $H $가 Hermitian $h \_ {pqrs} a ^ \dagger \_ {p} a ^ \dagger \_ {q} a {r} a {s} $와 같은 모든 비 Hermitian fermionic 연산자는 \_ \_ $H $에도 있는 켤레를 포함 합니다. 이러한 symmetries으로 분류 된 용어 그룹의 인덱스를 고유 하 게 만들려면 \_ \_ \_ \_ $n + m $ fermionic 연산자 $a ^ \aate{ \_ i \_ 1} \cdots a ^ \aaa { \_ i \_ n} a \_ {j 1} \_ \cdots a \_ {j \_ m}의 인덱스에 대해 $ (i 1, \cdots, $as i n, j 1, \cdots, j m) 인덱스에 대 한 정식 순서를 정의 합니다.
-   모든 생성 연산자 $a ^ \_ \_ \dagger $는 모든 annihilation 연산자 $a \_ {j \cdot} $ 앞에 배치 됩니다 \_ .
-   모든 생성 연산자 인덱스는 오름차순으로 정렬 됩니다. 즉, $i \_ 1< i \_ 2< \cdots < i \_ n $입니다.
-   모든 annihilation 연산자 인덱스는 내림차순으로 정렬 됩니다. 즉, $j \_ 1> j \_ 2 \cdots > j \_ m $입니다.
-   맨 왼쪽 인덱스는 \_ 1 \ le j m $ $i 가장 오른쪽 인덱스 보다 작거나 같습니다 \_ .

이 정식으로 정렬 된 인덱스 집합을 $ $ \begin{align} (i \_ 1, \cdots, i \_ n, j \_ 1, \cdots, j \_ m) \in S \_ {n, m}로 식별할 수 있습니다.
\end{align} $ $

이 정식 순서를 사용 하면 fermionic Hamiltonian $ $ \begin{align} H = \sum \_ {(p, q) \sum S \_ {1,1} } H ' \_ {pq} \frac{a ^ \sum \_ {p} a { \_ q} + a ^ \sum { \_ q} a \_ {p}} {2} + \sum \_ {(p, q, r)로 표현 될 수 있습니다. s) \sum s \_ {2,2} } H ' \_ {pqrs} \frac{a ^ \_ \aa{p} a ^ \aa{ \_ q} a \_ {r} a { \_ s} + a ^ \ara{ \_ s} a ^ \_ \_ \_ {2} \sum \_ {pq} $ 및 $h ' \_ {pqrs} $와 같이 적절 하 게 조정 된 1 ~ 2-전자 $h ' {} $

