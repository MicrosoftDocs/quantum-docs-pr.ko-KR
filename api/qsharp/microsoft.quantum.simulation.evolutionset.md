---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: EvolutionSet 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 41504837b281b1021a2d09ef75acc10315b4fd07
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710613"
---
# <a name="evolutionset-user-defined-type"></a>EvolutionSet 사용자 정의 형식

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지 [](https://nuget.org/packages/)


시뮬레이션 알고리즘을 구현 하는 데 쉽게 구현 하 고 사용할 수 있는 게이트 집합을 나타냅니다.

집합의 요소는로 인덱싱됩니다.  <xref:microsoft.quantum.simulation.generatorindex> 각 집합은에 대 한 함수에서로 설명 됩니다 .이 함수는 `GeneratorIndex` 시간을  <xref:microsoft.quantum.simulation.evolutionunitary> 나타내는 실수에 의해 매개 변수화 된 작업입니다.

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

