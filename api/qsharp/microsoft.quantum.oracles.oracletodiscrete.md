---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: OracleToDiscrete 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: 158a90bbd0c68406e0a8507ae99fc08fad3b6d19
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193848"
---
# <a name="oracletodiscrete-function"></a>OracleToDiscrete 함수

네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


"블랙 박스" oracle을 나타내는 작업을 수행 하는 경우 "블랙 박스" oracle을 여러 번 반복 하는 불연속 시간 oracle이 반환 됩니다.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>입력

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a>블랙 박스 [oracle: Adj](xref:microsoft.quantum.lang-ref.qubit)+ Ctl의> [Unit](xref:microsoft.quantum.lang-ref.unit)

지수화 작업입니다.



## <a name="output--discreteoracle"></a>출력: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

불연속 시간 oracle을 나타내는 "블랙 박스" oracle에 부분적으로 적용 된 작업입니다.