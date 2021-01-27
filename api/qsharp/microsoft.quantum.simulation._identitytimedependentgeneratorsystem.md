---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: _IdentityTimeDependentGeneratorSystem 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857996"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>_IdentityTimeDependentGeneratorSystem 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hamiltonian와 일치 하는 생성기 시스템을 반환 합니다 `H(s) = 0` `s` . 여기서는 일정 매개 변수입니다.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>입력

### <a name="schedule--double"></a>일정: [Double](xref:microsoft.quantum.lang-ref.double)

이 입력은 무시 되며 사용자 정의 형식과의 일관성을 위해 정의 됩니다 <xref:microsoft.quantum.canon.timedependentgeneratorsystem> .



## <a name="output--generatorsystem"></a>출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

모든 $s $에 대해 Hamiltonian $H (s) = $0의 진화를 나타내는 생성기 시스템입니다.