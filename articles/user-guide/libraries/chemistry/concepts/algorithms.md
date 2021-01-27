---
title: Hamiltonian Dynamics 시뮬레이션
description: Hamiltonian 시뮬레이션을 사용 하는 Trotter-Suzuki 수식 및 작업을 사용 하는 방법에 대해 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
no-loc:
- Q#
- $$v
ms.openlocfilehash: eeaa13b99ab07ce22f8a3306a756bf7ac7cde65b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857605"
---
# <a name="simulating-hamiltonian-dynamics"></a><span data-ttu-id="4969a-103">Hamiltonian Dynamics 시뮬레이션</span><span class="sxs-lookup"><span data-stu-id="4969a-103">Simulating Hamiltonian Dynamics</span></span>

<span data-ttu-id="4969a-104">Hamiltonian가 기본 연산자의 합계로 표시 된 후에는 잘 알려진 기술 호스트를 사용 하 여 기본 게이트 작업으로 dynamics를 컴파일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-104">Once the Hamiltonian has been expressed as a sum of elementary operators the dynamics can then be compiled into fundamental gate operations using a host of well-known techniques.</span></span>
<span data-ttu-id="4969a-105">Trotter – Suzuki 수식, unitaries의 선형 조합, 등 세 가지 효율적인 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-105">Three efficient approaches include are Trotter–Suzuki formulas, linear combinations of unitaries, and qubitization.</span></span>
<span data-ttu-id="4969a-106">이 세 가지 방법에 대해 설명 하 고 Q# Hamiltonian 시뮬레이션 라이브러리를 사용 하 여 이러한 메서드를 구현 하는 방법에 대 한 구체적인 예제를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-106">We explain these three approaches below and give concrete Q# examples of how to implement these methods using the Hamiltonian simulation library.</span></span>


