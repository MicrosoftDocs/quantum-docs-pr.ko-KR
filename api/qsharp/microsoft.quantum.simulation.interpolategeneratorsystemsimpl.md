---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystemsImpl
title: InterpolateGeneratorSystemsImpl 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystemsImpl
qsharp.summary: Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).
ms.openlocfilehash: a902a93968d221349f9a6fa977bbc1706971fcfd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855761"
---
# <a name="interpolategeneratorsystemsimpl-function"></a>InterpolateGeneratorSystemsImpl 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`GeneratorSystems` `s` 0에서 1 사이 (포함) 사이의 일정 매개 변수에 따라 두 개의를 선형으로 보간합니다.

```qsharp
function InterpolateGeneratorSystemsImpl (schedule : Double, generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>입력

### <a name="schedule--double"></a>일정: [Double](xref:microsoft.quantum.lang-ref.double)

일정 매개 변수 $s \in [0, 1] $입니다.


### <a name="generatorsystemstart--generatorsystem"></a>generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

시작 `GeneratorSystem` 입니다.


### <a name="generatorsystemend--generatorsystem"></a>generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

끝 `GeneratorSystem` 입니다.



## <a name="output--generatorsystem"></a>출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

`GeneratorSystem`가중치 $ (1-s) $ on `generatorSystemStart` 과 가중치 $s $ on으로 입력 생성기 시스템의 합계인 시스템을 나타내는 `generatorSystemEnd` 입니다.

## <a name="see-also"></a>참고 항목

- [GeneratorSystem.](xref:Microsoft.Quantum.Simulation.GeneratorSystem)