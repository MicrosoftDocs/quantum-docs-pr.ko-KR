---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: TrotterSimulationAlgorithm 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: b2cc9c29cbb40809540d143fcefd7cb0838bfea7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847785"
---
# <a name="trottersimulationalgorithm-function"></a>TrotterSimulationAlgorithm 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`SimulationAlgorithm` Trotter – Suzuki 분해를 사용 하 여 시간-진화 연산자 _exp (-iHt)_ 에 근사치를 적용 하는 함수입니다.

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a>입력

### <a name="trotterstepsize--double"></a>trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)

시뮬레이션 된 시간-단일 Trotter 단계에서 진화 합니다.


### <a name="trotterorder--int"></a>trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)

Trotter 통합자의 순서입니다. 이 값은 1 또는 짝수 여야 합니다.



## <a name="output--simulationalgorithm"></a>출력: [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)

`SimulationAlgorithm` 형식입니다.