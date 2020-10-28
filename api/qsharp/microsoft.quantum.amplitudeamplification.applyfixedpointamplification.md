---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: ApplyFixedPointAmplification 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721908"
---
# <a name="applyfixedpointamplification-operation"></a>ApplyFixedPointAmplification 작업

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지 [](https://nuget.org/packages/)


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