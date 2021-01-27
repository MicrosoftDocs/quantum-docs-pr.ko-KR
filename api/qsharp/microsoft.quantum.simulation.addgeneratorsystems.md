---
uid: Microsoft.Quantum.Simulation.AddGeneratorSystems
title: AddGeneratorSystems 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: b23fc89b941a7cdd93ee7938dda50eb14e3ed528
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857932"
---
# <a name="addgeneratorsystems-function"></a>AddGeneratorSystems 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


새를 `GeneratorSystem` 만드는 두 개의를 추가 `GeneratorSystem` 합니다.

```qsharp
function AddGeneratorSystems (generatorSystemA : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemB : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>입력

### <a name="generatorsystema--generatorsystem"></a>generatorSystemA: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

첫 번째 `GeneratorSystem`입니다.


### <a name="generatorsystemb--generatorsystem"></a>generatorSystemB: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

두 번째 `GeneratorSystem`입니다.



## <a name="output--generatorsystem"></a>출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

`GeneratorSystem`입력 생성기 시스템의 합계인 시스템을 나타내는입니다.

## <a name="see-also"></a>참고 항목

- [GeneratorSystem.](xref:Microsoft.Quantum.Simulation.GeneratorSystem)