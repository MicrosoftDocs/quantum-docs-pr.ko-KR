---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: InputEncoder 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: ed70d9f24af06f8918083307c98a5f6c4671f1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852934"
---
# <a name="inputencoder-function"></a>InputEncoder 함수

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


계수 및 허용 오차 집합이 지정 된 경우 각 계수를 계산 기준 상태의 해당 진폭으로 준비 하는 상태 준비 작업을 반환 합니다.

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>입력

### <a name="coefficients--double"></a>계수: [Double](xref:microsoft.quantum.lang-ref.double)[]

입력 상태로 인코딩될 계수입니다.



## <a name="output--stategenerator"></a>출력: [Stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

지정 된 레지스터에서 지정 된 계수를 입력 상태로 준비 하는 상태 준비 작업입니다.