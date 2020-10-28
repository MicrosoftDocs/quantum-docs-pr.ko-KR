---
uid: Microsoft.Quantum.Measurement.MResetY
title: MResetY 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 48aba7317d0e48d089ec6c4814efdee51bb8e2ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725009"
---
# <a name="mresety-operation"></a>MResetY 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지 [](https://nuget.org/packages/)


Y를 기준으로 단일의 비트를 측정 하 고 측정 다음에 고정 된 초기 상태로 다시 설정 합니다.

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a>Description

$Y $ 기준으로 단일 비트 측정을 수행 하 고, 측정값을 따라 $ \ket $로이를 반환 하는지 확인 {0} 합니다.

## <a name="input"></a>입력

### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

측정할 단일 비트입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

`target`Pauli $Y $ 기준으로 측정 한 결과입니다.