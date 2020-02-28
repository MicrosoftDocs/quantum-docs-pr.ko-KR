---
title: 상관 관계가 지정된 파동 함수
description: Microsoft 퀀텀 화학 라이브러리를 사용 하 여 wavefunctions의 동적 및 비동적 상관 관계에 대해 알아봅니다.
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.multireference
ms.openlocfilehash: 005ef86382ca72969b06a4206cab01f3845718e2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904437"
---
# <a name="correlated-wavefunctions"></a><span data-ttu-id="a9e8b-103">상관 관계가 지정된 파동 함수</span><span class="sxs-lookup"><span data-stu-id="a9e8b-103">Correlated wavefunctions</span></span>

<span data-ttu-id="a9e8b-104">특히 평형 기 하 도형 근처의 많은 시스템에서 [Hartree – Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) 이론은 단일 결정 참조 상태를 통해 분자 속성에 대 한 질적 설명을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-104">For many systems, particularly those near the equilibrium geometry, [Hartree–Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) theory provides a qualitative description of molecular properties through a single-determinant reference state.</span></span> <span data-ttu-id="a9e8b-105">그러나 양적 정확도를 얻기 위해 상관 관계 효과를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-105">However, in order to achieve quantitative accuracy, one must also consider correlation effects.</span></span> 

<span data-ttu-id="a9e8b-106">이 컨텍스트에서 동적 상관 관계와 동적이 지 않은 상관 관계 간에 dinstinguish 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-106">In this context, it is important to dinstinguish between dynamic and non-dynamic correlations.</span></span>
<span data-ttu-id="a9e8b-107">동적 상관 관계는 파괴의 추세에서 발생 하며, 예를 들어 interelectronic 반발력은 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-107">Dynamical correlations arise from the tendency of electrons to stay apart, such as due to interelectronic repulsion.</span></span> <span data-ttu-id="a9e8b-108">이 효과는 참조 상태에서 excitations of 파괴를 고려 하 여 모델링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-108">This effect can be modelled by considering excitations of electrons out of the reference state.</span></span> <span data-ttu-id="a9e8b-109">비-동적 상관 관계는 wavefunction이 시스템에 대 한 질적 설명만을 얻기 위해 0 번째 order에서 두 개 이상의 구성으로 지배 될 때 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-109">Non-dynamic correlations arise when the wavefunction is dominated by two or more configurations at zeroth order, even to achieve only a qualitative description of the system.</span></span>
<span data-ttu-id="a9e8b-110">이는 택배의 superposition에 대 한 것 이며 multireference wavefunction의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-110">This necessitates a superposition of determinants and is an example of a multireference wavefunction.</span></span>

<span data-ttu-id="a9e8b-111">화학 라이브러리는 택배의 superposition로 multireference 문제에 대 한 0 번째 order wavefunction를 지정 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-111">The chemistry library provides a way to specify a zeroth order wavefunction for the multireference problem as a superposition of determinants.</span></span> <span data-ttu-id="a9e8b-112">스파스 multireference wavefunctions를 호출 하는이 방법은 소수의 구성 요소만 superposition를 지정 하기에 충분 한 경우에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-112">This approach, which we call sparse multireference wavefunctions, is effective when only a few components suffice to specify the superposition.</span></span> <span data-ttu-id="a9e8b-113">또한 라이브러리는 일반화 된 단일 연결 클러스터 ansatz를 통해 단일 결정 참조의 위에 동적 상관 관계를 포함 하는 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-113">The library also provides a method to include dynamic correlations on top of a single-determinant reference via the generalized unitary coupled-cluster ansatz.</span></span> <span data-ttu-id="a9e8b-114">또한 퀀텀 컴퓨터에서 이러한 상태를 생성 하는 퀀텀 회로를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-114">Furthermore, it also constructs quantum circuits that generate these states on a quantum computer.</span></span> <span data-ttu-id="a9e8b-115">이러한 상태는 [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)에 지정 될 수 있으며, 이러한 상태를 화학 라이브러리를 통해 수동으로 지정 하는 기능도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-115">These states may be specified in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), and we also provide the functionality to manually specify these states through the chemistry library.</span></span>

