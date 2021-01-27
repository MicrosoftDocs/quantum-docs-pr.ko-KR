---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: AssertQubitWithinTolerance 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 7f57fc7a29d3eb86dc94cb24230d52b37eb6971d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853427"
---
# <a name="assertqubitwithintolerance-operation"></a>AssertQubitWithinTolerance 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


`q`지정 된 허용 오차까지 해당 하는 Pauli Z 연산자의 예상 된 eigenstate를 어설션 합니다.

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>입력

### <a name="expected--__invalidresult__"></a>예상: __잘못 <Result> 됨__

에서 예상 하는 것으로 예상 되는 상태는 `Zero` 또는 `One` 입니다.


### <a name="q--qubit"></a>q: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

상태가 어설션된의 비트입니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

예상 결과를 반환할 비트의 측정 확률에 대 한 허용 오차입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> 에서는 $ eigenstates $Z 아닌 임의의 eibit 상태를 어설션할 수 있습니다.

## <a name="see-also"></a>참고 항목

- [AssertQubitIsInStateWithinTolerance.](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)