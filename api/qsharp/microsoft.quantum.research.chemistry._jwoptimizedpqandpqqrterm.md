---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedPQandPQQRTerm
title: _JWOptimizedPQandPQQRTerm 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedPQandPQQRTerm
qsharp.summary: Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.
ms.openlocfilehash: 97ae285ede38883f058b3e7609f9a26fb9e4340a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854770"
---
# <a name="_jwoptimizedpqandpqqrterm-operation"></a>_JWOptimizedPQandPQQRTerm 작업

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .

패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .


에 설명 된 PQ 또는 PQQR 용어로 시간 진화를 적용 `GeneratorIndex` 합니다.

```qsharp
operation _JWOptimizedPQandPQQRTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="term--generatorindex"></a>용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` PQ 또는 PQQr term을 나타내는입니다.


### <a name="stepsize--double"></a>Stsize: [Double](xref:microsoft.quantum.lang-ref.double)

시간-진화 기간입니다.


### <a name="parityqubit--qubit"></a>Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

시간 진화의 부호를 결정 하는의 비트입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

Hamiltonian의 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

