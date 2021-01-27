---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: RotationPhases 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843972"
---
# <a name="rotationphases-user-defined-type"></a>RotationPhases 사용자 정의 형식

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


진폭 증폭에서 단일 비트 회전의 시퀀스에 대 한 단계입니다.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>설명

첫 번째 매개 변수는 단일가 나 비트 회전의 곱으로 표현 되는 반사의 단계 배열입니다.
[ G.H. 낮음, L. L. Chuang, https://arxiv.org/abs/1707.05391 ].