---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: IdentityGeneratorIndex 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: d2af2dafaf75a68546cb3f16c04cf4c7ee50c6ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724540"
---
# <a name="identitygeneratorindex-function"></a>IdentityGeneratorIndex 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지 [](https://nuget.org/packages/)


Id 진화 작업에 해당 하는 0 Hamiltonian와 일치 하는 생성기 인덱스를 반환 합니다 `H = 0` .

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>입력

### <a name="idxterm--int"></a>idxTerm: [Int](xref:microsoft.quantum.lang-ref.int)

이 입력은 무시 되며 사용자 정의 형식과의 일관성을 위해 정의 됩니다 <xref:microsoft.quantum.simulation.generatorsystem> .



## <a name="output--generatorindex"></a>출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Hamiltonian $H = $0의 진화를 나타내는 생성기 인덱스입니다.