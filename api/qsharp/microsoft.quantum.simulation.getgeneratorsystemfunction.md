---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: GetGeneratorSystemFunction 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 7b6eabd203cecf8c64f0bff3e06f08a0bec31bf2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852765"
---
# <a name="getgeneratorsystemfunction-function"></a>GetGeneratorSystemFunction 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`GeneratorIndex`에서 함수를 검색 `GeneratorSystem` 합니다.

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a>입력

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

해당 `GeneratorSystem`입니다.



## <a name="output--int---generatorindex"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Hamiltonian의 각 용어를 인덱싱하는 함수입니다 `GeneratorIndex` .

## <a name="see-also"></a>참고 항목

- [GeneratorIndex.](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [GeneratorSystem.](xref:Microsoft.Quantum.Simulation.GeneratorSystem)