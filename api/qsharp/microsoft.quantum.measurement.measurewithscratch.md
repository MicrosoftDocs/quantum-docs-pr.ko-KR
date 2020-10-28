---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: MeasureWithScratch 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 1ee25dbccd5bddde406cf8ed84dff77d96d7804e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720325"
---
# <a name="measurewithscratch-operation"></a>MeasureWithScratch 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지 [](https://nuget.org/packages/)


측정을 수행 하기 위해 명시적인 스크래치 비트를 사용 하 여 지정 된 Pauli 연산자를 측정 합니다.

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [pauli](xref:microsoft.quantum.lang-ref.pauli)[]

단일 수준 비트 Pauli 연산자의 배열로 지정 된 다중 기능 비트 Pauli 연산자입니다.


### <a name="target--qubit"></a>target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

측정할 비트 레지스터입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

레지스터에서 지정 된 Pauli 연산자를 측정 한 결과입니다 `target` .