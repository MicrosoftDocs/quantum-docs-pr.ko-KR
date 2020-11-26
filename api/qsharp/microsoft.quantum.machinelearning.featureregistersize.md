---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: FeatureRegisterSize 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: bc5d5a23cfb431f9506b15bc404ab6955d1c2a35
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196415"
---
# <a name="featureregistersize-function"></a>FeatureRegisterSize 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


특정 기능 벡터를 인코딩하는 데 필요한 원하는 비트 수를 반환 합니다.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>입력

### <a name="sample--double"></a>샘플: [Double](xref:microsoft.quantum.lang-ref.double)[]

요소 비트 레지스터로 인코딩할 샘플 기능 벡터입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

원하는 `sample` 비트 수로 표현 되는 원하는 비트 레지스터로 인코딩하는 데 필요한 크기입니다.