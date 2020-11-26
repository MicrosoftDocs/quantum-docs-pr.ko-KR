---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: MeasurePaulis 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 4faaf78f24fa28ae5e4f701b80d9297c910b975e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194222"
---
# <a name="measurepaulis-operation"></a>MeasurePaulis 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


여러 가지 기능을 제공 하는 배열에서 지정 된 측정 가젯을 사용 하 여 각 측정값을 측정 한 다음 결과의 배열을 반환 합니다.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>입력

### <a name="paulis--pauli"></a>paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[] []

측정할 다중값 비트 Pauli 연산자의 배열입니다.


### <a name="target--qubit"></a>target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

지정 된 연산자를 측정할 레지스터입니다.


### <a name="gadget--pauliqubit--__invalidresult__"></a>가젯: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => __잘못 되었습니다 <Result>__ . 

지정 된 여러 기능 비트 연산자의 측정을 수행 하는 연산입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 된__[]

의 각 요소를 측정 하 여 가져온 결과의 `paulis` 배열 `target` 입니다.