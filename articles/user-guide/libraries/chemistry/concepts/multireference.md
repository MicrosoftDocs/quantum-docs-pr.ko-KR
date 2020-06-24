---
title: 상관 관계가 지정된 파동 함수
description: Microsoft 퀀텀 화학 라이브러리를 사용 하 여 wavefunctions의 동적 및 비동적 상관 관계에 대해 알아봅니다.
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.multireference
ms.openlocfilehash: 005ef86382ca72969b06a4206cab01f3845718e2
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275909"
---
# <a name="correlated-wavefunctions"></a>상관 관계가 지정된 파동 함수

특히 평형 기 하 도형 근처의 많은 시스템에서 [Hartree – Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) 이론은 단일 결정 참조 상태를 통해 분자 속성에 대 한 질적 설명을 제공 합니다. 그러나 양적 정확도를 얻기 위해 상관 관계 효과를 고려해 야 합니다. 

이 컨텍스트에서 동적 상관 관계와 동적이 지 않은 상관 관계 간에 dinstinguish 하는 것이 중요 합니다.
동적 상관 관계는 파괴의 추세에서 발생 하며, 예를 들어 interelectronic 반발력은 때문입니다. 이 효과는 참조 상태에서 excitations of 파괴를 고려 하 여 모델링할 수 있습니다. 비-동적 상관 관계는 wavefunction이 시스템에 대 한 질적 설명만을 얻기 위해 0 번째 order에서 두 개 이상의 구성으로 지배 될 때 발생 합니다.
이는 택배의 superposition에 대 한 것 이며 multireference wavefunction의 예입니다.

화학 라이브러리는 택배의 superposition로 multireference 문제에 대 한 0 번째 order wavefunction를 지정 하는 방법을 제공 합니다. 스파스 multireference wavefunctions를 호출 하는이 방법은 소수의 구성 요소만 superposition를 지정 하기에 충분 한 경우에 적용 됩니다. 또한 라이브러리는 일반화 된 단일 연결 클러스터 ansatz를 통해 단일 결정 참조의 위에 동적 상관 관계를 포함 하는 메서드를 제공 합니다. 또한 퀀텀 컴퓨터에서 이러한 상태를 생성 하는 퀀텀 회로를 생성 합니다. 이러한 상태는 [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)에 지정 될 수 있으며, 이러한 상태를 화학 라이브러리를 통해 수동으로 지정 하는 기능도 제공 합니다.

## <a name="sparse-multi-reference-wavefunction"></a>스파스 다중 참조 wavefunction
다중 참조 상태 $ \ket{\ psi_ {\rm {MCSCF}} $은 (는) $N $-전자 s 이후 determininants의 선형 조합으로 명시적으로 지정할 수 있습니다.
\begin{align} \ket{\ psi_ {\rm {MCSCF}}} \propto \ sum_ {i_1 < i_2 < \cit< i_N} \ lambda_ {i_1} i_2} a ^ \ i_N {dagger_} \cdpi a ^ \ i_1 {dagger_} \ket {0} .
예를 들어 \end{align}에 대 한 상태 $ \propto (0.1 a ^ \ dagger_1a ^ \ dagger_2a ^ \ dagger_6-0.2 a ^ \ dagger_2a ^ \ dagger_1a ^ \ dagger_5) \ket {0} $는 다음과 같이 화학 라이브러리에 지정할 수 있습니다.
```csharp
// Create a list of tuples where the first item of each 
// tuple are indices to the creation operators acting on the
// vacuum state, and the second item is the coefficient
// of that basis state.
var superposition = new[] {
    (new[] {1, 2, 6}, 0.1),
    (new[] {2, 1, 5}, -0.2) };

// Create a fermion wavefunction object that represents the superposition.
var wavefunction = new FermionWavefunction<int>(superposition);
```
Superposition 구성 요소에 대 한 명시적 표현은 몇 가지 구성 요소만 지정 해야 하는 경우에 적용 됩니다. 필요한 상태를 정확 하 게 캡처하기 위해 많은 구성 요소가 필요한 경우에는이 표현을 사용 하지 않아야 합니다. 그 이유는 퀀텀 컴퓨터에서이 상태를 준비 하는 퀀텀 회로의 게이트 비용으로, superposition 구성 요소 수와 최소의 quadratically, superposition amplitudes의 1-표준을 사용 하 여 최대의입니다.

## <a name="unitary-coupled-cluster-wavefunction"></a>단일 연결-클러스터 wavefunction
Chemistery library를 사용 하 여 단일 연결 클러스터 wavefunction $ \ket{\ psi_ {\rm {UCC}}}을 지정할 수도 있습니다. 이 경우, 예를 들어, $ \ket{\ psi_ {\rm{SCF}}} $와 같은 단일 결정 참조 상태가 있습니다. 그런 다음, 단일 연결 클러스터 wavefunction의 구성 요소는 참조 상태에서 작동 하는 단일 연산자를 통해 implicity 지정 됩니다.
이 단일 연산자는 일반적으로 $e ^ {T-T ^ \dagger} $로 작성 됩니다. 여기서 $T-T ^ \aaa $는 Hermitian 클러스터 연산자입니다. 따라서 \begin{align} \ket{\ psi_ {\rm {UCC}}} = e ^ {T-T ^ \dagger}\ket{\ psi_ {\rm{SCF}}}.
\end{align}