## <a name="sparse-multi-reference-wavefunction"></a><span data-ttu-id="a9e8b-116">스파스 다중 참조 wavefunction</span><span class="sxs-lookup"><span data-stu-id="a9e8b-116">Sparse multi-reference wavefunction</span></span>
<span data-ttu-id="a9e8b-117">다중 참조 상태 $ \ket{\ psi_ {\rm {MCSCF}} $은 (는) $N $-전자 s 이후 determininants의 선형 조합으로 명시적으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-117">A multi-reference state $\ket{\psi_{\rm {MCSCF}}}$ may be specified explicitly as a linear combination of $N$-electron Slater determininants.</span></span>
<span data-ttu-id="a9e8b-118">\begin{align} \ket{\ psi_ {\rm {MCSCF}}} \propto \ sum_ {i_1 < i_2 < \cit< i_N} \ lambda_ {i_1} i_2} a ^ \ i_N {dagger_} \cdpi a ^ \ i_1 {dagger_} \ket i_2.{0}</span><span class="sxs-lookup"><span data-stu-id="a9e8b-118">\begin{align} \ket{\psi_{\rm {MCSCF}}} \propto \sum_{i_1 < i_2 < \cdots < i_N} \lambda_{i_1,i_2,\cdots,i_N} a^\dagger_{i_1}a^\dagger_{i_2}\cdots a^\dagger_{i_N}\ket{0}.</span></span>
<span data-ttu-id="a9e8b-119">예를 들어 \end{align}에 대 한 상태 $ \propto (0.1 a ^ \ dagger_1a ^ \ dagger_2a ^ \ dagger_6-0.2 a ^ \ dagger_2a ^ \ dagger_1a ^ \ dagger_5) \ket{0}$는 다음과 같이 연금술 라이브러리에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-119">\end{align} For example, the state $\propto(0.1 a^\dagger_1a^\dagger_2a^\dagger_6 - 0.2 a^\dagger_2a^\dagger_1a^\dagger_5)\ket{0}$ may be specified in the chemistry library as follows.</span></span>
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
<span data-ttu-id="a9e8b-120">Superposition 구성 요소에 대 한 명시적 표현은 몇 가지 구성 요소만 지정 해야 하는 경우에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-120">This explicit representation of the superposition components is effective when only a few components need to be specified.</span></span> <span data-ttu-id="a9e8b-121">필요한 상태를 정확 하 게 캡처하기 위해 많은 구성 요소가 필요한 경우에는이 표현을 사용 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-121">One should avoid using this representation when many components are required to accurately capture the desired state.</span></span> <span data-ttu-id="a9e8b-122">그 이유는 퀀텀 컴퓨터에서이 상태를 준비 하는 퀀텀 회로의 게이트 비용으로, superposition 구성 요소 수와 최소의 quadratically, superposition amplitudes의 1-표준을 사용 하 여 최대의입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-122">The reason for this is the gate cost of quantum circuit that prepares this state on a quantum computer, which scales at least linearly with the number of superposition components, and at most quadratically with the one-norm of the superposition amplitudes.</span></span>

## <a name="unitary-coupled-cluster-wavefunction"></a><span data-ttu-id="a9e8b-123">단일 연결-클러스터 wavefunction</span><span class="sxs-lookup"><span data-stu-id="a9e8b-123">Unitary coupled-cluster wavefunction</span></span>
<span data-ttu-id="a9e8b-124">Chemistery library를 사용 하 여 단일 연결 클러스터 wavefunction $ \ket{\ psi_ {\rm {UCC}}}을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-124">It is also possible to specify a unitary coupled-cluster wavefunction $\ket{\psi_{\rm {UCC}}}$ using the chemistery library.</span></span> <span data-ttu-id="a9e8b-125">이 경우, 예를 들어, $ \ket{\ psi_ {\rm{SCF}}} $와 같은 단일 결정 참조 상태가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-125">In this situation, we have a single-determinant reference state, say, $\ket{\psi_{\rm{SCF}}}$.</span></span> <span data-ttu-id="a9e8b-126">그런 다음, 단일 연결 클러스터 wavefunction의 구성 요소는 참조 상태에서 작동 하는 단일 연산자를 통해 implicity 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-126">The components of the unitary coupled-cluster wavefunction are then specified implicity through a unitary operator acting on a reference state.</span></span>
<span data-ttu-id="a9e8b-127">이 단일 연산자는 일반적으로 $e ^ {T-T ^ \dagger} $로 작성 됩니다. 여기서 $T-T ^ \aaa $는 Hermitian 클러스터 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-127">This unitary operator is commonly written as $e^{T-T^\dagger}$, where $T-T^\dagger$ is the anti-Hermitian cluster operator.</span></span> <span data-ttu-id="a9e8b-128">따라서 \begin{align} \ket{\ psi_ {\rm {UCC}}} = e ^ {T-T ^ \dagger}\ket{\ psi_ {\rm{SCF}}}.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-128">Thus \begin{align} \ket{\psi_{\rm {UCC}}} = e^{T-T^\dagger}\ket{\psi_{\rm{SCF}}}.</span></span>
<span data-ttu-id="a9e8b-129">\end{align}</span><span class="sxs-lookup"><span data-stu-id="a9e8b-129">\end{align}</span></span>

