---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedFermionEvolution
title: _JWOptimizedFermionEvolution 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedFermionEvolution
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 62fbd27f703a17a547d94e61c7a4981230a4b251
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854834"
---
# <a name="_jwoptimizedfermionevolution-operation"></a>_JWOptimizedFermionEvolution 작업

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .

패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .


동적 생성기를 simulatable 게이트 집합으로 나타내고 JWOptimized 된 단위로 확장 합니다.

자세한 내용은 [동적 생성기 모델링](../libraries/data-structures#dynamical-generator-modeling) 을 참조 하세요.

```qsharp
operation _JWOptimizedFermionEvolution (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

JWOptimized 된 기준에서 단일 진화로 나타낼 생성기 인덱스입니다.


### <a name="stepsize--double"></a>Stsize: [Double](xref:microsoft.quantum.lang-ref.double)

에서 참조 된 조건에 따라 진화 하는 기간에 대 한 승수 `generatorIndex` 입니다.


### <a name="parityqubit--qubit"></a>Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

시간 진화의 부호를 결정 하는의 비트입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

시간 진화 연산자에 의해 처리 된 등록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

