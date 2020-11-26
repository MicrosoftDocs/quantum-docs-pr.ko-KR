---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: SumGeneratorSystems 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 7cb18e161dce3a52d7c9a0bf6a45d4818db2b849
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192471"
---
# <a name="sumgeneratorsystems-function"></a>SumGeneratorSystems 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`GeneratorSystem`새 GeneratorSystem을 만들려면를 여러 개 추가 합니다.

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>입력

### <a name="generatorsystems--generatorsystem"></a>generatorSystems: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]

`GeneratorSystem[]` 형식의 배열입니다.



## <a name="output--generatorsystem"></a>출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

`GeneratorSystem`입력 생성기 시스템의 합계인 시스템을 나타내는입니다.

## <a name="see-also"></a>참고 항목

- [GeneratorSystem.](xref:Microsoft.Quantum.Simulation.GeneratorSystem)