<span data-ttu-id="a9e8b-130">또한 클러스터 연산자 $T = T_1 + T_2 + \ci$를 부분으로 분할 하는 것이 일반적입니다 .이 경우 _j $에 $T $j $-body 용어가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-130">It is also common to split the cluster operator $T = T_1 + T_2 + \cdots$ into parts, where each part $T_j$ contains $j$-body terms.</span></span> <span data-ttu-id="a9e8b-131">일반화 된 클러스터 이론에서 단일 (단일 본문 클러스터)는 \begin{align} T_1 = \ sum_ {pq} T ^ {p} _ {q} a ^ \ dagger_p a_q, \end{align} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-131">In generalized coupled-cluster theory, the one-body cluster operator (singles) is of the form \begin{align} T_1 = \sum_{pq}t^{p}_{q} a^\dagger_p a_q, \end{align}</span></span>

<span data-ttu-id="a9e8b-132">및 두 개의 본문 클러스터 연산자 (double)는 \begin{align} T_2 = \ sum_ {pqrs} T ^ {pq} _ {rs} a ^ \ dagger_p ^ \ dagger_q a_r a_s 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-132">and two-body cluster operator (doubles) is of the form \begin{align} T_2 = \sum_{pqrs}t^{pq}_{rs} a^\dagger_p a^\dagger_q a_r a_s.</span></span>
<span data-ttu-id="a9e8b-133">\end{align}</span><span class="sxs-lookup"><span data-stu-id="a9e8b-133">\end{align}</span></span>

<span data-ttu-id="a9e8b-134">더 높은 주문 용어 (삼중 쌍, quadruples 등)는 가능 하지만 현재는 연금술 라이브러리에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-134">Higher-order terms (triples, quadruples, etc.) are possible, but not currently supported by the chemistry library.</span></span>

<span data-ttu-id="a9e8b-135">예를 들어 $ \ket{\ psi_ {\rm{SCF}}} = a ^ \ dagger_1 a ^ \ dagger_2 \ket{0}$를 사용 하 고 let $T = 0.123 a ^ \ dagger_0 a_1 + 0.456 a ^ \ dagger_0a ^ \ dagger_3 a_1 a_2 dagger_3a-0.789 a ^ \ dagger_2 ^ \ a_1 a_0 $를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-135">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_1 a^\dagger_2\ket{0}$, and let $T= 0.123 a^\dagger_0 a_1 + 0.456 a^\dagger_0a^\dagger_3 a_1 a_2 - 0.789 a^\dagger_3a^\dagger_2 a_1 a_0$.</span></span> <span data-ttu-id="a9e8b-136">그러면 다음과 같이이 상태가 화학 라이브러리에서 인스턴스화됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-136">Then this state is instantiated in the chemistry library as follows.</span></span>
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

<span data-ttu-id="a9e8b-137">대신 정수 인덱스 대신 `SpinOrbital` 인덱스를 지정 하 여 Spin convervation을 명시적으로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-137">Spin convervation may be made explicit by instead specifying `SpinOrbital` indices instead of integer indices.</span></span> <span data-ttu-id="a9e8b-138">예를 들어 $ \ket{\ psi_ {\rm{SCF}}} = a ^ \ dagger_ {1, \uparrow} a ^ \ dagger_ {2, \downarrow}\ket{0}$ 및 let $T = 0.123 a ^ \ dagger_ {0을 사용할 수 있습니다. \uparrow} a_ {1, \uparrow} + 0.456 a ^ \ dagger_ {0, \uparrow} a ^ \ dagger_ {3, \downarrow} a_ {1, \uparrow} a_ {2, \downarrow}-0.789 a ^ \ dagger_ {3, \uparrow} a ^ \ dagger_ {2, \uparrow} a_ {1, \uparrow} a_ {0, \uparrow} $ be spin convserving.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-138">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_{1,\uparrow} a^\dagger_{2, \downarrow}\ket{0}$, and let $T= 0.123 a^\dagger_{0, \uparrow} a_{1, \uparrow} + 0.456 a^\dagger_{0, \uparrow} a^\dagger_{3, \downarrow} a_{1, \uparrow} a_{2, \downarrow} - 0.789 a^\dagger_{3,\uparrow} a^\dagger_{2,\uparrow} a_{1,\uparrow} a_{0, \uparrow}$ be spin convserving.</span></span> <span data-ttu-id="a9e8b-139">그러면 다음과 같이이 상태가 화학 라이브러리에서 인스턴스화됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-139">Then this state is instantiated in the chemistry library as follows.</span></span>
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

<span data-ttu-id="a9e8b-140">또한 annihilate는 모든 회전 대화를 열거 하는 편리한 함수를 제공 합니다 .이 연산자는 모든 spin-orbitals와 흥미만을 빈 spin-orbitals로만 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8b-140">We also provide a convenience function that enumerates over all spin-conversing cluster operators that annihilate only occupied spin-orbitals and excite to only unoccupied spin-orbitals.</span></span>
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
