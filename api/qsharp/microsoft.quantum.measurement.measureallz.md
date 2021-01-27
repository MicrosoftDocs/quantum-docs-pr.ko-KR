---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: MeasureAllZ 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854681"
---
# <a name="measureallz-operation"></a>MeasureAllZ 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


는 Pauli Z 기준으로 원하는 비트의 레지스터를 측정 합니다.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>설명

전체 레지스터의 패리티를 표시 하는 $Z \otimes Z \otimes \cst\otimes Z $ 기준으로 stbits의 레지스터를 측정 합니다.

## <a name="input"></a>입력

### <a name="register--qubit"></a>register: [](xref:microsoft.quantum.lang-ref.qubit)

측정할 레지스터입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

$Z \otimes Z \otimes \cst\otimes Z $를 측정 한 결과입니다.