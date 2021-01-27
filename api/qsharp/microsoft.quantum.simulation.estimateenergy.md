---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: EstimateEnergy 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: f9243557718e12d168afadbf641492291afd1704
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856759"
---
# <a name="estimateenergy-operation"></a>EstimateEnergy 작업

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`statePrepUnitary` `qpeUnitary` 을 사용 하 여 결과 상태에 대해 자동으로 할당 된 입력 상태 단계 추정에를 적용 하 여 상태 준비를 수행 `phaseEstAlgorithm` 합니다.

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a>입력

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

시뮬레이션을 수행 하는 데 사용 되는 비트 수입니다.


### <a name="stateprepunitary--qubit--unit"></a>statePrepUnitary: [](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

초기 동적 생성기에 대 한 상태 준비를 나타내는 oracle입니다.


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a>qpeUnitary: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl

동적 생성기에서 그라운드 상태 $ \ket{\phi} $ 및 접지 상태 에너지 $E = \\ \a, \delta t $ 인 시간 $ \delta t $의 진화를 나타내는 단일 $U 연산자를 나타내는 oracle


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double) 

지정 된 단일 작업에 대해 단계 예측을 수행 하는 작업입니다.
자세한 내용은 [반복 단계 예측](/quantum/libraries/characterization#iterative-phase-estimation) 을 참조 하세요.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

$U $로 표시 되는 생성기의 그라운드 상태 에너지 $ \\a$의 예상 $ \hat{\phi} $입니다.