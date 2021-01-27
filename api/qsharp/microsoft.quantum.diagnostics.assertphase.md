---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: AssertPhase 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830071"
---
# <a name="assertphase-operation"></a>AssertPhase 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Equal superposition 상태의 단계가 예상 값을 포함 한다는 것을 어설션 합니다.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>설명

이 작업을 수행 하면 일부 임의의 실제 $t $에 대해 $ \frac{e ^ {i t}} {\phi {2} } (e ^ {i\phi} \ {0} + e ^ {-i\eml} \ k) $로 표현 될 수 있는 퀀텀 상태의 $ \eml$ 단계가 {1} 예상 값을 갖습니다.

## <a name="input"></a>입력

### <a name="expected--double"></a>예상: [Double](xref:microsoft.quantum.lang-ref.double)

예상 값은 $ \\a\in (-\phi, \phi] $입니다.


### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

예상 상태를 저장 하는의 비트입니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

실제 및 예상의 차이에 대 한 절대 허용 오차입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

다음 어설션이 성공 합니다. `qubit` 는 상태 $ \ket{\psi} = e ^ {i 0.5} \ sqrt {1/2} \ k {0} + e ^ {i 0.5} \ a 1/2} \ k {1} $;입니다.

- `AssertPhase(0.0,qubit,10e-10);`

`qubit` 상태 $ \ket{\psi} = e ^ {i 0.5} \ sqrt {1/2} \ k {0} + e ^ {-i 0.5} \ sqrt {1/2} \ k {1} $;

- `AssertPhase(0.5,qubit,10e-10);`

`qubit` 상태 $ \ket{\psi} = e ^ {-i 2.2} \ sqrt {1/2} \ k {0} + e ^ {i 0.2} \ a s t 1/2} \ k {1} $;입니다.

- `AssertPhase(-1.2,qubit,10e-10);`