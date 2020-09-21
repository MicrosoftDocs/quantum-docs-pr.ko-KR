---
title: Hartree-Fock 이론
description: 퀀텀 시스템의 초기 상태를 구성 하는 간단한 방법인 Hartree – Fock 이론에 대해 알아보세요.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
no-loc:
- Q#
- $$v
ms.openlocfilehash: 53d6e4342e5b58886528e89871591e57d8e70c82
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835352"
---
# <a name="hartreefock-theory"></a>Hartree – Fock 이론

아마도 퀀텀 연금술 시뮬레이션에서 가장 중요 한 수량은 Hamiltonian 행렬의 최소 에너지 eigenvector 인 그라운드 상태입니다.
이는 반응 경로에서 단계의 시작과 끝을 설명 하는 퀀텀 상태와 실내 온도가 일반적으로 그라운드 상태임을 설명 하는 퀀텀 상태 간의 무료 에너지 차이로 인해 반응 율이 molecules는 것입니다.
일반적으로는 상당한 수의 구성에 대 한 배포 이기 때문에 일반적으로는 일반적으로 어려움 (퀀텀 컴퓨터 에서도)을 학습할 수 없습니다.
접지 상태 에너지와 같은 수량은 학습 될 수 있습니다.
예를 들어 $ \ket{\psi} $이 순수 퀀텀 상태 이면 \begin{equation} E = \bra{\psi} \hat{H} \ket{\psi} \begin{equation}는 시스템의 해당 상태에 있는 평균 에너지를 제공 합니다.
그런 다음 해당 값을 가장 작은 값으로 제공 하는 상태입니다. 결과적으로, 진정한 접지 상태와 최대한 가까운 상태를 선택 하는 것은 에너지를 직접 (variational eigensolvers에서 수행 되는 경우) 또는 단계 예측을 통해 예측 하는 데 매우 중요 합니다.

Hartree – Fock 이론은 퀀텀 시스템의 초기 상태를 구성 하는 간단한 방법을 제공 합니다. 양자는 퀀텀 시스템의 그라운드 상태에 대 한 단일 Slater 결정 근사값을 생성 합니다. 이를 위해 그라운드 상태 에너지를 최소화 하는 Fock 공간 내에서 회전을 찾습니다. 특히 $N $ 파괴 시스템의 경우이 메서드는 회전을 수행 합니다. \begin{equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket {0} \maps\ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket {0} \defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket {0} \end{c} Hermitian (즉, $u =-u ^ \ka$) matrix $u = \ sum_ {pq} u_ {pq} a ^ \ dagger_p a_q $. 행렬 $u $는 궤도 회전을 나타내고 $ \widetilde{a} ^ \ dagger_j $ 및 $ \widetilde{a} _j $은 Hartree – Fock 분자 spin-orbitals를 차지 하는 파괴에 대 한 만들기 및 annihilation 연산자를 나타냅니다.


행렬 $u $는 예상 되는 에너지 $ \bra {0} \ prod_ {j = 0} ^ {n-1} \widetilde{a} \_ j H \prod \_ {k = 0} ^ {n-1} \widetilde{a} ^ \ dagger_k \ket $를 최소화 하기 위해 최적화 됩니다 {0} . 이러한 최적화 문제는 일반적으로 어려울 수 있지만 Hartree – Fock 알고리즘은 특히 평형 기 하 도형에서 폐쇄형 셸 molecules에 대해 최적화 문제에 대 한 최적 솔루션으로 신속 하 게 수렴 하는 경향이 있습니다. 개체의 인스턴스로 이러한 상태를 지정할 수 있습니다 `FermionWavefunction` . 예 $a를 들어 ^ \ dagger_ dagger_ ^ \ {1} {2} dagger_ {6} \ket {0} $은 다음과 같이 화학 라이브러리에서 인스턴스화됩니다.
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
인덱스를 사용 하 여 웨이브 함수를 인덱싱하고 `SpinOrbital` 다음과 같이 이러한 인덱스를 정수로 변환할 수도 있습니다.
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

Hartree – Fock 이론에 대 한 가장 인상적인 기능은 파괴 간에 되거나 얽 히 없는 퀀텀 상태를 생성 한다는 것입니다.
즉, 분자 시스템의 속성에 대 한 적절 한 질적 설명을 제공 하는 경우가 많습니다. 

Hartree-Fock 상태는 다음과 같이에서 다시 구성할 수도 있습니다 `FermionHamiltonian`  .
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

그러나 특히 강력한 상관 관계가 지정 된 시스템의 경우 정확한 결과를 얻으려면 Hartree – Fock 이론 이상으로 퀀텀 상태를 지정 해야 합니다.
