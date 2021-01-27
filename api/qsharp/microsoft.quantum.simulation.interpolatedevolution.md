---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: InterpolatedEvolution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 4d2e04513c96c6e5f41e85f1df685e91e2973098
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858084"
---
# <a name="interpolatedevolution-function"></a>InterpolatedEvolution 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


균일 한 일정을 사용 하 여 두 생성기 간을 보간합니다. 결과 시간 종속 생성기에서 시뮬레이션 된 진화를 원하는 비트 레지스터에 적용 하는 작업을 반환 합니다.

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="interpolationtime--double"></a>interpolationTime: [Double](xref:microsoft.quantum.lang-ref.double)

보간을 수행할 시간입니다.


### <a name="evolutiongeneratorstart--evolutiongenerator"></a>evolutionGeneratorStart: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

진화를 시뮬레이션 하는 초기 생성기입니다.


### <a name="evolutiongeneratorend--evolutiongenerator"></a>evolutionGeneratorEnd: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

에서 발전을 시뮬레이트하는 최종 생성기입니다.


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a>timeDependentSimulationAlgorithm: [timeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

균일 한 보간 일정 중에 진화를 시뮬레이션 하는 데 사용 되는 시간 종속 시뮬레이션 알고리즘입니다.



## <a name="output--qubit--unit--is-adj--ctl"></a>출력:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.



## <a name="remarks"></a>설명

보간 시간이 adiabatic 조건을 충족 하도록 선택 된 경우이 함수는 최종 동적 생성기에 대해 adiabatic 상태 준비를 수행 하는 작업을 반환 합니다.