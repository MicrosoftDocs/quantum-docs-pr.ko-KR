---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: JordanWignerOptimizedFermionEvolutionSet 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: d2d916655b7538b39d5739d67dbb3fc9920cf67a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722139"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a>JordanWignerOptimizedFermionEvolutionSet 함수

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .

패키지 [](https://nuget.org/packages/)


동적 생성기를 simulatable 게이트 집합으로 나타내고 Pauli로 확장 합니다.

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a>입력

### <a name="parityqubit--qubit"></a>Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

시간 진화의 부호를 결정 하는의 비트입니다.



## <a name="output--evolutionset"></a>출력: [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)

`EvolutionSet` `GeneratorIndex` JWOptimized 된 기준에 대 한를 ' EvolutionUnitary에 매핑하는입니다.