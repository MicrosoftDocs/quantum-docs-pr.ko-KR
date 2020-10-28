---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: MeasureAllZ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711075"
---
# <a name="measureallz-operation"></a>MeasureAllZ 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지 [](https://nuget.org/packages/)


는 Pauli Z 기준으로 원하는 비트의 레지스터를 측정 합니다.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>Description

전체 레지스터의 패리티를 표시 하는 $Z \otimes Z \otimes \cst\otimes Z $ 기준으로 stbits의 레지스터를 측정 합니다.

## <a name="input"></a>입력

### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

측정할 레지스터입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

$Z \otimes Z \otimes \cst\otimes Z $를 측정 한 결과입니다.