---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: 샘플링 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722426"
---
# <a name="sampled-function"></a>샘플링 된 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지 [](https://nuget.org/packages/)


지정 된 일정을 사용 하 여 지정 된 배열을 샘플링 합니다.

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="schedule--samplingschedule"></a>일정: [Samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

샘플링 값에 사용할 일정입니다.


### <a name="values--t"></a>값: ' ' '

샘플링할 값의 배열입니다.



## <a name="output--t"></a>출력: ' t []

지정 된 일정에 따라 값의 요소 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

