---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: NQubitsRequired 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: 8f6c1bf3dfef3152a6ba8eada0980d6940724259
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854960"
---
# <a name="nqubitsrequired-function"></a>NQubitsRequired 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


지정 된 순차 분류자를 적용 하는 데 필요한 원하는 비트 수를 반환 합니다.

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a>입력

### <a name="model--sequentialmodel"></a>모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

순차 분류자가 적용 될 수 있는 레지스터의 최소 크기입니다.