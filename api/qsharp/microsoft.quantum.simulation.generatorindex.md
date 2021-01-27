---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: GeneratorIndex 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 762dac81ea0963443f0338cea1b879856c84b0ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858376"
---
# <a name="generatorindex-user-defined-type"></a>GeneratorIndex 사용자 정의 형식

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


모든 동적 생성기 집합의 단일 기본 용어를 나타냅니다. 예를 들어 Hermitian 연산자는 해당 생성기의 map이 해당 생성기의 시간 혁신을 통해 발생 하는 것입니다 `EvolutionSet` .

첫 번째 요소 (Int [], Double [])는 단일 용어로 이루어진 인덱스입니다. 예를 들어, Pauli 문자열 XXY 계수 0.5는 ([1, 1, 2], [0.5])으로 인덱싱됩니다. 또는 X cos φ + Y sin φ와 같이 연속 변수에 의해 매개 변수화 된 Hamiltonians은 ([], [φ])로 표현 될 수 있습니다. 두 번째 요소는 생성기가 작동 하는 하위 시스템을 인덱싱합니다.

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="example"></a>예

을 사용 하 여  <xref:microsoft.quantum.simulation.paulievolutionset> $ \pi X_2 X_5 Y_9 $ 연산자는 다음과 같이 표시 됩니다.

```qsharp
let index = GeneratorIndex(([1, 1, 2], [PI()]), [2, 5, 9]);
```

## <a name="remarks"></a>설명

> [!WARNING]
> 의 해석은 `GeneratorIndex` 특정 생성기 집합에 대 한 참조를 제외 하 고는 정의 되지 않습니다.

## <a name="see-also"></a>참고 항목

- [EvolutionSet.](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [PauliEvolutionSet.](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)