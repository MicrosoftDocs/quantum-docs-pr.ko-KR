---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: FixedPointReflectionPhases 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 6ab2a8c6cb0b390f96aa13ece5d5b89c196a6107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721859"
---
# <a name="fixedpointreflectionphases-function"></a>FixedPointReflectionPhases 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지 [](https://nuget.org/packages/)


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

## <a name="references"></a>참조

"고정 된 수의 쿼리 수와 함께 고정 소수점 진폭 증폭"의 단계를 사용 합니다.

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) "복합 퀀텀 게이트 방법론"도 참조 하세요.
- 형식의 단계에 대 한 [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) `RotationPhases` 입니다.