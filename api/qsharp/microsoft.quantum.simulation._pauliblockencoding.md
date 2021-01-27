---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: _PauliBlockEncoding 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: c27ef1a6b7cd7c84defe2a783e9fb1610e52d1e7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851074"
---
# <a name="_pauliblockencoding-function"></a>_PauliBlockEncoding 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hamiltonian에 대 한 블록 인코딩 단일를 만듭니다.

Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $는 각각 실제 계수 $ \ $P $를 포함 하는 Pauli 용어 _j alpha_j의 합계로 설명 됩니다.

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>입력

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

`GeneratorSystem`$H $를 Pauli 용어의 합계로 설명 하는입니다.


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a>statePrepUnitary: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

J\rightarrow V_j $ $f 함수를 지정 하 여 인덱스 $ \ket{j} $에 의해 제어 되는 단일 $V _j $를 적용 하는 단일 연산 $V $입니다.


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a>멀티플렉서: ([int](xref:microsoft.quantum.lang-ref.int),[int, int](xref:microsoft.quantum.lang-ref.int) -> [](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + ctl)-> ([LittleEndian,](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[sbit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + ctl





## <a name="output--doubleblockencodingreflection"></a>출력: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>첫 번째 매개 변수

계수 $ \alpha = \ sum_ {j} | \ alpha_j | $ 인 1-표준을 기반으로 합니다.

## <a name="second-parameter"></a>두 번째 매개 변수

`BlockEncodingReflection`Hamiltonian $U $의 단일 $U $입니다. 이 단일 항목은 $U ^ 2 = I $를 충족 하므로 리플렉션 이기도 합니다.

## <a name="remarks"></a>설명

작업 예: $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $의 상태를 준비 하 고 준비 하지 않으며, 곱하기 제어 되는 단일 구성 작업은 <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> 및 <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> 입니다.