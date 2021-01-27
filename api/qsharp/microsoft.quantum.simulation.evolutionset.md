---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: EvolutionSet 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 35c0b24da284a5871fd11b6d624102b853b89d19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856065"
---
# <a name="evolutionset-user-defined-type"></a>EvolutionSet 사용자 정의 형식

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


시뮬레이션 알고리즘을 구현 하는 데 쉽게 구현 하 고 사용할 수 있는 게이트 집합을 나타냅니다.

집합의 요소는로 인덱싱됩니다.  <xref:microsoft.quantum.simulation.generatorindex> 각 집합은에 대 한 함수에서로 설명 됩니다 .이 함수는 `GeneratorIndex` 시간을  <xref:microsoft.quantum.simulation.evolutionunitary> 나타내는 실수에 의해 매개 변수화 된 작업입니다.

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

