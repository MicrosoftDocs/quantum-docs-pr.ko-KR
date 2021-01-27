---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: AssertMeasurementProbability 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830832"
---
# <a name="assertmeasurementprobability-operation"></a>AssertMeasurementProbability 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 Pauli의 지정 된 비트를 측정 하는 어설션은 특정 허용 범위 내에서 지정 된 확률을 포함 하는 지정 된 결과를 갖게 됩니다.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="bases--pauli"></a>기본: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Multi-factor bit Pauli 연산자로 표현 된의 확률을 어설션하는 측정 효과입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

어설션을 만들 레지스터입니다.


### <a name="result--__invalidresult__"></a>결과: __잘못 <Result> 됨__

의 예상 결과 `Measure(bases, qubits)` 입니다.


### <a name="prob--double"></a>문제: [Double](xref:microsoft.quantum.lang-ref.double)

지정 된 결과가 예상 되는 확률입니다.


### <a name="msg--string"></a>msg: [문자열](xref:microsoft.quantum.lang-ref.string)

어설션이 실패 하는 경우 보고 될 메시지입니다.


### <a name="tol--double"></a>를: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a>설명

이 작업의 Adjoint 및 제어 된 버전은 조건을 확인 하지 않습니다.

## <a name="see-also"></a>참고 항목

- [AssertMeasurement.](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)