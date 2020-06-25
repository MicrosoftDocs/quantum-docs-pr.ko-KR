---
title: Symmetries of 분자 적분
description: 'Q # OrbitalIntegral 형식을 사용 하 여 분자 symmetries를 열거 하는 방법에 대해 알아봅니다.'
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
ms.openlocfilehash: b7e7b79af17af544c4a784eff08500498afc9f67
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275254"
---
# <a name="symmetries-of-molecular-integrals"></a><span data-ttu-id="a9ae5-103">Symmetries of 분자 적분</span><span class="sxs-lookup"><span data-stu-id="a9ae5-103">Symmetries of Molecular Integrals</span></span>

<span data-ttu-id="a9ae5-104">[전자 시스템에 대 한 퀀텀 모델](xref:microsoft.quantum.chemistry.concepts.quantummodels)에서 제공 되는 Hamiltonian 인 Hamiltonian의 고유 대칭은 서로를 서로 상호 작용 하 고 nuclei를 사용 하 여 파괴를 설명 하는, symmetries의 용어를 압축 하는 데 활용할 수 있는 몇 가지 Hamiltonian를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-104">The inherent symmetry of the Coulomb Hamiltonian, which is the Hamiltonian given in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels), that describes electrons interacting electrically with each other and with the nuclei, leads to a number of symmetries that can be exploited to compress the terms in the Hamiltonian.</span></span>
<span data-ttu-id="a9ae5-105">일반적으로 기본 함수 $ \ psi_j $에 대해 더 이상 가정이 생성 되지 않는 경우에는 \begin{st} h_ {pqrs} = h_ {qpsr}만 있으면 됩니다. \t $p, q $ 및 $r, s $가 통신에서 상호 관련 된 경우 해당 값이 동일 하 게 유지 된다는 것을 확인 하면 전자 시스템에 대 한 값이 동일 하 게 ★ 유지 된다는 것을 확인 하 여 [전자 시스템에 대 한](xref:microsoft.quantum.chemistry.concepts.quantummodels) 값이 동일 하 게 유지 된다는 것을 확인 했을 때 hpqrs ()</span><span class="sxs-lookup"><span data-stu-id="a9ae5-105">In general if no further assumptions are made about the basis functions $\psi_j$ then we only have that \begin{equation} h_{pqrs}= h_{qpsr},\tag{★}\label{eq:hpqrs} \end{equation} which can be immediately seen from the integrals in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) upon noting that their values remain identical if $p,q$ and $r,s$ are interchanged from anti-commutation.</span></span>

