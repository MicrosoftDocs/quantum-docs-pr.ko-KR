---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: ApplyFixedPointAmplification 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: 13e70b1ebd5e3bf0996e6a76f4bffe57ca2d2250
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191536"
---
# <a name="applyfixedpointamplification-operation"></a>ApplyFixedPointAmplification 작업

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Fixed-Point 진폭 증폭 알고리즘

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="statepreporacle--stateoracle"></a>statePrepOracle: [Stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

시작 상태를 준비 하는 단일 oracle.


### <a name="startqubits--qubit"></a>startQubits: [\Bit](xref:microsoft.quantum.lang-ref.qubit)[]

비트율 비트 레지스터



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

StartQubits는 $ \ket{0 \cdots 0} $ 상태 여야 합니다. 이 작업은 최대 쿼리 수에 도달 하거나 대상 상태가 발견 될 때까지 $2 $의 거듭제곱으로 많은 쿼리를 반복 합니다.