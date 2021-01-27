---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: StandardNormalDistribution 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857806"
---
# <a name="standardnormaldistribution-function"></a>StandardNormalDistribution 함수

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


평균 0과 분산이 1 인 정규 분포를 반환 합니다.

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a>출력: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>예

다음은 표준 정규 분포에서 10 개의 샘플을 그립니다.

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자.](xref:Microsoft.Quantum.Random.NormalDistribution)