또한 클러스터 연산자 $T = T_1 + T_2 + \ci$를 부분으로 분할 하는 것이 일반적입니다 .이 경우 _j $에 $T $j $-body 용어가 포함 됩니다. 일반화 된 클러스터 이론에서 단일 (단일 본문 클러스터)는 \begin{align} T_1 = \ sum_ {pq} T ^ {p} _ {q} a ^ \ dagger_p a_q, \end{align} 형식입니다.

및 두 개의 본문 클러스터 연산자 (double)는 \begin{align} T_2 = \ sum_ {pqrs} T ^ {pq} _ {rs} a ^ \ dagger_p ^ \ dagger_q a_r a_s 형식입니다.
\end{align}

더 높은 주문 용어 (삼중 쌍, quadruples 등)는 가능 하지만 현재는 연금술 라이브러리에서 지원 되지 않습니다.

예를 들어 $ \ket{\ psi_ {\rm{SCF}}} = a ^ \ dagger_1 a ^ \ dagger_2 \ket {0} $를 사용 하 여 $T = 0.123 a ^ \ dagger_0 a_1 + 0.456 a ^ \ dagger_0a ^ \ dagger_3 a_1 a_2 dagger_3a-0.789 a ^ \ dagger_2 ^ \ a_1 a_0 $를 사용 합니다. 그러면 다음과 같이이 상태가 화학 라이브러리에서 인스턴스화됩니다.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { 1, 2 };

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {0, 1}, 0.123),
    (new [] {0, 3, 1, 2}, 0.456),
    (new [] {3, 2, 1, 0}, 0.789)
};

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunction = new FermionWavefunction<int>(reference, clusterOperator);
```

대신 `SpinOrbital` 정수 인덱스 대신 인덱스를 지정 하 여 Spin convervation을 명시적으로 만들 수 있습니다. 예를 들어 $ \ket{\ psi_ {\rm{SCF}}} = a ^ \ dagger_ {1, \uparrow} a ^ \ dagger_ {2, \downarrow}\ket {0} $ 및 let $T = 0.123 a ^ \ dagger_ {0을 사용할 수 있습니다. \uparrow} a_ {1, \uparrow} + 0.456 a ^ \ dagger_ {0, \uparrow} a ^ \ dagger_ {3, \downarrow} a_ {1, \uparrow} a_ {2, \downarrow}-0.789 a ^ \ dagger_ {3, \uparrow} a ^ \ dagger_ {2, \uparrow} a_ {1, \uparrow} a_ {0, \uparrow} $ be spin convserving. 그러면 다음과 같이이 상태가 화학 라이브러리에서 인스턴스화됩니다.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {(0, Spin.u), (1, Spin.u)}, 0.123),
    (new [] {(0, Spin.u), (3, Spin.d), (1, Spin.u), (2, Spin.d)}, 0.456),
    (new [] {(3, Spin.u), (2, Spin.u), (1, Spin.u), (0, Spin.u)}, 0.789)
}.Select(o => (o.Item1.ToSpinOrbitals(), o.Item2);

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(reference, clusterOperator);

// Convert the wavefunction indexed by spin-orbitals to one indexed
// by integers
var wavefunctionInteger = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

또한 annihilate는 모든 회전 대화를 열거 하는 편리한 함수를 제공 합니다 .이 연산자는 모든 spin-orbitals와 흥미만을 빈 spin-orbitals로만 제공 합니다.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Generate all spin-conversing excitations from spin-orbitals 
// occupied by the reference state to virtual orbitals.
var generatedExcitations = reference.CreateAllUCCSDSingletExcitations(nOrbitals: 3).Excitations;

// This is the list of expected spin-consvering excitations
var expectedExcitations = new[]
{
    new []{ (0, Spin.u), (1,Spin.u)},
    new []{ (2, Spin.u), (1,Spin.u)},
    new []{ (0, Spin.d), (2,Spin.d)},
    new []{ (1, Spin.d), (2,Spin.d)},
    new []{ (0, Spin.u), (0, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.u), (1, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)},
    new []{ (1, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)}
}.Select(o => new IndexOrderedSequence<SpinOrbital>(o.ToLadderSequence()));

// The following two assertions are true, and verify that the generated 
// excitations exactly match the expected excitations.
var bool0 = generatedExcitations.Keys.All(expectedExcitations.Contains);
var bool1 = generatedExcitations.Count() == expectedExcitations.Count();
```
