---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: RotationPhases 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191366"
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