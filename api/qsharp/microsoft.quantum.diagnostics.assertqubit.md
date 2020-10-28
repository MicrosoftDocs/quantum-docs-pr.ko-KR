---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: AssertQubit 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712944"
---
# <a name="assertqubit-operation"></a>AssertQubit 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


`q`Eibit가 Pauli Z 연산자의 예상 eigenstate 임을 어설션 합니다.

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a>입력

### <a name="expected--__invalidresult__"></a>예상: __잘못 <Result> 됨__

에서 예상 하는 것으로 예상 되는 상태는 `Zero` 또는 `One` 입니다.


### <a name="q--qubit"></a>q: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

상태가 어설션된의 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> 에서는 $ eigenstates $Z 아닌 임의의 eibit 상태를 어설션할 수 있습니다.

## <a name="see-also"></a>참고 항목

- [AssertQubitIsInStateWithinTolerance.](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)