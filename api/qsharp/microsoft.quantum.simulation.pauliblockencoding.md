---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: PauliBlockEncoding 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848016"
---
# <a name="pauliblockencoding-function"></a>PauliBlockEncoding 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hamiltonian에 대 한 블록 인코딩 단일를 만듭니다.

Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $는 각각 실제 계수 $ \ $P $를 포함 하는 Pauli 용어 _j alpha_j의 합계로 설명 됩니다.

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>입력

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

`GeneratorSystem`$H $를 Pauli 용어의 합계로 설명 하는입니다.



## <a name="output--doubleblockencodingreflection"></a>출력: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>첫 번째 매개 변수

계수 $ \alpha = \ sum_ {j} | \ alpha_j | $ 인 1-표준을 기반으로 합니다.

## <a name="second-parameter"></a>두 번째 매개 변수

`BlockEncodingReflection`Hamiltonian $H $의 단일 $U $입니다. 이 단일 항목은 $U ^ 2 = I $를 충족 하므로 리플렉션 이기도 합니다.

## <a name="remarks"></a>설명

이는 $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ 상태를 준비 하 고 준비 하지 않으며 곱셈 제어 된 단일 및을 생성 하 여 얻을 수 <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> 있습니다.