<span data-ttu-id="a9ae5-106">사용자가 가우스 궤도를 h_ 기준으로 하는 경우에는 spin orbitals가 실제 값 이라고 가정 하면 pqrs {} = h_ {qpsr} = h_ {srqp} = h_ {rspq} = h_ {rqps} = h_ {psrq} = h_ {spqr} = h_ {qrsp} .\tag {★} \label{eq: hpqrsreal} \c{c} 위의 symmetries을 사용 하 여 Hamiltonian의 행렬 요소를 $8 $로 저장 하는 데 필요한 데이터를 줄일 수 있습니다. 이렇게 하면 일관 된 방식으로 데이터를 가져오는 것이 약간 더 어려워집니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-106">If we assume that the spin-orbitals are real-valued (as they are for Gaussian orbital bases) then we further have that \begin{equation} h_{pqrs} = h_{qpsr} = h_{srqp} = h_{rspq}=h_{rqps}=h_{psrq}=h_{spqr}=h_{qrsp}.\tag{★}\label{eq:hpqrsreal} \end{equation} Given such assumptions hold, we can use the above symmetries to reduce the data needed to store the matrix elements of the Hamiltonian by a factor of $8$; although doing so makes importing data in a consistent way slightly more challenging.</span></span>
<span data-ttu-id="a9ae5-107">다행히 Hamiltonian 시뮬레이션 라이브러리에는 [LIQUI $ | \rangle $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) 에서 또는 [Nwchem](http://www.nwchem-sw.org/index.php/Main_Page)에서 직접 정수 파일을 가져오는 데 사용할 수 있는 서브루틴이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-107">Fortunately the Hamiltonian simulation library has subroutines that can be used to import integral files from either [LIQUI$|\rangle$](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) or directly from [NWChem](http://www.nwchem-sw.org/index.php/Main_Page).</span></span>

<span data-ttu-id="a9ae5-108">분자 궤도 정수 (예: 이러한 $h \_ {pq} $ 및 $h \_ {pqrs} $ 용어)는 형식을 사용 하 여 표현 됩니다. `OrbitalIntegral` 이 형식을 사용 하면이 대칭을 표현 하는 데 도움이 되는 다양 한 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-108">Molecular orbital integrals (i.e. the $h\_{pq}$ and $h\_{pqrs}$ terms) such as these are represented using the `OrbitalIntegral` type, which provides a number of helpful functions to express this symmetry.</span></span>
```csharp
    // Load the namespace containing orbital integral objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // Create a `OrbitalIntegral` instance to store a one-electron molecular 
    // orbital integral data.
    var oneElectronOrbitalIndices = new[] { 0, 1 };
    var oneElectronCoefficient = 1.0;
    var oneElectronIntegral = new OrbitalIntegral(oneElectronOrbitalIndices, oneElectronCoefficient);

    // This enumerates all one-electron integrals with the same coefficient --
    // an array of equivalent `OrbitalIntegral` instances is generated. In this
    // case, there are two elements.
    var oneElectronIntegrals = oneElectronIntegral.EnumerateOrbitalSymmetries();

    // Create a `OrbitalIntegral` instance to store a two-electron molecular orbital integral data.
    var twoElectronOrbitalIndices = new[] { 0, 1, 2, 3 };
    var twoElectronCoefficient = 0.123;
    var twoElectronIntegral = new OrbitalIntegral(twoElectronOrbitalIndices, twoElectronCoefficient);

    // This enumerates all two-electron integrals with the same coefficient -- 
    // an array of equivalent `OrbitalIntegral` instances is generated. In 
    // this case, there are 8 elements.
    var twoElectronIntegrals = twoElectronIntegral.EnumerateOrbitalSymmetries();
```

<span data-ttu-id="a9ae5-109">동일 하 게 동일한 모든 궤도를 열거 하는 것 외에도로 표시 되는 Hamiltonian에 포함 된 모든 스핀 궤도 인덱스 목록이 `OrbitalIntegral` 다음과 같이 생성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-109">In addition to enumerating over all orbital integrals that are numerically identical, a list of all spin-orbital indices contained in the Hamiltonian represented by an `OrbitalIntegral` may be generated as follows.</span></span>
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a><span data-ttu-id="a9ae5-110">분자 적분에서 Fermionic Hamiltonians 생성</span><span class="sxs-lookup"><span data-stu-id="a9ae5-110">Constructing Fermionic Hamiltonians from Molecular Integrals</span></span>

<span data-ttu-id="a9ae5-111">를 추가 하 여 Fermionic Hamiltonian를 생성 하는 대신 `FermionTerm` 각 궤도의 정수 계열에 해당 하는 모든 용어를 자동으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-111">Rather than constructing a Fermionic Hamiltonian by adding `FermionTerm`s, all terms corresponding to each orbital integral may be added automatically.</span></span>
<span data-ttu-id="a9ae5-112">예를 들어 다음 코드는 모든 permutational symmetries에 대해 자동으로 열거 하 고 정식 순서로 용어를 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ae5-112">For example, the following code automatically enumerates over all permutational symmetries and orders the terms in canonical order:</span></span> 
```csharp
    // Load the namespace containing fermion objects. This
    // example also uses LINQ queries.
    using Microsoft.Quantum.Chemistry.Fermion;
    using System.Linq;

    // Create a `OrbitalIntegral` instance to store a two-electron molecular 
    // orbital integral data.
    var orbitalIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // Create an `OrbitalIntegralHamiltonian` instance to store the orbital integral
    // terms
    var orbitalIntegralHamiltonian = new OrbitalIntegralHamiltonian();
    orbitalIntegralHamiltonian.Add(orbitalIntegral);

    // Convert the orbital integral representation to a fermion
    // representation. This also requires choosing a convention for 
    // mapping spin orbital indices to integer indices.
    var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);

    // Alternatively, one can add orbital integrals directly to a fermion Hamiltonian
    // as follows. This automatically enumerates over all symmetries, and then
    // orders the `HermitianFermionTerm` instances in canonical order. We will need to
    // choose an indexing convention as well.
    fermionHamiltonian.AddRange(orbitalIntegral
        .ToHermitianFermionTerms(0, IndexConvention.UpDown)
        .Select(o => (o.Item1, o.Item2.ToDoubleCoeff())));
```