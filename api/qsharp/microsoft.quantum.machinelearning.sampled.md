---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: 샘플링 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854940"
---
# <a name="sampled-function"></a>샘플링 된 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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

