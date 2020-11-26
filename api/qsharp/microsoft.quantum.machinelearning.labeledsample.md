---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: LabeledSample 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: a7c7dae5cd9e82d66bb98313f4200838006ca291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196330"
---
# <a name="labeledsample-user-defined-type"></a>LabeledSample 사용자 정의 형식

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


예제가 속한 클래스를 사용 하 여 레이블이 지정 된 샘플입니다.

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a>명명 된 항목

### <a name="features--double"></a>기능: [Double](xref:microsoft.quantum.lang-ref.double)[]

지정 된 샘플에 대 한 기능 벡터입니다.
### <a name="label--int"></a>레이블: [Int](xref:microsoft.quantum.lang-ref.int)

이 샘플이 속한 클래스의 정수 레이블입니다.