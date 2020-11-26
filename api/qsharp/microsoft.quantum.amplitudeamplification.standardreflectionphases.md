---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: StandardReflectionPhases 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191128"
---
# <a name="standardreflectionphases-function"></a>StandardReflectionPhases 함수

네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


표준 진폭 증폭의 부분 반사 단계를 계산 합니다.

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>입력

### <a name="niterations--int"></a>nIterations: [Int](xref:microsoft.quantum.lang-ref.int)

에 대 한 부분 반사 단계를 생성 하는 진폭 증폭 반복의 수입니다.



## <a name="output--reflectionphases"></a>출력: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

부분 반사로 지정 된 단계를 구현 하는 작업입니다.

## <a name="remarks"></a>설명

모든 단계는 시작 상태와 대상 상태에 대 한 마지막 반사 ($0 $)에 대 한 첫 번째 리플렉션을 제외 하 고 $ \pi $입니다.