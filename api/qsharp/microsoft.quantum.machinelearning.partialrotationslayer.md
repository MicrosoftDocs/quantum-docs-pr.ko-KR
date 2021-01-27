---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: PartialRotationsLayer 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852930"
---
# <a name="partialrotationslayer-function"></a>PartialRotationsLayer 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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