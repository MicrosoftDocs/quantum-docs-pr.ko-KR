---
uid: Microsoft.Quantum.Measurement.MResetZ
title: MResetZ 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: fc9ba6576b56d7df1a57334e1da46b9c48376ecb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853733"
---
# <a name="mresetz-operation"></a>MResetZ 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Z 단위로 단일 비트를 측정 하 고, 측정값을 따라 고정 된 초기 상태로 다시 설정 합니다.

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a>설명

$Z $ 기준으로 단일 비트 측정을 수행 하 고, 측정값을 따라 $ \ket $로이를 반환 하는지 확인 {0} 합니다.

## <a name="input"></a>입력

### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

측정할 단일 비트입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`target`Pauli $Z $ 기준으로 측정 한 결과입니다.