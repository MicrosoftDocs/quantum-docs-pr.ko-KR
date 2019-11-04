---
title: Hartree-Fock 이론 | Microsoft Docs
description: Hartree-Fock 이론 문서
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
ms.openlocfilehash: e73111ae710e11ca6730581b8be711cf32783677
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184103"
---
# <a name="hartreefock-theory"></a><span data-ttu-id="51bf8-103">Hartree – Fock 이론</span><span class="sxs-lookup"><span data-stu-id="51bf8-103">Hartree–Fock Theory</span></span>

<span data-ttu-id="51bf8-104">아마도 퀀텀 연금술 시뮬레이션에서 가장 중요 한 수량은 Hamiltonian 행렬의 최소 에너지 eigenvector 인 그라운드 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-104">Perhaps the most important quantity in quantum chemistry simulation is the ground state, which is the minimum energy eigenvector of the Hamiltonian matrix.</span></span>
<span data-ttu-id="51bf8-105">이는 반응 경로에서 단계의 시작과 끝을 설명 하는 퀀텀 상태와 중간의 실내 온도에 대 한 퀀텀 상태 간의 무료 에너지 차이로 인해 반응 율이 molecules는 것입니다. 상태는 일반적으로 접지 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-105">This is because for most molecules at room temperature quantities such as reaction rates are dominated by free energy differences between quantum states that describe the beginning and end of a step in a reaction pathway and at room temperature such intermediate state are usually ground states.</span></span>
<span data-ttu-id="51bf8-106">일반적으로는 상당한 수의 구성에 대 한 배포 이기 때문에 일반적으로는 일반적으로 어려움 (퀀텀 컴퓨터 에서도)을 학습할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-106">While the ground state is typically too hard to learn (even with a quantum computer) because it is a distribution over an exponentially large number of configurations.</span></span>
<span data-ttu-id="51bf8-107">접지 상태 에너지와 같은 수량은 학습 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-107">Quantities such as ground state energy can be learned.</span></span>
<span data-ttu-id="51bf8-108">예를 들어 $ \ket{\psi} $이 순수 퀀텀 상태 이면 \begin{equation} E = \bra{\psi} \hat{H} \ket{\psi} \begin{equation}는 시스템의 해당 상태에 있는 평균 에너지를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-108">For example, if $\ket{\psi}$ is any pure quantum state then \begin{equation} E = \bra{ \psi } \hat{H} \ket{\psi} \end{equation} gives the mean energy that the system has in that state.</span></span>
<span data-ttu-id="51bf8-109">그런 다음 해당 값을 가장 작은 값으로 제공 하는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-109">The ground state then is the state that gives the smallest such value.</span></span> <span data-ttu-id="51bf8-110">결과적으로, 진정한 접지 상태와 최대한 가까운 상태를 선택 하는 것은 에너지를 직접 (variational eigensolvers에서 수행 되는 경우) 또는 단계 예측을 통해 예측 하는 데 매우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-110">As a result, choosing a state that is as close as possible to the true ground state is vitally important for estimating the energy either directly (as is done in variational eigensolvers) or through phase estimation.</span></span>

<span data-ttu-id="51bf8-111">Hartree – Fock 이론은 퀀텀 시스템의 초기 상태를 구성 하는 간단한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-111">Hartree–Fock theory gives a simple way to construct the initial state for quantum systems.</span></span> <span data-ttu-id="51bf8-112">양자는 퀀텀 시스템의 그라운드 상태에 대 한 단일 Slater 결정 근사값을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-112">It yields a single Slater-determinant approximation to the ground state of a quantum system.</span></span> <span data-ttu-id="51bf8-113">이를 위해 그라운드 상태 에너지를 최소화 하는 Fock 공간 내에서 회전을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-113">To that end, it finds a rotation within Fock-space that minimizes the ground state energy.</span></span> <span data-ttu-id="51bf8-114">특히, $N $ 파괴 시스템의 경우이 메서드는 회전을 수행 합니다. \begin{equation} \prod_{j = 0} ^ {N-1} a ^ \dagger_j \ket{0} \maps\prod_{j = 0} ^ {N-1} e ^ {u} a ^ \dagger_j e ^ {-u} \ket{0}\defeq\prod_{j = 0} ^ {N-1} \widetilde{a} ^ \ _j \ket{0}, \end{equation} Hermitian (예: $u =-u ^ \pq $) matrix $u = \sum_{pq} u_ {\dagger_p} a ^ a_q $.</span><span class="sxs-lookup"><span data-stu-id="51bf8-114">In particular, for a system of $N$ electrons the method performs the rotation \begin{equation} \prod_{j=0}^{N-1} a^\dagger_j \ket{0} \mapsto \prod_{j=0}^{N-1} e^{u} a^\dagger_j e^{-u} \ket{0}\defeq\prod_{j=0}^{N-1}  \widetilde{a}^\dagger_j  \ket{0}, \end{equation} with an anti-Hermitian (i.e. $u= -u^\dagger$) matrix $u = \sum_{pq} u_{pq} a^\dagger_p a_q$.</span></span> <span data-ttu-id="51bf8-115">행렬 $u $는 궤도 회전을 나타내고 $ \widetilde{a} ^ \dagger_j $ 및 $ \widetilde{a}_j $는 파괴을 차지 하는 Hartree에 대 한 만들기 및 annihilation 연산자를 나타냄 Fock – 분자 spin-orbitals로 표시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-115">It should be noted that the matrix $u$ represents the orbital rotations and $\widetilde{a}^\dagger_j$ and $\widetilde{a}_j$ represent creation and annihilation operators for electrons occupying Hartree–Fock molecular spin-orbitals.</span></span>


