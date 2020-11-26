---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: CyclicEntanglingLayer 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5421765e36ef3e8e744e118206dafcb2bb582cc2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211936"
---
# <a name="cyclicentanglinglayer-function"></a>CyclicEntanglingLayer 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


지정 된 축을 따라 단일 제어 회전의 배열을 반환 하 고,이를 통해 주기적의 레지스터를 정렬 하 고, 고유 모델 매개 변수에 의해 매개 변수화 됩니다.

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>입력

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 계층에 의해 처리 되는의 비트 수입니다.


### <a name="axis--pauli"></a>축: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

지정 된 계층의 각 회전에 대 한 회전 축입니다.


### <a name="stride--int"></a>stride: [Int](xref:microsoft.quantum.lang-ref.int)

각 회전에 대해 대상과 컨트롤 인덱스를 분리 하는 것입니다.



## <a name="output--controlledrotation"></a>출력: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

주기적의 레지스터를 중심으로 하는 두 개의 고 비트 제어 되는 회전의 배열입니다 `nQubits` .