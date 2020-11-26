---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: ControlledRotation 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 1e664b470caeba656ea4a73f70bbc0ef5fe76f7e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196568"
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

## <a name="remarks"></a>설명

`ControlIndices`을 (를) 빈 인덱스 배열 ()로 설정 하 여 미제어 회전을 표현할 수 있습니다 `new Int[0]` .