<span data-ttu-id="51bf8-116">행렬 $u $는 예상 되는 에너지 $ \bra{0} \prod_{j = 0} ^ {N-1} \widetilde{a}\_j H \prod\_{k = 0} ^ {N-1} \widetilde{a} ^ \dagger_k\ket{0}$를 최소화 하도록 최적화 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-116">The matrix $u$ is then optimized to minimize the expected energy $\bra{0} \prod_{j=0}^{N-1}  \widetilde{a}\_j  H \prod\_{k=0}^{N-1}  \widetilde{a}^\dagger_k\ket{0}$.</span></span> <span data-ttu-id="51bf8-117">이러한 최적화 문제는 일반적으로 어려울 수 있지만 Hartree – Fock 알고리즘은 특히 평형 기 하 도형에서 폐쇄형 셸 molecules에 대해 최적화 문제에 대 한 최적 솔루션으로 신속 하 게 수렴 하는 경향이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-117">While such optimization problems may be generically hard, in practice the Hartree–Fock algorithm tends to rapidly converge to a near-optimal solution to the optimization problem, especially for closed-shell molecules in the equilibrium geometries.</span></span> <span data-ttu-id="51bf8-118">`FermionWavefunction` 개체의 인스턴스로 이러한 상태를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-118">We may specify these states as an instance of the `FermionWavefunction` object.</span></span> <span data-ttu-id="51bf8-119">예를 들어 $a ^ \dagger_{1}^ \dagger_{2}^ \dagger_{6}\ket{0}$은 다음과 같이 화학 라이브러리에서 인스턴스화됩니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-119">For instance, the state $a^\dagger_{1}a^\dagger_{2}a^\dagger_{6}\ket{0}$ is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
<span data-ttu-id="51bf8-120">`SpinOrbital` 인덱스를 사용 하 여 웨이브 함수를 인덱싱하고 다음과 같이 이러한 인덱스를 정수로 변환할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-120">It is also possible to index wave functions with `SpinOrbital` indices, and then convert these indices to integers as follows.</span></span>
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="51bf8-121">Hartree – Fock 이론에 대 한 가장 인상적인 기능은 파괴 간에 되거나 얽 히 없는 퀀텀 상태를 생성 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-121">The most striking feature about Hartree–Fock theory is that it yields a quantum state that has no entanglement between the electrons.</span></span>
<span data-ttu-id="51bf8-122">즉, 분자 시스템의 속성에 대 한 적절 한 질적 설명을 제공 하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-122">This means that it often provides a suitable qualitative description of properties of molecular systems.</span></span> 

<span data-ttu-id="51bf8-123">Hartree-Fock 상태는 다음과 같이 `FermionHamiltonian`에서 다시 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-123">The Hartree-Fock state may also be reconstructed from a `FermionHamiltonian`  as follows.</span></span>
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

<span data-ttu-id="51bf8-124">그러나 특히 강력한 상관 관계가 지정 된 시스템의 경우 정확한 결과를 얻으려면 Hartree – Fock 이론 이상으로 퀀텀 상태를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bf8-124">However, obtaining accurate results, especially for strongly correlated systems, necessitate quantum states that go beyond Hartree–Fock theory.</span></span>