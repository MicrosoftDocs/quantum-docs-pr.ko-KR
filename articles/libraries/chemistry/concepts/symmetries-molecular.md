---
title: Symmetries of 분자 적분 | Microsoft Docs
description: Symmetries of 분자 적분 개념 문서
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
ms.openlocfilehash: 041d600bc8d65e7d67f5fe7d61a69426fb42ffbc
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442387"
---
# <a name="symmetries-of-molecular-integrals"></a>Symmetries of 분자 적분

[전자 시스템에 대 한 퀀텀 모델](xref:microsoft.quantum.chemistry.concepts.quantummodels)에서 제공 되는 Hamiltonian 인 Hamiltonian의 고유 대칭은 서로를 서로 상호 작용 하 고 nuclei를 사용 하 여 파괴에 대해 설명 하는 여러 가지 symmetries이 될 수 있습니다. Hamiltonian 용어를 압축 하는 데 활용 됩니다.
일반적으로 기본 함수 $ \psi_j $에 대 한 추가 가정이 생성 되지 않는 경우에는 다음 [에 대 한 퀀텀 모델의 정수에서 즉시 볼 수 있는 \begin{equation} h_ {pqrs} = h_ {qpsr}, \tag{★} \label{eq: hpqrs} \begin{equation}만 있으면 됩니다. ](xref:microsoft.quantum.chemistry.concepts.quantummodels)$P, q $ 및 $r, s $가 통신에서 상호 관련 된 경우 해당 값이 동일 하 게 유지 된다는 것을 바탕으로 한 전자 시스템.

계산 orbitals가 실제 값 (가우스 궤도 기반) 인 것으로 가정 하면 \begin{ke} h_ {pqrs} = h_ {qpsr} = h_ {srqp} = h_ {rspq} = h_ {rqps} = h_ {psrq} = h_ {spqr} = h_ {qrsp} .\tag {★} \label{eq: hpqrsreal} \end{ 수식} 이러한 가정을 보유 한 경우 위의 symmetries을 사용 하 여 Hamiltonian의 행렬 요소를 $8 $로 저장 하는 데 필요한 데이터를 줄일 수 있습니다. 이렇게 하면 일관 된 방식으로 데이터를 가져오는 것이 약간 더 어려워집니다.
다행히 Hamiltonian 시뮬레이션 라이브러리에는 [LIQUI $ | \rangle $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) 에서 또는 [Nwchem](http://www.nwchem-sw.org/index.php/Main_Page)에서 직접 정수 파일을 가져오는 데 사용할 수 있는 서브루틴이 있습니다.

분자 궤도 정수 (예: $h\_{pq} $ 및 $h\_{pqrs} $ 용어)는이 대칭을 표현 하는 데 도움이 되는 다양 한 기능을 제공 하는 `OrbitalIntegral` 유형을 사용 하 여 표현 됩니다.
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

동일 하 게 동일한 모든 궤도를 열거 하는 것 외에도 `OrbitalIntegral` 표시 되는 Hamiltonian에 포함 된 모든 스핀 궤도 인덱스 목록은 다음과 같이 생성할 수 있습니다.
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a>분자 적분에서 Fermionic Hamiltonians 생성

`FermionTerm`s를 추가 하 여 Fermionic Hamiltonian를 구성 하는 대신 각 궤도의 정수 계열에 해당 하는 모든 용어가 자동으로 추가 될 수 있습니다.
예를 들어 다음 코드는 모든 permutational symmetries에 대해 자동으로 열거 하 고 정식 순서로 용어를 정렬 합니다. 
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
