---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: ControlledRotation 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847405"
---
# <a name="controlledrotation-user-defined-type"></a>ControlledRotation 사용자 정의 형식

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


대상 및 컨트롤 인덱스, 회전 축 및 모델 매개 변수 벡터로의 인덱스를 기준으로 제어 되는 회전을 설명 합니다.

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a>명명 된 항목

### <a name="targetindex--int"></a>TargetIndex: [Int](xref:microsoft.quantum.lang-ref.int)

이 제어 된 회전에 대 한 대상의 인덱스입니다.
### <a name="controlindices--int"></a>ControlIndices: [Int](xref:microsoft.quantum.lang-ref.int)[]

이 회전의 컨트롤에 해당 하는 컨트롤의 배열입니다.
### <a name="axis--pauli"></a>축: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

이 회전의 축입니다.
### <a name="parameterindex--int"></a>ParameterIndex: [Int](xref:microsoft.quantum.lang-ref.int)

이 회전의 각도를 설명 하는 모델 매개 변수 벡터의 인덱스입니다.

## <a name="example"></a>예

다음은 두 번째 비트율 비트에 의해 제어 되 고 순차 모델에서 네 번째 매개 변수로 지정 된 각도를 사용 하 여 레지스터에서 첫 번째 고 비트의 $X $ 축에 대 한 회전을 나타냅니다.

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a>설명

`ControlIndices`을 (를) 빈 인덱스 배열 ()로 설정 하 여 미제어 회전을 표현할 수 있습니다 `new Int[0]` .