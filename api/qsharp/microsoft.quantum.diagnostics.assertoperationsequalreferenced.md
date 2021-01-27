---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: AssertOperationsEqualReferenced 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 045f00a720e9f4d2e6993c66ace44a81e192ff30
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853474"
---
# <a name="assertoperationsequalreferenced-operation"></a>AssertOperationsEqualReferenced 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


두 작업이 지정 된 경우는 모든 입력 상태에 대해 동일 하 게 작동 한다는 것을 어설션 합니다.

이 어설션은 Choi – Jamiołkowski isomorphism를 사용 하 여 두 entangled 레지스터의를 사용 하는 것으로 어설션을 줄이는 방법으로 구현 됩니다.
따라서이 작업은 테스트 되는 각 작업에 대 한 단일 호출만 필요 하지만 할당 해야 하는 것은 두 배입니다.
이 어설션을 사용 하면 예를 들어, 작업의 최적화 된 버전이 naive 구현에 동일 하 게 작동 하거나, 비 퀀텀 입력 범위에서 작동 하는 작업이 알려진 사례에 동의 하는 경우를 확인할 수 있습니다.

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>입력

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

각 작업에 전달할 비트 수입니다.


### <a name="actual--qubit--unit"></a>actual: [bit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

테스트할 작업입니다.


### <a name="expected--qubit--unit--is-adj"></a>예상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj

테스트 중인 작업의 예상 동작을 정의 하는 작업입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이 작업을 수행 하려면 예상 되는 동작을 모델링 하는 작업이 adjointable 해야 합니다. 따라서 역은 대상 레지스터 에서만 수행 될 수 있습니다.
공식적으로는 이러한 요구 사항을 완화 하는 바꾸기 작업을 지정할 수 있지만,이 경우에는 바꾸기 작업이 임의의 퀀텀 작업에 대해 일반적으로 실제로 realizable 되지 않으므로이 옵션으로 여기에 포함 되지 않습니다.