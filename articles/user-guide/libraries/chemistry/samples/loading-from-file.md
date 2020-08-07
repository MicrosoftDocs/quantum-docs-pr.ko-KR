---
title: 파일에서 해밀토니안 로드
description: Broombridge 스키마를 사용 하 여 large Hamiltonian를 자동으로 생성 하는 방법을 알아봅니다.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.loadhamiltonian
no-loc:
- Q#
- $$v
ms.openlocfilehash: 57e25bf55009797b01695cef0f3d29b94662ccc0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869242"
---
# <a name="loading-a-hamiltonian-from-file"></a>파일에서 해밀토니안 로드
이전에는 개별 용어를 추가 하 여 Hamiltonians를 만들었습니다. 이는 작은 예제에 적합 하지만, 규모의 퀀텀 연금술에는 수백만 또는 수십억 개의 용어로 Hamiltonians 필요 합니다. NWChem과 같은 화학 패키지에 의해 생성 된 이러한 Hamiltonians는 너무 커서 수동으로 가져올 수 없습니다. 이 샘플에서는 `FermionHamiltonian` [Broombridge 스키마](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)로 표시 되는 분자 인스턴스가 자동으로 생성 되는 방법을 설명 합니다. 참조의 경우 제공 된 `LithiumHydrideGUI` 샘플 또는 샘플을 검사할 수 있습니다 `RunSimulation` . [LIQUi |>](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/)에서 사용 하는 형식에서 가져오기에 대 한 제한 된 지원을 사용할 수도 있습니다.

샘플 리포지토리의 폴더에 제공 되는 Nitrogen 분자의 예제를 살펴보겠습니다 `IntegralData/YAML` . 스키마를 로드 하는 방법은 `Broombridge` 간단 합니다.

```csharp
// This is the name of the file we want to load
var filename = @"n2_1_00Re_sto3g.nw.out.yaml";
// This is the directory containing the file
var root = @"IntegralData\YAML";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge($@"{root}\{filename}");

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.First()`, which selects the first element of the list.
var problem = broombridge.ProblemDescriptions.First();

// This extracts the `OrbitalIntegralHamiltonian` from Broombridge format,
// then converts it to a fermion Hamiltonian, then to a Jordan-Wigner
// representation.
var orbitalIntegralHamiltonian = problem.OrbitalIntegralHamiltonian;
var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);
var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);
```

Broombridge 스키마에는 준비 될 초기 상태에 대 한 제안도 포함 되어 있습니다. `"|G⟩"`이러한 상태에 대 한 레이블 (예: 또는)은 `"|E1⟩"` 파일을 검사 하 여 확인할 수 있습니다. 이러한 초기 상태를 준비 하기 위해 `qSharpData` 퀀텀 알고리즘에서 사용 되는은 Q# [이전 섹션과](xref:microsoft.quantum.chemistry.examples.energyestimate)비슷하지만 원하는 초기 상태를 선택 하는 추가 매개 변수를 사용 하 여 가져옵니다. 예를 들어
```csharp
// The desired initial state, assuming that a description of it is present in the
// Broombridge schema.
var state = "|E1>";
var wavefunction = problem.Wavefunctions[state].ToIndexing(IndexConvention.UpDown);

// This creates the qSharpData consumable by the Q# chemistry library algorithms.
var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
var qSharpWavefunctionData = wavefunction.ToQSharpFormat();
var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

위의 모든 단계는 다음과 같이 제공 된 편리한 메서드를 사용 하 여 축약 될 수 있습니다.
```csharp
// This is the name of the file we want to load
var filename = "...";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge(filename);

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.Single()`, which selects the only element of the list.
var problem = broombridge.ProblemDescriptions.Single();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
// If no state is specified, the Hartree-Fock state is used by default.
var qSharpData = problem.ToQSharpFormat("|E1>");
```

LIQUi의 Hamiltonian를 로드할 수도 있습니다. 매우 유사한 구문을 사용 하 여> 형식 

```csharp
// This is the name of the file we want to load
var filename = @"fe2s2_sto3g.dat"; // This is Ferrodoxin.
// This is the directory containing the file
var root = @"IntegralData\Liquid";

// Deserialize the LiQuiD format.
var problem = LiQuiD.Deserialize($@"{root}\{filename}").First();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
var qSharpData = problem.ToQSharpFormat();
```

Broombridge의 모든 인스턴스 또는 중간 단계에서이 프로세스를 수행 하면 지정 된 전자 구조 문제에 대해 퀀텀 단계 예측과 같은 퀀텀 알고리즘이 실행 될 수 있습니다.