## <a name="trottersuzuki-formulas"></a><span data-ttu-id="4969a-107">Trotter – Suzuki 수식</span><span class="sxs-lookup"><span data-stu-id="4969a-107">Trotter–Suzuki Formulas</span></span>
<span data-ttu-id="4969a-108">Trotter – Suzuki 수식의 개념은 간단 합니다. 즉, Hamiltonian를 시뮬레이션을 위한 합계로 표현 하 고, 총 진화를 이러한 간단한 evolutions의 시퀀스로 대략적으로 표현 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-108">The idea behind Trotter–Suzuki formulas is simple: express the Hamiltonian as a sum of easy to simulate Hamiltonians and then approximate the total evolution as a sequence of these simpler evolutions.</span></span>
<span data-ttu-id="4969a-109">특히 $H = \ sum_ {j = 1} ^ m H_j $를 사용 하 여 Hamiltonian 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-109">In particular, let $H=\sum_{j=1}^m H_j$ be the Hamiltonian.</span></span>
<span data-ttu-id="4969a-110">그런 다음 $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \ prod_ {j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $이는 $t \ll $1 인 경우이 근사값의 오류는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-110">Then, $$ e^{-i\sum_{j=1}^m H_j t} =\prod_{j=1}^m e^{-iH_j t} + O(m^2 t^2), $$ which is to say that, if $t\ll 1$, then the error in this approximation becomes negligible.</span></span>
<span data-ttu-id="4969a-111">$E ^ {-i H t} $가 일반 지 수 인 경우이 근사값의 오류는 $O 되지 않습니다 (m ^ 2 t ^ 2) $: 0입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-111">Note that if $e^{-i H t}$ were an ordinary exponential then the error in this approximation would not be $O(m^2 t^2)$: it would be zero.</span></span>
<span data-ttu-id="4969a-112">이 오류는 $e ^ {-iHt} $이 (가) 연산자 지 수이 고 $H _j $ 용어가 commute (예 *:*$H _j H_k \ne H_k H_j $) 때문에이 수식을 사용할 때 오류가 발생 하는 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-112">This error occurs because $e^{-iHt}$ is an operator exponential and as a result there is an error incurred when using this formula due to the fact that the $H_j$ terms do not commute (*i.e.*, $H_j H_k \ne H_k H_j$ in general).</span></span>

<span data-ttu-id="4969a-113">$T $가 큰 경우에는 Trotter – Suzuki 수식을 사용 하 여 간단한 시간 단계 시퀀스로 분리 하 여 dynamics를 정확 하 게 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-113">If $t$ is large, Trotter–Suzuki formulas can still be used to simulate the dynamics accurately by breaking it up into a sequence of short time-steps.</span></span>
<span data-ttu-id="4969a-114">$R $를 사용 하 여 진행 시간에서 수행 되는 단계 수를 지정 합니다. 따라서 각 시간 단계는 시간 $t/r $로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-114">Let $r$ be the number of steps taken in the time evolution, so each time step runs for time $t/r$.</span></span> <span data-ttu-id="4969a-115">그런 다음 $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \left (\ prod_ {j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r)를 사용할 수 있습니다. $ $-$가 $m ^ 2 t ^ 2/\ 엡실론 $로 확장 하는 경우 $ \left>$0에 대 한 최대 $ \left $로 오류를 만들 수 있음을 의미 합니다. $r</span><span class="sxs-lookup"><span data-stu-id="4969a-115">Then, we have that $$ e^{-i\sum_{j=1}^m H_j t} =\left(\prod_{j=1}^m e^{-iH_j t/r}\right)^r + O(m^2 t^2/r), $$ which implies that if $r$ scales as $m^2 t^2/\epsilon$ then the error can be made at most $\epsilon$ for any $\epsilon>0$.</span></span>

<span data-ttu-id="4969a-116">오류 용어가 취소 되는 연산자 지 수 시퀀스를 구성 하 여 보다 정확한 근사치을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-116">More accurate approximations can be built by constructing a sequence of operator exponentials such that the error terms cancel.</span></span>
<span data-ttu-id="4969a-117">가장 간단한 수식, 두 번째 order Trotter-Suzuki 수식, $ $ U_2 (t) = \left (\ prod_ {j = 1} ^ {m} e ^ {-iH_j t/2r} \ prod_ {j = m} 형식으로 사용 합니다. ^ 1 e ^ {iH_j t/2r} \ right) ^ r = e ^ {-iHt} + O (m ^ 3 t ^ 3/r ^ 2), $ $ x = ^ {3/2} t ^ {3/2}/\sqrt {\ 엡실론} $로 크기를 조정 하려면 $r $를 선택 하 여 $ \left>$0에 대해 $ \left $ 보다 작은 값을 만들 수 있습니다. $m</span><span class="sxs-lookup"><span data-stu-id="4969a-117">The simplest such formula, the second order Trotter-Suzuki formula, takes the form $$ U_2(t) = \left(\prod_{j=1}^{m} e^{-iH_j t/2r} \prod_{j=m}^1 e^{-iH_j t/2r}\right)^r = e^{-iHt} + O(m^3 t^3/r^2), $$ the error of which can be made less than $\epsilon$ for any $\epsilon>0$ by choosing $r$ to scale as $m^{3/2}t^{3/2}/\sqrt{\epsilon}$.</span></span>

<span data-ttu-id="4969a-118">보다 고차 수식, 특히 ($ 2k $) $k>$0에 대 한 순서를 재귀적으로 생성할 수 있습니다. $ $ U_ {2k} (t) = [U_ {2k-2} (s_k \~ t)] ^ 2 U_ {2k-2} ([1-4s_k] t) [U_ {2k-2} (s_k \~ t)] ^ 2 = e ^ {-iht} + O ((m) ^ {2k + 1}/r ^ {2k}), $ $ where $s _k = (4-4 ^ {1/(2k-1)}) ^ {-1} $.</span><span class="sxs-lookup"><span data-stu-id="4969a-118">Even higher-order formulas, specifically ($2k$)th-order for $k>0$, can be constructed recursively: $$ U_{2k}(t) = [U_{2k-2}(s_k\~ t)]^2 U_{2k-2}([1-4s_k]t) [U_{2k-2}(s_k\~ t)]^2 = e^{-iHt} + O((m t)^{2k+1}/r^{2k}), $$ where $s_k = (4-4^{1/(2k-1)})^{-1}$.</span></span>

<span data-ttu-id="4969a-119">가장 간단한 방법은 Suzuki에서 처음으로 도입 된 다음 네 번째 순서 ($k = $2) 수식입니다. $ $ U_4 (t) = [U_2 (s_2 \~ t)] ^ 2 U_2 ([1-4s_2] t) [U_2 (s_2 \~ t)] ^ 2 = e ^ {-iht} + O (m ^ 5t ^ 5/r ^ 4), $ $ where $s _2 = (4-4 ^ {1/3}) ^ {-1} $.</span><span class="sxs-lookup"><span data-stu-id="4969a-119">The simplest is the following fourth order ($k=2$) formula, originally introduced by Suzuki: $$ U_4(t) = [U_2(s_2\~ t)]^2 U_2([1-4s_2]t) [U_2(s_2\~ t)]^2 = e^{-iHt} +O(m^5t^5/r^4), $$ where $s_2 = (4-4^{1/3})^{-1}$.</span></span>
<span data-ttu-id="4969a-120">일반적으로는 임의의 상위 수식이 비슷하게 생성 될 수 있습니다. 그러나 더 복잡 한 통합자를 사용 하 여 발생 하는 비용은 대부분의 실질적인 문제에 대 한 네 번째 순서의 이점 보다 더 큽니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-120">In general, arbitrarily high-order formulas can be similarly constructed; however, the costs incurred from using more complex integrators often outweigh the benefits beyond fourth order for most practical problems.</span></span>

<span data-ttu-id="4969a-121">위의 전략이 작동 하려면 $e ^ {iH_j t} $의 광범위 한 클래스를 시뮬레이트하는 메서드가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-121">In order to make the above strategies work, we need to have a method for simulating a wide class of $e^{-iH_j t}$.</span></span>
<span data-ttu-id="4969a-122">여기에서 사용할 수 있는 가장 간단한 Hamiltonians 패밀리는 Pauli 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-122">The simplest family of Hamiltonians, and arguably most useful, that we could use here are Pauli operators.</span></span>
<span data-ttu-id="4969a-123">Pauli 연산자는 Clifford 작업 (양자 컴퓨팅의 표준 게이트)을 사용 하 여 diagonalized 수 있으므로 쉽게 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-123">Pauli operators can be easily simulated because they can be diagonalized using Clifford operations (which are standard gates in quantum computing).</span></span>
<span data-ttu-id="4969a-124">또한 diagonalized 된 후에는 해당 고유 값가 작동 하는 eibits의 패리티를 계산 하 여 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-124">Further, once they have been diagonalized, their eigenvalues can be found by computing the parity of the qubits on which they act.</span></span>

<span data-ttu-id="4969a-125">예를 들어 $ $ e ^ {-iX\otimes X t} = (H\otimes H) e ^ {-iZ\otimes Z t} (H\otimes H), $ $ where $ $ e ^ {-i Z Z \otimes Z t} = \begin{bmatrix} e ^ {-it} & 0 & 0 & 0 </span><span class="sxs-lookup"><span data-stu-id="4969a-125">For example, $$ e^{-iX\otimes X t}= (H\otimes H)e^{-iZ\otimes Z t}(H\otimes H), $$ where $$ e^{-i Z \otimes Z t} = \begin{bmatrix} e^{-it} & 0  & 0  & 0 </span></span>\\\
        <span data-ttu-id="4969a-126">0 & e ^ {i t} & 0 & 0 </span><span class="sxs-lookup"><span data-stu-id="4969a-126">0 & e^{i t}  & 0 & 0 </span></span>\\\
        <span data-ttu-id="4969a-127">0 & 0 & e ^ {it} & 0 </span><span class="sxs-lookup"><span data-stu-id="4969a-127">0 & 0 & e^{it} & 0 </span></span>\\\
        <span data-ttu-id="4969a-128">0 & 0 & 0 & e ^ {-it} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="4969a-128">0 & 0 & 0 & e^{-it} \end{bmatrix}.</span></span>
<span data-ttu-id="4969a-129">$ $ 여기에서 $e ^ {-iHt} \ket {00} = e ^ {it} \ket {00} $ 및 $e ^ {-iht} \ket {01} = e ^ {-it} \ket {01} $를 사용할 수 있습니다 .이는 $0 $의 패리티는 $0 $이 고 비트 문자열 $1 $는 $1 $입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-129">$$ Here, $e^{-iHt} \ket{00} = e^{it} \ket{00}$ and $e^{-iHt} \ket{01} = e^{-it} \ket{01}$, which can be seen directly as a consequence of the fact that the parity of $00$ is $0$ while the parity of the bit string $01$ is $1$.</span></span>

<span data-ttu-id="4969a-130">Q#다음 작업을 사용 하 여 직접 지 수 Pauli 연산자를 구현할 수 있습니다 <xref:Microsoft.Quantum.Intrinsic.Exp> .</span><span class="sxs-lookup"><span data-stu-id="4969a-130">Exponentials of Pauli operators can be implemented directly in Q# using the <xref:Microsoft.Quantum.Intrinsic.Exp> operation:</span></span>
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies 𝑒^{- 𝑖 𝑋⊗𝑋 𝑡} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

<span data-ttu-id="4969a-131">Fermionic Hamiltonians의 경우 [요르단 – Wigner 분해](xref:microsoft.quantum.chemistry.concepts.jordanwigner) 는 Hamiltonian를 Pauli 연산자의 합계에 편리 하 게 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-131">For Fermionic Hamiltonians, the [Jordan–Wigner decomposition](xref:microsoft.quantum.chemistry.concepts.jordanwigner) conveniently maps the Hamiltonian into a sum of Pauli operators.</span></span>
<span data-ttu-id="4969a-132">즉, 위와 같은 방법으로 화학 시뮬레이션을 쉽게 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-132">This means that the above approach can easily be adapted to simulating chemistry.</span></span>
<span data-ttu-id="4969a-133">Jordan-Wigner 표현의 모든 Pauli를 수동으로 반복 하는 대신, 다음은 연금술 내에서 이러한 시뮬레이션을 실행 하는 방법을 보여 주는 간단한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-133">Rather than manually looping over all Pauli terms in the Jordan-Wigner representation, below is a simple example of how running such a simulation within the chemistry would look.</span></span>
<span data-ttu-id="4969a-134">시작 지점은 코드에서 클래스의 인스턴스로 표시 되는 Fermionic Hamiltonian의 [요르단 – Wigner 인코딩입니다](xref:microsoft.quantum.chemistry.concepts.jordanwigner) `JordanWignerEncoding` .</span><span class="sxs-lookup"><span data-stu-id="4969a-134">Our starting point is a [Jordan–Wigner encoding](xref:microsoft.quantum.chemistry.concepts.jordanwigner) of the Fermionic Hamiltonian, expressed in code as an instance of the `JordanWignerEncoding` class.</span></span>

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

<span data-ttu-id="4969a-135">시뮬레이션 알고리즘에서 사용할 수 있는 요르단 – Wigner 표현의 형식은 Q# 사용자 정의 형식입니다 `JordanWignerEncodingData` .</span><span class="sxs-lookup"><span data-stu-id="4969a-135">This format of the Jordan–Wigner representation that is consumable by the Q# simulation algorithms is a user-defined type `JordanWignerEncodingData`.</span></span>
<span data-ttu-id="4969a-136">내에서 Q# 이 형식은 `TrotterStepOracle` Trotter-Suzuki 통합자를 사용 하 여 실행에 필요한 다른 매개 변수와 함께 시간 진화를 사용 하는 연산자를 반환 하는 편의 함수에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-136">Within Q#, this format is passed to a convenience function `TrotterStepOracle` that returns an operator approximating time-evolution using the Trotter—Suzuki integrator, in addition to other parameters required for its run.</span></span>

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

<span data-ttu-id="4969a-137">중요 한 점은이 구현은 [퀀텀 컴퓨터를 사용 하 여 전자 구조 Hamiltonians의 시뮬레이션](https://arxiv.org/abs/1001.3855) 에 설명 된 몇 가지 최적화를 적용 하며, 필요한 단일 비트 회전 수를 최소화 하 고 시뮬레이션 오류를 줄이는 데 퀀텀 [에 대 한 퀀텀 알고리즘을 개선](https://arxiv.org/abs/1403.1539) 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-137">Importantly, this implementation applies some optimizations discussed in [Simulation of Electronic Structure Hamiltonians Using Quantum Computers](https://arxiv.org/abs/1001.3855) and [Improving Quantum Algorithms for Quantum Chemistry](https://arxiv.org/abs/1403.1539) to minimize the number of single-qubit rotations required, as well as reduce simulation errors.</span></span>

## <a name="qubitization"></a><span data-ttu-id="4969a-138">고 비트</span><span class="sxs-lookup"><span data-stu-id="4969a-138">Qubitization</span></span>

<span data-ttu-id="4969a-139">이는 퀀텀 워크의 아이디어를 사용 하 여 퀀텀 dynamics를 시뮬레이트하는 다른 시뮬레이션 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-139">Qubitization is an alternative approach to simulation that uses ideas from quantum walks to simulate quantum dynamics.</span></span>
<span data-ttu-id="4969a-140">Trotter 수식 보다 더 많은 비트를 필요로 하는 반면,이 메서드는 진화 시간 및 오류 허용 오차를 사용 하 여 최적의 확장을 약속 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-140">While qubitization requires more qubits than Trotter formulas, the method promises optimal scaling with the evolution time and the error tolerance.</span></span>
<span data-ttu-id="4969a-141">이러한 이유로, 일반적으로 Hamiltonian dynamics를 시뮬레이션 하 고 특히 전자 구조 문제를 해결 하기 위한 선호 하는 방법이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-141">For these reasons it has become a favored method for simulating Hamiltonian dynamics in general, and for solving the electronic structure problem in particular.</span></span>

<span data-ttu-id="4969a-142">높은 수준에서 다음과 같은 단계를 통해이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-142">At a high level, qubitization accomplishes this through the following steps.</span></span>
<span data-ttu-id="4969a-143">첫째, $H = \ sum_j h_j H_j $ (단일 및 Hermitian $H _j $ 및 $h _j \ge $0)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-143">First, let $H=\sum_j h_j H_j$ for unitary and Hermitian $H_j$ and $h_j\ge 0$.</span></span>
<span data-ttu-id="4969a-144">한 쌍의 반사를 수행 하 여 stbitsourceis $ $W = e ^ {\pm i \pm ^ {-1} (H/| h | _1)}, $ $ where $ | H | _1 = \ sum_j | h_j | $에 해당 하는 연산자를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-144">By performing a pair of reflections, qubitization implements an operator that is equivalent to $$W=e^{\pm i \cos^{-1}(H/|h|_1)},$$ where $|h|_1 = \sum_j |h_j|$.</span></span>
<span data-ttu-id="4969a-145">다음 단계에서는 $e ^ {i\pm \cos ^ {-1} (E_k/| h | _1)} $에서 연습 연산자의 고유 값를 변환 합니다. 여기서 $E _k $은 $H $ to $e ^ {-iE_k t} $의 고유 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-145">The next step involves transforming the eigenvalues of the walk operator from $e^{i\pm \cos^{-1}(E_k/|h|_1)}$, where $E_k$ are the eigenvalues of $H$ to $e^{-iE_k t}$.</span></span>
<span data-ttu-id="4969a-146">이는 [퀀텀 신호 처리](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501)를 포함 하 여 다양 한 퀀텀 단일 값 변환 방법을 사용 하 여 달성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-146">This can be achieved using a variety of quantum singular value transformation methods including [quantum signal processing](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).</span></span>

<span data-ttu-id="4969a-147">또는 정적 수량 (예: Hamiltonian의 그라운드 상태 에너지)만 필요한 경우에는 결과의 코사인을 수행 하 여 결과에서 그라운드 상태 에너지를 추정 하기 위해 [단계 예측](xref:microsoft.quantum.libraries.characterization) 을 $W $에 직접 적용 접미사 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-147">Alternatively, if only static quantities are desired (such as the ground state energy of the Hamiltonian) then it suffices to apply [phase estimation](xref:microsoft.quantum.libraries.characterization) directly to $W$ to estimate the ground state energy from the result by taking the cosine of the result.</span></span>
<span data-ttu-id="4969a-148">이는 퀀텀 단수형 value 변환 메서드를 사용 하는 대신 spectral 변환을 일반적으로 수행할 수 있도록 하기 때문에 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-148">This is significant because it allows the spectral transformation to be performed classically rather than using a quantum singular value transformation method.</span></span>

<span data-ttu-id="4969a-149">좀 더 자세한 수준에서 구현 하려면 Hamiltonian에 대 한 인터페이스를 제공 하는 두 개의 서브루틴이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-149">On a more detailed level, the implementation of qubitization requires two subroutines that provide the interfaces for the Hamiltonian.</span></span>
<span data-ttu-id="4969a-150">Trotter – Suzuki 메서드와 달리 이러한 서브루틴은 기존이 아닌 양자 이며 구현에는 Trotter 기반 시뮬레이션에 필요한 것 보다 더 많은 로그를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-150">Unlike Trotter–Suzuki methods, these subroutines are quantum not classical and their implementation will necessitate using logarithmically more qubits than would be required for a Trotter-based simulation.</span></span>

<span data-ttu-id="4969a-151">\Operatorname{Select}를 사용 하는 첫 번째 퀀텀 서브루틴은 $ \operatorname{Select} $ 라고 하며, 각 $H _j $이 \Ket{j} 및 단일 것으로 간주 되는 \begin{c} \ket{j} \ket{\psi} = \ket{\psi} H_j Hermitian</span><span class="sxs-lookup"><span data-stu-id="4969a-151">The first quantum subroutine that qubitization uses is called $\operatorname{Select}$ and it is promised to yield \begin{equation} \operatorname{Select} \ket{j} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{equation} where each $H_j$ is assumed to be Hermitian and unitary.</span></span>
<span data-ttu-id="4969a-152">이는 제한적이 지 않은 것 처럼 보일 수 있지만, Pauli 연산자는 Hermitian 및 단일 이며, 따라서 퀀텀 화학 시뮬레이션 같은 응용 프로그램은이 프레임 워크에 자연스럽 게 속합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-152">While this may seem to be restrictive, recall that Pauli operators are Hermitian and unitary and so applications like quantum chemistry simulation naturally fall into this framework.</span></span>
<span data-ttu-id="4969a-153">$ \Operatorname{Select} $ 연산은 실제로 리플렉션 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-153">The $\operatorname{Select}$ operation, perhaps surprisingly, is actually a reflection operation.</span></span>
<span data-ttu-id="4969a-154">$ \Operatorname{Select} ^ 2 \ k {j} \ket{\psi} = \ket{j} \ket{\psi} $는 각 $H _j $가 단일 및 Hermitian 이므로 고유 값 $ \pm $1을 포함 하기 때문에이를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-154">This can be seen from the fact that $\operatorname{Select}^2\ket{j} \ket{\psi} = \ket{j} \ket{\psi}$ since each $H_j$ is unitary and Hermitian and thus has eigenvalues $\pm 1$.</span></span>

<span data-ttu-id="4969a-155">두 번째 서브루틴을 $ \operatorname{Prepare} $ 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-155">The second subroutine is called $\operatorname{Prepare}$.</span></span>
<span data-ttu-id="4969a-156">Select 작업은 각 Hamiltonian 약관 $H에 대 한 액세스를 제공 하는 수단을 제공 하지만 _j $ 준비 서브루틴은 _j $, \begin{equation} \operatorname{Prepare}\ket {0} = \ sum_j \sqrt{\frac{h_j} {| H | _1}} \ket{j}.에 $h 액세스 하기 위한 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-156">While the select operation provides a means to coherently access each of the Hamiltonian terms $H_j$ the prepare subroutine gives a method for accessing the coefficients $h_j$, \begin{equation} \operatorname{Prepare}\ket{0} = \sum_j \sqrt{\frac{h_j}{|h|_1}}\ket{j}.</span></span>
<span data-ttu-id="4969a-157">\end{equation} 다음에는 곱하기 제어 단계 게이트를 사용 하 여 $ $ \Lambda\ket {0} ^ {\otimes n} = \begin{cases} \- \ket{x} & \text{if} x = 0이 표시 됩니다. </span><span class="sxs-lookup"><span data-stu-id="4969a-157">\end{equation} Then, by using a multiply controlled phase gate, we see that $$ \Lambda\ket{0}^{\otimes n} = \begin{cases} \-\ket{x} & \text{if } x = 0 </span></span>\\\
        <span data-ttu-id="4969a-158">\ket{x} & \text{otherwise} \end{cases}.</span><span class="sxs-lookup"><span data-stu-id="4969a-158">\ket{x}   & \text{otherwise} \end{cases}.</span></span>
$$

<span data-ttu-id="4969a-159">$ \Operatorname{Prepare} $ 작업은 stbitsource에서 직접 사용 되지 않지만 $ \operatorname{Prepare} $에서 $ $ \begin{align} R &amp; = 1-2 \ a m e {Prepare} \ket {0} \bra \operatorname{Prepare} {0} ^ {-1} \\ \\ &amp; = \operatorname{Prepare} \lambda \operatorname{Prepare} ^ {-1} 을 만드는 상태에 대 한 리플렉션을 구현 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-159">The $\operatorname{Prepare}$ operation is not used directly in qubitization, but rather is used to implement a reflection about the state that $\operatorname{Prepare}$ creates $$ \begin{align} R &amp; = 1 - 2\operatorname{Prepare} \ket{0}\bra{0} \operatorname{Prepare}^{-1} \\\\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare}^{-1}.</span></span>
<span data-ttu-id="4969a-160">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="4969a-160">\end{align} $$</span></span>

<span data-ttu-id="4969a-161">$ \Operatorname{Select} $ 및 $R $ 작업을 $ $ W = \operatorname{Select} R, $ $로 설명 하는 연습 연산자 ($W $)를 사용 하 여 $ $ W = R, $ $으로 지정할 수 있습니다. 즉, ^ {\pm i \pm ^ {-1} (H/| h | _1)} $를 $e 하는 것과 동일한 연산자 (최대 isometry)를 구현 하</span><span class="sxs-lookup"><span data-stu-id="4969a-161">The walk operator, $W$, can be expressed in terms of the $\operatorname{Select}$ and $R$ operations as $$ W = \operatorname{Select} R, $$ which again can be seen to implement an operator that is equivalent (up to an isometry) to $e^{\pm i \cos^{-1}(H/|h|_1)}$.</span></span>

<span data-ttu-id="4969a-162">이러한 서브루틴은에서 쉽게 설정할 수 Q# 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-162">These subroutines are easy to set up in Q#.</span></span>
<span data-ttu-id="4969a-163">예를 들어 단순 Ising Hamiltonian $H = X_1 + X_2 + Z_1 Z_2 $를 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-163">As an example, consider the simple qubit transverse-Ising Hamiltonian where $H = X_1 + X_2 + Z_1 Z_2$.</span></span>
<span data-ttu-id="4969a-164">이 경우 $ Q# \operatorname{Select} $ 작업을 구현 하는 코드는에 의해 호출 되는 <xref:Microsoft.Quantum.Canon.MultiplexOperations> 반면 $ \operatorname{Prepare} $ 작업은를 사용 하 여 구현할 수 있습니다 <xref:Microsoft.Quantum.Preparation.PrepareArbitraryState> .</span><span class="sxs-lookup"><span data-stu-id="4969a-164">In this case, Q# code that would implement the $\operatorname{Select}$ operation is invoked by <xref:Microsoft.Quantum.Canon.MultiplexOperations>, whereas the $\operatorname{Prepare}$ operation can be implemented using <xref:Microsoft.Quantum.Preparation.PrepareArbitraryState>.</span></span>
<span data-ttu-id="4969a-165">Hubbard 모델 시뮬레이션을 포함 하는 예제는 [ Q# 샘플](https://github.com/microsoft/Quantum/tree/main/samples/simulation/hubbard)로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-165">An example that involves simulating the Hubbard model can be found as a [Q# sample](https://github.com/microsoft/Quantum/tree/main/samples/simulation/hubbard).</span></span>

<span data-ttu-id="4969a-166">임의 화학 문제에 대해 이러한 단계를 수동으로 지정 하려면 화학 라이브러리를 사용 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-166">Manually specifying these steps for arbitrary chemistry problems would require much effort, which is avoided using the chemistry library.</span></span>
<span data-ttu-id="4969a-167">위의 Trotter – Suzuki 시뮬레이션 알고리즘과 마찬가지로는 `JordanWignerEncodingData` `QubitizationOracle` 해당 실행에 필요한 다른 매개 변수와 함께을 반환 하는 편의 함수에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-167">Similarly to the Trotter–Suzuki simulation algorithm above, the `JordanWignerEncodingData` is passed to the convenience function `QubitizationOracle` that returns the walk-operator, in addition to other parameters required for its run.</span></span>

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

<span data-ttu-id="4969a-168">중요 하 게 구현은 <xref:Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle> Pauli 문자열의 선형 조합으로 지정 된 임의의 Hamiltonians에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-168">Importantly, the implementation <xref:Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle> is applicable to arbitrary Hamiltonians specified as a linear combination of Pauli strings.</span></span>
<span data-ttu-id="4969a-169">화학 시뮬레이션에 최적화 된 버전은를 사용 하 여 호출 됩니다 <xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle> .</span><span class="sxs-lookup"><span data-stu-id="4969a-169">A version optimized for chemistry simulations is invoked using <xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle>.</span></span>
<span data-ttu-id="4969a-170">이 버전은 [선형 t 복잡성을 사용 하 여 퀀텀 회로의 전자 Spectra Encoding](https://arxiv.org/abs/1805.03662)에 설명 된 기술을 사용 하 여 T 게이트 수를 최소화 하도록 최적화 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4969a-170">This version is optimized to minimize the number of T gates using techniques discussed in [Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity](https://arxiv.org/abs/1805.03662).</span></span>
