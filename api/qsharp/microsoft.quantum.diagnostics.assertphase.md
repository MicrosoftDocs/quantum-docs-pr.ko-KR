---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: AssertPhase 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 9130d6c735d90abbc51989ef4a68a8eff8b41371
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202263"
---
# <a name="assertphase-operation"></a>AssertPhase 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Equal superposition 상태의 단계가 예상 값을 포함 한다는 것을 어설션 합니다.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>Description

이 작업을 수행 하면 일부 임의의 실제 $t $에 대해 $ \frac{e ^ {i t}} {\phi {2} } (e ^ {i\phi} \ {0} + e ^ {-i\eml} \ k) $로 표현 될 수 있는 퀀텀 상태의 $ \eml$ 단계가 {1} 예상 값을 갖습니다.

## <a name="input"></a>입력

### <a name="expected--double"></a>예상: [Double](xref:microsoft.quantum.lang-ref.double)

예상 값은 $ \\a\in (-\phi, \phi] $입니다.


### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

예상 상태를 저장 하는의 비트입니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

실제 및 예상의 차이에 대 한 절대 허용 오차입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

