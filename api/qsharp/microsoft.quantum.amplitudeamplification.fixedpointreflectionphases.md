---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: FixedPointReflectionPhases 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191451"
---
# <a name="fixedpointreflectionphases-function"></a>FixedPointReflectionPhases 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


고정 소수점 진폭 증폭의 부분 반사 단계를 계산 합니다.

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>입력

### <a name="nqueries--int"></a>nQueries: [Int](xref:microsoft.quantum.lang-ref.int)

Oracle 상태 준비에 대 한 쿼리 수입니다. 홀수 정수 여야 합니다.


### <a name="successmin--double"></a>successMin: [Double](xref:microsoft.quantum.lang-ref.double)

대상 최소 성공 확률입니다.



## <a name="output--reflectionphases"></a>출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

고정 소수점 진폭 진폭 퀀텀 알고리즘 구현에 사용할 수 있는 일련의 단계입니다.

## <a name="references"></a>참조 항목

"고정 된 수의 쿼리 수와 함께 고정 소수점 진폭 증폭"의 단계를 사용 합니다.

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) "복합 퀀텀 게이트 방법론"도 참조 하세요.
- 형식의 단계에 대 한 [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) `RotationPhases` 입니다.