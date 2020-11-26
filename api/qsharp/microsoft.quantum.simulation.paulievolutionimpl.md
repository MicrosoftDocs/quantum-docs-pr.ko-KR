---
uid: Microsoft.Quantum.Simulation.PauliEvolutionImpl
title: PauliEvolutionImpl 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.

  See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 868f3eef187e8e993127cfcab21e1574583ac845
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229140"
---
# <a name="paulievolutionimpl-operation"></a>PauliEvolutionImpl 작업

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


동적 생성기를 simulatable 게이트 집합으로 나타내고 Pauli로 확장 합니다.

자세한 내용은 [동적 생성기 모델링](/quantum/libraries/data-structures#dynamical-generator-modeling) 을 참조 하세요.

```qsharp
operation PauliEvolutionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, delta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Pauli 단위로 단일 진화로 나타낼 생성기 인덱스입니다.


### <a name="delta--double"></a>델타: [Double](xref:microsoft.quantum.lang-ref.double)

에서 참조 된 조건에 따라 진화 하는 기간에 대 한 승수 `generatorIndex` 입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

시간 진화 연산자에 의해 처리 된 등록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

