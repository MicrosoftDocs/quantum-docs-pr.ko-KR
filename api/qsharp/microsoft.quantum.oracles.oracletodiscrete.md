---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: OracleToDiscrete 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842531"
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

## <a name="example"></a>예

`OracleToDiscrete(U)(3, target)` 는 세 번 반복 되는 것과 같습니다 `U(target)` .