---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: PartialRotationsLayer 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ab964d2c43a13a5daf64aefdeccd1c26cd371ff4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722433"
---
# <a name="partialrotationslayer-function"></a>PartialRotationsLayer 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지 [](https://nuget.org/packages/)


고유 모델 매개 변수에 의해 매개 변수화 된 지정 된 축을 따라 단일가 비트 회전의 배열을 반환 합니다.

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>입력

### <a name="idxsqubits--int"></a>idxsQubits: [Int](xref:microsoft.quantum.lang-ref.int)[]

각 회전의 대상으로 사용할 비트의 인덱스입니다.


### <a name="axis--pauli"></a>축: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

지정 된 계층의 각 회전에 대 한 회전 축입니다.



## <a name="output--controlledrotation"></a>출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

지정 된 축에 대 한 제어 되는 회전의 배열입니다. 각 비트에 하나씩 `nQubits` 있습니다.