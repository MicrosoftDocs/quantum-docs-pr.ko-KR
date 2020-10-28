---
uid: Microsoft.Quantum.Measurement.MResetZ
title: MResetZ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 9f084b03504deea9fcf25e4c797c4bde3c97a995
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711054"
---
# <a name="mresetz-operation"></a>MResetZ 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지 [](https://nuget.org/packages/)


Z 단위로 단일 비트를 측정 하 고, 측정값을 따라 고정 된 초기 상태로 다시 설정 합니다.

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a>Description

$Z $ 기준으로 단일 비트 측정을 수행 하 고, 측정값을 따라 $ \ket $로이를 반환 하는지 확인 {0} 합니다.

## <a name="input"></a>입력

### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

측정할 단일 비트입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`target`Pauli $Z $ 기준으로 측정 한 결과입니다.