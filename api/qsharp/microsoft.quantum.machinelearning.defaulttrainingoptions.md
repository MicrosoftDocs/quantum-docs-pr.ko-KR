---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: DefaultTrainingOptions 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856001"
---
# <a name="defaulttrainingoptions-function"></a>DefaultTrainingOptions 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


학습용 분류자에 대 한 기본 옵션 집합을 반환 합니다.

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a>출력: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

분류자를 학습 하는 데 사용할 적절 한 기본 교육 옵션 집합입니다.

## <a name="example"></a>예

기본 옵션을 사용 하지만 추가 측정을 사용 하려면 연산자를 사용 합니다 `w/` .

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```